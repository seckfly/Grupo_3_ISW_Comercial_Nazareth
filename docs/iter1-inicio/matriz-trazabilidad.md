# Matriz de trazabilidad: Comercial Nazareth

La matriz relaciona requisitos funcionales y no funcionales con casos de uso, historias de usuario, referencias técnicas y comprobaciones descritas en el informe de avance. Las referencias a componentes y rutas identifican elementos consignados en ese informe; no son archivos de código incluidos aquí. Los identificadores PR-01 a PR-19 nombran comprobaciones propuestas, no pull requests de GitHub.

## Requisitos funcionales

| RF | CU o HU | Referencia técnica y estado descrito | Comprobación propuesta |
|---|---|---|---|
| RF-01 | CU01 / HU-02, HU-03 | saleService.createSale; sales y sale_items. La interfaz confirma una venta local. | PR-01: total y stock transaccional. |
| RF-02 | CU06 / HU-04 | /api/dashboard, Product y products. La interfaz usa datos de ejemplo. | PR-02: stock menor o igual al umbral. |
| RF-03 | CU08 / HU-09 | Datos del proveedor dentro de la orden; sin servicio de compras. | PR-09: identificación obligatoria conservada en la orden. |
| RF-04 | CU08 / HU-10 | No hay servicio ni tablas de orden. | PR-10: guardar una orden no modifica el stock. |
| RF-05 | CU09 / HU-11 | inventory_movements permite registrar entradas, sin servicio de recepción. | PR-11: recepción sin duplicados. |
| RF-06 | HU-01 / acceso transversal | AuthContext, authController, autenticación y control de rol separados. | PR-06: sesión y autorización. |
| RF-07 | CU03 / HU-07 | Products, filterCatalog y endpoint /products. | PR-07: filtros y estado vacío. |
| RF-08 | CU04 / HU-06 | Promotions, Promotion y promotionService; interfaz y API separadas. | PR-08: descuento y fechas. |
| RF-09 | CU05 / HU-08 | createReservation y localStorage; no hay API de reservas. | PR-05: solicitud y código. |
| RF-10 | CU02 / HU-05 | createSale.customerId y sales.customer_id; selector de interfaz no conectado. | PR-04: venta con y sin cliente. |
| RF-11 | Consulta administrativa | Customers y mockData. | PR-12: consulta de cliente. |
| RF-12 | Consulta administrativa | Reports, Overview y /api/dashboard. | PR-13: resumen contrastado con ventas. |
| RF-13 | Configuración | Settings, User y userService. | PR-14: gestión y protección de cuenta. |
| RF-14 | Portal de clientes | ClientHome y Account; historial y puntos de ejemplo. | PR-15: historial de cuenta. |
| RF-15 | CU06 | Inventory y products; el formulario no guarda el producto. | PR-16: alta y ajuste de producto. |

## Requisitos no funcionales

| RNF | Artefacto técnico | Criterio de verificación |
|---|---|---|
| RNF-01 | SaleDrawer y servicio de venta. | PR-17: medir diez ventas simples y comprobar el límite de 15 segundos en las condiciones declaradas. |
| RNF-02 | visibleNavigation, auth y requireRole. | PR-06: comprobar la navegación por perfil y el rechazo HTTP 401/403 cuando corresponda. |
| RNF-03 | Rutas products y dashboard. | PR-18: medir diez consultas por operación y verificar el límite de tres segundos bajo el entorno declarado. |
| RNF-04 | createSale y transacción SQL. | PR-01: comprobar venta completa o reversión sin efectos parciales. |
| RNF-05 | cartSummary, paymentState y calculateSaleTotal. | PR-03: comprobar total de S/ 20,10, pago en efectivo de S/ 50,00 y vuelto de S/ 29,90, con dos decimales. |
| RNF-06 | Base comercial_nazareth y procedimiento de respaldo. | PR-19: generar una copia y comprobar la recuperación de los registros incluidos. |

La matriz conserva los estados descritos en el informe. La existencia de un artefacto o de una comprobación definida no se interpreta como evidencia de una ejecución nueva.
