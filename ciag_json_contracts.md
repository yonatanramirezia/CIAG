# CIAG — Contratos Computacionales JSON

### CIAG GitHub Public — Versión 1.0

> ⚠️ **Nota sobre esta versión:** este documento forma parte de la primera versión pública (v1.0) del repositorio CIAG. Su contenido está sujeto a cambios y actualizaciones a medida que el proyecto avance en su implementación real con empresas, en base a la realidad operativa del sistema. Lo aquí descrito refleja el estado conceptual y arquitectónico actual del proyecto.

---

## Un sistema que se comunica mediante contratos, no mediante conversación libre

CIAG no funciona como un asistente conversacional que responde de forma abierta. Se comunica exclusivamente mediante **contratos computacionales en formato JSON**: documentos estructurados, deterministas y validados, que garantizan que la información se intercambie siempre con la misma forma y bajo las mismas reglas, sin importar qué empresa la envíe o desde qué sistema lo haga.

Este enfoque es lo que permite que los resultados de CIAG sean reproducibles, auditables y libres de la ambigüedad propia del lenguaje natural.

---

## Los seis contratos base

Toda la operación fundamental de CIAG se sostiene sobre seis contratos oficiales:

| Contrato | Qué hace |
|---|---|
| **`CIAG_INPUT`** | Es el punto único de entrada: recibe y valida la información que la empresa envía, antes de que cualquier análisis comience. |
| **`CIAG_DIAGNOSTIC_OUTPUT`** | Contiene el diagnóstico generado por CIAG-DX: qué se encontró, con qué nivel de riesgo y con qué evidencia. |
| **`CIAG_REMEDIATION_OUTPUT`** | Documenta las acciones correctivas ejecutadas por CIAG-CORE, cuando la empresa cuenta con licitación empresarial activa. |
| **`CIAG_FORENSIC_TRACE`** | Registra de forma inalterable la evidencia de todo lo ocurrido durante el proceso, para efectos de auditoría. |
| **`CIAG_RUNTIME_STATE`** | Refleja en tiempo real el estado operativo del sistema para esa empresa (activo, restringido, en período de prueba, entre otros). |
| **`CIAG_ENTERPRISE_PROFILE`** | Define el contexto de la organización —sector, criticidad, requisitos regulatorios— para que CIAG aplique el nivel de gobernanza correspondiente. |

---

## Un servicio que se adapta: de la PYME al gobierno

El servicio de contratos `.json` de CIAG no está diseñado para un único tipo de organización. Se adapta según las necesidades reales de cada cliente, ya sea una pequeña o mediana empresa (PYME), una empresa de mayor escala, o una entidad gubernamental.

Esto significa que una organización puede consultar el servicio cada vez que lo requiera —para revisar información, aclarar una duda operativa, solicitar una solución concreta, o simplemente apoyar la toma de decisiones— sin depender de ciclos de auditoría fijos ni de la disponibilidad de un equipo humano dedicado exclusivamente a esa tarea.

---

## Auditoría automática, en la nube, respetando la protección de datos

El servicio de contratos JSON de CIAG opera sobre infraestructura desplegada en la nube (actualmente Railway, aunque la arquitectura no depende de forma permanente de un único proveedor).

Esto permite que las empresas obtengan una **auditoría automática y continua** de su información, sin necesidad de instalar herramientas adicionales dentro de su propia infraestructura. Todo el proceso se diseña para respetar las normas de protección de información vigentes en el entorno laboral y jurisdicción de cada organización, procesando únicamente la información necesaria para el diagnóstico o la solución solicitada.

---

## Esta automatización no reemplaza a las personas — las organizaciones se adaptan al resultado

Es importante aclarar un punto que suele generar dudas: la auditoría automática que ofrece CIAG, a través del diagnóstico y la solución entregados en formato `.json`, **no está diseñada para afectar negativamente a los trabajadores de una organización**.

Lo que ocurre, en la práctica, es lo contrario: son las organizaciones y sus equipos quienes se apoyan en el diagnóstico y la solución entregados por CIAG para ajustar procesos, corregir inconsistencias y mejorar su forma de operar. El resultado de los contratos `.json` funciona como una herramienta de apoyo para las personas responsables de cada área, no como un mecanismo que sustituye su trabajo o su criterio.

---

Para más información sobre cómo se genera y utiliza esta información dentro del sistema, ver [`ciag_pipeline.md`](ciag_pipeline.md). Para más información sobre los principios de seguridad aplicados a esta información, ver [`ciag_security_model.md`](ciag_security_model.md).
