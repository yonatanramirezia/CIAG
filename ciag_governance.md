# CIAG — Gobernanza

### CIAG GitHub Public — Versión 1.0

> ⚠️ **Nota sobre esta versión:** este documento forma parte de la primera versión pública (v1.0) del repositorio CIAG. Su contenido está sujeto a cambios y actualizaciones a medida que el proyecto avance en su implementación real con empresas, en base a la realidad operativa del sistema. Lo aquí descrito refleja el estado conceptual y arquitectónico actual del proyecto.

---

## ¿Qué es la gobernanza determinista?

La gobernanza determinista es el conjunto de reglas fijas, verificables y no negociables bajo las cuales opera CIAG. A diferencia de un sistema que decide según lo que "parece razonable" en el momento, CIAG decide siempre según reglas previamente definidas, aplicadas de la misma forma sin importar quién consulte el sistema ni cuándo lo haga.

Esta gobernanza no es un conjunto de configuraciones opcionales: es el marco que le da a CIAG su identidad. Sin gobernanza determinista, no existiría forma de garantizar que dos evaluaciones equivalentes produzcan siempre el mismo resultado.

---

## Un marco constitucional, no un conjunto de reglas sueltas

CIAG no funciona como una colección de validaciones independientes. Funciona como un **marco constitucional**: un conjunto coherente de principios que se sostienen entre sí y que se aplican de manera uniforme desde el primer momento en que la información ingresa al sistema, hasta el último paso en que se entrega un resultado certificado a la empresa.

Ese marco se organiza, en términos generales, alrededor de dos tipos de reglas:

- **Mandamientos** — principios que rigen el comportamiento y el proceso: qué debe verificarse, qué debe evitarse, y cómo debe comportarse el sistema en cada etapa del análisis.
- **Pilares** — principios que rigen la integridad y la identidad estructural del sistema: qué debe permanecer estable y verificable en cualquier circunstancia.

No es objetivo de este documento público detallar cada uno de estos principios de forma técnica, pero sí es importante que quede clara su función: son la base sobre la cual se construye cada decisión de CIAG, y ninguna parte del sistema puede operar en contradicción con ellos.

La **coherencia** es, en este sentido, uno de los valores más importantes de todo el proyecto: los mismos principios que gobiernan la primera etapa del proceso son los que gobiernan la última. No hay una versión "relajada" de la gobernanza en ningún punto del recorrido.

---

## Los tres resultados posibles: VERDE, ROJO — y AMARILLO durante el proceso

Ya se explicó en [`ciag_determinism.md`](ciag_determinism.md) que el resultado final de una evaluación de CIAG siempre se comunica como **VERDE** (cumple los criterios) o **ROJO** (requiere atención).

Sin embargo, durante el proceso interno de análisis —antes de llegar a esa conclusión final— puede existir un estado intermedio: **AMARILLO**. Este estado no es un resultado final ni se entrega como tal a la empresa; representa una condición de ambigüedad o incertidumbre detectada en alguna etapa del análisis, que el sistema debe resolver internamente antes de poder emitir una decisión.

CIAG no permite que una evaluación quede finalizada en estado de ambigüedad. Todo proceso interno en AMARILLO debe resolverse, mediante las reglas de gobernanza correspondientes, hacia una decisión binaria y determinista: VERDE o ROJO. Esto garantiza que la empresa nunca reciba una respuesta ambigua o a medias — solo resultados claros, ya procesados y resueltos.

---

## El rol del ser humano: autoridad final

Uno de los principios más importantes de la gobernanza de CIAG es que **la inteligencia artificial no actúa como autoridad final de decisión**. Esa autoridad pertenece siempre a las personas responsables dentro de cada organización.

CIAG no sustituye directivos, analistas, auditores ni especialistas. Su función es ofrecer información confiable, evaluar riesgos y garantizar que los procesos automatizados respeten las reglas establecidas — pero la decisión estratégica final, sobre qué hacer con esa información, siempre corresponde a las personas.

---

## CIAG como puente determinista entre el ser humano y la IA

Es importante aclarar qué papel cumple exactamente la inteligencia artificial dentro de este sistema, porque suele malinterpretarse.

CIAG **no reemplaza** a los modelos de inteligencia artificial probabilística que una empresa ya utiliza, ni reemplaza el criterio o la decisión de las personas. En cambio, actúa como un **puente de comunicación determinista** entre ambos: toma el análisis que puede generar una inteligencia artificial —naturalmente probabilística por diseño— y lo somete a un proceso de validación, gobernanza y verificación antes de que ese análisis pueda convertirse en una decisión o una acción real dentro de la organización.

Dicho de otra forma: CIAG no compite con la inteligencia artificial ni con el ser humano — conecta a ambos bajo un mismo marco de reglas claras, permitiendo que la capacidad analítica de la IA y el criterio humano trabajen juntos, de forma ordenada y verificable, en la toma de decisiones y la solución de problemas empresariales reales.

---

Para más información sobre cómo se traduce esta gobernanza en la práctica, ver [`ciag_determinism.md`](ciag_determinism.md) y [`ciag_architecture.md`](ciag_architecture.md).
