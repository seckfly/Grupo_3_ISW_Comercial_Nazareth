# Revisión por pares: ITER-1

Revisor: Marco Antonio Martell Alvarez

Fecha: 19/10/2026

Pull Request: https://github.com/seckfly/Grupo_3_ISW_Comercial_Nazareth/pull/1

| # | Pregunta | Sí / No | Hallazgo o comentario |
|---|---|---|---|
| 1 | ¿La Visión define claramente qué incluye y qué no incluye? | Sí, con observación | Precisar el alcance de compras y recepción. |
| 2 | ¿El roadmap tiene entregables y responsable en cada iteración? | Parcialmente | Asignar los cargos a integrantes concretos. |
| 3 | ¿La matriz fase-artefacto es coherente con el roadmap? | Parcialmente | Unificar los entregables de ambos documentos. |
| 4 | ¿El diagrama muestra el flujo principal y al menos dos excepciones? | Sí, con observaciones | Completar las salidas de errores y la vinculación opcional del cliente. |
| 5 | ¿Los nombres de actores y conceptos coinciden en todos los documentos? | Sí | El señor Humberto desempeña los cuatro roles internos. |
| 6 | ¿Cada riesgo tiene mitigación y responsable? | Parcialmente | Concretar responsables y comprobación de resultados. |
| 7 | ¿Los identificadores y los commits siguen las convenciones? | Parcialmente | Referenciar las partes afectadas en los siguientes commits. |

## Respuestas del revisor

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

## Hallazgos y correcciones

| # | Hallazgo | Corrección | Estado | Commit o enlace |
|---|---|---|---|---|
| 1 | La inclusión de compras y recepción necesita una redacción más precisa. | Aclarar que pertenecen al alcance y distinguir su implementación posterior. | Por atender | |
| 2 | El roadmap y los riesgos asignan funciones sin identificar integrantes. | Asociar cada responsabilidad con un integrante del grupo. | Por atender | |
| 3 | La matriz y el roadmap difieren en algunos entregables. | Unificar la planificación de requisitos, pruebas, manual y modelo de estados de compra. | Por atender | |
| 4 | Las ramas E1, E2 y C1 del diagrama no tienen continuación. | Indicar el retorno o la terminación de cada rama. | Por atender | |
| 5 | El diagrama de actividad omite la vinculación opcional del cliente. | Representar el flujo alterno A1 mediante CU02. | Por atender | |
| 6 | Las mitigaciones no indican cómo comprobar su resultado. | Definir la comprobación correspondiente a cada medida. | Por atender | |
| 7 | Algunos commits no identifican las partes afectadas. | Incluir la referencia correspondiente en los siguientes commits. | Por aplicar | |
