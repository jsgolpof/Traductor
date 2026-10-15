# F7 — Retirada

Alineada con *Disposal* de ISO/IEC/IEEE 12207:2017.

## Propósito

Apagar el sistema sin dejar datos expuestos, obligaciones incumplidas ni usuarios tirados.

## Criterios de entrada

- Decisión de retirada tomada y escrita por el responsable de producto.
- Interesados avisados con el plazo acordado.

## Actividades

1. Avisar a los usuarios con antelación suficiente, y dejar constancia del aviso.
2. Dar salida a los datos: exportación en formato utilizable para quien los necesite, y para quien tenga derecho a ellos.
3. Migrar lo que vaya a otro sistema, y verificar la migración antes de apagar el origen.
4. Eliminar los datos personales conforme al plazo de conservación que corresponda. Si hay obligación legal de conservar, archivar con acceso restringido y dejar escrito el plazo y el responsable.
5. Revocar credenciales, claves de API, accesos y permisos.
6. Dar de baja la infraestructura y los contratos asociados, y cancelar las suscripciones.
7. Archivar el repositorio y la documentación, con la fecha de archivo.
8. Escribir el acta de cierre: qué se aprendió, qué se haría distinto, qué queda archivado y dónde.

## Artefactos de salida

| Artefacto | Ubicación |
|-----------|-----------|
| Acta de cierre | `docs/proyecto/acta-de-cierre.md` |
| Registro de eliminación y archivo de datos | `docs/proyecto/acta-de-cierre.md` |

## Criterios de puerta G6 — Proyecto cerrado

- [ ] Usuarios avisados, con constancia.
- [ ] Datos exportados y entregados a quien correspondía.
- [ ] Datos personales eliminados, o archivados con plazo y responsable escritos.
- [ ] Credenciales y accesos revocados.
- [ ] Infraestructura y contratos dados de baja.
- [ ] Repositorio y documentación archivados.
- [ ] Acta de cierre escrita, con las lecciones aprendidas.

Aprobador: responsable de producto.
