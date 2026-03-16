---
name: sota-research
description: State of the Art (SOTA) research skill. Use when investigating any technical, theoretical, or architectural topic before building something. Synthesizes 5 source pillars — scientific articles, industry standards, reports, best practices, and expert opinions — to establish what already exists and works, preventing reinvention of the wheel. Includes built-in file-based planning (planning-with-files) so all findings persist across the session.
allowed-tools: [WebSearch, WebFetch, Read, Write, Bash]
---

# SOTA Research — Estado del Arte

> **Principio rector**: Antes de diseñar una solución, establece con precisión qué ya existe, qué está probado, y qué es estándar. El conocimiento de un campo tiene capas — desde la opinión práctica hasta el consenso científico. Este skill las recorre todas — y escribe todo a disco para que nada se pierda.

---

## Trigger de uso

Invoca este skill cuando:
- Vas a tomar una decisión de arquitectura técnica
- Quieres saber si existe un estándar para algo que vas a diseñar
- Necesitas saber cuál es el enfoque actual para resolver un problema específico
- Quieres evitar reinventar la rueda antes de implementar algo
- Necesitas argumentar técnicamente una decisión con evidencia científica e industrial

**Ejemplos de invocación:**
- `/sota-research Legal Case Management Systems`
- `/sota-research State machine modeling for legal workflows`
- `/sota-research Multi-tenant SaaS architecture patterns`
- `/sota-research Semantic search in legal documents`

---

## Los 5 Pilares del SOTA

| Pilar | Qué busca | Fuentes típicas |
|-------|-----------|-----------------|
| **1. Artículos Científicos** | Qué está probado empíricamente con rigor metodológico | arXiv, IEEE Xplore, ACM DL, Springer, SSRN, PubMed |
| **2. Estándares Internacionales** | Qué está normalizado y adoptado globalmente | ISO, IEEE, IETF/RFC, W3C, NIST, OMG, OASIS |
| **3. Reportes de la Industria** | Qué adopta el mercado y cuáles son las tendencias reales | Gartner, IDC, McKinsey, Forrester, State of X Reports, CNCF Survey |
| **4. Mejores Prácticas** | Qué funciona en producción real | Documentación oficial, patrones de arquitectura, postmortems, books |
| **5. Opiniones de Expertos** | Qué piensan los referentes del campo | Blogs de practitioners, conferencias (GOTO, Strange Loop, QCon), papers de opinionistas |

---

## ⚡ PASO OBLIGATORIO ANTES DE EMPEZAR — Crear los 3 archivos de planificación

> **Regla no negociable**: NUNCA comiences la investigación sin crear primero estos 3 archivos. Son tu memoria en disco. El contexto de la conversación es RAM volátil — estos archivos son tu disco persistente.

### Crear `sota_task_plan.md`

Crea este archivo en el directorio de trabajo actual con el siguiente contenido adaptado al tema:

