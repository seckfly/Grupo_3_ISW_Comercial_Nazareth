# Convenciones del repositorio

## Identificadores

- RF-##: requisito funcional.
- RNF-##: requisito no funcional.
- HU-##: historia de usuario.
- CU##: caso de uso.
- RSK-###: riesgo.
- ITER-#: iteración RUP.
- CLS-Nombre: clase del modelo.

Los identificadores RF, RNF, HU y CU conservan el significado del informe del proyecto. CU07 no forma parte del modelo vigente; no se reutiliza ese identificador para otro caso de uso.

## Carpetas y archivos

- docs/iterN-fase/: documentos de cada iteración.
- modelos/iterN/: fuentes y exportaciones de diagramas.
- Nombres de archivo en minúsculas y separados por guiones.
- Los diagramas usan el mismo nombre base para el archivo editable y la exportación.
- Mantener la documentación técnica separada del código ejecutable; indicar cuándo un elemento es solo una especificación o una vista de referencia.

## Commits

Formato: ITER1: descripción concreta (IDs afectados cuando corresponda).

Ejemplo: ITER1: [RF-01, CU01] documenta el flujo de venta.

No reescribir el historial para corregir mensajes anteriores. Aplicar la convención a los cambios nuevos.

## Versiones

Formato del tag: vX.Y-iterN.

Tag de cierre de la primera iteración: v1.0-iter1. Publicarlo solo después de la revisión independiente, el cierre de los puntos pendientes y la fusión del PR.
