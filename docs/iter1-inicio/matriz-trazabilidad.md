# Matriz de trazabilidad: Comercial Nazareth

Esta matriz consolida los vínculos de RF, RNF, CU, HU y artefactos registrados en la documentación del proyecto. El estado técnico describe la evidencia reportada; no significa que la función esté validada de extremo a extremo.

## Requisitos funcionales

| RF | Caso de uso | Historia de usuario | Artefacto de referencia | Estado técnico reportado | Pendiente de cierre |
|---|---|---|---|---|---|
| RF-01 | CU01 | HU-02, HU-03 | PR-01 | Parcial: existe una transacción en backend, pero la interfaz confirma una venta local. | Integrar UI, servicio y MySQL; probar confirmación y rollback. |
| RF-02 | CU06 | HU-04 | PR-02 | Parcial: consulta API disponible; la interfaz usa datos de ejemplo. | Conectar la vista y probar el umbral mínimo. |
| RF-03 | CU08 | HU-09 | PR-09 | Especificado; no hay servicio de compras. | Implementar los datos del proveedor dentro de la orden si se prioriza CU08. |
| RF-04 | CU08 | HU-10 | PR-10 | Especificado; no implementado. | Persistir orden, líneas, costos, estado y total estimado. |
| RF-05 | CU09 | HU-11 | PR-11 | Especificado; existe soporte parcial de inventario, pero no se acredita un servicio transaccional de recepción. | Implementar recepción transaccional y movimientos de entrada. |
| RF-06 | Transversal | HU-01 | PR-06 | Sesión de demostración local y autenticación JWT separada. | Integrar autenticación, navegación y autorización por rol. |
| RF-07 | CU03 | HU-07 | PR-07 | Catálogo local y endpoint de consulta disponible. | Verificar la integración de búsqueda, disponibilidad, favoritos y listas. |
| RF-08 | CU04 | HU-06 | PR-08 | CRUD local y endpoints separados. | Conectar interfaz y API; validar vigencia y estado de campañas. |
| RF-09 | CU05 | HU-08 | PR-05 | Solicitud almacenada localmente; no hay API de reservas. | Definir integración y dejar claro que la solicitud no bloquea stock. |
| RF-10 | CU02 | HU-05 | PR-04 | La API admite customerId opcional; selector de interfaz pendiente. | Integrar la selección de cliente y probar la venta sin cliente. |
| RF-11 | Consulta administrativa | No registrado en el vínculo recuperado | PR-12 | Vista con datos de ejemplo y sin ruta de clientes reportada. | Confirmar el vínculo HU en el informe e integrar la consulta real. |
| RF-12 | Consulta administrativa | No registrado en el vínculo recuperado | PR-13 | Resumen API parcial; reportes con datos de ejemplo. | Confirmar el vínculo HU y validar los resultados por periodo. |
| RF-13 | Transversal | No registrado en el vínculo recuperado | PR-14 | Gestión local y endpoints separados, sin sincronización. | Confirmar el vínculo HU e integrar el control de accesos. |
| RF-14 | Portal de clientes | No registrado en el vínculo recuperado | PR-15 | Vista de referencia con historial y puntos predeterminados. | Confirmar el vínculo HU e integrar datos de la cuenta. |
| RF-15 | CU06 | No registrado en el vínculo recuperado | PR-16 | Formulario visual y tabla products; guardado y ajustes pendientes. | Confirmar el vínculo HU y completar persistencia e historial de ajustes. |

La indicación "No registrado en el vínculo recuperado" señala una brecha por cotejar con el informe; no significa que la historia de usuario no exista.

## Requisitos no funcionales

| RNF | Criterio | Artefacto de referencia | Estado / evidencia pendiente |
|---|---|---|---|
| RNF-01 | Venta simple de hasta 3 líneas en menos de 15 s, excluyendo la espera de pago externo. | SaleDrawer y servicio de venta · PR-17 | No se recuperó una medición de tiempo reproducible. Medir el flujo acordado y guardar el resultado. |
| RNF-02 | El cliente no ve opciones administrativas y la API rechaza roles no autorizados. | visibleNavigation, auth, requireRole · PR-06 | La sesión de demostración y JWT están separados. Probar navegación y llamadas directas a la API. |
| RNF-03 | Productos, stock y resumen responden en ≤3 s con un usuario concurrente y catálogo local de demostración. | Rutas products y dashboard · PR-18 | No se recuperó una medición. Registrar entorno, datos y tiempo de respuesta. |
| RNF-04 | Venta, detalle y movimiento se confirman juntos; ante error no quedan cambios parciales. | createSale y transacción SQL · PR-01 | La transacción backend está disponible, pero la UI no la invoca. Ejecutar pruebas integradas y de rollback. |
| RNF-05 | Totales y subtotales con 2 decimales; diferencia permitida S/ 0,00. | cartSummary, paymentState, calculateSaleTotal · PR-03 | Se reporta diferencia entre cálculos de interfaz y backend. Unificar la regla y probar casos con descuento. |
| RNF-06 | Al menos una copia diaria y recuperación de prueba con ventas incluidas. | Base comercial_nazareth y respaldo · PR-19 | Procedimiento de respaldo por implementar y validar mediante restauración de prueba. |

## Vínculos de historias de usuario recuperados

| HU | RF relacionado |
|---|---|
| HU-01 | RF-06 |
| HU-02 | RF-01 |
| HU-03 | RF-01 |
| HU-04 | RF-02 |
| HU-05 | RF-10 |
| HU-06 | RF-08 |
| HU-07 | RF-07 |
| HU-08 | RF-09 |
| HU-09 | RF-03 |
| HU-10 | RF-04 |
| HU-11 | RF-05 |

Esta matriz conserva los vínculos disponibles. Antes de cerrar la iteración, cotejar los textos completos de HU-01 a HU-11 y los criterios de aceptación con el informe académico para evitar duplicar o reconstruir historias de memoria.

## Evidencia y reglas de actualización

- Una función se marca como integrada cuando existe evidencia de interfaz, API y persistencia funcionando en conjunto.
- Una prueba backend aislada no acredita la integración de la interfaz ni la aceptación del usuario.
- Toda modificación de un RF o RNF debe actualizar sus CU, HU, artefactos y pruebas relacionadas.
- Los riesgos y las mitigaciones se mantienen abiertos hasta adjuntar evidencia verificable.