```markdown
# SOTA Task Plan: [TEMA]
Fecha de inicio: [FECHA]
Contexto de aplicación: [para qué decisión o proyecto se usa esta investigación]

## Goal
Establecer el estado del arte de [TEMA] sintetizando evidencia científica, estándares,
adopción de mercado, mejores prácticas y opinión experta, para tomar decisiones
informadas y no reinventar la rueda.

## Current Phase
Fase 0 — Definición de alcance

## Phases

### Fase 0: Definición de alcance
- [ ] Clarificar el tema exacto y sus límites
- [ ] Definir preguntas clave a responder
- [ ] Definir horizonte temporal (ej: 2020-presente)
- [ ] Crear sota_findings.md y sota_progress.md
- **Status:** in_progress

### Fase 1: Artículos Científicos
- [ ] Ejecutar queries de búsqueda en arXiv, IEEE, ACM
- [ ] Identificar papers fundacionales y surveys
- [ ] Extraer hallazgos clave → sota_findings.md (Pilar 1)
- **Status:** pending

### Fase 2: Estándares Internacionales
- [ ] Identificar cuerpos de estándares relevantes al dominio
- [ ] Verificar estándares aplicables (ISO, IEEE, RFC, NIST, OMG)
- [ ] Extraer qué normaliza cada estándar → sota_findings.md (Pilar 2)
- **Status:** pending

### Fase 3: Reportes de la Industria
- [ ] Buscar State of X reports, Gartner, ThoughtWorks Radar
- [ ] Identificar tasas de adopción y herramientas líderes
- [ ] Extraer pulso del mercado → sota_findings.md (Pilar 3)
- **Status:** pending

### Fase 4: Mejores Prácticas
- [ ] Buscar en blogs de ingeniería, ADRs, documentación de proyectos maduros
- [ ] Identificar prácticas establecidas y anti-patrones
- [ ] Extraer prácticas consolidadas → sota_findings.md (Pilar 4)
- **Status:** pending

### Fase 5: Opiniones de Expertos
- [ ] Buscar en HackerNews, InfoQ, blogs de practitioners reconocidos
- [ ] Identificar consenso y puntos de disenso
- [ ] Extraer panorama de opinión → sota_findings.md (Pilar 5)
- **Status:** pending

### Fase 6: Síntesis y Reporte Final
- [ ] Leer sota_findings.md completo antes de sintetizar
- [ ] Redactar SOTA Report de 11 secciones
- [ ] Guardar reporte final como sota_report_[TEMA].md
- **Status:** pending

## Preguntas clave a responder
1. ¿Qué enfoques ya existen para resolver [TEMA]?
2. ¿Cuál es el consenso científico/industrial?
3. ¿Existen estándares formales?
4. ¿Qué errores comunes se deben evitar?
5. ¿Qué herramientas/librerías son de facto?

## Decisiones tomadas
| Decisión | Razonamiento |
|----------|-------------|
|          |             |

## Errores encontrados
| Error | Intento | Resolución |
|-------|---------|------------|
|       | 1       |            |
```

### Crear `sota_findings.md`

```markdown
# SOTA Findings: [TEMA]
Fecha: [FECHA]
Tema investigado: [descripción exacta]

> Regla de los 2 actos: Después de cada 2 búsquedas, actualizar este archivo. No esperar al final.

---

## Pilar 1 — Artículos Científicos
<!-- Actualizar después de cada 2 WebSearches en esta fase -->

### Papers encontrados
| Título | Autores | Año | Venue | Hallazgo clave | DOI/Link |
|--------|---------|-----|-------|---------------|----------|
|        |         |     |       |               |          |

### Paper fundacional de referencia
- Título:
- Por qué es fundacional:

### Enfoques validados empíricamente
-

### Brechas identificadas por la literatura
-

---

## Pilar 2 — Estándares Internacionales
<!-- Actualizar después de cada 2 WebSearches en esta fase -->

### Estándares aplicables
| Estándar | Organismo | Año | Qué normaliza | Relevancia | Link oficial |
|----------|-----------|-----|---------------|------------|-------------|
|          |           |     |               |            |             |

### Estándares que NO aplican (y por qué)
-

---

## Pilar 3 — Reportes de la Industria
<!-- Actualizar después de cada 2 WebSearches en esta fase -->

### Reportes encontrados
| Reporte | Fuente | Año | Hallazgo clave | Link |
|---------|--------|-----|---------------|------|
|         |        |     |               |      |

### Tasa de adopción actual
-

### Herramientas líderes del mercado
-

### Tendencia (creciendo / maduro / en declive)
-

### Pain points más reportados
-

---

## Pilar 4 — Mejores Prácticas
<!-- Actualizar después de cada 2 WebSearches en esta fase -->

### Prácticas establecidas
| Práctica | Fundamento/Origen | Anti-patrón asociado |
|----------|------------------|---------------------|
|          |                  |                     |

### Herramientas/librerías de facto
| Nombre | Qué hace | Stars GitHub | Madurez | Link |
|--------|----------|-------------|---------|------|
|        |          |             |         |      |

### Anti-patrones críticos a evitar
-

---

## Pilar 5 — Opiniones de Expertos
<!-- Actualizar después de cada 2 WebSearches en esta fase -->

### Consenso del campo
-

### Debates activos (donde no hay acuerdo)
-

### Cambios recientes de paradigma
-

### Voces disidentes relevantes
| Experto/Fuente | Posición | Argumento central |
|----------------|---------|------------------|
|                |         |                  |

---

## Recursos y fuentes consultadas
<!-- Agregar cada URL/fuente a medida que se consulta -->

### Papers
-

### Estándares
-

### Reportes
-

### Blogs / Conferencias
-

### Debates / Foros
-
```

