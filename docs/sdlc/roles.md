# Roles y responsabilidades

Son papeles, no personas. En un proyecto pequeño una misma persona puede llevar varios, y eso está bien siempre que al firmar una puerta sepa con qué sombrero firma. Lo que no se puede es saltarse la comprobación porque la haga quien hizo el trabajo.

## Responsable de producto

Responde por el para qué. Decide el alcance y las prioridades, acepta las entregas, aprueba o rechaza las solicitudes de cambio, y acepta por escrito los defectos que se quedan abiertos.

Firma: G0, G1, G4, G5, G6.

## Responsable técnico

Responde por el cómo. Decide la arquitectura y la pila tecnológica, escribe los ADR, define la estrategia de pruebas y el umbral de cobertura, y revisa el código antes de la integración.

Firma: G2, G3, G4.

## Desarrollo

Implementa, escribe pruebas, mantiene la trazabilidad al día y registra las desviaciones respecto al diseño.

## Verificación

Diseña y ejecuta los casos de prueba, y registra los resultados tal como salen. Cuando lo hace la misma persona que ha escrito el código, conviene escribir los casos de prueba a partir de la ERS, no del código, y hacerlo antes de mirar la implementación.

## Operación

Vigila el sistema en producción, atiende las incidencias de primer nivel y ejecuta los despliegues y las reversiones.

## Asistente de IA

Cuando el trabajo se hace con un asistente de IA, este actúa en los papeles de desarrollo y verificación, y propone en los de arquitectura. No firma puertas. Las reglas de cómo debe trabajar están en el `CLAUDE.md` de la raíz del repositorio.

## Matriz de aprobación

| Puerta | Aprueba | Verifica |
|--------|---------|----------|
| G0 Concepto | Responsable de producto | — |
| G1 Requisitos | Responsable de producto | Responsable técnico |
| G2 Diseño | Responsable técnico | — |
| G3 Código completo | Responsable técnico | Desarrollo |
| G4 Apto para despliegue | Producto y técnico | Verificación |
| G5 Aceptado en producción | Responsable de producto | Operación |
| G6 Cierre | Responsable de producto | — |
