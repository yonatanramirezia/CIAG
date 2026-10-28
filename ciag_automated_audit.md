# CIAG — Auditoría Automática

### CIAG GitHub Public — Versión 1.2

> ⚠️ **Nota sobre esta versión:** este documento forma parte de la versión pública 1.2 del repositorio CIAG, actualizada el 26 de octubre de 2026: se amplía a 23 tipos de empresa y se agregan la misión y visión del proyecto y los canales públicos. El servicio .JSON ya responde en el servidor real. El contenido puede seguir cambiando a medida que el proyecto avance con empresas, en base a la realidad operativa del sistema.

---

## ¿Qué es la auditoría automática de CIAG?

La auditoría automática es, en esencia, el propio sistema CIAG operando de forma continua en la nube: una plataforma que las empresas pueden consultar durante el día, y todos los días, sin depender de ciclos de revisión programados ni de la disponibilidad de un equipo humano dedicado exclusivamente a esa tarea.

En la práctica, esto automatiza la parte repetitiva de la revisión, que en el modelo tradicional puede tomar semanas en programarse, ejecutarse y consolidarse en un informe. Con CIAG, esa misma necesidad —entender el estado real de la información, detectar riesgos, y apoyar la toma de decisiones— puede resolverse en **pocos segundos** (en las pruebas reales, menos de 3 segundos de extremo a extremo), en el momento en que la empresa lo requiere y cuantas veces lo requiera.

**CIAG no reemplaza la auditoría ni a los auditores:** es una herramienta importante para ellos. Libera su tiempo de la revisión repetitiva para dedicarlo a lo que requiere criterio humano: analizar, decidir e implementar soluciones.

Lo que distingue a esta auditoría automática de una revisión manual tradicional es que la información que entrega es:

- **limpia** — estructurada y libre de ambigüedad, gracias al formato determinista de los contratos `.json`;
- **trazable** — cada resultado puede reconstruirse y verificarse en cualquier momento posterior;
- **basada en reglas fijas** — no se basa en impresiones ni en criterios subjetivos, sino en reglas aplicadas de forma consistente sobre la información recibida.

---

## El retorno de inversión (ROI), en base a información real

Uno de los cambios más importantes que introduce este modelo es la forma en que una organización puede evaluar el retorno de su inversión en CIAG.

En un esquema tradicional, el ROI de una auditoría o una asesoría suele ser, en buena medida, una estimación: se proyecta un beneficio esperado, pero rara vez se puede observar de forma continua y verificable. Con la auditoría automática de CIAG, la organización puede consultar el estado de su información **cada día**, lo que permite observar el impacto del sistema sobre sus procesos de forma cercana al tiempo real, en lugar de depender de una proyección hecha una sola vez al inicio del proyecto.

Esto también ayuda a que la empresa revise sus cifras y procesos internos con la situación real reflejada por la información que envía, en lugar de depender exclusivamente de cortes de auditoría periódicos.

Es importante aclarar que esto no constituye una garantía financiera ni una promesa de resultados específicos: lo que ofrece CIAG es una base de información continua, verificable y actualizada, sobre la cual la organización puede tomar sus propias decisiones financieras y operativas con mayor certeza.

---

## ¿Qué información puedo llevar al proyecto CIAG? ¿Qué puede analizar?

CIAG está diseñado para recibir y analizar distintos tipos de información empresarial, siempre a través de los contratos computacionales oficiales. En términos generales, una organización puede llevar información relacionada con:

- **software y sistemas** — el comportamiento y la configuración de aplicaciones o plataformas propias;
- **registros de actividad (logs)** — eventos y trazas generadas por los sistemas de la empresa;
- **configuraciones** — parámetros y ajustes de los entornos evaluados;
- **arquitectura** — la estructura general de los sistemas o procesos que se desean analizar;
- **integraciones (APIs)** — cómo se conectan distintos sistemas entre sí;
- **datos operativos** — información relevante para el proceso de diagnóstico solicitado.

Toda esta información se procesa únicamente dentro del alcance autorizado por el contrato correspondiente, y siempre respetando las políticas de privacidad y protección de datos aplicables a cada organización. CIAG no requiere acceso irrestricto a los sistemas de una empresa: solo procesa la información que la organización decide enviar para el análisis solicitado.

---

## Beneficios en profundidad para empresas y gobiernos

Más allá del diagnóstico puntual, trabajar con CIAG mediante archivos `.json` aporta beneficios que se profundizan con el uso continuo del sistema:

- **Decisiones mejor fundamentadas** — al contar con información estructurada, verificable y actualizada, los responsables de cada área pueden tomar decisiones con mayor certeza y menor dependencia de estimaciones.
- **Reducción de riesgos operativos** — la detección temprana de inconsistencias permite actuar antes de que un problema se convierta en un incidente mayor.
- **Menor carga en la revisión repetitiva** — la información queda disponible de forma continua, y la auditoría se concentra en lo que requiere criterio humano.
- **Nuevos puestos de trabajo reales** — alrededor de cada resultado, auditores, ingenieros y especialistas implementan la solución dentro de la empresa.
- **Evidencia lista para reguladores y auditores externos** — la trazabilidad generada por CIAG facilita los procesos de cumplimiento normativo, sin necesidad de reconstruir manualmente el historial de decisiones.
- **Adaptabilidad institucional** — tanto empresas privadas como entidades gubernamentales pueden ajustar el uso del sistema a su propia escala, sector y nivel de criticidad operativa.
- **Fortalecimiento de la confianza institucional** — ante clientes, socios, inversionistas y organismos de control, contar con un sistema de gobernanza determinista y auditable es, en sí mismo, un elemento diferenciador.

---

## Después del resultado: trabajo de personas

Recibir el resultado es el comienzo del trabajo. La empresa reúne a personas con experiencia y conocimiento real para implementar la solución indicada, y una inteligencia artificial puede ayudar, si se desea, a interpretar el resultado ya emitido (ver [`ciag_ai_assistant_role.md`](ciag_ai_assistant_role.md)). Las recomendaciones no se ejecutan solas: las personas deciden y actúan.

---

Para más información sobre cómo se estructura este servicio, ver [`ciag_json_contracts.md`](ciag_json_contracts.md). Para más información sobre los principios de seguridad y protección de la información, ver [`ciag_security_model.md`](ciag_security_model.md).