### Crear `sota_progress.md`

```markdown
# SOTA Progress Log: [TEMA]
Sesión: [FECHA]

## Estado actual
- Fase activa: Fase 0
- Búsquedas realizadas: 0
- Hallazgos guardados: 0

---

## Fase 0 — Definición de alcance
- **Status:** in_progress
- **Iniciada:** [timestamp]
- Acciones:
  -
- Archivos creados:
  - sota_task_plan.md
  - sota_findings.md
  - sota_progress.md

## Fase 1 — Artículos Científicos
- **Status:** pending
- Búsquedas ejecutadas: 0 / ~6
- Acciones:
  -

## Fase 2 — Estándares Internacionales
- **Status:** pending
- Búsquedas ejecutadas: 0 / ~6
- Acciones:
  -

## Fase 3 — Reportes de la Industria
- **Status:** pending
- Búsquedas ejecutadas: 0 / ~6
- Acciones:
  -

## Fase 4 — Mejores Prácticas
- **Status:** pending
- Búsquedas ejecutadas: 0 / ~7
- Acciones:
  -

## Fase 5 — Opiniones de Expertos
- **Status:** pending
- Búsquedas ejecutadas: 0 / ~6
- Acciones:
  -

## Fase 6 — Síntesis
- **Status:** pending
- Acciones:
  -

---

## Log de errores de búsqueda
| Timestamp | Query fallida | Intento | Alternativa usada |
|-----------|--------------|---------|------------------|
|           |              | 1       |                  |

## 5-Question Reboot Check
| Pregunta | Respuesta |
|----------|-----------|
| ¿Dónde estoy? | Fase 0 |
| ¿A dónde voy? | Fases 1-6 |
| ¿Cuál es el goal? | SOTA de [TEMA] |
| ¿Qué aprendí? | Ver sota_findings.md |
| ¿Qué hice? | Ver arriba |
```

---

## Regla de los 2 Actos (2-Action Rule) — CRÍTICA

> **Después de cada 2 búsquedas (WebSearch), DEBES escribir lo encontrado a `sota_findings.md` antes de continuar.**

Esto previene que los hallazgos se pierdan cuando el contexto se llena. La información que no está en disco no existe.

```
WebSearch #1 → resultado en contexto
WebSearch #2 → resultado en contexto
→ STOP: Escribir ambos hallazgos a sota_findings.md (Pilar correspondiente)
→ CONTINUAR con WebSearch #3
```

**Nunca acumules más de 2 búsquedas sin persistir.** Si ya escribiste, puedes continuar.

---

## Workflow de Investigación

```
SOTA Research Progress:
- [ ] INIT: Crear sota_task_plan.md, sota_findings.md, sota_progress.md
- [ ] Fase 0: Definir dominio, alcance y preguntas clave
- [ ] Fase 1: Artículos científicos → actualizar sota_findings.md Pilar 1
- [ ] Fase 2: Estándares internacionales → actualizar sota_findings.md Pilar 2
- [ ] Fase 3: Reportes de la industria → actualizar sota_findings.md Pilar 3
- [ ] Fase 4: Mejores prácticas → actualizar sota_findings.md Pilar 4
- [ ] Fase 5: Opiniones de expertos → actualizar sota_findings.md Pilar 5
- [ ] Fase 6: LEER sota_findings.md completo → sintetizar → sota_report_[TEMA].md
```

Al terminar cada fase: actualizar `sota_task_plan.md` (status: complete) y `sota_progress.md`.

---

## Fase 0 — Definir el dominio y el alcance

Antes de buscar, clarifica y escribe en `sota_task_plan.md`:

