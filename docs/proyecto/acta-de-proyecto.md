# Acta de proyecto — Traductor

| | |
|---|---|
| Versión | 0.2 |
| Fecha | 2026-10-15 |
| Autor | Responsable de producto, con asistencia de IA |
| Estado | borrador |

Los apartados marcados `PENDIENTE` bloquean la puerta G0. Ver `docs/proyecto/puertas/G0-concepto.md`.

## 1. Problema

El responsable de este proyecto imparte formación presencial en habilidades y competencias interpersonales a empresas. Imparte en castellano, de forma oral e interactiva. Parte de sus alumnos no habla castellano: su idioma es inglés, portugués, hindi u otros.

Hoy esos alumnos siguen la formación en un idioma que no dominan. El efecto es doble. Pierden contenido, y en una formación de habilidades pierden además lo que más importa: el matiz, el ejemplo, la dinámica de grupo. Una formación en habilidades que no se entiende con precisión no transfiere la habilidad.

La alternativa existente es contratar intérpretes humanos, con un coste por hora que esta actividad no puede absorber.

## 2. Interesados

| Papel | Quién | Qué necesita | Qué puede bloquear |
|-------|-------|--------------|--------------------|
| Usuario principal y responsable de producto | El profesor | Impartir en castellano sin cambiar su forma de dar clase | Todo |
| Usuario receptor | Los alumnos | Seguir la formación en su idioma, sin fricción para conectarse | La adopción, si el acceso es incómodo |
| Cliente contratante | La empresa que contrata la formación | Que la formación funcione en sus instalaciones y cumpla sus políticas | El uso de su red wifi, y el tratamiento de la voz de sus empleados |
| Operación | El profesor | Arrancarlo solo, en cinco minutos, antes de empezar la clase | — |

## 3. Necesidades de los interesados

| ID | Interesado | Necesidad | Prioridad |
|----|-----------|-----------|-----------|
| NEC-01 | Alumno | Recibir por audio, en su idioma y en tiempo real, lo que el profesor dice en castellano | imprescindible |
| NEC-02 | Profesor | No alterar su forma de impartir: habla seguido, interactúa, se mueve por la sala | imprescindible |
| NEC-03 | Profesor | Coste de operación nulo o próximo a cero | imprescindible |
| NEC-04 | Alumno | Conectarse sin instalar nada y sin crear cuenta | PENDIENTE: confirmar si es imprescindible o deseable |
| NEC-04b | Alumno remoto | Seguir la formación desde fuera de la sala | imprescindible |
| NEC-05 | Profesor | Arrancar y dejarlo funcionando sin asistencia técnica | imprescindible |
| NEC-06 | Empresa cliente | Que el uso sea compatible con su política de datos y de red | PENDIENTE: confirmar si alguna empresa cliente lo va a exigir por escrito |
| NEC-07 | Alumno | Hacer preguntas y ser entendido por el profesor | descartada para esta versión, decisión de 2026-10-15. Se conserva el número |

## 4. Alcance

### Entra

- Captura del audio del profesor hablando en castellano.
- Traducción de ese audio a los idiomas de destino seleccionados.
- Síntesis de voz en cada idioma de destino.
- Entrega del audio traducido al dispositivo de cada alumno, con selección de idioma por el propio alumno.
- Uso en formación presencial y en formación remota.

### No entra

- **Traducción de las intervenciones de los alumnos hacia el castellano.** Decisión de 2026-10-15: el flujo es solo de ida, del profesor a los alumnos. Las preguntas se siguen gestionando como hasta ahora. Queda como requisito aplazado con el número NEC-07 reservado.
- Traducción de documentos, presentaciones ni material de apoyo.
- Subtítulos en pantalla o en el dispositivo del alumno. Solo audio.
- Grabación y archivo de las sesiones.
- Clonación de la voz del profesor en el idioma de destino. La voz sintética será una voz genérica.
- Gestión de alumnos, asistencia o facturación.

Las cinco últimas exclusiones son propuesta de la asistencia técnica, no decisión expresa del responsable de producto. Se dan por aceptadas salvo corrección al firmar G0.

Sobre el flujo de ida conviene ser explícito: en una formación de habilidades el alumno interviene constantemente, y con esta decisión sus intervenciones quedan fuera del sistema. Es una limitación real del alcance, aceptada a cambio de que el proyecto sea abordable.

## 5. Restricciones

