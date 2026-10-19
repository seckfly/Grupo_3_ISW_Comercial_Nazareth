# Riesgos por fase

Las probabilidades e impactos son una valoración inicial para planificar el trabajo. Deben revisarse con el equipo.

| ID | Fase | Riesgo | Probabilidad | Impacto | Mitigación | Responsable funcional |
|---|---|---|---|---|---|---|
| RSK-001 | Elaboración | La interfaz de venta no invoca la transacción disponible en el backend. | Alta | Alto | Integrar CU01 con el servicio transaccional y probar cabecera, detalle y stock en una misma operación. | Arquitectura e integración, por asignar |
| RSK-002 | Inicio / Construcción | El stock de demostración puede no coincidir con el inventario físico. | Alta | Alto | Contar existencias, cargar saldos iniciales y comprobar los movimientos de entrada y salida. | Responsable de inventario, por asignar |
| RSK-003 | Elaboración | El cálculo de descuentos de la interfaz no coincide con el cálculo base del backend. | Alta | Alto | Acordar una regla, aplicar un único cálculo y probar los totales antes de integrar. | Análisis e integración, por asignar |
| RSK-004 | Construcción | CU08 y CU09 están especificados, pero compras y recepción no están integradas. | Alta | Medio | Definir modelo de datos y servicios, y no presentar estas funciones como disponibles hasta probarlas. | Desarrollo y pruebas, por asignar |
| RSK-005 | Elaboración | La solicitud de separación no garantiza que el stock quede bloqueado. | Media | Alto | Mantener el estado como solicitud y definir el control de existencias antes de llamarla reserva confirmada. | Análisis funcional, por asignar |

## Seguimiento

Cada riesgo debe tener una tarjeta en la lista Riesgos del tablero Trello del proyecto cuando ese tablero esté creado. El riesgo se cierra solo cuando existe evidencia de la mitigación.