# F2 — Diseño

Alineada con *Architecture Definition* y *Design Definition* de ISO/IEC/IEEE 12207:2017.

## Propósito

Decidir la estructura del sistema y justificar las decisiones. El diseño existe para que la construcción sea mecánica y para que dentro de un año se entienda por qué el sistema es así.

## Criterios de entrada

- G1 aprobada.
- ERS en línea base.

## Actividades

1. Definir la arquitectura: componentes, responsabilidad de cada uno, interfaces entre ellos, flujo de datos.
2. Asignar cada requisito a los componentes que lo implementan. Un requisito sin componente asignado es un agujero en el diseño.
3. Elegir la pila tecnológica y registrar la decisión como ADR, con las alternativas descartadas.
4. Diseñar el modelo de datos, incluida la clasificación de los datos personales si los hay.
5. Diseñar los aspectos transversales: autenticación, autorización, registro de actividad, gestión de errores, configuración, secretos.
6. Definir la estrategia de pruebas: qué se prueba con pruebas unitarias, qué con pruebas de integración, qué manualmente, y qué cobertura se exige.
7. Analizar la seguridad: superficie de ataque, datos sensibles, dependencias de terceros.
8. Actualizar la matriz de trazabilidad con la columna de componente.
9. Registrar cada decisión con alternativas reales como ADR en `docs/proyecto/decisiones/`.

## Artefactos de salida

| Artefacto | Plantilla | Ubicación |
|-----------|-----------|-----------|
| Documento de arquitectura | `plantillas/documento-de-arquitectura.md` | `docs/proyecto/arquitectura.md` |
| ADR, uno por decisión | `plantillas/adr.md` | `docs/proyecto/decisiones/ADR-nnnn-titulo.md` |
| Plan de pruebas | `plantillas/plan-de-pruebas.md` | `docs/proyecto/plan-de-pruebas.md` |
| Matriz de trazabilidad actualizada | — | `docs/proyecto/matriz-de-trazabilidad.md` |

## Criterios de puerta G2 — Línea base de diseño

- [ ] Todos los componentes tienen responsabilidad e interfaces definidas.
- [ ] Todo requisito imprescindible o importante está asignado a al menos un componente.
- [ ] Las decisiones con alternativas tienen su ADR, y el ADR dice qué se descartó y por qué.
- [ ] El modelo de datos está definido, y los datos personales están clasificados.
- [ ] Autenticación, autorización y gestión de secretos están resueltas en el diseño, no aplazadas.
- [ ] El plan de pruebas existe y fija el umbral de cobertura.
- [ ] Los riesgos técnicos nuevos están en el registro de riesgos.

Aprobador: responsable técnico.
