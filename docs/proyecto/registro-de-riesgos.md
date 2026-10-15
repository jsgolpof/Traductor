# Registro de riesgos — Traductor

| | |
|---|---|
| Versión | 0.1 |
| Fecha | 2026-10-15 |
| Estado | vivo |

## Escalas

Probabilidad: 1 improbable, 2 posible, 3 probable, 4 muy probable.
Impacto: 1 menor, 2 moderado, 3 grave, 4 crítico.
Exposición = probabilidad × impacto. A partir de 9 exige respuesta asignada con responsable y fecha.

## Riesgos abiertos

| ID | Riesgo | Causa | Efecto si ocurre | P | I | Exp | Estrategia | Respuesta | Responsable | Revisión |
|----|--------|-------|------------------|---|---|-----|------------|-----------|-------------|----------|
| R-01 | El presupuesto de 0 € es incompatible con las alternativas que funcionan hoy | La traducción de voz en tiempo real tiene coste por minuto en todos los proveedores comerciales | El proyecto se queda sin alternativa viable, o se elige la autoalojada por descarte y no por mérito | 4 | 3 | 12 | reducir | Decidir en G0 si el coste se puede repercutir a la empresa cliente. Si la respuesta es no, aceptar la alternativa F y su mayor latencia | Producto | G0 |
| R-02 | La latencia hace el sistema inservible para una formación interactiva | Reconocimiento de voz, traducción y síntesis se suman en cadena, y la síntesis se multiplica por idioma | El alumno recibe la frase cuando el profesor ya ha cambiado de tema. El sistema se abandona tras la primera clase | 3 | 4 | 12 | reducir | Medir la latencia real en un prototipo desechable en F1, antes de diseñar nada. Fijar el umbral tolerable como requisito | Técnico | F1 |
| R-03 | La traducción falla justo en lo que importa: matices, ejemplos, juegos de palabras | La materia es habilidades interpersonales, no contenido técnico con terminología estable | El alumno entiende las palabras y no el contenido. El sistema aparenta funcionar y no funciona | 3 | 3 | 9 | reducir | CE-06: lista de 30 términos y expresiones de referencia, revisada por un hablante nativo de cada idioma | Producto | F4 |
| R-04 | La red wifi del cliente no sirve: ancho de banda, portal cautivo, restricciones de la empresa | La formación es en instalaciones ajenas, con una red que el profesor no controla | La clase empieza sin sistema, delante de los alumnos | 3 | 3 | 9 | evitar | Diseñar para funcionar en red local propia, sin depender de internet ni de la red del cliente. Es un requisito, no una preferencia | Técnico | F2 |
| R-05 | El portátil no da para varios idiomas simultáneos | La alternativa autoalojada ejecuta reconocimiento, traducción y una síntesis por idioma, a la vez, mientras el profesor da clase | Se limita el número de idiomas simultáneos, o hay cortes de audio | 3 | 3 | 9 | reducir | Medir en el prototipo de F1 con el hardware real. Si no da, decidir entre limitar idiomas o repercutir coste | Técnico | F1 |
| R-06 | Se construye algo que ya existe, gratis o barato | No se han probado a fondo las herramientas gratuitas con modo difusión | Semanas de trabajo propio tiradas | 3 | 3 | 9 | evitar | Probar las candidatas de la alternativa D en una sesión real antes de escribir código. Es una tarea de F1, y puede cerrar el proyecto | Producto | F1 |
| R-07 | Dedicación insuficiente | El proyecto compite con la actividad profesional que lo financia | El proyecto queda a medias y la primera formación multilingüe llega sin solución | 3 | 3 | 9 | aceptar | Fijar un alcance mínimo atado a una fecha de formación real | Producto | G0 |
| R-08 | Tratamiento de la voz de los alumnos sin base jurídica ni información previa | El micrófono está abierto en la sala, y la voz es dato personal | Reclamación de un alumno o de la empresa cliente, con el agravante de que el profesor presta servicio a empresas | 2 | 4 | 8 | evitar | Resolver en F1: base jurídica, aviso previo, retención cero. Preferir la alternativa que no saque el audio de la sala | Producto | F1 |
| R-09 | Los alumnos no llevan auriculares | No se ha previsto como requisito material de la formación | Varias voces sintéticas suenan a la vez sobre la voz del profesor. La sala se vuelve inutilizable | 3 | 2 | 6 | evitar | Incluir los auriculares en los requisitos previos que se comunican a la empresa cliente antes de la formación | Producto | F2 |
| R-10 | El proveedor gratuito cambia condiciones, mete límites o cierra | Los planes gratuitos de este sector son promocionales | El sistema deja de funcionar sin aviso, posiblemente el día de una formación | 3 | 2 | 6 | reducir | Si se elige un proveedor externo, tener un camino de salida probado hacia la alternativa autoalojada | Técnico | F2 |
| R-11 | La calidad de la síntesis de voz es desigual entre idiomas | La oferta de voces y su naturalidad varía mucho según el idioma, y el hindi no está al nivel del inglés | Unos alumnos reciben un servicio claramente peor que otros | 3 | 2 | 6 | reducir | Evaluar la síntesis idioma por idioma en F1, con la lista cerrada de RES-03 | Técnico | F1 |

## Riesgos cerrados

| ID | Riesgo | Cierre | Fecha | Se materializó | Qué se aprendió |
|----|--------|--------|-------|----------------|-----------------|
| — | | | | | |

## Observaciones

Los cuatro riesgos de exposición más alta (R-01, R-02, R-05, R-06) se resuelven con lo mismo: un prototipo desechable en F1 que mida latencia y consumo con el hardware real, y una prueba de las herramientas que ya existen. Antes de eso, cualquier decisión de arquitectura sería una apuesta.

## Historial

| Versión | Fecha | Autor | Cambio |
|---------|-------|-------|--------|
| 0.1 | 2026-10-15 | Responsable de producto, con asistencia de IA | Apertura del registro en F0, con 11 riesgos |
