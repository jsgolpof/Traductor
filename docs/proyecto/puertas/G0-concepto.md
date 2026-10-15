# Acta de puerta G0 — Concepto aprobado

| | |
|---|---|
| Proyecto | Traductor |
| Fecha de preparación | 2026-10-15 |
| Versión del acta | 0.2 |
| Preparada por | Asistencia de IA |
| Estado | **pendiente de firma. Faltan tres datos** |

## Criterios evaluados

Criterios tomados de `docs/sdlc/F0-concepcion.md`. Documentos de referencia: acta de proyecto v0.2 y registro de riesgos v0.2.

| # | Criterio | Cumple | Evidencia |
|---|----------|--------|-----------|
| 1 | El problema está descrito sin nombrar la solución técnica | sí | Acta de proyecto, apartado 1 |
| 2 | Los interesados están identificados con nombre y papel | sí | Apartado 2. Cuatro papeles, incluida la empresa cliente como interesado con capacidad de bloqueo |
| 3 | El alcance tiene una lista explícita de exclusiones | sí | Apartado 4. Las dos exclusiones de peso quedaron decididas el 2026-10-15: entra la formación remota, no entran las intervenciones de los alumnos. Las otras cinco se dan por aceptadas salvo corrección en esta firma |
| 4 | Los criterios de éxito son medibles y tienen valor objetivo | **no** | Apartado 7. CE-01 fijado en 5 s y CE-03 en 0 €. Siguen sin valor CE-02, CE-04 y CE-06 |
| 5 | Se han evaluado alternativas, y está escrito por qué se descarta cada una | sí | Apartado 6. Seis alternativas. Elegida F, desarrollo propio autoalojado, por ser la única compatible con 0 € sin repercutir coste. La alternativa D queda como primera tarea de F1 y puede sustituirla |
| 6 | Los riesgos de probabilidad e impacto altos tienen respuesta asignada | sí | Registro de riesgos v0.2. Trece riesgos, todos con respuesta. R-01 y R-13 aceptados de forma expresa |
| 7 | Hay un presupuesto de tiempo o dinero escrito | **no** | El de dinero está y está confirmado: 0 €. El de tiempo sigue sin escribirse |

## Desviaciones

| Criterio | Qué falta | Se acepta | Condición |
|----------|-----------|-----------|-----------|
| 4 | Valor objetivo de CE-02, CE-04 y CE-06 | no | Decisión del responsable de producto |
| 7 | Horas semanales disponibles y fecha objetivo | no | Decisión del responsable de producto |
| — | Lista cerrada de idiomas de destino (RES-03) y hardware disponible (RES-06) | no | Dato del responsable de producto. Sin ellos no se puede dimensionar el prototipo de F1 |

## Decisiones registradas el 2026-10-15

| Decisión | Efecto |
|----------|--------|
| El coste no se repercute a la empresa cliente. Presupuesto 0 € real | Descarta las alternativas B, C y E. Elegida F |
| Flujo solo de ida, del profesor a los alumnos | Excluye NEC-07, que queda aplazada con número reservado. Riesgo R-13 aceptado |
| Retardo máximo tolerable: 5 s | Fija CE-01. Es alcanzable con la alternativa F según las fuentes consultadas, y hay que medirlo |
| La formación es presencial y remota | Añade RES-07. Impide la solución exclusivamente local, reabre la dependencia de la red del cliente (R-04) y crea R-12 |

## Decisión de la puerta

| | |
|---|---|
| Decisión | pendiente |
| Aprobador | Responsable de producto |
| Firma | — |

Cinco de los siete criterios se cumplen. Los dos que faltan se cierran con tres datos: valores de CE-02, CE-04 y CE-06; horas semanales y fecha objetivo; lista de idiomas y hardware disponible.

## Acciones abiertas

| # | Acción | Responsable | Plazo |
|---|--------|-------------|-------|
| 1 | Cerrar la lista de idiomas de destino (RES-03) | Producto | Antes de G0 |
| 2 | Indicar el hardware disponible: modelo de portátil, memoria y si tiene GPU (RES-06) | Producto | Antes de G0 |
| 3 | Fijar el valor de CE-02, CE-04 y CE-06 | Producto | Antes de G0 |
| 4 | Indicar horas semanales disponibles y si hay una formación en calendario como objetivo | Producto | Antes de G0 |
| 5 | Confirmar o corregir las cinco exclusiones propuestas del apartado 4 | Producto | Al firmar |

## Nota sobre el orden de trabajo en F1

Una vez firmada G0, la primera tarea no es escribir requisitos. Es un prototipo desechable que mida tres cosas con el hardware real y la lista cerrada de idiomas: latencia de punta a punta, consumo del equipo con todos los idiomas a la vez, y ancho de banda de subida por alumno remoto. En paralelo, probar las herramientas gratuitas de la alternativa D.

Esa tarea cierra o reduce R-02, R-05, R-06 y R-12, que son cuatro de los cinco riesgos de mayor exposición. Y puede cambiar la respuesta a la pregunta de si este proyecto debe construirse, que sigue siendo la pregunta pertinente mientras no esté medida.
