# Documento de Visión v1: Comercial Nazareth

## 1. Propósito

Apoyar el registro de ventas y el control de productos de Comercial Nazareth. El sistema también contempla un portal para que los clientes registrados consulten productos, promociones, historial y beneficios.

## 2. Problema

El negocio necesita consultar y actualizar ventas y existencias desde un mismo sistema. El informe del proyecto identifica brechas entre las pantallas del prototipo y los servicios del backend, por lo que la integración de ventas y la consistencia del inventario requieren trabajo adicional.

## 3. Alcance

Incluye:
- Registrar ventas, sus productos, cantidades, importes y método de pago.
- Consultar catálogo y existencias.
- Gestionar promociones e información de clientes.
- Permitir que los clientes registrados consulten su cuenta y soliciten la separación de productos.
- Especificar el registro de órdenes de compra y la recepción de mercadería.

Los casos de uso CU08 y CU09 corresponden a compras y recepción. El informe los documenta como ampliaciones pendientes de implementación.

No incluye:
- Pasarela bancaria ni confirmación automática de pagos de Yape o Plin.
- Pago a proveedores.
- Contabilidad integral.
- Facturación electrónica.
- Envío automático de órdenes a proveedores.

## 4. Interesados

| Interesado | Necesidad |
|---|---|
| Humberto Dávalos, propietario y trabajador del negocio | Registrar ventas y consultar existencias para organizar la reposición |
| Cliente registrado | Consultar catálogo, promociones, historial y beneficios; solicitar separación de productos |
| Proveedor | Recibir órdenes y entregar mercadería por el proceso comercial acordado fuera del sistema |

Humberto desempeña los roles internos descritos en el informe. No se modelan como personas diferentes.

## 5. Objetivos verificables

- Registrar una venta con cabecera, detalle, método de pago y movimiento de salida.
- Evitar confirmar una venta cuando no hay existencias suficientes.
- Mantener el stock relacionado con las ventas y las recepciones registradas.
- Restringir las funciones administrativas al perfil autorizado.
- Distinguir las solicitudes de separación de una reserva de stock confirmada.

## 6. Requisitos de alto nivel

- Registrar y consultar ventas.
- Consultar productos, precios y existencias.
- Gestionar promociones y las funciones de cuenta del cliente descritas en el informe.
- Registrar solicitudes de separación.
- Mantener productos e inventario.
- Especificar órdenes de compra y recepción de mercadería sin presentarlas como funciones ya integradas.

La lista completa de RF, RNF e historias de usuario se conserva en el informe fuente y se debe transcribir desde allí cuando se actualice la matriz de trazabilidad.

## 7. Restricciones conocidas

La interfaz de venta confirma una operación local sin invocar la transacción disponible en el backend. La política de descuentos de la interfaz tampoco coincide con el cálculo base del backend. Por ello, el flujo completo de venta no debe describirse como integrado hasta verificar la conexión y sus pruebas.

El informe identifica el negocio como Comercial Nazareth, en Ascope, La Libertad. La diferencia entre el número de grupo del informe y el nombre solicitado para este repositorio queda registrada en el control de pendientes.