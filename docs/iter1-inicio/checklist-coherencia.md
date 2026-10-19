# Checklist de coherencia

Estado: revisión documental inicial. No equivale a una revisión por pares ni a una prueba del sistema integrado.

| # | Verificación | Estado | Observación |
|---|---|---|---|
| 1 | Visión, SRS y diagrama usan el mismo nombre para el proceso crítico. | Conforme | Se usa CU01 Registrar venta. |
| 2 | Las alternativas del proceso aparecen en la descripción de CU01. | Conforme | Se documentan A1, A2, E1, E2, E3 y C1. |
| 3 | La documentación distingue el alcance implementado del especificado. | Conforme | CU08 y CU09 se identifican como ampliaciones pendientes. |
| 4 | La venta se describe como integrada con el backend. | Pendiente | El informe señala que la interfaz confirma una venta local sin invocar la transacción del backend. |
| 5 | La regla de descuentos coincide entre interfaz y backend. | Pendiente | El informe señala una diferencia que debe corregirse y probarse. |
| 6 | Las tablas completas de RF, RNF e historias están trazadas. | Pendiente | El SRS breve conserva los identificadores recuperados; faltan cotejar los textos completos del informe. |
| 7 | El número de grupo coincide entre el informe y el nombre del repositorio. | Pendiente | El informe base identifica al equipo como Grupo 4; el repositorio solicitado se llama Grupo 3. Confirmar antes de la entrega académica. |
| 8 | Se completó la revisión por pares. | Pendiente | No se registra una revisión hasta que una persona revise el PR y deje comentarios. |

## Criterio de cierre

Los pendientes deben resolverse con el informe fuente, el código o una revisión real. No se marcarán como conformes por asumir que la función existe.