| ID | Tipo | Restricción | Origen |
|----|------|-------------|--------|
| RES-01 | Presupuesto | No hay presupuesto de gasto. El coste recurrente es 0 €, confirmado el 2026-10-15, y no se repercute al cliente | Responsable de producto |
| RES-02 | Funcional | El idioma de origen es siempre el castellano | Responsable de producto |
| RES-03 | Funcional | Idiomas de destino: inglés, portugués, hindi y otros. `PENDIENTE: lista cerrada` | Responsable de producto |
| RES-04 | Entorno | La formación es presencial, en instalaciones del cliente, con su red wifi o sin ella | Responsable de producto |
| RES-07 | Entorno | También hay alumnos remotos, fuera de la sala. El sistema tiene que ser accesible desde internet, lo que impide una solución exclusivamente local | Responsable de producto, 2026-10-15 |
| RES-05 | Entorno | Cada alumno necesita auriculares. Sin auriculares, varias voces sintéticas suenan a la vez en la misma sala | Análisis técnico |
| RES-06 | Técnica | El equipo disponible es el portátil del profesor. `PENDIENTE: modelo, memoria y si tiene GPU` | Análisis técnico |

## 6. Alternativas evaluadas

Las cifras de los proveedores son sus propias afirmaciones comerciales, no medidas propias. Hay que verificarlas en F2 antes de decidir. Las de coste por API provienen de comparativas de terceros publicadas en 2026 y varían entre fuentes.

| Alternativa | Coste aproximado | Por qué se descarta o se mantiene |
|-------------|------------------|-----------------------------------|
| **A. No hacer nada** | 0 € | Se mantiene como referencia. El alumno sigue perdiendo contenido |
| **B. Intérpretes humanos** | Decenas de euros por hora y por idioma | Descartada por RES-01 |
| **C. Plataforma comercial de interpretación con IA** (TraductorEnVivo, Wordly, JotMe, Vasco Audience y similares) | Desde unas decenas de euros por hora según el proveedor. Varias declaran audio traducido, acceso por código QR y latencia por debajo de 1,5 s | Incompatible con RES-01 tal como está escrita. Se mantiene abierta si el coste se puede repercutir a la empresa cliente. `PENDIENTE: decisión` |
| **D. Herramientas gratuitas existentes** | 0 € | Hay opciones con modo difusión y acceso del oyente por navegador. El problema: las que son gratuitas suelen entregar subtítulos, no audio, o limitan los minutos del plan gratuito. Hay que probarlas antes de descartar. `PENDIENTE: prueba en F1` |
| **E. Desarrollo propio con APIs de pago por uso** | Orden de magnitud: decenas de euros por curso de 4 h con 3 idiomas | Reconocimiento de voz en streaming entre 0,12 y 1,00 $/h según proveedor; síntesis de voz desde unos 0,70 $/h de audio generado, y se multiplica por cada idioma; traducción de texto aparte. Incompatible con RES-01, compatible con un modelo de repercutir coste |
| **F. Desarrollo propio autoalojado con modelos abiertos** | 0 € de coste marginal | Única opción con coste recurrente real de 0 €. Requiere hardware propio suficiente y asume más latencia: las fuentes sitúan el reconocimiento de voz en streaming entre 1 y 5 s, al que hay que sumar traducción y síntesis por cada idioma |

**Alternativa elegida: F, desarrollo propio autoalojado con modelos abiertos.** Decisión derivada de la respuesta del 2026-10-15: el coste no se puede repercutir al cliente y el presupuesto es 0 € real. Eso descarta B, C y E, que tienen coste por minuto o por hora.

La alternativa D sigue viva, y no como formalidad: antes de escribir una línea de código de producción hay que probar las herramientas gratuitas con modo difusión en una sesión real. Si alguna entrega audio traducido a varios idiomas dentro del plan gratuito, sustituye a F y el proyecto se reduce a aprender a usarla. Es la primera tarea de F1 y puede cerrar el proyecto antes de empezarlo.

La combinación de RES-01 y RES-07 es la restricción más dura del proyecto: coste cero y alumnos conectados desde fuera de la sala. Obliga a que todo el procesamiento ocurra en el equipo del profesor y a exponerlo a internet por un medio también gratuito. Es posible, y deja dos límites que habrá que medir en F1: el ancho de banda de subida disponible en las instalaciones del cliente, y cuántos alumnos remotos aguanta antes de degradarse.

## 7. Criterios de éxito