```
Tema central: [el concepto exacto a investigar]
Contexto de aplicación: [en qué sistema/producto/decisión se usará]
Preguntas clave a responder:
  - ¿Qué enfoques ya existen para resolver esto?
  - ¿Cuál es el consenso científico/industrial?
  - ¿Existen estándares formales?
  - ¿Qué errores comunes se deben evitar?
Exclusiones: [lo que está fuera de alcance]
Horizonte temporal: [últimos N años — típico: 2020-presente]
```

**Al finalizar Fase 0:**
- Marcar Fase 0 como `complete` en `sota_task_plan.md`
- Actualizar `sota_progress.md` con "Fase 0 completa"
- Actualizar "Current Phase" a "Fase 1"

---

## Fase 1 — Artículos Científicos

**Objetivo**: Identificar qué ha sido validado con evidencia empírica.

### Queries a ejecutar

```
WebSearch: "[TEMA] systematic review [AÑO_INICIO]-[AÑO_FIN]"
WebSearch: "[TEMA] survey paper recent"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 1

WebSearch: "[TEMA] empirical study [AÑO]"
WebSearch: "arxiv [TEMA] [AÑO]"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 1

WebSearch: "IEEE [TEMA] state of the art"
WebSearch: "ACM [TEMA] best paper"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 1
```

### Qué extraer de cada paper

Para cada artículo relevante encontrado, anotar en `sota_findings.md`:
- **Título + autores + año + publicación**
- **Problema que resuelve** (qué gap llena)
- **Metodología** (cómo lo probaron)
- **Hallazgos principales** (qué encontraron)
- **Limitaciones declaradas** (qué no cubre)
- **Citaciones relevantes** (qué otros papers cita que valen la pena)

### Señales de un paper valioso
- Citado por 50+ papers (indica consenso en el campo)
- Publicado en venue de alto impacto (Nature, ICSE, VLDB, NeurIPS, CHI, etc.)
- Incluye comparación empírica de múltiples enfoques
- Es un "survey" o "systematic literature review" del tema

**Al finalizar Fase 1:**
- Marcar Fase 1 como `complete` en `sota_task_plan.md`
- Actualizar estado en `sota_progress.md`

---

## Fase 2 — Estándares Internacionales

**Objetivo**: Identificar qué está formalizado, normalizado, o regulado.

### Cuerpos de estándares a consultar según dominio

| Dominio | Cuerpos relevantes |
|---------|-------------------|
| Software/Arquitectura | ISO/IEC 25010, IEEE 42010, ISO 12207, TOGAF |
| Seguridad | ISO 27001, NIST SP 800-x, OWASP, FIPS |
| APIs/Protocolos | IETF RFC, W3C, OpenAPI Spec |
| Datos/Modelos | ISO 11179, DCAT, Schema.org, Dublin Core |
| Procesos/Calidad | ISO 9001, CMMI, ITIL, COBIT |
| IA/ML | ISO 42001, IEEE 7000, NIST AI RMF |
| Accesibilidad | WCAG (W3C), Section 508 |
| Modelado | OMG (UML, BPMN, DMN, SysML), ISO 19505 |

### Queries a ejecutar

```
WebSearch: "ISO standard [TEMA]"
WebSearch: "IEEE standard [TEMA]"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 2

WebSearch: "RFC [TEMA] protocol"
WebSearch: "NIST guidelines [TEMA]"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 2

WebSearch: "[TEMA] international standard compliance"
WebSearch: "[TEMA] W3C specification"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 2
```

### Qué extraer → sota_findings.md Pilar 2

- **Número y nombre del estándar**
- **Organismo emisor y año**
- **Qué define/normaliza exactamente**
- **Si es de adopción obligatoria o voluntaria**
- **Herramientas/frameworks que lo implementan**
- **Si hay versión vigente vs versión obsoleta**

**Al finalizar Fase 2:**
- Marcar Fase 2 como `complete` en `sota_task_plan.md`
- Actualizar estado en `sota_progress.md`

---

## Fase 3 — Reportes de la Industria

**Objetivo**: Entender qué adopta el mercado real, a qué velocidad, y con qué resultados.

