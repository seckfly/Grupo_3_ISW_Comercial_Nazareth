# SRS breve: Comercial Nazareth

Este documento resume el alcance y el caso de uso crítico para la iteración de Inicio. No sustituye las tablas completas de RF, RNF e historias de usuario del informe fuente.

## Funciones y casos de uso

| Caso de uso | Nombre del informe | Alcance documentado |
|---|---|---|
| CU01 | Registrar venta | Registrar productos, cantidades, total y método de pago; guardar el detalle y el movimiento de salida |
| CU02 | Vincular cliente a la venta | Asociar un cliente registrado cuando corresponda; la venta puede continuar sin una cuenta vinculada |
| CU03 | Consultar catálogo | Consultar productos para apoyar la venta y el portal |
| CU04 | Gestionar promociones | Administrar las promociones del negocio |
| CU05 | Reservar producto (Separación en tienda) | Registrar una solicitud de separación; el prototipo no garantiza el bloqueo del stock |
| CU06 | Gestionar inventario | Mantener productos y existencias |
| CU08 | Registrar orden de compra | Función especificada como ampliación, pendiente de implementación |
| CU09 | Gestionar compras (Recepción de mercadería) | Registrar la recepción de mercadería como ampliación, pendiente de implementación |

CU07 no forma parte del modelo vigente del informe actualizado.

## CU01: condiciones y trazabilidad

Precondición: sesión del perfil administrativo de Humberto y productos activos con precio y stock registrados.

Postcondición: venta y detalle guardados, stock disminuido y movimiento de salida registrado.

Trazabilidad reportada para CU01: RF-01, RF-07, RF-10, RNF-01, RNF-04 y RNF-05.

## Requisitos no funcionales recuperados del informe

- RNF-01: una venta simple de hasta tres líneas debe poder confirmarse en menos de 15 segundos, sin contar la espera de un pago externo.
- RNF-02: las opciones administrativas deben quedar fuera de la navegación del perfil cliente y las operaciones protegidas deben rechazar un rol no autorizado.
- RNF-03: productos, stock y resumen deben responder en tres segundos o menos con un usuario concurrente y el catálogo de demostración en entorno local.

El informe contiene 15 RF, 6 RNF y 11 historias de usuario. No se reconstruyen aquí los textos de los requisitos que no están transcritos en este documento. Antes de declarar completa la matriz, hay que cotejar los textos y prioridades restantes con el informe actualizado.