"Que cumpla con su cometido" no es un criterio verificable, y sin criterios verificables la fase F4 no puede cerrarse: no habría forma de decir si el sistema sirve. Lo que sigue es una propuesta de criterios con valores a confirmar.

| ID | Criterio | Valor objetivo propuesto | Cómo se mide | Cuándo |
|----|----------|--------------------------|--------------|--------|
| CE-01 | Retardo entre la frase hablada y su audio traducido | ≤ 5 s de media. Confirmado el 2026-10-15 | Cronometrado sobre grabación, 20 frases de muestra | F4 y primera sesión real |
| CE-02 | El alumno puede seguir la formación | ≥ 80 % de los alumnos responden que pudieron seguirla sin perder contenido relevante. `PENDIENTE: confirmar` | Una pregunta al final de la sesión | Primeras 3 sesiones reales |
| CE-03 | Coste por sesión | 0 €. Confirmado el 2026-10-15 | Factura del proveedor, si hay alguno | Mensual |
| CE-04 | Tiempo de alta del alumno | ≤ 2 min, sin instalar nada. `PENDIENTE: confirmar` | Cronometrado con 3 alumnos reales | F4 |
| CE-05 | Continuidad | Una sesión de 4 h sin cortes que obliguen a detener la clase | Registro de incidencias de la sesión | Primeras 3 sesiones reales |
| CE-06 | Fidelidad terminológica | El vocabulario propio de la materia se traduce de forma correcta y estable. `PENDIENTE: definir cómo se mide` | Lista de 30 términos de referencia, revisada por un hablante del idioma | F4 |

CE-06 es el criterio con más riesgo de los seis. Una formación en habilidades vive de ejemplos, matices y juegos de palabras, y es justo lo que peor traduce una máquina.

## 8. Presupuesto y plazo

| | |
|---|---|
| Presupuesto de gasto | 0 € |
| Esfuerzo propio disponible | PENDIENTE: horas a la semana |
| Fecha objetivo de primera prueba real | PENDIENTE |
| ¿Hay una formación concreta en el calendario que sea el objetivo? | PENDIENTE |

La última pregunta importa más de lo que parece: una fecha real con alumnos reales ordena las prioridades mejor que cualquier plan.

## 9. Tratamiento de datos personales

¿El sistema trata datos personales? **Sí**, aunque no trate documentos.

El responsable de producto indicó que no va a tratar documentos con datos personales, y así es. Pero la voz de una persona identificada es un dato personal por sí misma, y el sistema captura voz de forma continua:

- **Voz del profesor.** Es su propia voz, y la trata él. Riesgo bajo.
- **Voz de los alumnos.** Si en algún momento el sistema capta las intervenciones de los alumnos, aunque sea de forma incidental porque el micrófono está abierto en la sala, se están tratando datos personales de empleados de una empresa cliente.
- **Contenido de lo que se dice.** En una formación de habilidades aparecen situaciones laborales concretas, conflictos y a veces nombres de compañeros. Eso no es anecdótico.

Lo que se deriva, y hay que resolver en F1 y F2:

| Cuestión | Estado |
|----------|--------|
| Base jurídica para captar la voz de los alumnos | PENDIENTE |
| Información a los alumnos antes de empezar | PENDIENTE: previsible un aviso verbal y un cartel |
| Retención | Objetivo: cero. Procesamiento en tránsito, sin grabar ni almacenar |
| Transferencia internacional | Depende de la alternativa. Un proveedor fuera del Espacio Económico Europeo introduce una transferencia que hay que justificar. Una solución autoalojada la elimina por completo |
| Encargado del tratamiento | Si se usa un proveedor en la nube, hace falta su contrato de encargo |
| Posición de la empresa cliente | PENDIENTE: alguna puede exigir que el audio no salga de su red |

Esto no es un obstáculo para el proyecto, y es un argumento de peso a favor de la alternativa F: si todo ocurre en el portátil del profesor, la mayor parte del problema desaparece.

## 10. Historial

| Versión | Fecha | Autor | Cambio | SC |
|---------|-------|-------|--------|----|
| 0.1 | 2026-10-15 | Responsable de producto, con asistencia de IA | Versión inicial. Alternativas documentadas con fuentes externas. Huecos marcados PENDIENTE | — |
| 0.2 | 2026-10-15 | Responsable de producto, con asistencia de IA | Decisiones del responsable de producto: presupuesto 0 € sin repercutir, flujo solo de ida, retardo máximo 5 s, formación presencial y remota. Alternativa F elegida. Nueva restricción RES-07 | — |
