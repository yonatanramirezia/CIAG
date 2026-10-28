# CIAG — Contratos Computacionales JSON

### CIAG GitHub Public — Versión 1.2

> ⚠️ **Nota sobre esta versión:** este documento forma parte de la versión pública 1.2 del repositorio CIAG, actualizada el 26 de octubre de 2026: se amplía a 23 tipos de empresa y se agregan la misión y visión del proyecto y los canales públicos. El servicio .JSON ya responde en el servidor real. El contenido puede seguir cambiando a medida que el proyecto avance con empresas, en base a la realidad operativa del sistema.

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
| **`CIAG_REMEDIATION_OUTPUT`** | Documenta las acciones correctivas recomendadas por CIAG-CORE y la evidencia de su implementación por parte de la empresa. |
| **`CIAG_FORENSIC_TRACE`** | Registra, con huellas de verificación, la evidencia de todo lo ocurrido durante el proceso, para efectos de auditoría. |
| **`CIAG_RUNTIME_STATE`** | Refleja en tiempo real el estado operativo del sistema para esa empresa (activo, restringido, en período de prueba, entre otros). |
| **`CIAG_ENTERPRISE_PROFILE`** | Define el contexto de la organización —sector, criticidad, requisitos regulatorios— para que CIAG aplique el nivel de gobernanza correspondiente. |

---

## Cómo se envía el archivo hoy

La empresa llena el archivo `CIAG_INPUT.json` (14 campos con estructura fija) y lo envía directamente al servicio. No necesita programar: puede hacerlo con una aplicación de **Atajos HTTP** en el celular o la tableta, que guarda la dirección del servicio, el tipo de petición y el archivo para repetir el envío con un toque. La respuesta llega en la misma conexión, en pocos segundos, con el resultado VERDE o ROJO y tres documentos: resolución, informe y trazabilidad.

Si la empresa lo desea, una inteligencia artificial puede ayudarle a llenar el archivo, a configurar el atajo y a interpretar el resultado. No se deben enviar datos personales, contraseñas ni claves: la revisión no los necesita.

---

## Un servicio que se adapta: de la PYME al gobierno

El servicio de contratos `.json` de CIAG no está diseñado para un único tipo de organización. Se adapta según las necesidades reales de cada cliente, ya sea una pequeña o mediana empresa (PYME), una empresa de mayor escala, o una entidad gubernamental.

Hay 23 tipos de empresa documentados (por ejemplo banca, salud, industria, energía, comercio o gobierno). Esto significa que una organización puede consultar el servicio cada vez que lo requiera —para revisar información, aclarar una duda operativa, solicitar una solución concreta, o simplemente apoyar la toma de decisiones— sin depender de ciclos de auditoría fijos ni de la disponibilidad de un equipo humano dedicado exclusivamente a esa tarea.

---

## Auditoría automática, en la nube, respetando la protección de datos

El servicio de contratos JSON de CIAG opera sobre infraestructura desplegada en la nube (actualmente Railway, aunque la arquitectura no depende de forma permanente de un único proveedor).

Esto permite que las empresas obtengan una **auditoría automática y continua** de su información, sin necesidad de instalar herramientas adicionales dentro de su propia infraestructura. Todo el proceso se diseña para respetar las normas de protección de información vigentes en el entorno laboral y jurisdicción de cada organización, procesando únicamente la información necesaria para el diagnóstico o la solución solicitada.

---

## Esta automatización no reemplaza a las personas — las organizaciones se adaptan al resultado

Es importante aclarar un punto que suele generar dudas: la auditoría automática que ofrece CIAG, a través del diagnóstico y la solución entregados en formato `.json`, **no está diseñada para afectar negativamente a los trabajadores de una organización**.

Lo que ocurre, en la práctica, es lo contrario: son las organizaciones y sus equipos quienes se apoyan en el diagnóstico y la solución entregados por CIAG para ajustar procesos, corregir inconsistencias y mejorar su forma de operar. El resultado de los contratos `.json` funciona como una herramienta de apoyo para las personas responsables de cada área, no como un mecanismo que sustituye su trabajo o su criterio. Más aún: después de cada resultado, la empresa reúne a auditores, ingenieros y especialistas para implementar la solución, lo que crea trabajo real alrededor del servicio.

---

Para más información sobre cómo se genera y utiliza esta información dentro del sistema, ver [`ciag_pipeline.md`](ciag_pipeline.md). Para más información sobre los principios de seguridad aplicados a esta información, ver [`ciag_security_model.md`](ciag_security_model.md).
