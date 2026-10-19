# Roadmap RUP: Comercial Nazareth

| Fase | Iteración | Objetivo | Entregables | Responsable | Plazo |
|---|---|---|---|---|---|
| Inicio | ITER-1 | Delimitar el alcance y elegir el proceso crítico. | Visión, SRS breve, matriz fase-artefacto, diagrama de casos de uso del informe, diagrama de actividad de CU01, glosario, checklist y riesgos. | Analista funcional | Semana 1 |
| Elaboración | ITER-2 | Validar requisitos y resolver los riesgos de integración. | Casos de uso revisados, diagramas de clases y secuencia de CU01, diseño de integración y casos de prueba. | Arquitectura de software | Semanas 2-3 |
| Construcción | ITER-3 | Integrar y probar las funciones priorizadas. | Integración de CU01, validaciones de stock y pago, pruebas funcionales y modelo de estados de compra si se confirma su alcance. | Desarrollo y pruebas | Semanas 4-6 |
| Transición | ITER-4 | Preparar la entrega y comprobar la aceptación. | Manual de usuario, pruebas de aceptación, validación de datos iniciales y registro de entrega. | Coordinación de entrega | Semana 7 |

## Riesgos que afectan el plan

- RSK-001: la interfaz de venta no invoca la transacción del backend.
- RSK-002: el stock de demostración puede diferir del inventario físico.
- RSK-003: el cálculo de descuentos difiere entre interfaz y backend.
- RSK-004: las órdenes de compra y la recepción están especificadas, pero no implementadas.
- RSK-005: la solicitud de separación no bloquea existencias.