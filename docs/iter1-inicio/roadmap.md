# Roadmap RUP: Comercial Nazareth

El trabajo documentado en la línea base de ITER-1 se elaboró durante las semanas académicas 8, 9 y 10. Este roadmap planifica las cuatro fases RUP. Los entregables de ITER-2 a ITER-4 son previstos; no se presentan como artefactos ya producidos en la versión v1.0-iter1.

| Fase | Iteración | Objetivo | Entregables previstos | Responsable | Plazo | Criterio de cierre |
|---|---|---|---|---|---|---|
| Inicio | ITER-1 | Delimitar el alcance y modelar el proceso crítico. | Visión, SRS breve, diagramas de casos de uso y actividad, matriz fase-artefacto, trazabilidad, glosario, checklist y riesgos. | Marco Antonio Martell Alvarez y Alejandro Horna Quezada. | Semana 8 | Alcance, requisitos y modelos mantienen los mismos términos y reglas. |
| Elaboración | ITER-2 | Precisar los requisitos y resolver las decisiones técnicas que afectan la venta. | SRS revisado, matriz de trazabilidad RF-HU-CU actualizada y escenarios para datos inválidos, falta de stock y fallo de persistencia. | Isaí Samuel Bejarano Benites, con apoyo de Cesar Jeremin Alonso Chuquimango Reyes. | Semana 9 | Cada requisito priorizado tiene un criterio comprobable y sus flujos alternos están documentados. |
| Construcción | ITER-3 | Integrar y comprobar las funciones priorizadas. | Integración de CU01 con el servicio transaccional, consistencia del cálculo monetario, validaciones de stock y pago, vinculación opcional del cliente y pruebas funcionales de los escenarios definidos. | Marco Antonio Martell Alvarez y Alejandro Horna Quezada. | Semanas 9-10 | Las pruebas muestran que venta, detalle y movimiento de stock se confirman juntos o se revierten. |
| Transición | ITER-4 | Preparar la entrega y verificar su aceptación. | Manual de usuario, pruebas de aceptación, validación del stock inicial, comprobación de respaldo y recuperación, documentación de entrega y tag de la versión entregada. | Marco Antonio Martell Alvarez y Alonso Castillo Davalos. | Semana 10 | La documentación corresponde a las funciones entregadas, las pruebas de aceptación están registradas y la versión queda identificada en el repositorio. |

## Criterios de trabajo

- CU01 es el proceso crítico porque relaciona el cobro, el detalle de venta y el inventario.
- Los diagramas se limitan a los necesarios para explicar el sistema y comprobar ese proceso.
- El tablero de Trello organiza las tareas por estado de avance y mantiene una lista separada de riesgos.
- Los cinco riesgos principales se revisan durante el trabajo de las iteraciones.
- La revisión de coherencia de ITER-1 quedó registrada por Marco Antonio Martell Alvarez.

La etiqueta v1.0-iter1 identifica la línea base de Inicio. La versión correspondiente a la entrega de Transición se identificará cuando esa fase se complete.
