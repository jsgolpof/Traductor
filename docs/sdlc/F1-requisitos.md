# F1 — Requisitos

Alineada con *System/Software Requirements Definition* de ISO/IEC/IEEE 12207:2017.

## Propósito

Convertir las necesidades de F0 en requisitos verificables, identificados y acordados. Un requisito que no se puede verificar no es un requisito: es un deseo.

## Criterios de entrada

- G0 aprobada.
- Acta de proyecto en vigor.

## Actividades

1. Derivar requisitos funcionales de las necesidades de los interesados. Cada necesidad produce uno o varios requisitos, y queda trazada.
2. Derivar requisitos no funcionales: rendimiento, capacidad, disponibilidad, seguridad, privacidad, usabilidad, mantenibilidad, portabilidad, requisitos legales.
3. Registrar las restricciones como tales, separadas de los requisitos.
4. Asignar prioridad a cada requisito con MoSCoW: imprescindible, importante, deseable, descartado para esta versión.
5. Definir el criterio de verificación de cada requisito: cómo se va a demostrar que se cumple, y con qué método (inspección, análisis, demostración o prueba).
6. Revisar el conjunto buscando ambigüedad, contradicciones y duplicados.
7. Abrir la matriz de trazabilidad y rellenar las columnas de origen y requisito.
8. Actualizar el registro de riesgos con lo aprendido.

## Reglas de redacción de requisitos

- Una obligación por requisito. Si hay un "y", probablemente son dos requisitos.
- Forma activa: "El sistema debe ...".
- Sin palabras no verificables: rápido, amigable, robusto, eficiente, moderno, intuitivo. Si aparece una, falta un número.
- Sin solución técnica dentro del requisito, salvo que sea una restricción impuesta, y entonces va al apartado de restricciones.
- Cada requisito lleva su identificador definitivo desde el momento en que se escribe.

## Artefactos de salida

| Artefacto | Plantilla | Ubicación |
|-----------|-----------|-----------|
| Especificación de requisitos (ERS) | `plantillas/especificacion-de-requisitos.md` | `docs/proyecto/especificacion-de-requisitos.md` |
| Matriz de trazabilidad (parcial) | `plantillas/matriz-de-trazabilidad.md` | `docs/proyecto/matriz-de-trazabilidad.md` |
| Registro de riesgos actualizado | — | `docs/proyecto/registro-de-riesgos.md` |

## Criterios de puerta G1 — Línea base de requisitos

- [ ] Todo requisito tiene identificador, prioridad y criterio de verificación.
- [ ] Ningún requisito contiene términos no verificables sin un valor numérico asociado.
- [ ] Toda necesidad de interesado del acta está cubierta por al menos un requisito, o está explícitamente aplazada.
- [ ] Los requisitos no funcionales cubren, como mínimo, rendimiento, seguridad y tratamiento de datos personales. Si alguno no aplica, está escrito por qué.
- [ ] No hay requisitos en conflicto sin resolver.
- [ ] La matriz de trazabilidad existe y recoge todos los requisitos.
- [ ] El responsable de producto ha revisado y aceptado la lista completa.

Aprobador: responsable de producto. A partir de esta puerta, la ERS es línea base: cualquier cambio entra por solicitud de cambio.
