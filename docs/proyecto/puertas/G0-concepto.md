# Acta de puerta G0 — Concepto aprobado

| | |
|---|---|
| Proyecto | Traductor |
| Fecha de preparación | 2026-10-15 |
| Preparada por | Asistencia de IA |
| Estado | **pendiente de firma. No procede aprobar todavía** |

## Criterios evaluados

Criterios tomados de `docs/sdlc/F0-concepcion.md`.

| # | Criterio | Cumple | Evidencia |
|---|----------|--------|-----------|
| 1 | El problema está descrito sin nombrar la solución técnica | sí | Acta de proyecto, apartado 1 |
| 2 | Los interesados están identificados con nombre y papel | parcial | Apartado 2. Los papeles están, los nombres no. Se añadió la empresa cliente como interesado con capacidad de bloqueo, que no figuraba en la información inicial |
| 3 | El alcance tiene una lista explícita de exclusiones | **no** | Apartado 4. La lista es una propuesta sin confirmar. Dos exclusiones son decisiones de peso: formación remota, y traducción de las preguntas de los alumnos |
| 4 | Los criterios de éxito son medibles y tienen valor objetivo | **no** | Apartado 7. Seis criterios propuestos, todos con valor pendiente de confirmar. La formulación inicial, "cuando cumpla con su cometido", no es verificable |
| 5 | Se han evaluado alternativas, y está escrito por qué se descarta cada una | sí, con reserva | Apartado 6. Seis alternativas con coste. Las cifras son de los proveedores o de comparativas de terceros, no medidas propias. La alternativa elegida está pendiente |
| 6 | Los riesgos de probabilidad e impacto altos tienen respuesta asignada | parcial | Registro de riesgos. R-01 y R-07 necesitan una decisión del responsable de producto para cerrar su respuesta |
| 7 | Hay un presupuesto de tiempo o dinero escrito | parcial | Apartado 8. El de dinero está: 0 €. El de tiempo no, y además el de dinero entra en conflicto con cuatro de las seis alternativas |

## Desviaciones

| Criterio | Qué falta | Se acepta | Condición y plazo |
|----------|-----------|-----------|-------------------|
| 3 | Confirmar las exclusiones, y decidir sobre formación remota y preguntas de los alumnos | no | Decisión del responsable de producto |
| 4 | Fijar el valor objetivo de CE-01 a CE-06 | no | Decisión del responsable de producto |
| 5 | Elegir alternativa, que depende de si el coste se puede repercutir al cliente | no | Decisión del responsable de producto |
| 6 | Cerrar la respuesta a R-01 y R-07 | no | Decisión del responsable de producto |
| 7 | Horas semanales disponibles y fecha objetivo | no | Decisión del responsable de producto |

## Decisión

| | |
|---|---|
| Decisión | pendiente |
| Aprobador | Responsable de producto |
| Firma | — |

Cuatro de los siete criterios no se cumplen, y los cinco huecos dependen de decisiones que solo puede tomar el responsable de producto. Ninguno requiere trabajo técnico previo.

## Acciones abiertas

| # | Acción | Responsable | Plazo |
|---|--------|-------------|-------|
| 1 | Decidir si el coste de la herramienta se puede repercutir a la empresa cliente | Producto | Antes de G0 |
| 2 | Cerrar la lista de idiomas de destino (RES-03) | Producto | Antes de G0 |
| 3 | Decidir si entran la formación remota y la traducción de las preguntas de los alumnos | Producto | Antes de G0 |
| 4 | Fijar el retardo máximo tolerable (CE-01) y el resto de valores objetivo | Producto | Antes de G0 |
| 5 | Indicar horas semanales disponibles y si hay una formación en calendario como objetivo | Producto | Antes de G0 |
| 6 | Indicar el hardware disponible: modelo de portátil, memoria y si tiene GPU (RES-06) | Producto | Antes de G0 |

## Nota sobre el orden de trabajo

Una vez firmada G0, la primera tarea de F1 no es escribir requisitos: es probar las herramientas que ya existen y medir la latencia de un prototipo desechable con el hardware real. Cierra o reduce R-01, R-02, R-05 y R-06, y puede cambiar la respuesta a la pregunta de si este proyecto debe construirse.