### Fuentes de reportes a consultar

**Analistas y consultoras:**
- Gartner Magic Quadrant / Hype Cycle
- IDC MarketScape
- Forrester Wave
- McKinsey Global Institute
- Deloitte Tech Trends

**Reportes "State of X" anuales:**
- State of DevOps Report (DORA/Google)
- State of JS / State of CSS
- Stack Overflow Developer Survey
- JetBrains Developer Ecosystem
- GitHub Octoverse
- CNCF Annual Survey
- State of API (Postman)
- ThoughtWorks Technology Radar

**Reportes sectoriales:**
- Por industria específica (legal tech, fintech, etc.)
- Reportes de VC sobre tendencias

### Queries a ejecutar

```
WebSearch: "state of [TEMA] report [AÑO]"
WebSearch: "Gartner [TEMA] [AÑO]"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 3

WebSearch: "[TEMA] industry adoption survey [AÑO]"
WebSearch: "ThoughtWorks technology radar [TEMA]"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 3

WebSearch: "[TEMA] market trends [AÑO] report"
WebSearch: "[TEMA] usage statistics developer survey"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 3
```

### Qué extraer → sota_findings.md Pilar 3

- **Tasa de adopción actual** (% de empresas que usan X)
- **Tendencia** (creciendo / maduro / en declive)
- **Líderes del mercado** (quiénes son los players)
- **Pain points más comunes** reportados por usuarios
- **Predicciones a 2-3 años**
- **Comparación vs alternativas**

**Al finalizar Fase 3:**
- Marcar Fase 3 como `complete` en `sota_task_plan.md`
- Actualizar estado en `sota_progress.md`

---

## Fase 4 — Mejores Prácticas

**Objetivo**: Identificar qué funciona en producción real, fuera del contexto académico.

### Fuentes a consultar

**Documentación oficial de proyectos maduros:**
- Documentación de frameworks líderes
- Architecture Decision Records (ADRs) públicos
- Wikis de proyectos open source con +10k stars

**Libros de referencia del campo:**
- O'Reilly, Manning, Pragmatic Programmer, Addison-Wesley

**Postmortems y case studies:**
- Netflix Tech Blog, Uber Engineering, Airbnb Engineering
- Google SRE Books, AWS Architecture Center
- CNCF Case Studies

**Patrones documentados:**
- Martin Fowler's bliki / patterns.eaa.dev
- cloud.google.com/architecture/patterns
- docs.microsoft.com/azure/architecture/patterns
- aws.amazon.com/architecture

### Queries a ejecutar

```
WebSearch: "[TEMA] best practices production [AÑO]"
WebSearch: "[TEMA] patterns architecture guide"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 4

WebSearch: "[EMPRESA_TECH_LIDERES] [TEMA] engineering blog"
WebSearch: "[TEMA] lessons learned at scale"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 4

WebSearch: "Martin Fowler [TEMA]"
WebSearch: "[TEMA] anti-patterns common mistakes"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 4

WebSearch: "awesome [TEMA] github curated list"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 4
```

### Qué extraer → sota_findings.md Pilar 4

- **Prácticas recomendadas** (con su razonamiento)
- **Anti-patrones** (qué no hacer y por qué)
- **Herramientas/librerías de facto** (las que el ecosistema converge)
- **Decisiones de diseño comunes** y sus trade-offs
- **Señales de madurez** del ecosistema (documentación, comunidad, mantenimiento)

**Al finalizar Fase 4:**
- Marcar Fase 4 como `complete` en `sota_task_plan.md`
- Actualizar estado en `sota_progress.md`

---

## Fase 5 — Opiniones de Expertos

**Objetivo**: Capturar el conocimiento tácito que no siempre aparece en papers o estándares.

### Fuentes a consultar

**Blogs de practitioners reconocidos:**
- Martin Fowler (martinfowler.com), Joel Spolsky, Paul Graham
- Referentes específicos del dominio a investigar

**Conferencias técnicas:**
- GOTO Conference, Strange Loop, QCon, InfoQ, USENIX

