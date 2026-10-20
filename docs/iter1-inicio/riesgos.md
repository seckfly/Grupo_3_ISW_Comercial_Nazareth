# Registro de riesgos

Los cinco riesgos corresponden a los problemas técnicos descritos en el informe. La probabilidad y el impacto se valoran para orientar su tratamiento y se revisan al cierre de cada iteración.

| ID | Fase | Riesgo | Probabilidad | Impacto | Mitigación | Responsable | Comprobación |
|---|---|---|---|---|---|---|---|
| RSK-001 | Elaboración / Construcción | La interfaz confirma una venta sin invocar la transacción del backend ni actualizar el stock compartido. | Alta | Alto | Integrar CU01 con el servicio transaccional y centralizar el guardado de venta, detalle y salida de stock. | Marco Antonio Martell Alvarez | Ejecutar una venta desde la interfaz, verificar los tres registros y comprobar que un error revierte la operación. |
| RSK-002 | Inicio / Construcción | El stock inicial puede diferir de las existencias físicas. | Alta | Alto | Realizar un conteo inicial y conciliarlo con los productos cargados antes del uso operativo. | Alejandro Horna Quezada | Comparar el conteo físico con el inventario registrado y documentar las diferencias corregidas. |
| RSK-003 | Construcción | La sesión de demostración y la autenticación JWT no están integradas, con riesgo de acceso fuera del perfil previsto. | Media | Alto | Integrar autenticación y autorización por rol, y limitar el acceso a los datos de clientes. | Isaí Samuel Bejarano Benites | Comprobar la navegación por perfil y verificar que la API rechace solicitudes no autorizadas. |
| RSK-004 | Elaboración / Construcción | El estado de una función puede diferir entre requisitos, modelos e implementación. | Alta | Alto | Contrastar SRS, casos de uso, diagramas y estado técnico mediante el checklist de coherencia. | Alonso Castillo Davalos | Revisar los requisitos priorizados y confirmar que cada documento describa el mismo comportamiento. |
| RSK-005 | Elaboración / Construcción | Las diferencias entre totales, detalles y cantidades acumuladas pueden producir reportes incorrectos o saldos de stock erróneos. | Alta | Alto | Conciliar los totales con la suma de los detalles y validar cantidades repetidas de un mismo producto antes de confirmar la venta. | Cesar Jeremin Alonso Chuquimango Reyes | Ejecutar las comprobaciones PR-01 y PR-03 y verificar que el total y el stock coincidan con los datos de la operación. |

