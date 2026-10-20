# Roadmap RUP: Comercial Nazareth

Las duraciones son estimaciones relativas para organizar el trabajo; no son fechas de entrega confirmadas. Los responsables se proponen en función de las áreas de trabajo y deben validarse con el grupo.

| Fase | Iteración | Objetivo | Entregables | Responsable propuesto | Duración estimada | Criterio de salida |
|---|---|---|---|---|---|---|
| Inicio | ITER-1 | Delimitar el alcance y documentar el proceso crítico. | Visión, SRS breve, casos de uso vigentes, diagramas, matriz de trazabilidad, glosario, checklist, registro de riesgos y revisión documental. | Marco Antonio Martell Alvarez, coordinación; Isaí Samuel Bejarano Benites, análisis funcional. | 1 semana | Documentos alineados, diagramas cotejados y PR revisado por una persona distinta de su autor. |
| Elaboración | ITER-2 | Validar requisitos y resolver riesgos de integración antes de ampliar funciones. | SRS revisado, casos de uso validados, diagramas de clases y secuencia de CU01, diseño de integración y escenarios Gherkin. | Isaí Samuel Bejarano Benites, requisitos; Alonso Castillo Davalos, arquitectura y modelos. | Semanas 2-3 | Cada requisito priorizado tiene criterio de aceptación y relación con su diseño y prueba. |
| Construcción | ITER-3 | Integrar y probar las funciones priorizadas. | Integración de CU01 con la transacción backend, cálculo monetario consistente, validaciones de stock y pago, vinculación opcional del cliente y pruebas funcionales. Las compras y recepción se desarrollan solo si se confirma su prioridad. | Cesar Jeremin Alonso Chuquimango Reyes, desarrollo e integración; Alejandro Horna Quezada, pruebas. | Semanas 4-6 | Pruebas automatizadas aprobadas, escenarios de aceptación ejecutados y compilación de frontend correcta. |
| Transición | ITER-4 | Preparar la entrega y comprobar la aceptación. | Manual de usuario, pruebas de aceptación, validación de datos iniciales, comprobación de respaldo y recuperación, registro de entrega y etiqueta de versión. | Alejandro Horna Quezada, aceptación; Marco Antonio Martell Alvarez, coordinación de entrega. | Semana 7 | Evidencias de aceptación registradas, documentación actualizada y entrega revisada por el grupo. |

## Orden de trabajo para ITER-1

1. Cerrar la coherencia entre Visión, SRS, matriz fase-artefacto y matriz de trazabilidad.
2. Revisar los diagramas y confirmar que sus fuentes editables y exportaciones representan el mismo flujo.
3. Incorporar las comprobaciones de mitigación al registro de riesgos.
4. Conseguir una revisión por pares independiente en el PR #1.
5. Confirmar responsables y añadir el enlace del Trello antes de cerrar la planificación.

## Riesgos que afectan el plan

- RSK-001: la interfaz de venta no invoca la transacción disponible en el backend.
- RSK-002: el stock de demostración puede diferir de las existencias físicas.
- RSK-003: el cálculo de descuentos difiere entre interfaz y backend.
- RSK-004: las órdenes de compra y la recepción están especificadas, pero no implementadas.
- RSK-005: la solicitud de separación no bloquea existencias.
- RSK-006: la sesión de demostración y la autenticación JWT no están integradas.
- RSK-007: el formulario de productos no completa el guardado ni los ajustes de stock.
- RSK-008: algunas consultas administrativas y del portal usan datos de ejemplo.
- RSK-009: falta comprobar un procedimiento de respaldo y recuperación de la base.
- RSK-010: las pruebas backend registradas no demuestran por sí solas la integración completa.

El detalle, la mitigación y la comprobación de cada riesgo están en [riesgos.md](riesgos.md). Las asignaciones por integrante se describen en [responsables.md](responsables.md).
