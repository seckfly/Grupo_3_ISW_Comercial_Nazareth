# Riesgos por fase

| ID | Fase | Riesgo | Probabilidad | Impacto | Mitigación | Responsable |
|---|---|---|---|---|---|---|
| RSK-001 | Elaboración | La interfaz de venta no invoca la transacción disponible en el backend. | Alta | Alto | Integrar CU01 con el servicio transaccional y probar que venta, detalle y stock se confirmen en una operación. | Responsable de integración |
| RSK-002 | Inicio / Construcción | El stock de demostración puede diferir de las existencias físicas. | Alta | Alto | Hacer el conteo inicial y conciliarlo con los productos antes de usar el sistema operativamente. | Responsable de inventario |
| RSK-003 | Elaboración | El cálculo de descuentos de la interfaz difiere del cálculo base del backend. | Alta | Alto | Definir una regla común, aplicarla en el servicio y probar los importes con casos conocidos. | Responsable de integración |
| RSK-004 | Construcción | Las órdenes de compra y la recepción están especificadas, pero no implementadas. | Alta | Medio | Definir datos y servicios antes de desarrollar CU08 y CU09; no considerar el stock actualizado hasta confirmar la recepción. | Responsable de desarrollo |
| RSK-005 | Elaboración | La solicitud de separación no garantiza el bloqueo de existencias. | Media | Alto | Mantenerla como solicitud y definir el control de stock antes de tratarla como reserva confirmada. | Responsable funcional |

Revisar estos riesgos al cierre de cada iteración y actualizar su mitigación cuando cambie el diseño o el estado de implementación.