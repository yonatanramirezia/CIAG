# CIAG — ¿Qué es?

### CIAG GitHub Public — Versión 1.0

> ⚠️ **Nota sobre esta versión:** este documento forma parte de la primera versión pública (v1.0) del repositorio CIAG. Su contenido está sujeto a cambios y actualizaciones a medida que el proyecto avance en su implementación real con empresas, en base a la realidad operativa del sistema. Lo aquí descrito refleja el estado conceptual y arquitectónico actual del proyecto.

---

## ¿Qué es CIAG en términos simples?

CIAG (Constitución de Inteligencia Artificial Global) es un sistema de gobernanza para Inteligencia Artificial y software que supervisa, analiza y valida el comportamiento de otros sistemas antes de que una decisión se considere válida.

Su función es transformar resultados inciertos o probabilísticos en resultados verificables, trazables y deterministas, ayudando a que las organizaciones puedan confiar en la información que utilizan para tomar decisiones.

CIAG no reemplaza el software ni la inteligencia artificial que una empresa ya utiliza. Funciona como una capa adicional de supervisión que se integra con los sistemas existentes para revisar, validar y certificar sus resultados, de modo que la empresa conserva sus plataformas actuales mientras incorpora un mecanismo de control y confiabilidad sobre sus procesos críticos.

---

## ¿Qué problema resuelve?

La adopción de la inteligencia artificial ha crecido más rápido que los mecanismos de gobernanza para supervisarla. Actualmente, muchas organizaciones enfrentan desafíos como:

- decisiones automatizadas difíciles de explicar;
- falta de trazabilidad sobre cómo un sistema de IA llegó a una conclusión;
- ausencia de controles unificados cuando se utilizan múltiples modelos de IA al mismo tiempo;
- dependencia de sistemas probabilísticos cuyos resultados pueden variar ante una misma situación;
- dificultad para demostrar, ante auditores, clientes o reguladores, que un proceso automatizado es confiable.

CIAG nace para reducir estos riesgos mediante una arquitectura de gobernanza computacional determinista, aportando reglas, validación y trazabilidad sobre el uso de la inteligencia artificial dentro de una organización.

---

## La filosofía central: de lo probabilístico a lo determinista

Los modelos de inteligencia artificial tradicionales generan respuestas basadas en probabilidades, por lo que una misma consulta puede producir resultados distintos según el contexto o el modelo utilizado.

CIAG no modifica el funcionamiento interno de esos modelos. En cambio, toma sus resultados y los somete a un proceso de validación basado en reglas, contratos y criterios de gobernanza previamente definidos. Solo cuando un resultado cumple esas condiciones puede convertirse en una decisión válida para la organización.

En otras palabras: **la inteligencia artificial puede proponer una respuesta, pero es CIAG quien determina si esa respuesta puede convertirse en una decisión confiable.**

Este principio se resume en una idea simple y central para todo el sistema:

> La misma entrada, bajo las mismas condiciones, siempre debe producir el mismo resultado.

---

## Lo que CIAG no es

- No es un modelo de lenguaje ni un chatbot.
- No sustituye el criterio humano ni la decisión estratégica de una organización.
- No pretende reemplazar a los equipos de tecnología o de IT de una empresa.
- No es una "super-IA" reguladora que actúa por encima de las personas.

La decisión final continúa siendo siempre responsabilidad de las personas autorizadas dentro de cada organización. CIAG gobierna procesos automatizados; no gobierna a las personas.

---

## En resumen: una capa de gobernanza determinista

CIAG puede resumirse como una **capa de gobernanza determinista** que se integra a la operación de una empresa para transformar procesos que normalmente requerirían auditoría y diagnóstico constante y manual, en un proceso automatizado, estructurado y verificable.

Esa gobernanza se materializa a través de un **servicio basado en contratos computacionales en formato JSON**: la empresa envía la información que desea que CIAG analice, y el sistema entrega de vuelta una respuesta clara y definida —no una opinión ni una estimación—, con evidencia, trazabilidad y una clasificación determinista del resultado.

Esto le permite a una organización obtener, de forma automática, un diagnóstico o una validación que de otro modo dependería de revisiones periódicas, auditorías puntuales o intervención manual constante.

---

## Infraestructura del servicio

El servicio de CIAG se despliega actualmente sobre infraestructura en la nube, utilizando **Railway** como plataforma de orquestación y ejecución.

La arquitectura de CIAG fue diseñada para no depender de forma permanente de un único proveedor de infraestructura. Si en el futuro resulta conveniente o necesario migrar hacia otra plataforma, la arquitectura está preparada para adaptarse a esos cambios, manteniendo la misma gobernanza, los mismos principios deterministas y el mismo comportamiento del sistema, independientemente de dónde se ejecute.

---

Para más información sobre cómo se estructura el sistema, ver [`ciag_layers.md`](ciag_layers.md) y [`ciag_architecture.md`](ciag_architecture.md). Para más información sobre el servicio de contratos JSON, ver [`ciag_json_contracts.md`](ciag_json_contracts.md).
