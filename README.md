# Traductor

Traducción simultánea por audio para formación presencial. El profesor imparte en castellano y cada alumno recibe en su dispositivo, en tiempo real y en su idioma, lo que se dice en la sala.

Descripción completa en `docs/proyecto/acta-de-proyecto.md`.

## Estado

| | |
|---|---|
| Fase actual | F0 — Concepción |
| Última puerta aprobada | ninguna |
| Próxima puerta | G0 — Concepto aprobado, preparada y pendiente de firma |
| Qué bloquea G0 | Tres datos del responsable de producto: idiomas, hardware y dedicación. Ver `docs/proyecto/puertas/G0-concepto.md` |
| Actualizado | 2026-10-15 |

## Estructura del repositorio

```
docs/
├── sdlc/           Proceso de desarrollo: fases, puertas, roles, configuración
├── plantillas/     Plantillas de los documentos que exige el proceso
└── proyecto/       Documentos de este proyecto
    ├── puertas/    Actas de las puertas aprobadas
    └── decisiones/ ADR
CLAUDE.md           Reglas de trabajo para el asistente de IA en este repositorio
```

## Por dónde empezar

Lee `docs/sdlc/README.md`. Define las fases, los artefactos obligatorios de cada una y los criterios de cada puerta.

El proceso de `docs/sdlc/` y `docs/plantillas/` es reutilizable: para arrancar otro proyecto, se copian esos dos directorios al repositorio nuevo.
