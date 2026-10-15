# Proceso de desarrollo (SDLC)

Este directorio define cómo se lleva un proyecto desde la idea hasta su retirada: qué fases hay, qué documento produce cada una y qué hay que cumplir para pasar a la siguiente.

La estructura sigue los procesos técnicos de ISO/IEC/IEEE 12207:2017. No es un proceso certificado ni lo pretende: se han tomado las fases, los artefactos y el control por puertas, y se ha dejado fuera la parte de procesos de acuerdo y habilitación organizativa, que no aplica a un equipo pequeño.

## Fases y puertas

| Fase | Nombre | Puerta de salida | Artefacto principal |
|------|--------|------------------|---------------------|
| F0 | Concepción | G0 — Concepto aprobado | Acta de proyecto |
| F1 | Requisitos | G1 — Línea base de requisitos | Especificación de requisitos (ERS) |
| F2 | Diseño | G2 — Línea base de diseño | Documento de arquitectura + ADR |
| F3 | Construcción | G3 — Código completo | Código integrado + matriz de trazabilidad al día |
| F4 | Verificación y validación | G4 — Apto para despliegue | Informe de pruebas |
| F5 | Transición y despliegue | G5 — Aceptado en producción | Plan de despliegue ejecutado |
| F6 | Operación y mantenimiento | — (ciclo continuo) | Registro de incidencias y solicitudes de cambio |
| F7 | Retirada | G6 — Proyecto cerrado | Acta de cierre |

Cada fase tiene su documento en este directorio, con criterios de entrada, actividades, artefactos de salida y criterios de puerta.

F6 no termina: las solicitudes de cambio aprobadas reabren el ciclo en la fase que corresponda (normalmente F1 o F2) para el alcance del cambio, no para todo el sistema.

## Reglas que no se saltan

1. No se escribe código de producción antes de G1. Prototipos desechables sí, y se marcan como desechables.
2. Todo requisito tiene identificador y al menos un caso de prueba que lo verifica. Sin eso, G4 no pasa.
3. Toda decisión de arquitectura con alternativas reales se registra como ADR antes de implementarla.
4. Un cambio sobre una línea base aprobada entra por solicitud de cambio, no por commit directo.
5. Cada puerta deja un acta firmada en `docs/proyecto/puertas/`, aunque la firme la misma persona que hizo el trabajo.

## Convenciones de identificadores

| Tipo | Formato | Ejemplo | Donde vive |
|------|---------|---------|------------|
| Requisito funcional | `RF-nnn` | RF-012 | ERS |
| Requisito no funcional | `RNF-nnn` | RNF-004 | ERS |
| Restricción | `RES-nnn` | RES-002 | ERS |
| Decisión de arquitectura | `ADR-nnnn` | ADR-0003 | `docs/proyecto/decisiones/` |
| Riesgo | `R-nn` | R-07 | Registro de riesgos |
| Caso de prueba | `CP-nnn` | CP-045 | Especificación de pruebas |
| Incidencia | `INC-nnn` | INC-011 | Registro de incidencias |
| Solicitud de cambio | `SC-nnn` | SC-003 | Registro de cambios |
| Componente | `CMP-nn` | CMP-04 | Documento de arquitectura |

Los identificadores no se reutilizan ni se renumeran. Un requisito eliminado se marca como obsoleto y conserva su número.

## Cómo arrancar un proyecto nuevo con esto

1. Copia `docs/sdlc/` y `docs/plantillas/` al repositorio nuevo.
2. Crea `docs/proyecto/` con los subdirectorios `puertas/` y `decisiones/`.
3. Rellena el acta de proyecto desde `plantillas/acta-de-proyecto.md`.
4. Convoca G0.
5. Sigue las fases en orden.

## Coste de este proceso, y qué recortar

Un proceso formal completo en un proyecto de una persona puede costar más tiempo en documentación que en código. Donde paga: cuando hay un cliente que acepta entregas, cuando hay que demostrar diligencia ante un auditor o un tercero, cuando el sistema tiene requisitos legales o de seguridad, y cuando el proyecto va a sobrevivir a la memoria de quien lo escribió.

Si en algún momento el proceso estorba, el orden sensato para recortar es este:

1. Primero, fusiona las actas de puerta en un único registro de puertas con una fila por puerta.
2. Después, reduce la especificación de pruebas a los requisitos de prioridad alta y los de seguridad.
3. Después, quita el análisis cuantitativo del registro de riesgos y deja solo probabilidad e impacto cualitativos.

Lo que no conviene recortar nunca: los identificadores de requisitos, la trazabilidad requisito a prueba, y los ADR. Son lo que hace que el proyecto siga siendo entendible dentro de un año.
