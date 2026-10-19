# Documento de Visión v1: Comercial Nazareth

## 1. Propósito

Organizar el registro de ventas y el control de productos de Comercial Nazareth, con un portal para clientes registrados.

## 2. Problema

Las ventas se anotan en cuadernos y las existencias se estiman mediante revisión visual. Humberto Dávalos, propietario y único trabajador, necesita relacionar las ventas con el stock para saber qué productos reponer y en qué cantidad.

## 3. Alcance

Incluye:
- Registrar ventas, productos, cantidades, importes y métodos de pago.
- Consultar productos, precios, existencias y alertas por stock mínimo.
- Mantener productos e inventario.
- Gestionar promociones.
- Permitir que los clientes registrados consulten el catálogo, sus datos, historial y beneficios.
- Registrar solicitudes de separación de productos.
- Consultar resúmenes de ventas y administrar cuentas según el perfil.
- Especificar las órdenes de compra y la recepción de mercadería.

No incluye:
- Procesamiento bancario o confirmación automática de pagos de Yape y Plin.
- Pagos a proveedores.
- Facturación electrónica.
- Contabilidad integral ni apertura y cierre formal de caja.
- Cuentas de acceso para proveedores.
- Notificaciones automáticas.
- Detección de stock mediante cámaras.

Las funciones de compra y recepción están especificadas, pero no implementadas en el avance técnico. La solicitud de separación no garantiza que el stock quede bloqueado.

## 4. Interesados

| Interesado | Necesidad |
|---|---|
| Humberto Dávalos | Registrar ventas, controlar existencias y decidir la reposición. Desempeña los roles internos de Vendedor, Administrador, Responsable de almacén y Responsable de compras. |
| Cliente registrado | Consultar productos, promociones, historial y beneficios, y solicitar separaciones. |
| Comprador sin registro | Comprar en tienda sin crear una cuenta. |
| Proveedor | Entregar mercadería y coordinar la compra con Humberto fuera de la aplicación. |

## 5. Criterios de éxito

- El total de una venta coincide con la suma de sus líneas, redondeada a dos decimales.
- Una venta confirmada descuenta la cantidad vendida; una operación rechazada no deja movimientos parciales.
- La consulta de alertas incluye productos activos con stock menor o igual al umbral configurado.
- Una venta simple de hasta tres líneas puede confirmarse en menos de 15 segundos, sin contar la espera de un pago externo.

## 6. Requisitos de alto nivel

- RF-01 a RF-05: ventas, existencias y abastecimiento especificado.
- RF-06: acceso según perfil.
- RF-07 y RF-08: catálogo y promociones.
- RF-09 y RF-10: separación de productos y vinculación opcional del cliente.
- RF-11 y RF-12: consulta de clientes frecuentes, resumen y reportes.
- RF-13 y RF-14: administración de accesos y portal de clientes.
- RF-15: mantenimiento de productos e inventario.

## 7. Restricciones

El sistema usa React/Vite, Express y MySQL. Yape y Plin se registran como método de pago; la referencia de operación no confirma una transacción bancaria. El proveedor no accede al sistema.