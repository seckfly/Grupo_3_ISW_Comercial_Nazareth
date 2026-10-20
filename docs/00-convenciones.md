# Convenciones del repositorio

## Identificadores

- RF-##: requisito funcional.
- RNF-##: requisito no funcional.
- HU-##: historia de usuario.
- CU##: caso de uso.
- RSK-###: riesgo.
- ITER-#: iteración RUP.
- CLS-Nombre: clase del modelo.

Los identificadores conservan la numeración del informe del proyecto. No se reutiliza un ID para otro elemento.

## Carpetas y archivos

- docs/iterN-fase/: documentación de cada iteración.
- modelos/iterN/: archivos editables y exportaciones de diagramas.
- Nombres de archivo en minúsculas, con palabras separadas por guiones.
- El archivo editable y su exportación comparten el mismo nombre base.
- La documentación describe el comportamiento esperado; el estado técnico se consigna según la evidencia disponible.

## Ramas

- main conserva la línea base del repositorio.
- iter1-inicio corresponde al trabajo de Inicio.
- Las siguientes iteraciones usan ramas independientes: iter2-elaboracion, iter3-construccion e iter4-transicion.

## Commits

Formato: ITER1: descripción concreta (IDs afectados cuando corresponda).

Ejemplo: ITER1: [RF-01, CU01] documenta el flujo de venta.

## Versiones

Formato: vX.Y-iterN.

La versión de cierre de la primera iteración se identifica como v1.0-iter1.
