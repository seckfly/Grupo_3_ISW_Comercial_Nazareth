# Proceso crítico: CU01 Registrar venta

## Motivo de selección

Una venta afecta el importe cobrado, el detalle registrado y las existencias. El informe identifica una brecha entre la interfaz y la transacción del backend, por lo que la integración de este flujo es un riesgo principal.

## Precondición

Sesión del perfil administrativo de Humberto; productos activos con precio y stock registrados.

## Flujo principal

1. Seleccionar productos y cantidades mediante la consulta de catálogo CU03.
2. Comprobar que los productos estén activos y tengan stock suficiente.
3. Calcular el total y elegir efectivo, Yape o Plin.
4. Registrar el monto recibido en efectivo o la referencia del pago digital.
5. Guardar la cabecera y el detalle de la venta, registrar los movimientos y descontar las existencias.
6. Confirmar la operación y mostrar la identificación de la venta.

## Alternativas y excepciones

- A1. Si el comprador está registrado, vincularlo mediante CU02. Si no tiene cuenta, continuar sin vincular cliente.
- A2. En efectivo, mostrar el vuelto cuando corresponda. En pagos digitales, solicitar la referencia de seis dígitos.
- E1. Si el stock es insuficiente, rechazar la operación.
- E2. Si la venta está vacía o el método de pago no está admitido, solicitar la corrección.
- E3. Si falla la persistencia, revertir la transacción para evitar una venta parcial.
- C1. Si falla el registro dentro de la transacción, no dejar existencias descontadas sin una venta confirmada.

El ticket imprimible se describe como comprobante interno.

## Estado de implementación

El informe indica que el backend contiene la transacción, pero la interfaz confirma una venta local sin invocarla. También indica que la política de descuentos de la interfaz no se aplica en el cálculo base del backend. El diagrama representa el flujo especificado; no demuestra que la integración esté terminada.