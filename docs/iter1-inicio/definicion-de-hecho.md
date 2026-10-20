# Definición de hecho

Estos controles se acordaron para considerar terminado un cambio funcional del proyecto. Se aplican cuando el repositorio incorpore código y pruebas; la documentación por sí sola no demuestra que una función esté terminada.

| # | Control | Evidencia requerida |
|---|---|---|
| 1 | Código revisado mediante un pull request aprobado. | Revisión registrada por una persona distinta del autor. |
| 2 | Pruebas Vitest/Node aprobadas. | Resultado de ejecución sin pruebas fallidas. |
| 3 | Escenarios de aceptación Gherkin ejecutados. | Escenarios y resultados registrados, incluidos los casos alternos relevantes. |
| 4 | Autenticación JWT y protección por rol verificadas. | Pruebas de acceso permitido y rechazado en interfaz y API. |
| 5 | Cambios del esquema SQL documentados. | Script o migración revisada y documentación de la base actualizada. |
| 6 | Compilación de frontend correcta. | Ejecución de vite build sin errores. |
| 7 | README y DATABASE.md actualizados. | Documentación coherente con el comportamiento implementado y la estructura real de la base. |

## Aplicación al estado actual

El PR #1 contiene documentos y modelos de ITER-1, no una entrega funcional de frontend, backend y base de datos. Por tanto, los controles de código, pruebas, JWT, SQL y compilación quedan pendientes hasta que se incorpore el código correspondiente. La revisión documental de este PR tampoco sustituye una revisión por pares independiente.

No se debe cerrar un requisito como implementado por tener un diagrama, una pantalla de referencia o una prueba aislada. Debe comprobarse el comportamiento que exige la matriz de trazabilidad.
