# CIAG — Modelo de Estados en Tiempo de Ejecución (Runtime)

### CIAG GitHub Public — Versión 1.0

> ⚠️ **Nota sobre esta versión:** este documento forma parte de la primera versión pública (v1.0) del repositorio CIAG. Su contenido está sujeto a cambios y actualizaciones a medida que el proyecto avance en su implementación real con empresas, en base a la realidad operativa del sistema. Algunos aspectos aquí descritos corresponden al diseño arquitectónico del sistema y podrán ajustarse conforme el proyecto se lleve a la práctica en producción.

---

## ¿Qué significa que el sistema tenga "estados"?

Cuando se habla del "estado" de CIAG, es importante distinguir entre dos dimensiones completamente distintas, que muchas veces se confunden pero que responden preguntas diferentes:

1. **El estado de una evaluación específica** — qué está pasando, en este momento, con la información concreta que una empresa envió para ser analizada.
2. **El estado contractual de la empresa dentro de la plataforma** — si la organización, como cliente, tiene actualmente acceso habilitado al sistema.

Ambas dimensiones son deterministas y auditables, pero operan en niveles distintos: una es sobre el *proceso de análisis*, y la otra es sobre la *relación contractual*.

---

## 1. El estado de una evaluación específica

Cuando una empresa envía información a CIAG mediante un contrato `.json`, esa información atraviesa un proceso con verificaciones claras en cada etapa. A nivel conceptual, este proceso responde preguntas como:

- ¿La información de entrada fue **aceptada**, o se detectaron fallas u observaciones que impiden continuar?
- Si hubo observaciones, ¿de qué tipo son y qué tan graves resultan?
- ¿El resultado final generado por el sistema es **estable y correcto**, o requiere una revisión adicional?
- ¿Cuántas veces pasó esa información por el proceso de diagnóstico y corrección?

Sobre este último punto: la arquitectura de CIAG está diseñada bajo un modelo de **hasta tres iteraciones** por evaluación:

1. **Diagnóstico** — análisis inicial y detección de hallazgos.
2. **Corrección** — aplicación de la solución correspondiente, cuando aplica.
3. **Certificación** — una revalidación final que confirma que el resultado es estable antes de entregarlo como definitivo a la empresa.

Este ciclo de verificación en varias etapas es lo que permite que el resultado final no dependa de un único paso de análisis, sino de un proceso revisado y confirmado antes de considerarse certificado.

---

## 2. El estado contractual de la empresa en la plataforma

De forma independiente al estado de una evaluación puntual, existe el estado general de la empresa como cliente dentro de la plataforma en la nube donde opera CIAG. Este estado responde a la pregunta: **¿la empresa puede, en este momento, seguir utilizando el servicio?**

De forma general, una empresa puede encontrarse en situaciones como:

- **activa** — con acceso normal al servicio, dentro del alcance de su contrato o licitación vigente;
- **restringida** — con acceso limitado, por ejemplo mientras se resuelve alguna situación puntual;
- **suspendida** — sin acceso operativo, generalmente asociado a un incumplimiento temporal;
- **en revisión de pago o de renovación** — cuando existe una condición administrativa pendiente antes de continuar con normalidad.

Es importante ser claros en un punto: **el acceso al servicio no es incondicional**. Si una empresa incumple las condiciones establecidas en su contrato o en su licitación empresarial, CIAG contempla la posibilidad de restringir, suspender o —en casos de incumplimiento grave— revocar el acceso al servicio. Esto no ocurre de forma arbitraria: responde a reglas de gobernanza predefinidas, que se aplican de la misma forma a cualquier empresa, sin excepciones basadas en criterio subjetivo.

Este mecanismo protege tanto la integridad del sistema como la relación contractual entre CIAG y cada una de las empresas que lo utilizan.

---

## Por qué se separan estas dos dimensiones

Separar el estado de una evaluación del estado contractual de la empresa permite que ambos aspectos se gobiernen con reglas propias y consistentes:

- una evaluación puede fallar por razones técnicas (información incompleta, inconsistencias detectadas) sin que eso afecte el estado contractual de la empresa;
- una empresa puede tener su acceso restringido por razones administrativas o de incumplimiento, sin que eso invalide evaluaciones previas ya certificadas.

Esta separación es coherente con el mismo principio de determinismo y gobernanza que rige el resto del sistema: cada dimensión del estado se evalúa de forma independiente, con sus propias reglas, y ninguna de ellas se mezcla ni se decide "a criterio" en el momento.

---

Para más información sobre el flujo general de procesamiento, ver [`ciag_pipeline.md`](ciag_pipeline.md). Para más información sobre los principios de gobernanza que rigen estos estados, ver [`ciag_governance.md`](ciag_governance.md).
