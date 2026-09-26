# CIAG — Modelo de Seguridad

### CIAG GitHub Public — Versión 1.0

> ⚠️ **Nota sobre esta versión:** este documento forma parte de la primera versión pública (v1.0) del repositorio CIAG. Su contenido está sujeto a cambios y actualizaciones a medida que el proyecto avance en su implementación real con empresas, en base a la realidad operativa del sistema. Lo aquí descrito refleja el estado conceptual y arquitectónico actual del proyecto.

---

## Principios generales de seguridad

La seguridad dentro de CIAG se sostiene sobre cuatro principios que operan de forma conjunta en cada etapa del sistema:

- **Cifrado** — la información se protege mediante mecanismos criptográficos, tanto durante su transmisión como en los mecanismos de verificación de integridad de los contratos computacionales.
- **Trazabilidad** — cada operación queda asociada a un identificador único que permite reconstruir, en cualquier momento posterior, qué ocurrió y en qué orden.
- **Auditoría** — todo el proceso genera evidencia verificable, disponible para revisión interna, externa o regulatoria cuando corresponde.
- **Protección de datos** — la información de cada empresa se procesa exclusivamente dentro del alcance autorizado para el análisis solicitado, sin exposición innecesaria.

Estos cuatro principios no son controles aislados: forman parte de la misma gobernanza determinista descrita en [`ciag_governance.md`](ciag_governance.md), y se aplican de la misma manera en cada capa del sistema.

---

## Protección de datos: la información permanece bajo control de la empresa

Uno de los principios de diseño más importantes de CIAG es que la información de una empresa **permanece dentro de su propio entorno controlado**. Las organizaciones trabajan con CIAG desde su propia infraestructura, apoyada en la plataforma en la nube sobre la que opera el sistema (actualmente Railway), sin que ello implique una pérdida de control sobre su información.

Solo se procesa la información estrictamente necesaria para el análisis solicitado, siempre a través de los contratos computacionales oficiales, y nunca de forma abierta o sin estructura definida.

Este diseño está pensado para ser compatible con la normativa de protección de datos personales vigente en Colombia, así como con los principios generales de protección de la información reconocidos internacionalmente. La arquitectura de CIAG busca que cada implementación pueda ajustarse a los requisitos regulatorios específicos del país y del sector donde opere cada empresa.

---

## El rol de la inteligencia artificial dentro de CIAG

Es importante ser transparentes sobre un punto: **el propio proyecto CIAG fue construido con apoyo de herramientas de inteligencia artificial**, utilizadas durante su fase de investigación, documentación y desarrollo, siempre bajo la dirección, validación y criterio de su fundador. La inteligencia artificial fue una herramienta de apoyo en la construcción; las decisiones de arquitectura, gobernanza y diseño siempre fueron humanas.

Dentro de la operación del sistema, la inteligencia artificial cumple también un rol de apoyo, no de autoridad. Una vez que la información de una empresa pasa por CIAG-DX y CIAG-CORE y se genera un resultado certificado en formato `.json`, una inteligencia artificial puede actuar como **asistente dentro de la empresa**, ayudando a traducir ese resultado técnico a un lenguaje más claro y orientando sobre cómo implementar lo indicado por el diagnóstico o la solución.

Este uso de la IA como asistente **nunca sustituye ni reinterpreta** el resultado determinista ya generado por CIAG: su función es exclusivamente facilitar la comprensión y la implementación práctica de ese resultado dentro de la organización, siempre bajo la supervisión de las personas responsables.

---

Para más información sobre la relación entre el ser humano y la inteligencia artificial dentro de la gobernanza de CIAG, ver [`ciag_governance.md`](ciag_governance.md). Para más información sobre el cumplimiento de marcos regulatorios internacionales, ver [`ciag_regulatory_compliance.md`](ciag_regulatory_compliance.md).
