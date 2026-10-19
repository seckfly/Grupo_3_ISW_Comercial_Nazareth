# SRS breve: Comercial Nazareth

## Requisitos funcionales

| ID | Requisito | Comportamiento requerido | CU | Estado técnico |
|---|---|---|---|---|
| RF-01 | Registrar venta | Registrar productos, cantidades y método de pago; calcular el total y conservar venta, detalle y salida de stock en una operación. | CU01 | Servicio transaccional disponible; la interfaz confirma una venta local. |
| RF-02 | Consultar existencias y alertas | Mostrar el stock y señalar productos activos cuya cantidad sea menor o igual al umbral mínimo configurado. | CU06 | Consulta API disponible; la interfaz usa datos de ejemplo. |
| RF-03 | Identificar proveedor de la orden | Guardar razón social, RUC y teléfono del proveedor dentro de la orden, sin exigir un catálogo independiente. | CU08 | Especificado; sin servicio de compras. |
| RF-04 | Registrar orden de compra | Conservar proveedor, productos, cantidades, costos y estado pendiente, recibida o anulada; calcular el total estimado. | CU08 | Especificado; sin implementación. |
| RF-05 | Registrar recepción | Registrar cantidades recibidas de una orden pendiente, aumentar el stock y crear movimientos de entrada en una transacción. | CU09 | Especificado; no existe servicio de recepción. |
| RF-06 | Acceder según perfil | Permitir inicio y cierre de sesión y mostrar la navegación correspondiente al perfil administrativo o al cliente registrado. | Transversal | Sesión de demostración local y autenticación JWT separada. |
| RF-07 | Consultar catálogo | Buscar productos por nombre y categoría, mostrar precio y disponibilidad, y permitir favoritos y listas en el portal. | CU03 | Catálogo local; endpoint de consulta disponible. |
| RF-08 | Gestionar promociones | Crear, editar, pausar, activar y eliminar campañas por producto, con descuento, vigencia y estado. | CU04 | CRUD local y endpoints separados. |
| RF-09 | Solicitar separación | Crear una solicitud con productos, importe estimado y código, conservando el estado pendiente de confirmación. | CU05 | Solicitud local; sin API de reservas. |
| RF-10 | Vincular cliente a la venta | Asociar un cliente registrado cuando se identifique y permitir ventas sin cliente vinculado. | CU02 | API admite customerId opcional; selector de interfaz pendiente. |
| RF-11 | Consultar clientes frecuentes | Mostrar nombre, contacto, frecuencia e historial básico de clientes identificados. | Consulta administrativa | Vista con datos de ejemplo; sin ruta de clientes. |
| RF-12 | Consultar resumen y reportes | Mostrar ventas, métodos de pago y productos con movimiento por periodo. | Consulta administrativa | Resumen API parcial; reportes de interfaz con datos de ejemplo. |
| RF-13 | Administrar accesos | Registrar, editar y desactivar cuentas con rol autorizado y proteger la cuenta administrativa. | Transversal | Gestión local y endpoints separados, sin sincronización. |
| RF-14 | Consultar cuenta y beneficios | Mostrar al cliente registrado sus datos, historial de compras y puntos asociados a su cuenta. | Portal de clientes | Vista de referencia con puntos e historial predeterminados. |
| RF-15 | Mantener productos e inventario | Registrar y actualizar productos, precios y stock inicial; permitir ajustes autorizados sin perder el historial. | CU06 | Formulario visual y tabla products; guardado y ajustes pendientes. |

## Casos de uso

| ID | Nombre | Actor | Requisitos relacionados |
|---|---|---|---|
| CU01 | Registrar venta | Vendedor | RF-01, RF-07, RF-10 |
| CU02 | Vincular cliente a la venta | Vendedor, dentro de CU01 | RF-10 |
| CU03 | Consultar catálogo | Cliente registrado, Vendedor y Responsable de compras | RF-07 |
| CU04 | Gestionar promociones | Administrador | RF-08 |
| CU05 | Reservar producto (Separación en tienda) | Cliente registrado | RF-09 |
| CU06 | Gestionar inventario | Responsable de almacén | RF-02, RF-15 |
| CU08 | Registrar orden de compra | Responsable de compras | RF-03, RF-04, RF-07 |
| CU09 | Gestionar compras (Recepción de mercadería) | Responsable de compras | RF-05 |

CU01 incluye CU03. CU02 extiende CU01 cuando el comprador se identifica como cliente registrado. CU05 y CU08 incluyen CU03. CU08 extiende CU06 cuando el stock está por debajo del mínimo y Humberto decide reponer. La recepción requiere una orden pendiente.

## Requisitos no funcionales

| ID | Requisito | Criterio de aceptación |
|---|---|---|
| RNF-01 | Rapidez de registro | Una venta de hasta tres líneas, con precios cargados y un administrador, se confirma en menos de 15 segundos, sin contar la espera de un pago externo. |
| RNF-02 | Separación de perfiles | El 100 % de las opciones administrativas queda fuera de la navegación del perfil cliente y las operaciones protegidas rechazan roles no autorizados. |
| RNF-03 | Tiempo de consulta | Productos, stock y resumen responden en tres segundos o menos, con un usuario concurrente y el catálogo de demostración en entorno local. |
| RNF-04 | Integridad de venta | El 100 % de las ventas aceptadas conserva venta, detalle y movimiento. Ante un error, ninguna modificación queda confirmada parcialmente. |
| RNF-05 | Consistencia monetaria | Totales y subtotales usan dos decimales, con diferencia admitida de S/ 0,00 respecto del cálculo redondeado. |
| RNF-06 | Respaldo recuperable | Conservar al menos una copia de la base de datos al cierre de cada jornada y recuperar una copia de prueba con las ventas incluidas. |

## Reglas del negocio

- RB-01: Yape y Plin se registran como método de pago. El código de operación no confirma el pago bancario.
- RB-02: la venta usa el precio consultado por el servicio y redondea a dos decimales. El cálculo de descuentos debe coincidir entre interfaz y backend.
- RB-03: una venta puede registrarse sin cliente asociado.
- RB-04: una orden de compra no aumenta el stock. El incremento ocurre al confirmar la recepción.
- RB-05: una solicitud de separación no confirma una venta ni garantiza el bloqueo de existencias.
- RB-06: la alerta muestra stock menor o igual al mínimo; la decisión de crear una orden se toma cuando el stock está por debajo del mínimo.
- RB-07: los datos del proveedor se guardan en la orden. El proveedor no tiene credenciales ni un caso de uso independiente.
- RB-08: una recepción parcial mantiene la orden pendiente y acumula cantidades recibidas. Se rechazan referencias duplicadas y cantidades superiores al saldo por recibir.