# CIAG — Arquitectura: CIAG-DX y CIAG-CORE

### CIAG GitHub Public — Versión 1.2

> ⚠️ **Nota sobre esta versión:** este documento forma parte de la versión pública 1.2 del repositorio CIAG, actualizada el 26 de octubre de 2026: se amplía a 23 tipos de empresa y se agregan la misión y visión del proyecto y los canales públicos. El servicio .JSON ya responde en el servidor real. El contenido puede seguir cambiando a medida que el proyecto avance con empresas, en base a la realidad operativa del sistema.

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

CIAG-CORE es el subsistema responsable de **evaluar y recomendar**.

Una vez que CIAG-DX genera un diagnóstico, CIAG-CORE evalúa esa información bajo las reglas de gobernanza autorizadas y emite **recomendaciones** claras, documentadas y verificables sobre qué corregir.

CIAG-CORE **nunca actúa sin un diagnóstico previo válido**, y **no ejecuta cambios en los sistemas de la empresa**: recomienda, y son las personas responsables quienes deciden e implementan. Cada recomendación queda registrada con su evidencia.

---

## Por qué esta separación importa

Separar diagnóstico y solución en dos subsistemas distintos aporta:

- **verificación independiente** — quien detecta un problema no es quien decide ni ejecuta la corrección;
- **menor riesgo de errores en cascada** — una corrección nunca se recomienda sin haber sido evaluada primero;
- **trazabilidad más clara** — es posible distinguir en todo momento qué fue análisis y qué fue acción real sobre el sistema;
- **gobernanza más sólida** — cada subsistema opera dentro de límites estrictamente definidos, sin invadir el terreno del otro.

---

## Cómo se contrata el servicio

La empresa puede acceder al servicio de dos formas:

- **Contrato de 30 días:** la empresa usa el servicio durante 30 días con sus propios archivos, y recibe en cada respuesta el diagnóstico y las recomendaciones. Es una etapa de evaluación y conocimiento mutuo entre la empresa y la plataforma.
- **Licitación empresarial:** vigencia anual y renovable, con asesoría y reuniones periódicas para revisar los resultados y acompañar su implementación.

En ambos casos CIAG no cambia directamente los sistemas de la empresa: la solución la implementan las personas, con el apoyo opcional de una inteligencia artificial para interpretar el resultado. Esto abre trabajo real para auditores, ingenieros y especialistas.

---

Para más información sobre el flujo general entre ambos subsistemas, ver [`ciag_pipeline.md`](ciag_pipeline.md). Para más información sobre los principios de gobernanza que regulan esta separación, ver [`ciag_governance.md`](ciag_governance.md).