**Plataformas de debate técnico:**
- Hacker News — threads de "Ask HN"
- Reddit r/programming, r/softwarearchitecture
- Stack Overflow — preguntas con muchos votos y respuestas largas

### Queries a ejecutar

```
WebSearch: "[EXPERTO_CONOCIDO] opinion [TEMA]"
WebSearch: "Hacker News [TEMA] discussion [AÑO]"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 5

WebSearch: "GOTO [AÑO] [TEMA] talk"
WebSearch: "InfoQ [TEMA] article [AÑO]"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 5

WebSearch: "[TEMA] reddit discussion [AÑO]"
WebSearch: "[TEMA] controversy debate practitioners"
→ STOP: Escribir hallazgos a sota_findings.md Pilar 5
```

### Qué extraer → sota_findings.md Pilar 5

- **Posición del experto** (a favor / en contra / matizado)
- **Argumento central** (qué razonamiento usa)
- **Contexto de aplicación** (en qué situaciones aplica)
- **Puntos de disenso** (dónde los expertos no están de acuerdo)
- **Señales de cambio de opinión** (lo que era best practice y ya no lo es)

**Al finalizar Fase 5:**
- Marcar Fase 5 como `complete` en `sota_task_plan.md`
- Actualizar estado en `sota_progress.md`

---

## Fase 6 — Síntesis SOTA

**Objetivo**: Convertir los 5 pilares en conocimiento accionable.

### ANTES de sintetizar — Reboot check obligatorio

Leer `sota_findings.md` completo. Luego responder:

| Pregunta | Respuesta desde archivos |
|----------|--------------------------|
| ¿Qué enfoques existen? | sota_findings.md Pilar 1 |
| ¿Qué está normalizado? | sota_findings.md Pilar 2 |
| ¿Qué adopta el mercado? | sota_findings.md Pilar 3 |
| ¿Qué funciona en prod? | sota_findings.md Pilar 4 |
| ¿Qué dice el campo? | sota_findings.md Pilar 5 |

Solo sintetizar después de leer los hallazgos. No sintetizar desde el contexto solo.

### Estructura del Reporte Final — guardar como `sota_report_[TEMA].md`

```markdown
# SOTA Report: [TEMA]
Fecha: [FECHA]
Alcance investigado: [descripción]

---

## 1. Resumen Ejecutivo SOTA
[3-5 bullets con lo más importante para quien no leerá todo]

---

## 2. Qué existe hoy (Panorama)

### Enfoques principales identificados
| Enfoque | Descripción breve | Madurez | Adopción |
|---------|------------------|---------|---------|
| A | ... | Alta/Media/Baja | % o cualitativo |
| B | ... | | |

### Soluciones / Herramientas de facto
- **[Tool A]**: qué hace, cuándo usarlo
- **[Tool B]**: qué hace, cuándo usarlo

---

## 3. Qué está probado científicamente
- Finding 1 — [Paper, año, venue]
- Finding 2 — [Paper, año, venue]

Paper fundacional de referencia: [título + DOI]

---

## 4. Qué está normalizado (Estándares)
- **[Estándar X]**: qué define y cómo aplica
- **[Estándar Y]**: qué define y cómo aplica

---

## 5. Qué adopta la industria (Mercado)
- Adopción actual: [datos]
- Tendencia: [dirección]
- Herramientas líderes: [lista]

---

## 6. Qué funciona en producción (Mejores Prácticas)

### Hacer
- [Práctica 1 con razonamiento]
- [Práctica 2 con razonamiento]

### No hacer (Anti-patrones)
- [Anti-patrón 1 con explicación]
- [Anti-patrón 2 con explicación]

---

## 7. Qué dicen los expertos (Opinión del campo)
- Consenso: [lo que todos aceptan]
- Debate activo: [donde hay disenso]
- Cambio reciente de paradigma: [si aplica]

---

## 8. No reinventes la rueda — Recursos directamente usables

### Librerías / Frameworks validados
| Nombre | Qué hace | Stars | Madurez | Link |
|--------|----------|-------|---------|------|

### Especificaciones / Estándares directamente adoptables
- [Estándar X]: URL oficial

### Papers de implementación de referencia
- [Paper Y]: descripción + DOI

---

## 9. Brechas y oportunidades
[Lo que el SOTA NO resuelve bien todavía — aquí es donde puede haber innovación genuina]

---

## 10. Recomendación para nuestro contexto
[Dado el contexto del proyecto, el enfoque recomendado es X porque Y]

**Decisiones clave a tomar:**
- [ ] Decisión 1
- [ ] Decisión 2

**Próximos pasos de implementación:**
1. Paso 1
2. Paso 2

---

## 11. Fuentes consultadas
[Lista completa de fuentes con URLs, organizadas por pilar]
```

