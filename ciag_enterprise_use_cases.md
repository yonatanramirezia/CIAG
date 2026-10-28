# CIAG — Casos de Uso por Sector

### CIAG GitHub Public — Versión 1.2

> ⚠️ **Nota sobre esta versión:** este documento forma parte de la versión pública 1.2 del repositorio CIAG, actualizada el 26 de octubre de 2026: se amplía a 23 tipos de empresa y se agregan la misión y visión del proyecto y los canales públicos. El servicio .JSON ya responde en el servidor real. El contenido puede seguir cambiando a medida que el proyecto avance con empresas, en base a la realidad operativa del sistema. Los casos de uso son de carácter general y no representan compromisos, cifras ni condiciones contractuales específicas.

---

## Un sistema pensado para adaptarse a distintos sectores

La arquitectura de CIAG fue diseñada para adaptarse a organizaciones de naturalezas muy distintas, mediante perfiles empresariales, contratos computacionales y políticas de gobernanza específicas para cada sector. Los principios fundamentales —determinismo, trazabilidad, auditabilidad e identidad semántica— permanecen constantes en todos los casos; lo que cambia es el contexto y las reglas particulares que se configuran según la actividad de cada organización.

A continuación, un resumen general de cómo trabajar con CIAG mediante archivos `.json` puede beneficiar a distintos tipos de organización.

---

## Los 23 tipos de empresa

El servicio tiene reglas y contexto propios para 23 tipos de empresa: banca, fintech, seguros, comercio, servicios profesionales, general, gobierno, defensa, educación, salud, energía, telecomunicaciones, transporte, logística, industria, semiconductores, medios, investigación, nube, programación, páginas web, inteligencia artificial y piloto. Todos están documentados; en el servidor real ya se comprobó el tipo industrial, y los demás se probarán uno a uno. A continuación se describen algunos ejemplos.

---

## 🏥 Salud (hospitales y entidades de salud)

Los hospitales y entidades de salud manejan grandes volúmenes de información sensible: historiales, inventarios de insumos médicos, procesos administrativos y decisiones de recursos que impactan directamente la operación diaria.

CIAG puede apoyar a este sector ayudando a mantener información clara sobre inventarios, procesos administrativos y económicos, facilitando decisiones mejor fundamentadas en materia de recursos, cumplimiento normativo del sector salud, y continuidad operativa — todo con la trazabilidad necesaria para procesos de auditoría interna o regulatoria.

---

## 🏦 Banca y servicios financieros

El sector bancario requiere un nivel de precisión y confianza matemática particularmente alto, dado que gestiona recursos financieros de terceros.

CIAG puede apoyar el manejo de información relacionada con recursos, procesos internos y cumplimiento normativo del sector financiero, ofreciendo diagnósticos deterministas que ayudan a fortalecer la integridad de la información utilizada en la toma de decisiones económicas y operativas.

---

## 🏛️ Gobierno

Las entidades gubernamentales enfrentan el reto de administrar recursos públicos, cumplir marcos legales complejos, y coordinar la operación de distintos ministerios o dependencias con altos estándares de transparencia.

CIAG puede apoyar a este sector ayudando a mantener trazabilidad sobre el cumplimiento de normativas y leyes aplicables, y a organizar de forma más clara la información relacionada con la gestión de ministerios, dependencias y recursos públicos, favoreciendo la transparencia y la rendición de cuentas ante la ciudadanía y los organismos de control.

---

## 🛡️ Defensa

El sector defensa opera bajo exigencias de seguridad, confidencialidad y trazabilidad especialmente estrictas, donde la neutralización oportuna de riesgos y la protección de la información son prioritarias.

CIAG puede apoyar a este sector con un enfoque orientado a la supervivencia y protección del sistema, priorizando la detección temprana de inconsistencias y el manejo trazable de información crítica, siempre bajo los más altos estándares de confidencialidad y gobernanza determinista.

---

## 🔬 Semiconductores, robótica y hardware

Las empresas dedicadas a semiconductores, robótica y desarrollo de hardware manejan procesos de ingeniería complejos, cadenas de producción y decisiones técnicas de alto impacto.

CIAG puede apoyar a este sector ayudando a mantener trazabilidad sobre procesos técnicos y decisiones de ingeniería, facilitando diagnósticos consistentes que apoyen la toma de decisiones en entornos de alta complejidad técnica y operativa.

---

## 💻 Tecnología y software

Las empresas de tecnología y desarrollo de software suelen operar con múltiples sistemas, integraciones y modelos de inteligencia artificial funcionando de forma simultánea.

CIAG puede apoyar a este sector ofreciendo una capa de gobernanza determinista sobre esos sistemas, ayudando a mantener consistencia, trazabilidad y auditabilidad incluso cuando conviven distintas herramientas y proveedores tecnológicos dentro de una misma organización.

---

## 🏢 PYMES (pequeñas y medianas empresas)

Las pequeñas y medianas empresas suelen enfrentar el reto de fortalecer su gobernanza y sus procesos internos sin contar con equipos extensos dedicados exclusivamente a auditoría o cumplimiento.

CIAG puede apoyar a las PYMES entregando diagnósticos claros y accesibles sobre su información, ayudando a identificar riesgos e inconsistencias de forma temprana, y ofreciendo una base de gobernanza que puede crecer junto con la empresa a medida que esta se expande.

---

## 🏭 Industria

Las empresas industriales manejan procesos de producción, mantenimiento y seguridad operativa. Fue el tipo comprobado primero en el servidor real: una empresa de prueba recibió VERDE con información normal y ROJO ante un texto con inyección de código y ante un ataque combinado, en pocos segundos.

---

## Un principio común a todos los sectores

Sin importar el sector, el valor central que CIAG aporta es el mismo: convertir información dispersa, procesos manuales o decisiones basadas en estimaciones, en un proceso de diagnóstico y solución determinista, trazable y verificable — adaptado siempre al contexto, la criticidad y las necesidades regulatorias específicas de cada tipo de organización. En todos los casos, después del resultado, son auditores, ingenieros y especialistas quienes implementan la solución, con la ayuda opcional de una inteligencia artificial para interpretarlo.

---

Para más información sobre cómo funciona el servicio de contratos `.json` que sostiene estos casos de uso, ver [`ciag_json_contracts.md`](ciag_json_contracts.md). Para más información sobre la auditoría automática, ver [`ciag_automated_audit.md`](ciag_automated_audit.md).
