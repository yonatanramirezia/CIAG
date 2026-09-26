# CIAG — Capas del Sistema

### CIAG GitHub Public — Versión 1.0

> ⚠️ **Nota sobre esta versión:** este documento forma parte de la primera versión pública (v1.0) del repositorio CIAG. Su contenido está sujeto a cambios y actualizaciones a medida que el proyecto avance en su implementación real con empresas, en base a la realidad operativa del sistema. Lo aquí descrito refleja el estado conceptual y arquitectónico actual del proyecto.

---

## ¿Por qué capas?

CIAG está organizado en múltiples capas especializadas, cada una con una única responsabilidad dentro del sistema. Esta separación permite que cada componente haga únicamente aquello para lo que fue diseñado, haciendo el sistema más estable, mantenible y fácil de auditar.

Ninguna capa puede asumir la responsabilidad de otra. Esta separación estricta es uno de los principios de gobernanza más importantes de la arquitectura.

A continuación, un resumen general del propósito de cada capa, sin entrar en detalles de implementación.

---

## Resumen de capas

| Capa | Propósito general |
|---|---|
| **Capa 0 — Fundación** | Prepara, valida y gobierna el estado inicial del sistema antes de que cualquier proceso comience a operar. |
| **Capa 1 — Normalización** | Recibe y normaliza toda entrada de información, garantizando que llegue limpia, consistente y segura. |
| **Capa 2 — Interpretación Semántica** | Analiza el significado de la información recibida para construir una comprensión estructurada del contexto. |
| **Capa 3 — Evaluación de Riesgo** | Evalúa el nivel de riesgo de la información procesada mediante criterios deterministas. |
| **Capa 4 — Memoria y Perfilado** | Administra el contexto y la memoria operativa necesarios para dar continuidad al análisis. |
| **Capa 5 — Inteligencia de Amenazas** | Centraliza el conocimiento estructurado sobre amenazas y riesgos conocidos. |
| **Capa 6 — Predicción** | Genera modelos de predicción y análisis evolutivo a partir de la información disponible. |
| **Capa 7 — Correlación** | Correlaciona eventos, señales y patrones dispersos en estructuras relacionales coherentes. |
| **Capa 8 — Defensa Activa** | Gestiona mecanismos de defensa dinámica y adaptación frente a amenazas o comportamientos anómalos. |
| **Capa 9 — Respuesta Autónoma** | Controla la generación, ejecución segura y evaluación de respuestas dentro de entornos controlados. |
| **Capa 10 — Gobernanza Final** | Valida, audita y regula las decisiones generadas por las capas anteriores antes de su consolidación. |
| **Capa 11 — Forense y Legal** | Genera, verifica y exporta evidencia forense auditable para procesos legales y de cumplimiento. |
| **Capa 12 — Observabilidad** | Registra, mide y exporta la actividad del sistema sin intervenir en su funcionamiento. |
| **Capa 13 — Salida (Output)** | Convierte los resultados internos en reportes y explicaciones comprensibles para personas y sistemas externos. |
| **Capa 14 — Interfaz** | Expone los resultados oficiales de CIAG hacia consumidores externos de forma controlada. |
| **Capa 15 — Contratos JSON** | Define y mantiene los contratos computacionales oficiales mediante los cuales CIAG intercambia información. |
| **Capa 16 — Orquestación de Contratos** | Coordina el ciclo de vida y la ejecución ordenada de los contratos computacionales del sistema. |

---

## El flujo general

Estas capas no operan de forma aislada: siguen un flujo ordenado y obligatorio, desde que la información ingresa al sistema hasta que se entrega un resultado certificado a la empresa.

Para más información sobre ese flujo, ver [`ciag_pipeline.md`](ciag_pipeline.md). Para más información sobre la separación entre diagnóstico y solución, ver [`ciag_architecture.md`](ciag_architecture.md).