**Al finalizar Fase 6:**
- Marcar Fase 6 como `complete` en `sota_task_plan.md`
- Actualizar `sota_progress.md` con "Investigación SOTA completada"

---

## Reglas de planificación en archivo (planning-with-files)

Estas reglas son obligatorias durante toda la investigación:

### Regla 1 — Crear primero, buscar después
Nunca ejecutar una búsqueda sin haber creado los 3 archivos de planificación.

### Regla 2 — Los 2 actos
Después de cada 2 WebSearches, escribir hallazgos a `sota_findings.md`. No acumular más.

### Regla 3 — Leer antes de decidir
Antes de la síntesis final (Fase 6), leer `sota_findings.md` completo para re-orientar el contexto.

### Regla 4 — Actualizar después de cada fase
Al completar cada fase: actualizar status en `sota_task_plan.md` + log en `sota_progress.md`.

### Regla 5 — Loggear todos los errores de búsqueda
Si una query no retorna resultados útiles, registrar en `sota_progress.md` y mutar el enfoque.

### Regla 6 — Nunca repetir una búsqueda fallida
Si query X no funcionó, usar una alternativa. Registrar qué se intentó.

### Protocolo de 3 intentos para búsquedas fallidas
```
Intento 1: Query original
  → Sin resultados → Intento 2: Reformular con sinónimos o términos más generales
  → Sin resultados → Intento 3: Cambiar de fuente (de IEEE a arXiv, de paper a blog)
  → Sin resultados → Registrar en sota_progress.md y continuar con siguiente pilar
```

---

## Heurísticas de calidad del SOTA

### ¿Cuándo el SOTA es suficiente?
- Tienes al menos 1 paper de referencia del área
- Identificaste si existe un estándar formal o no
- Sabes qué herramientas usan las empresas similares
- Identificaste los anti-patrones principales
- Tienes una opinión del campo (consenso o debate)

### Señales de que el SOTA está incompleto
- Solo encontraste fuentes de un mismo tipo (solo papers O solo blogs)
- La información más reciente tiene más de 2 años
- No encontraste ningún estándar formal en un dominio maduro
- No hay herramientas de facto identificadas
- Solo encontraste una perspectiva (solo a favor o solo en contra)

### Señales de que la investigación fue superficial
- Las fuentes son todas del mismo dominio cultural (solo inglés, solo EE.UU.)
- No hay ningún punto de disenso o debate en los hallazgos
- Los hallazgos son obvios y no agregan conocimiento nuevo
- No se identificó ningún anti-patrón

---

## Principios del SOTA bien hecho

1. **Primarias sobre secundarias**: Un paper original vale más que 10 resúmenes del mismo paper.
2. **Recencia importa**: En tecnología, 3 años puede ser una era. Prioriza 2022-presente.
3. **El consenso no es unanimidad**: Identifica el mainstream Y las voces disidentes valiosas.
4. **Busca el "por qué" detrás del "qué"**: No solo qué hace el mundo, sino por qué eligió hacerlo así.
5. **Contextualiza la transferibilidad**: Un SOTA de Google a escala no aplica igual a un equipo de 5.
6. **Distingue hype de adopción real**: Que esté en el Gartner Hype Cycle no significa que sea maduro.
7. **El SOTA tiene fecha de vencimiento**: Documenta siempre cuándo fue hecha la investigación.
8. **Lo que no está en disco no existe**: Si no está en sota_findings.md, no entrará en la síntesis.
