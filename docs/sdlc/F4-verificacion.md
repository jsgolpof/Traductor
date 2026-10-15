# F4 — Verificación y validación

Alineada con *Verification* y *Validation* de ISO/IEC/IEEE 12207:2017.

## Propósito

Demostrar dos cosas distintas. Verificación: el sistema cumple sus requisitos. Validación: el sistema resuelve el problema del acta de proyecto. Un sistema puede pasar la primera y fallar la segunda.

## Criterios de entrada

- G3 aprobada.
- Entorno de pruebas disponible y equivalente al de producción en lo que afecte al resultado.

## Actividades

1. Ejecutar los casos de prueba de la especificación de pruebas y registrar el resultado de cada uno.
2. Probar los requisitos no funcionales con medidas, no con impresiones: tiempos, volúmenes, concurrencia.
3. Ejecutar las pruebas de seguridad previstas: autenticación, autorización, validación de entradas, dependencias con vulnerabilidades conocidas.
4. Validar con los interesados, sobre el sistema funcionando, contra los criterios de éxito del acta.
5. Registrar cada fallo como incidencia, clasificarlo por severidad y decidir si bloquea el despliegue.
6. Corregir, y volver a ejecutar las pruebas afectadas más una pasada de regresión.
7. Cerrar la matriz de trazabilidad: cada requisito, su caso de prueba y su resultado.

## Clasificación de severidad de incidencias

| Severidad | Definición | Efecto en G4 |
|-----------|------------|--------------|
| Crítica | Pérdida de datos, brecha de seguridad, sistema inutilizable | Bloquea |
| Alta | Un requisito imprescindible no se cumple, sin alternativa viable | Bloquea |
| Media | Un requisito se cumple de forma parcial o hay una alternativa aceptable | No bloquea si está aceptada por escrito |
| Baja | Defecto cosmético o de conveniencia | No bloquea |

## Artefactos de salida

| Artefacto | Plantilla | Ubicación |
|-----------|-----------|-----------|
| Especificación de casos de prueba | `plantillas/casos-de-prueba.md` | `docs/proyecto/casos-de-prueba.md` |
| Informe de pruebas | `plantillas/informe-de-pruebas.md` | `docs/proyecto/informe-de-pruebas.md` |
| Registro de incidencias | `plantillas/registro-de-incidencias.md` | `docs/proyecto/registro-de-incidencias.md` |
| Matriz de trazabilidad completa | — | `docs/proyecto/matriz-de-trazabilidad.md` |

## Criterios de puerta G4 — Apto para despliegue

- [ ] Todos los casos de prueba se han ejecutado, y cada uno tiene resultado registrado.
- [ ] Ningún requisito imprescindible tiene su prueba en rojo.
- [ ] No queda ninguna incidencia crítica ni alta abierta.
- [ ] Las incidencias medias que quedan abiertas están aceptadas por escrito por el responsable de producto.
- [ ] Los requisitos no funcionales se han medido, y la medida consta en el informe.
- [ ] La validación con los interesados está hecha y registrada.
- [ ] La trazabilidad requisito a prueba está cerrada al cien por cien.

Aprobadores: responsable técnico y responsable de producto.
