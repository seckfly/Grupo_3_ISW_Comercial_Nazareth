# Proceso crítico: CU01 Registrar venta

La venta es el proceso crítico porque relaciona el cobro, el detalle de productos y el movimiento de inventario.

## Precondición

Humberto tiene una sesión administrativa activa. Los productos están activos y cuentan con precio y stock registrados.

## Flujo principal

1. Consultar el catálogo mediante CU03 y seleccionar productos y cantidades.
2. Validar que la venta contenga productos, que las cantidades sean positivas y que exista stock suficiente.
3. Calcular el total y seleccionar efectivo, Yape o Plin.
4. En efectivo, registrar el monto recibido y calcular el vuelto cuando corresponda. En pago digital, guardar la referencia de operación.
5. Guardar cabecera, detalle y salida de stock dentro de una transacción.
6. Confirmar la operación y mostrar el identificador de venta.

## Flujos alternos

- A1. Si el comprador se identifica como cliente registrado, vincularlo mediante CU02. La venta también puede continuar sin una cuenta asociada.
- A2. Si el pago en efectivo supera el total, mostrar el vuelto. Para Yape o Plin, registrar la referencia de operación.

## Excepciones y compensación

- E1. Si falta stock, indicar qué producto no tiene cantidad suficiente y rechazar el intento actual. El usuario puede iniciar una nueva selección.
- E2. Si la venta está vacía o las cantidades no son válidas, solicitar la corrección.
- E3. Si falla el guardado, no confirmar la venta.
- C1. Revertir la transacción para evitar una venta parcial o un descuento de existencias sin venta confirmada.

## Estado técnico descrito en el informe

La interfaz confirma una venta local y no invoca la transacción disponible en el backend. El cálculo de descuentos de la interfaz tampoco coincide con el cálculo base del backend.

## Diagrama de actividad

![Diagrama de actividad de CU01: Registrar venta](../../modelos/iter1/actividad-registrar-venta.svg)

Figura. Diagrama de actividad de CU01, elaborado en diagrams.net (draw.io) a partir del flujo especificado en el proyecto.
