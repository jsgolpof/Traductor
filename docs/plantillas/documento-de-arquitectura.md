# Arquitectura — <nombre del proyecto>

| | |
|---|---|
| Versión | 0.1 |
| Fecha | AAAA-MM-DD |
| Autor | |
| Estado | borrador / en revisión / línea base / obsoleto |

## 1. Visión general

Qué tipo de sistema es y cómo se organiza, en un párrafo. Un diagrama si ayuda.

## 2. Decisiones estructurantes

Las que condicionan todo lo demás, cada una con su ADR.

| Decisión | ADR |
|----------|-----|
| Pila tecnológica | ADR-0001 |
| Modelo de despliegue | ADR-0002 |
| Almacenamiento de datos | ADR-0003 |

## 3. Componentes

### CMP-01 — <nombre>

| | |
|---|---|
| Responsabilidad | Una frase. Si hacen falta dos, probablemente son dos componentes |
| Requisitos que implementa | RF-001, RF-004 |
| Interfaz que expone | |
| De qué depende | CMP-02, servicio externo X |
| Tecnología | |
| Dónde vive | `ruta/` |

## 4. Interfaces

| Interfaz | Entre | Protocolo / formato | Contrato |
|----------|-------|---------------------|----------|
| | | | |

## 5. Modelo de datos

Entidades, atributos, relaciones, claves. Y la clasificación de cada dato:

| Entidad | Atributo | Tipo | Dato personal | Categoría RGPD | Conservación |
|---------|----------|------|---------------|----------------|--------------|
| | | | sí / no | ordinario / artículo 9 | |

## 6. Aspectos transversales

| Aspecto | Decisión |
|---------|----------|
| Autenticación | |
| Autorización | |
| Gestión de secretos | |
| Registro de actividad | |
| Gestión de errores | |
| Configuración por entorno | |
| Copias de seguridad | |
| Observabilidad | |

## 7. Análisis de seguridad

| Activo | Amenaza | Vector | Mitigación en el diseño | Riesgo residual |
|--------|---------|--------|-------------------------|-----------------|
| | | | | |

## 8. Dependencias de terceros

| Dependencia | Versión | Para qué | Licencia | Riesgo de abandono | Alternativa |
|-------------|---------|----------|----------|--------------------|-------------|
| | | | | | |

## 9. Entornos

| Entorno | Para qué | Diferencias con producción |
|---------|----------|---------------------------|
| local | | |
| pruebas | | |
| producción | — | — |

## 10. Deuda técnica aceptada

Lo que se hace a sabiendas de que no es lo correcto, con su motivo y su fecha de revisión.

| Qué | Por qué se acepta | Coste de arreglarlo después | Revisión |
|-----|-------------------|-----------------------------|----------|
| | | | |

## 11. Historial

| Versión | Fecha | Autor | Cambio | SC |
|---------|-------|-------|--------|----|
| 0.1 | | | Versión inicial | — |
