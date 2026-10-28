# CIAG — Flujo General del Sistema

### CIAG GitHub Public — Versión 1.2

> ⚠️ **Nota sobre esta versión:** este documento forma parte de la versión pública 1.2 del repositorio CIAG, actualizada el 26 de octubre de 2026: se amplía a 23 tipos de empresa y se agregan la misión y visión del proyecto y los canales públicos. El servicio .JSON ya responde en el servidor real. El contenido puede seguir cambiando a medida que el proyecto avance con empresas, en base a la realidad operativa del sistema.

---

## El flujo general

Toda interacción entre una empresa y CIAG sigue un recorrido ordenado, obligatorio y determinista. Ninguna etapa puede omitirse ni alterarse.

```
EMPRESA
   │
   │  envía información mediante un contrato computacional (.json)
   ▼
CIAG-DX  (Diagnóstico)
   │
   │  analiza la información y genera hallazgos
   ▼
CIAG-CORE  (Solución)
   │
   │  evalúa y emite recomendaciones, cuando corresponde
   ▼
EMPRESA
   (recibe el resultado: veredicto, resolución, informe y trazabilidad)
```

Este flujo garantiza que ninguna respuesta llegue a la empresa sin haber pasado primero por un proceso completo de análisis, gobernanza y —cuando aplica— recomendaciones de corrección.

---

## CIAG-DX y CIAG-CORE, en una frase cada uno

- **CIAG-DX (Diagnóstico):** observa, analiza y detecta. Es el componente que identifica riesgos, inconsistencias o situaciones que requieren atención.
- **CIAG-CORE (Solución):** evalúa y recomienda. Una vez que CIAG-DX identifica una situación, CIAG-CORE determina la respuesta recomendada, siempre siguiendo las reglas de gobernanza definidas. CIAG no ejecuta cambios en los sistemas de la empresa: la ejecución la hacen las personas responsables.

En términos simples: CIAG-DX descubre lo que ocurre, y CIAG-CORE recomienda qué hacer con esa información.

---

## Cómo se comunica todo esto: los contratos JSON

La comunicación entre la empresa y CIAG —y entre los propios componentes internos del sistema— ocurre siempre mediante **contratos computacionales en formato JSON**. Estos contratos son documentos estructurados y deterministas que garantizan que la información se intercambie siempre de la misma forma, sin ambigüedad.

Existen seis contratos base que sostienen el flujo general del sistema:

| Contrato | Para qué se envía / qué resuelve |
|---|---|
| **Entrada empresarial** | Es el punto único de ingreso: normaliza y valida la información que la empresa envía, antes de que cualquier análisis comience. Evita que datos incompletos, inseguros o mal estructurados lleguen al sistema. |
| **Salida de diagnóstico** | Contiene los hallazgos del análisis: qué se encontró, con qué nivel de gravedad, y qué evidencia lo respalda. Le da a la empresa un informe claro y verificable del estado real de lo evaluado. |
| **Salida de remediación** | Documenta las acciones correctivas recomendadas y la evidencia de qué cambió y por qué cuando las personas de la empresa las implementan. Convierte un diagnóstico en una solución real y auditable. |
| **Trazabilidad forense** | Registra, con huellas de verificación, todo lo ocurrido durante el proceso. Permite reconstruir, en cualquier momento posterior, exactamente qué pasó — clave para auditorías y cumplimiento normativo. |
| **Estado de runtime** | Refleja en tiempo real si el sistema está activo, restringido o en algún estado especial. Da visibilidad constante sobre la disponibilidad del servicio. |
| **Perfil empresarial** | Define el contexto de la organización (sector, criticidad, requisitos regulatorios), permitiendo que CIAG aplique el nivel de exigencia correcto según el tipo de empresa. |

---

## Qué solución real obtiene una empresa con esto

Gracias a este flujo, una empresa que utiliza CIAG puede obtener, sin intervención manual constante:

- un **diagnóstico objetivo** sobre el estado real de sus sistemas o procesos evaluados;
- **evidencia verificable** que puede mostrarse a auditores, socios o reguladores;
- **recomendaciones documentadas** para corregir, en lugar de solo un reporte de problemas;
- **trazabilidad completa** de cada decisión, disponible para revisión posterior;
- una **respuesta consistente**, sin depender del criterio de una sola persona ni de una revisión manual puntual.

En otras palabras: el flujo EMPRESA → CIAG-DX → CIAG-CORE → EMPRESA convierte lo que normalmente sería una auditoría manual, puntual y costosa, en un proceso automatizado, determinista y disponible de forma continua.

---

## Después del resultado

Todo el recorrido, desde el envío hasta la respuesta, toma pocos segundos. Lo que sigue es trabajo de personas: la empresa reúne a auditores, ingenieros y especialistas con experiencia real para implementar la solución que indica el resultado. Una inteligencia artificial puede ayudar, si la empresa lo desea, a interpretar el resultado ya emitido (ver [`ciag_ai_assistant_role.md`](ciag_ai_assistant_role.md)).

---

Para más información sobre la estructura conceptual de estos contratos, ver [`ciag_json_contracts.md`](ciag_json_contracts.md). Para más información sobre las capas internas que participan en este flujo, ver [`ciag_layers.md`](ciag_layers.md).
