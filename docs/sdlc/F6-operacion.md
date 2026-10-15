# F6 — Operación y mantenimiento

Alineada con *Operation* y *Maintenance* de ISO/IEC/IEEE 12207:2017.

## Propósito

Mantener el sistema en servicio y gestionar su evolución sin perder el control de lo que hay desplegado.

Esta fase no tiene puerta de salida. Dura mientras el sistema esté en uso, y solo termina al entrar en F7.

## Actividades permanentes

1. Vigilar el sistema contra los umbrales definidos en los requisitos no funcionales.
2. Atender incidencias según su severidad, y registrarlas todas, incluidas las que se resuelven reiniciando algo.
3. Analizar la causa raíz de las incidencias críticas y altas. Un parche sin causa raíz identificada se marca como provisional y genera una tarea de seguimiento.
4. Gestionar las solicitudes de cambio.
5. Revisar las dependencias periódicamente: vulnerabilidades publicadas, versiones sin mantenimiento, licencias.
6. Mantener los documentos del proyecto al día. Un documento que miente es peor que no tenerlo.

## Tipos de mantenimiento

| Tipo | Qué es | Vía de entrada |
|------|--------|----------------|
| Correctivo | Arreglar un defecto | Incidencia |
| Evolutivo | Añadir o cambiar funcionalidad | Solicitud de cambio |
| Adaptativo | Ajustar a un cambio del entorno: versión de dependencia, cambio normativo | Solicitud de cambio |
| Preventivo | Reducir deuda técnica o riesgo futuro, sin cambiar el comportamiento | Solicitud de cambio |

## Gestión de cambios

Toda modificación sobre una línea base aprobada entra por solicitud de cambio, con la plantilla `plantillas/solicitud-de-cambio.md`. El flujo:

1. Se registra la solicitud con su identificador `SC-nnn`.
2. Se evalúa: qué requisitos toca, qué componentes, qué esfuerzo, qué riesgos introduce, qué pasa si no se hace.
3. El responsable de producto la aprueba, la rechaza o la aplaza. La decisión se escribe, también si es un rechazo.
4. Si se aprueba, el ciclo se reabre en la fase que corresponda al alcance del cambio, y se recorren sus puertas solo para ese alcance.
5. Al cerrarse, se actualizan la ERS, la arquitectura, la matriz de trazabilidad y las pruebas.

Excepción por urgencia: ante una incidencia crítica en producción se puede corregir primero y documentar después, con un plazo máximo de 48 horas para registrar la solicitud de cambio retroactiva y actualizar los documentos. La excepción se anota en el registro de cambios como tal.

## Artefactos

| Artefacto | Plantilla | Ubicación |
|-----------|-----------|-----------|
| Registro de incidencias | `plantillas/registro-de-incidencias.md` | `docs/proyecto/registro-de-incidencias.md` |
| Registro de solicitudes de cambio | `plantillas/solicitud-de-cambio.md` | `docs/proyecto/registro-de-cambios.md` |

## Revisión periódica

Una vez al trimestre, o al cerrar una versión, se revisa: incidencias por severidad, tiempo medio de resolución, cumplimiento de los requisitos no funcionales medidos en producción, riesgos materializados y estado de las dependencias. El resultado se anota en el registro de riesgos.
