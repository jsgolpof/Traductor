# Gestión de configuración

Qué está bajo control, cómo se versiona y cómo se identifica lo que hay desplegado.

## Elementos bajo control de configuración

| Elemento | Dónde | Control |
|----------|-------|---------|
| Código fuente | repositorio | Git, rama por cambio |
| Documentos del proyecto | `docs/proyecto/` | Git, versión en el encabezado del documento |
| Proceso y plantillas | `docs/sdlc/`, `docs/plantillas/` | Git |
| Configuración de entornos | repositorio, sin secretos | Git |
| Secretos | gestor de secretos o variables de entorno | Nunca en el repositorio |
| Dependencias | fichero de bloqueo de versiones | Git, versiones fijadas |

## Ramas

- `main`: refleja lo que está en producción o listo para estarlo. Siempre compila y pasa las pruebas.
- `feature/<id>-<descripcion>`: un requisito o un cambio. El identificador es el del requisito, la incidencia o la solicitud de cambio.
- `fix/<id>-<descripcion>`: corrección de una incidencia.
- `claude/<nombre>`: ramas de trabajo de las sesiones de asistente de IA.

Una rama se integra en `main` cuando sus pruebas pasan y el diff está revisado.

## Versionado

Versionado semántico `MAYOR.MENOR.PARCHE`:

- MAYOR: cambio incompatible para quien usa el sistema o su interfaz.
- MENOR: funcionalidad nueva compatible.
- PARCHE: corrección sin cambio de comportamiento previsto.

Cada versión desplegada se etiqueta en Git y se anota en el registro de despliegues con la fecha y el identificador del commit.

## Versionado de documentos

Cada documento del proyecto lleva en su encabezado: versión, fecha, autor y estado (borrador, en revisión, línea base, obsoleto). Un documento en línea base solo se modifica mediante una solicitud de cambio aprobada, y al modificarse sube su versión y deja constancia en su historial.

## Historial en los documentos

Al final de cada documento del proyecto:

| Versión | Fecha | Autor | Cambio | SC |
|---------|-------|-------|--------|----|
| 1.0 | | | Versión inicial, línea base en G1 | — |
