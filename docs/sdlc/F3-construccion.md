# F3 — Construcción

Alineada con *Implementation* e *Integration* de ISO/IEC/IEEE 12207:2017.

## Propósito

Escribir el código que implementa el diseño, integrarlo y dejarlo en un estado que se pueda verificar.

## Criterios de entrada

- G2 aprobada.
- Arquitectura y plan de pruebas en línea base.

## Actividades

1. Implementar por componentes, en el orden que marque la dependencia entre ellos y el riesgo: primero lo que puede invalidar el diseño.
2. Escribir las pruebas unitarias junto al código, no después.
3. Integrar de forma continua: la rama principal del proyecto queda siempre en estado compilable y con las pruebas en verde.
4. Revisar el código antes de integrar. En un equipo de una persona, la revisión es una pasada propia sobre el diff completo, con la ERS delante.
5. Mantener la matriz de trazabilidad: cada requisito implementado apunta a su módulo o fichero.
6. Registrar en el ADR correspondiente cualquier desviación del diseño, o abrir un ADR nuevo que sustituya al anterior.
7. Documentar las interfaces públicas a medida que se escriben.

## Reglas de integración

- Un commit hace una cosa y su mensaje dice qué y por qué.
- El mensaje de commit referencia el requisito o la incidencia que atiende: `RF-012`, `INC-004`.
- No se integra código con pruebas en rojo ni con pruebas deshabilitadas para pasar.
- Las dependencias nuevas se justifican: qué aporta, qué licencia tiene, quién la mantiene.

## Artefactos de salida

| Artefacto | Ubicación |
|-----------|-----------|
| Código fuente integrado | repositorio |
| Pruebas unitarias y de integración | repositorio |
| Matriz de trazabilidad con columna de implementación | `docs/proyecto/matriz-de-trazabilidad.md` |
| Documentación de interfaces | según el proyecto |

## Criterios de puerta G3 — Código completo

- [ ] Todos los requisitos imprescindibles están implementados.
- [ ] Los requisitos importantes están implementados o aplazados por escrito, con el aplazamiento aceptado.
- [ ] La rama principal compila y pasa todas las pruebas.
- [ ] Se alcanza el umbral de cobertura fijado en el plan de pruebas.
- [ ] No hay pruebas deshabilitadas, ignoradas ni marcadas para saltar.
- [ ] La matriz de trazabilidad está al día.
- [ ] Las desviaciones respecto al diseño están registradas.

Aprobador: responsable técnico.
