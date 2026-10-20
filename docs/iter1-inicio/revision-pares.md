# Registro de revisión documental y seguimiento de hallazgos: ITER-1

Fecha de las observaciones iniciales: 19/10/2026  
Última actualización del seguimiento: 20/10/2026  
Revisor consignado en el documento original: Marco Antonio Martell Alvarez  
Pull Request: [#1 · ITER1: artefactos de Inicio para Comercial Nazareth](https://github.com/seckfly/Grupo_4_ISW_Comercial_Nazareth/pull/1)

## Estado de esta revisión

Este archivo conserva las observaciones iniciales y las respuestas registradas, y actualiza el estado de cada hallazgo. El PR #1 y sus commits figuran bajo la cuenta seckfly, con commits atribuidos a Marco Martell. Por tanto, el registro actual no acredita una revisión por pares independiente.

GitHub no muestra revisiones formales ni comentarios de revisión en el PR #1. Antes de fusionarlo, otro integrante debe revisar los cambios y registrar su evaluación en GitHub. No se han solicitado revisores ni invitado colaboradores.

| # | Pregunta | Resultado inicial | Hallazgo o comentario |
|---|---|---|---|
| 1 | ¿La Visión define claramente qué incluye y qué no incluye? | Sí, con observación | Precisar el alcance de compras y recepción. |
| 2 | ¿El roadmap tiene entregables y responsable en cada iteración? | Parcialmente | Asignar los cargos a integrantes concretos. |
| 3 | ¿La matriz fase-artefacto es coherente con el roadmap? | Parcialmente | Unificar los entregables de ambos documentos. |
| 4 | ¿El diagrama muestra el flujo principal y al menos dos excepciones? | Sí, con observaciones | Completar las salidas de errores y la vinculación opcional del cliente. |
| 5 | ¿Los nombres de actores y conceptos coinciden en todos los documentos? | Sí | El señor Humberto desempeña los cuatro roles internos. |
| 6 | ¿Cada riesgo tiene mitigación y responsable? | Parcialmente | Concretar responsables y comprobación de resultados. |
| 7 | ¿Los identificadores y los commits siguen las convenciones? | Parcialmente | Referenciar las partes afectadas en los siguientes commits. |

## Observaciones registradas

### 1. Visión y alcance

Sí, queda claro qué busca resolver el sistema y qué funciones incluye. También se entiende qué cosas quedan fuera. Lo que sí ajustaría es la parte de compras y recepción de mercadería, para que se entienda que pertenecen al proyecto, aunque todavía no estén desarrolladas. Fuera de esa precisión, mantendría el alcance.

### 2. Roadmap y responsables

La organización me parece adecuada. Cada etapa tiene un objetivo, sus entregables y un plazo, y el orden permite avanzar desde la planificación hasta la entrega. Lo que falta es colocar los nombres de los integrantes junto a las responsabilidades, porque ahora aparecen los cargos, pero no quién se encargará de cada uno.

### 3. Matriz y roadmap

En general, ambos siguen el mismo orden de trabajo. Sin embargo, hay algunos entregables que aparecen en la matriz y no están mencionados de la misma manera en el roadmap, como la revisión de requisitos y la preparación del manual. Corregiría esas diferencias para que no haya dudas sobre qué debemos presentar en cada etapa.

### 4. Diagrama de actividad

El proceso de registrar una venta se entiende y no me parece demasiado complicado. Se puede seguir el recorrido principal y reconocer qué ocurre cuando hay datos incorrectos, falta stock o falla el registro. Sí completaría las salidas de esos errores, porque algunas quedan sin indicar cómo continúa o termina el proceso. También añadiría la opción de vincular al cliente, que ya aparece descrita en el documento.

### 5. Actores y conceptos

Sí, los nombres se mantienen de forma consistente. Aunque el señor Humberto realiza todo el trabajo del negocio, tiene sentido separar sus roles según la responsabilidad que cumple en cada momento: vender, administrar, controlar el almacén o realizar compras. Eso ayuda a entender el sistema y no significa que estemos hablando de cuatro trabajadores distintos.

### 6. Riesgos

Los riesgos sí tienen medidas propuestas para atenderlos. Por ejemplo, se plantea comprobar que las ventas actualicen correctamente el inventario y revisar que los descuentos se calculen igual en todo el sistema. Me parece una buena base, pero falta asignar esas tareas a personas concretas y definir cómo comprobaremos que cada problema quedó resuelto. Tener una medida escrita todavía no significa haberla aplicado.

### 7. Convenciones

En general, los documentos y archivos siguen las convenciones del repositorio. Los identificadores permiten reconocer los requisitos, los casos de uso y los riesgos, y los mensajes de los cambios indican la iteración a la que pertenecen. Mejoraría algunos mensajes futuros para que también señalen qué parte del proyecto se modificó, cuando corresponda.

## Seguimiento de hallazgos

| # | Hallazgo | Corrección aplicada o requerida | Estado | Evidencia / siguiente paso |
|---|---|---|---|---|
| 1 | La inclusión de compras y recepción necesita una redacción más precisa. | La Visión y el SRS aclaran que forman parte del alcance especificado, pero aún no están implementadas. | Aplicado en documentación | [Visión](vision.md) y [SRS](srs-breve.md). |
| 2 | El roadmap y los riesgos asignan funciones sin identificar integrantes. | Se añadieron nombres y una distribución inicial de trabajo. | Propuesto; confirmar con el grupo | [Responsables](responsables.md). No se han invitado colaboradores. |
| 3 | La matriz y el roadmap difieren en algunos entregables. | La matriz ahora incluye los artefactos del roadmap y distingue el trabajo planificado del entregado. | Aplicado en documentación | [Matriz fase-artefacto](matriz-fase-artefacto.md) y [roadmap](roadmap.md). |
| 4 | Las ramas E1, E2 y C1 del diagrama requieren salidas claras. | La fuente editable y el SVG contienen las excepciones de stock, datos inválidos, persistencia y compensación. | Contenido actualizado; revisión visual pendiente | Comparar la geometría y los conectores de draw.io y SVG antes del cierre. |
| 5 | El diagrama de actividad omite la vinculación opcional del cliente. | El flujo documenta CU02 como alternativa cuando el comprador se identifica. | Aplicado en documentación y fuente del diagrama | [Proceso crítico CU01](proceso-critico.md). |
| 6 | Las mitigaciones no indican cómo comprobar su resultado. | Se agregó una comprobación verificable para cada riesgo. | Aplicado en documentación | [Registro de riesgos](riesgos.md). Los riesgos siguen abiertos hasta que exista evidencia. |
| 7 | Algunos commits no identifican las partes afectadas. | Se precisó la convención para incluir IDs cuando corresponda. | Convención definida; historial conservado | Los commits existentes no se reescriben. |
| 8 | La revisión registrada no es independiente. | Un integrante distinto del autor debe revisar el PR y registrar la revisión en GitHub. | Pendiente | El PR #1 no tiene revisiones formales registradas. |
| 9 | Falta el enlace del tablero de trabajo. | Añadir la URL del Trello cuando el grupo la tenga definida. | Pendiente | No se inventa una URL. |

## Condiciones para cerrar la revisión

- Un integrante distinto del autor revisa el PR #1 y registra la revisión en GitHub.
- El grupo confirma o ajusta la distribución de responsabilidades.
- Se cotejan visualmente los diagramas con el informe y sus fuentes editables.
- Se añade el enlace de Trello.
- Se actualiza el estado de cada riesgo con evidencia, sin marcar mitigaciones como completadas por el solo hecho de estar documentadas.
