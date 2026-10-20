# Registro de riesgos

Los riesgos RSK-001 a RSK-005 conservan la evaluación inicial del documento. Las valoraciones añadidas para RSK-006 a RSK-010 son propuestas basadas en los vacíos técnicos descritos en el SRS; el grupo debe confirmarlas. Todas las mitigaciones permanecen abiertas hasta que se registre evidencia.

| ID | Fase | Riesgo | Probabilidad | Impacto | Mitigación | Comprobación de la mitigación | Estado |
|---|---|---|---|---|---|---|---|
| RSK-001 | Elaboración | La interfaz de venta no invoca la transacción disponible en el backend. | Alta | Alto | Integrar CU01 con el servicio transaccional y guardar venta, detalle y salida de stock en una operación. | Ejecutar una venta integrada y comprobar en la base que los tres registros se confirman juntos; provocar un error y verificar rollback. | Abierto |
| RSK-002 | Inicio / Construcción | El stock de demostración puede diferir de las existencias físicas. | Alta | Alto | Hacer el conteo inicial y conciliarlo con los productos antes del uso operativo. | Comparar el conteo físico con el inventario cargado y registrar las diferencias corregidas. | Abierto |
| RSK-003 | Elaboración | El cálculo de descuentos de la interfaz difiere del cálculo base del backend. | Alta | Alto | Definir una regla común y aplicarla en el servicio de venta. | Probar casos con y sin descuento; comparar subtotales y total con el cálculo redondeado a dos decimales. | Abierto |
| RSK-004 | Construcción | Las órdenes de compra y la recepción están especificadas, pero no implementadas. | Alta | Medio | Confirmar prioridad, definir tablas y servicios, y no aumentar stock hasta confirmar la recepción. | Crear una orden pendiente y probar recepción total y parcial; comprobar movimientos y stock en la misma transacción. | Abierto |
| RSK-005 | Elaboración | La solicitud de separación no garantiza el bloqueo de existencias. | Media | Alto | Mantenerla como solicitud pendiente y no presentarla como reserva confirmada hasta definir el control de stock. | Comprobar que una solicitud no descuenta ni bloquea stock y que la interfaz informa su estado real. | Abierto |
| RSK-006 | Construcción | La sesión de demostración y la autenticación JWT están separadas. | Alta* | Alto* | Integrar el inicio de sesión con las rutas protegidas y el control de roles. | Verificar que un cliente no acceda a opciones administrativas y que la API rechace una solicitud con rol no autorizado. | Abierto |
| RSK-007 | Construcción | El formulario de productos no completa el guardado ni los ajustes de stock. | Alta* | Alto* | Completar persistencia, validaciones y registro de movimientos para los ajustes autorizados. | Crear y editar un producto; realizar un ajuste y verificar los datos guardados y el movimiento correspondiente. | Abierto |
| RSK-008 | Construcción | Algunas consultas administrativas y del portal usan datos de ejemplo o servicios parciales. | Media* | Medio* | Conectar las vistas priorizadas con las consultas reales y señalar los datos que aún sean demostrativos. | Comparar las respuestas de la interfaz con los registros de prueba de la base y comprobar el estado vacío y los errores de consulta. | Abierto |
| RSK-009 | Transición | No está acreditado un procedimiento de respaldo y recuperación de la base de datos. | Media* | Alto* | Definir una copia al cierre de jornada y un procedimiento de recuperación probado. | Generar una copia, restaurarla en un entorno de prueba y comprobar que incluye las ventas del respaldo. | Abierto |
| RSK-010 | Elaboración / Construcción | Las pruebas backend registradas no demuestran integración completa entre interfaz, API y MySQL. | Alta* | Alto* | Añadir pruebas de integración y escenarios Gherkin para los flujos priorizados. | Ejecutar el flujo de venta desde la interfaz hasta la base, probar errores y adjuntar resultados. | Abierto |

* Valoración inicial propuesta para discutir con el equipo.

## Seguimiento

- Actualizar este registro al cierre de cada iteración.
- Una mitigación escrita no equivale a un riesgo resuelto.
- Cambiar el estado a mitigado solo después de adjuntar una prueba, captura, resultado automatizado o registro verificable.
- Vincular la evidencia con el requisito, caso de uso o pull request correspondiente.
