# Traductor

PENDIENTE: descripción del proyecto. Se rellena al cerrar el acta de proyecto (fase F0).

## Estado

| | |
|---|---|
| Fase actual | F0 — Concepción |
| Última puerta aprobada | ninguna |
| Próxima puerta | G0 — Concepto aprobado |

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
