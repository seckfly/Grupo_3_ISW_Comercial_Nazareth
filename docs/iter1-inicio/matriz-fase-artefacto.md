# Matriz fase-artefacto

La matriz refleja la evolución prevista de cada entregable. Que una fase futura indique "Final" no significa que esa fase ya se haya ejecutado.

Estados: **Borrador** (primera versión), **Base** (contenido inicial disponible), **Refinar** (revisar o completar), **Planificado** (previsto para esa fase), **Final** (entrega al cierre de la fase), **—** (no aplica).

| Artefacto | Inicio · ITER-1 | Elaboración · ITER-2 | Construcción · ITER-3 | Transición · ITER-4 |
|---|---|---|---|---|
| Documento de Visión | Base | Refinar alcance y prioridades | Verificar contra lo implementado | Final |
| SRS breve | Base | Validar requisitos y criterios | Actualizar estados técnicos | Final |
| Casos de uso vigentes | Base | Validar actores y flujos | Ajustar según integración | Final |
| Diagrama de casos de uso | Base: PNG incorporado | Cotejar con el modelo vigente | Actualizar si cambia el alcance | Final |
| Diagrama de actividad de CU01 | Base: draw.io y SVG | Refinar con escenarios de prueba | Cotejar con el flujo implementado | Final |
| Matriz de trazabilidad | Base | Completar vínculos faltantes y criterios | Actualizar con pruebas y cambios | Final |
| Glosario | Base | Refinar términos ambiguos | Mantener nombres coherentes con la aplicación | Final |
| Checklist de coherencia | Base: revisión inicial | Actualizar tras revisión independiente | Repetir al cerrar funciones | Cierre |
| Registro de riesgos | Base: riesgos iniciales | Revisar probabilidad e impacto | Registrar evidencias de mitigación | Cierre |
| Registro de revisión | Base: observaciones documentales | Añadir revisión independiente | Registrar revisiones de código | Final |
| Diagrama de clases | — | Planificado | Refinar contra la implementación | Final |
| Diagrama de secuencia de CU01 | — | Planificado | Refinar contra la integración | Final |
| Diseño de integración | — | Planificado | Validar en la implementación | Final |
| Diagrama de estados de la orden de compra | — | Borrador si se confirma el alcance | Refinar con CU08-CU09 | Final si permanece en alcance |
| Escenarios Gherkin y casos de prueba | — | Definir criterios y escenarios | Ejecutar y adjuntar resultados | Pruebas de aceptación |
| Definición de hecho | Base documental | Ajustar al flujo de trabajo | Aplicar a cada cambio de código | Verificar antes de la entrega |
| Manual de usuario | — | Planificado | Borrador | Final |
| Datos iniciales y respaldo recuperable | — | Definir procedimiento | Preparar y probar recuperación | Validar y registrar evidencia |
| Registro de entrega | — | — | Preparar | Final |

## Reglas de uso

- El roadmap define el objetivo, los responsables propuestos y la duración estimada de cada iteración.
- Esta matriz define cuándo se prepara, revisa y cierra cada artefacto.
- La matriz de trazabilidad relaciona RF, RNF, CU, HU, artefactos y evidencia técnica; no sustituye esta matriz de fases.
- Las órdenes de compra y la recepción están especificadas en el SRS, pero su implementación sigue pendiente. El diagrama de estados de compra se mantiene condicionado a la prioridad acordada.
