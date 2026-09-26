# CIAG — Alineación con Marcos Regulatorios

### CIAG GitHub Public — Versión 1.0

> ⚠️ **Nota sobre esta versión:** este documento forma parte de la primera versión pública (v1.0) del repositorio CIAG. Su contenido está sujeto a cambios y actualizaciones a medida que el proyecto avance en su implementación real con empresas, en base a la realidad operativa del sistema. Lo aquí descrito refleja el estado conceptual y arquitectónico actual del proyecto, y no constituye una certificación legal ni una garantía de cumplimiento normativo absoluto.

---

## ¿Por qué es importante este documento?

La adopción de la inteligencia artificial a nivel global se ha acelerado más rápido que la creación de marcos regulatorios claros para gobernarla. Sin embargo, esa situación está cambiando: cada vez más países y regiones están estableciendo normativas específicas sobre el uso responsable de la IA en procesos empresariales, financieros, de salud y de gobierno.

CIAG fue diseñado desde su origen con esta realidad en mente: no como una solución que reacciona después de que aparece una nueva ley, sino como una arquitectura de gobernanza pensada para poder adaptarse a la evolución normativa sin perder su identidad ni su determinismo.

---

## Un componente dedicado a la integridad y la adaptación normativa

Dentro de la arquitectura de CIAG existe un componente específico responsable de la protección criptográfica de la información y de mantener el sistema alineado con la evolución de los marcos regulatorios internacionales.

Este componente cumple, entre otras, las siguientes funciones:

- proteger la integridad y autenticidad de los contratos computacionales y de la evidencia generada por el sistema;
- generar y verificar mecanismos de autenticidad sobre la información procesada;
- servir de apoyo a los procesos de auditoría y trazabilidad;
- adaptarse a nuevos estándares de seguridad, cifrado o normativa sin requerir una reconstrucción del núcleo determinista de CIAG.

Este diseño permite que, cuando una regulación cambie o aparezca un nuevo estándar internacional, la arquitectura pueda actualizarse en los componentes correspondientes, sin comprometer la estabilidad del resto del sistema.

---

## Identificación, trazabilidad y verificación

Cada operación procesada por CIAG queda asociada a un identificador único que permite su seguimiento y verificación posterior. Gracias a este mecanismo, es posible reconstruir de forma auditable el recorrido completo de una decisión: qué información ingresó, qué reglas se aplicaron, y qué resultado se obtuvo — sin necesidad de exponer el funcionamiento interno del sistema ni comprometer la confidencialidad de la información de la empresa.

Esta capacidad de identificación y trazabilidad es uno de los principios estructurales de CIAG, y es lo que permite que sus resultados puedan ser revisados por auditores internos, auditores externos o entes reguladores cuando así se requiera.

---

## Marcos y estándares con los que CIAG busca alinearse

CIAG fue diseñado para facilitar procesos de gobernanza, trazabilidad, auditoría y gestión de riesgos alineados con los principales marcos regulatorios y estándares internacionales vigentes. Esto no sustituye una certificación oficial ni garantiza por sí solo el cumplimiento legal de una organización, pero proporciona una base técnica que ayuda a las empresas a prepararse frente a esos requisitos.

Entre los marcos con los que CIAG busca mantenerse alineado se encuentran, de forma general:

- **Unión Europea:** el Reglamento de Inteligencia Artificial de la Unión Europea (EU AI Act) y el Reglamento General de Protección de Datos (GDPR).
- **Estados Unidos:** los marcos de referencia del NIST (Instituto Nacional de Estándares y Tecnología) para gestión de riesgos en Inteligencia Artificial y ciberseguridad.
- **China:** normativa sobre protección de información personal e Inteligencia Artificial Generativa.
- **Colombia:** la legislación vigente en materia de protección de datos personales, hábeas data y delitos informáticos.
- **Marcos internacionales adicionales:** normas ISO/IEC relacionadas con gestión de Inteligencia Artificial y seguridad de la información, los principios de IA de la OCDE, y buenas prácticas reconocidas internacionalmente para sistemas basados en modelos de lenguaje.

La filosofía de CIAG es mantener una arquitectura de gobernanza determinista capaz de adaptarse a la evolución normativa global, sin necesidad de reconstruir su núcleo cada vez que aparece un nuevo estándar o regulación.

---

Para más información sobre los principios generales de seguridad del sistema, ver [`ciag_security_model.md`](ciag_security_model.md). Para más información sobre los principios de gobernanza, ver [`ciag_governance.md`](ciag_governance.md).
