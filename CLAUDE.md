# Instrucciones para Claude en este repositorio

Este proyecto se desarrolla siguiendo el proceso formal definido en `docs/sdlc/`. Lee `docs/sdlc/README.md` antes de hacer cualquier cosa en este repositorio. No improvises un proceso distinto.

## Antes de empezar cualquier trabajo

1. Mira en qué fase está el proyecto: la última acta aprobada en `docs/proyecto/puertas/` lo dice.
2. Lee el documento de esa fase en `docs/sdlc/` y respeta sus criterios de entrada.
3. Si lo que se pide corresponde a una fase posterior a la actual, dilo y no lo hagas. Propón cerrar primero la puerta pendiente.

## Reglas que no puedes saltarte

- **No escribas código de producción antes de que G1 esté aprobada.** Si hace falta explorar algo, haz un prototipo, ponlo en `prototipos/` y di por escrito que es desechable.
- **No apruebes puertas.** Las puertas las firma una persona. Tú preparas la evidencia, rellenas el acta con la plantilla `docs/plantillas/acta-de-puerta.md`, marcas qué criterios se cumplen y qué falta, y lo dejas pendiente de firma.
- **No modifiques un documento en línea base sin solicitud de cambio.** Si hay que cambiar la ERS o la arquitectura después de su puerta, abre una `SC-nnn` con la plantilla, y espera la decisión.
- **Mantén la matriz de trazabilidad al día en el mismo cambio.** Si implementas RF-012, la fila de RF-012 en `docs/proyecto/matriz-de-trazabilidad.md` se actualiza en ese mismo commit.
- **Registra las decisiones de arquitectura como ADR antes de implementarlas**, no después, y solo cuando haya alternativas reales. Numeración secuencial en `docs/proyecto/decisiones/`.
- **No metas secretos en el repositorio.** Ni claves, ni tokens, ni contraseñas, ni ficheros `.env` con valores reales.
- **No deshabilites pruebas para que pase la suite.** Si una prueba falla, o se arregla el código o se corrige la prueba justificando por qué estaba mal.

## Convenciones

- Los documentos y los commits se escriben en español. Los identificadores de código, en inglés, salvo que el proyecto decida otra cosa en un ADR.
- Identificadores: ver la tabla de `docs/sdlc/README.md`. No reutilices ni renumeres identificadores.
- Mensaje de commit: una línea de resumen que empiece por el identificador al que atiende, y un cuerpo que explique por qué.

```
RF-012: valida la entrada antes de llamar al servicio externo

El requisito exige rechazar las entradas inválidas antes de consumir cuota
del proveedor. Añade la comprobación en el adaptador y el caso de prueba
CP-031.
```

- Ramas: `feature/<id>-<descripcion>`, `fix/<id>-<descripcion>`. Ver `docs/sdlc/gestion-de-configuracion.md`.
- Documentos del proyecto en `docs/proyecto/`. El proceso y las plantillas, en `docs/sdlc/` y `docs/plantillas/`, no se tocan al trabajar en el proyecto.

## Cuándo tienes que parar y preguntar

- Falta un requisito para implementar lo que se pide, o el requisito es ambiguo.
- Lo que se pide contradice un requisito en línea base o un ADR aceptado.
- Hay que elegir entre dos diseños y la decisión tiene consecuencias que no se pueden revertir fácilmente.
- Aparecen datos personales donde la arquitectura no los había previsto.
- Lo que se pide se sale del alcance del acta de proyecto.

En estos casos, escribe la pregunta con las opciones y sus consecuencias. No elijas tú por descarte.

## Qué entregar al terminar una tarea

- El código, con sus pruebas.
- La matriz de trazabilidad actualizada.
- Los documentos afectados actualizados, con su historial de versiones.
- Un resumen de qué quedó sin hacer y por qué, si quedó algo.
- Commit y push a la rama de trabajo de la sesión.

## No inventes datos del proyecto

Si no sabes qué decide el responsable de producto sobre un requisito, un criterio de éxito o una prioridad, pregúntalo. No rellenes un documento del proyecto con contenido plausible inventado. Los huecos se marcan como `PENDIENTE: <qué falta y quién lo decide>`.
