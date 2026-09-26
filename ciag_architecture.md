# CIAG — Arquitectura: CIAG-DX y CIAG-CORE

### CIAG GitHub Public — Versión 1.0

> ⚠️ **Nota sobre esta versión:** este documento forma parte de la primera versión pública (v1.0) del repositorio CIAG. Su contenido está sujeto a cambios y actualizaciones a medida que el proyecto avance en su implementación real con empresas, en base a la realidad operativa del sistema. Lo aquí descrito refleja el estado conceptual y arquitectónico actual del proyecto.

---

## Dos subsistemas, dos responsabilidades

La arquitectura de CIAG está dividida en dos grandes subsistemas complementarios, cada uno con una responsabilidad exclusiva y no intercambiable: **CIAG-DX** y **CIAG-CORE**.

Esta separación no es una decisión de conveniencia técnica: es un principio de gobernanza. Ningún componente del sistema puede diagnosticar y ejecutar remediaciones al mismo tiempo. Separar ambas funciones es lo que permite que exista una verificación independiente antes de que cualquier corrección se aplique.

---

## CIAG-DX — Diagnóstico

CIAG-DX es el subsistema responsable de **observar, analizar y detectar**.

Su función es recibir la información de la empresa, procesarla de forma determinista, y entregar un diagnóstico objetivo: qué se encontró, con qué nivel de riesgo, y con qué evidencia se respalda esa conclusión.

CIAG-DX **nunca ejecuta acciones correctivas ni modifica sistemas de la empresa**. Su responsabilidad termina en el momento en que entrega el diagnóstico. Cualquier corrección, si la empresa la requiere, corresponde a un subsistema distinto.

---

## CIAG-CORE — Solución

CIAG-CORE es el subsistema responsable de **decidir y actuar**.

Una vez que CIAG-DX genera un diagnóstico, CIAG-CORE evalúa esa información bajo las reglas de gobernanza autorizadas y, cuando corresponde, ejecuta acciones correctivas de forma controlada, documentada y verificable.

CIAG-CORE **nunca actúa sin un diagnóstico previo válido**, y su ejecución siempre queda registrada con evidencia completa de qué se hizo y por qué.

---

## Por qué esta separación importa

Separar diagnóstico y solución en dos subsistemas distintos aporta:

- **verificación independiente** — quien detecta un problema no es quien decide ni ejecuta la corrección;
- **menor riesgo de errores en cascada** — una corrección nunca se aplica sin haber sido evaluada primero;
- **trazabilidad más clara** — es posible distinguir en todo momento qué fue análisis y qué fue acción real sobre el sistema;
- **gobernanza más sólida** — cada subsistema opera dentro de límites estrictamente definidos, sin invadir el terreno del otro.

---

## Cómo se activa cada subsistema: importante para entender el servicio

Es importante aclarar que **CIAG no opera con ambos subsistemas activos desde el primer contacto con una empresa**. El acceso a cada uno depende del tipo de servicio contratado:

- **Contrato inicial (diagnóstico):** una empresa que inicia su relación con CIAG accede, en primera instancia, únicamente a **CIAG-DX**. Durante este período —de 30 días— el sistema entrega diagnósticos reales sobre la información de la empresa, pero **no ejecuta ninguna remediación ni acción correctiva real**. Es una etapa de evaluación y conocimiento mutuo entre la empresa y la plataforma.

- **Licitación empresarial (servicio completo):** el acceso a **CIAG-CORE** —es decir, la capacidad real de ejecutar correcciones— solo se habilita una vez que la empresa formaliza una **licitación empresarial**, con vigencia anual y renovable. Es en esta etapa donde CIAG-DX y CIAG-CORE operan juntos, de forma coordinada, ofreciendo el servicio completo de diagnóstico y solución.

Esta distinción es importante porque evita una idea equivocada frecuente: **el servicio inicial no es el servicio completo.** El diagnóstico por sí solo ya aporta valor real a una organización, pero la capacidad de corrección automatizada y sostenida en el tiempo pertenece exclusivamente a la etapa de licitación empresarial formal.

---

Para más información sobre el flujo general entre ambos subsistemas, ver [`ciag_pipeline.md`](ciag_pipeline.md). Para más información sobre los principios de gobernanza que regulan esta separación, ver [`ciag_governance.md`](ciag_governance.md).
