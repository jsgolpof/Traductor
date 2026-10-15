# F5 — Transición y despliegue

Alineada con *Transition* de ISO/IEC/IEEE 12207:2017.

## Propósito

Poner el sistema en producción de forma reversible, y dejar a quien lo opera en condiciones de hacerlo.

## Criterios de entrada

- G4 aprobada.
- Entorno de producción preparado.

## Actividades

1. Escribir el plan de despliegue: pasos ordenados, responsable de cada uno, duración estimada, ventana.
2. Escribir el plan de reversión antes de desplegar, y comprobar que funciona. Un plan de reversión sin probar no cuenta.
3. Preparar la migración de datos, si la hay, con copia de seguridad previa verificada.
4. Desplegar, siguiendo el plan y anotando desviaciones.
5. Ejecutar las pruebas de humo en producción.
6. Entregar la documentación de operación: cómo se arranca, cómo se para, qué se monitoriza, qué hacer cuando falla, a quién se avisa.
7. Formar a los usuarios si el sistema lo requiere.
8. Declarar el periodo de garantía: cuánto tiempo y con qué tiempo de respuesta se atienden los fallos tras el despliegue.

## Artefactos de salida

| Artefacto | Plantilla | Ubicación |
|-----------|-----------|-----------|
| Plan de despliegue y reversión | `plantillas/plan-de-despliegue.md` | `docs/proyecto/plan-de-despliegue.md` |
| Manual de operación | — | `docs/proyecto/operacion.md` |
| Registro del despliegue | en el propio plan | `docs/proyecto/plan-de-despliegue.md` |

## Criterios de puerta G5 — Aceptado en producción

- [ ] El despliegue se ha ejecutado y está registrado, con sus desviaciones.
- [ ] Las pruebas de humo en producción han pasado.
- [ ] El plan de reversión está escrito y se ha comprobado que funciona.
- [ ] Existe copia de seguridad previa al despliegue, y se ha verificado que se puede restaurar.
- [ ] El manual de operación está entregado.
- [ ] La monitorización y los avisos están activos.
- [ ] El responsable de producto acepta formalmente la entrega.

Aprobador: responsable de producto.
