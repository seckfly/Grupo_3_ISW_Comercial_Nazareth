# Checklist de coherencia

Este checklist distingue los puntos comprobados de los que todavía necesitan evidencia. No se marca como conforme una tarea solo porque exista un documento que la mencione.

| # | Verificación | Resultado | Observación |
|---|---|---|---|
| 1 | La Visión delimita qué incluye y qué queda fuera. | Conforme | Compras y recepción están dentro del alcance especificado, pero no se presentan como funciones implementadas. |
| 2 | El roadmap define entregables, responsables y duración. | Parcial | Se añadieron nombres como propuesta operativa. Falta confirmarlos con el grupo; las semanas son estimaciones, no fechas acordadas. |
| 3 | La matriz fase-artefacto coincide con el roadmap. | Conforme tras actualización | Se incorporaron trazabilidad, glosario, checklist, riesgos, revisión, integración, pruebas, manual y entrega. |
| 4 | El diagrama de actividad muestra el flujo principal y las excepciones. | Parcial | La fuente editable contiene las ramas de falta de stock, datos inválidos, error de persistencia y compensación. Falta una revisión visual final independiente de los conectores y la exportación. |
| 5 | Los términos y actores se nombran de forma consistente. | Conforme | Humberto desempeña los cuatro roles internos; el proveedor no tiene acceso a la aplicación. |
| 6 | Los requisitos conservan los identificadores del informe. | Conforme | Se mantienen RF-01 a RF-15 y RNF-01 a RNF-06. |
| 7 | Los casos de uso conservan los identificadores del modelo vigente. | Conforme | Se documentan CU01-CU06, CU08 y CU09. CU07 no forma parte del modelo vigente. |
| 8 | El diagrama de casos de uso está incorporado al repositorio. | Parcial | El archivo PNG existe. Antes del cierre debe cotejarse visualmente con la versión final del informe y con los identificadores del SRS. |
| 9 | La documentación identifica al equipo como Grupo 4. | Conforme | README y documentos de ITER-1 usan Grupo 4. |
| 10 | El SVG corresponde al archivo editable de CU01. | Parcial | Ambos archivos contienen los elementos principales. Falta una comprobación visual final de la geometría y los conectores. |
| 11 | La documentación distingue implementación, datos locales y funciones especificadas. | Conforme | El SRS identifica los estados técnicos y señala las integraciones pendientes. |
| 12 | Cada riesgo tiene una mitigación y una forma de comprobarla. | Conforme en documentación | Se añadió una comprobación por riesgo. Las mitigaciones siguen abiertas hasta que exista evidencia de ejecución. |
| 13 | Existe una revisión por pares independiente en el PR. | Pendiente | El PR #1 no tiene revisiones formales registradas en GitHub. El registro documental existente no sustituye la revisión de otro integrante. |
| 14 | El enlace de Trello está incluido. | Pendiente | El repositorio todavía no contiene la URL del tablero. |
| 15 | Se puede publicar v1.0-iter1. | Pendiente | Esperar revisión independiente, validaciones finales y cierre del PR. |
| 16 | La regla de reposición es inequívoca en el límite del stock mínimo. | Pendiente de confirmar | La alerta se activa con stock menor o igual al umbral, mientras que la decisión de reposición se describe para stock inferior al umbral. Confirmar el comportamiento cuando ambos valores son iguales. |

## Condición de cierre

ITER-1 no se considera cerrada hasta resolver los puntos pendientes o registrar explícitamente por qué alguno se traslada a la siguiente iteración.
