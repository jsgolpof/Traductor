# Plan de pruebas — <nombre del proyecto>

| | |
|---|---|
| Versión | 0.1 |
| Fecha | AAAA-MM-DD |
| Estado | borrador / línea base |

## 1. Alcance

Qué se prueba y qué no se prueba, con el motivo de cada exclusión.

## 2. Niveles de prueba

| Nivel | Qué cubre | Quién | Herramienta | Cuándo se ejecuta |
|-------|-----------|-------|-------------|-------------------|
| Unitaria | Lógica de una unidad aislada | Desarrollo | | En cada cambio |
| Integración | Interacción entre componentes e interfaces | Desarrollo | | En cada integración a main |
| Sistema | Requisitos funcionales de punta a punta | Verificación | | F4 |
| No funcional | Rendimiento, carga, seguridad | Verificación | | F4 |
| Aceptación | Criterios de éxito del acta | Producto | | F4 |
| Humo | Que lo desplegado arranca y responde | Operación | | F5, tras cada despliegue |
| Regresión | Que lo que funcionaba sigue funcionando | Verificación | | Tras cada corrección |

## 3. Criterios de cobertura

| Métrica | Umbral exigido |
|---------|----------------|
| Cobertura de líneas | |
| Cobertura de ramas | |
| Requisitos imprescindibles con caso de prueba | 100 % |
| Requisitos no funcionales medidos | 100 % |

## 4. Entorno de pruebas

Qué hace falta, en qué se diferencia de producción y qué datos se usan. Si se usan datos reales con información personal, hay que anonimizarlos antes, y aquí se dice cómo.

## 5. Criterios de entrada y salida

Entrada en F4: G3 aprobada, entorno disponible, casos de prueba escritos.

Salida de F4: los criterios de la puerta G4 en `docs/sdlc/F4-verificacion.md`.

## 6. Criterios de suspensión

Cuándo se para la campaña de pruebas en lugar de seguir: por ejemplo, cuando un fallo bloquea más del 30 % de los casos previstos, o cuando el entorno no es representativo.

## 7. Riesgos de la propia estrategia de pruebas

Qué queda sin cubrir y qué se asume con ello.

| Hueco | Riesgo que se asume | Mitigación |
|-------|---------------------|------------|
| | | |

## 8. Historial

| Versión | Fecha | Autor | Cambio |
|---------|-------|-------|--------|
| 0.1 | | | Versión inicial |
