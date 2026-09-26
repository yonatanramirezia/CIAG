# CIAG — Determinismo

### CIAG GitHub Public — Versión 1.0

> ⚠️ **Nota sobre esta versión:** este documento forma parte de la primera versión pública (v1.0) del repositorio CIAG. Su contenido está sujeto a cambios y actualizaciones a medida que el proyecto avance en su implementación real con empresas, en base a la realidad operativa del sistema. Lo aquí descrito refleja el estado conceptual y arquitectónico actual del proyecto.

---

## El principio central

Todo el sistema CIAG se sostiene sobre un único principio, más importante que cualquier otro:

> **La misma entrada, bajo las mismas condiciones, siempre debe producir el mismo resultado.**

Esto significa que si una empresa envía la misma información, en el mismo contexto y bajo las mismas reglas de gobernanza, CIAG entregará exactamente la misma respuesta, sin importar cuántas veces se repita el proceso ni cuándo se ejecute.

Este principio no es una casualidad del diseño: es la razón de ser de CIAG. Un sistema que se supone debe generar confianza y servir de base para decisiones importantes no puede comportarse de forma distinta cada vez que se le consulta lo mismo.

---

## ¿Dónde vive la probabilidad, entonces?

Los modelos de inteligencia artificial que pueden participar como apoyo dentro de los procesos de CIAG son, por naturaleza, probabilísticos: pueden generar respuestas distintas ante la misma pregunta.

CIAG no elimina esa naturaleza probabilística de la IA, pero sí la contiene: la probabilidad puede existir únicamente durante el análisis interno, nunca en el resultado final que recibe la empresa. Antes de que cualquier resultado se considere válido, debe pasar por reglas, contratos y procesos de validación que son —estos sí— completamente deterministas.

En otras palabras: la IA puede ayudar a pensar, pero no decide sola. Quien decide es la gobernanza determinista de CIAG.

---

## La decisión final: VERDE o ROJO

Para que un sistema sea realmente útil en la toma de decisiones, su resultado final debe ser simple de interpretar. Por eso, CIAG utiliza una clasificación binaria para comunicar el resultado de una evaluación:

- **VERDE** — según la información analizada y las reglas de gobernanza configuradas, la operación cumple los criterios establecidos y puede continuar con normalidad.
- **ROJO** — CIAG ha detectado una condición que requiere atención antes de continuar con el proceso evaluado.

Es importante aclarar que un resultado ROJO no significa automáticamente un error grave o una falla: significa que el sistema identificó una situación que debe revisarse para reducir riesgos y mantener la integridad de la operación. El objetivo de esta clasificación es facilitar decisiones rápidas, claras y respaldadas por un proceso de evaluación determinista, en lugar de dejar la interpretación del resultado a criterios subjetivos.

---

## ¿Por qué importa el determinismo?

El determinismo es lo que permite que los resultados de CIAG puedan:

- **reproducirse** — la misma evaluación, repetida en el tiempo, da el mismo resultado;
- **auditarse** — un tercero puede verificar que el proceso se siguió correctamente;
- **explicarse** — cada resultado puede justificarse con evidencia concreta, no con una intuición;
- **generar confianza** — una organización puede apoyarse en esos resultados para tomar decisiones reales, sabiendo que no dependen del azar ni de una variación inexplicable del sistema.

Sin determinismo, ningún proceso automatizado podría considerarse verdaderamente confiable para decisiones críticas de negocio, cumplimiento normativo o auditoría. El determinismo es, en ese sentido, la base sobre la que se sostiene toda la propuesta de valor de CIAG.

---

Para más información sobre cómo se estructura el sistema de gobernanza que sostiene este principio, ver [`ciag_governance.md`](ciag_governance.md).
