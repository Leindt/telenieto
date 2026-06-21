# GEO Audit Report: Telenieto

**Audit Date:** 2026-06-21
**URL:** https://telenieto.es/
**Business Type:** Local Business (asistencia tecnológica a domicilio para mayores)
**Pages Analyzed:** 6 (index, 3 guías SEO, aviso-legal, privacidad)

---

## Executive Summary

**Overall GEO Score: 56/100 (Poor)**

Telenieto tiene una base técnica y de schema excepcional para un sitio de este tamaño — HTML estático, sin bloqueo de crawlers de IA, FAQ/HowTo/LocalBusiness/Speakable bien implementados. El problema no es el sitio en sí: es que **no existe ninguna señal de la marca fuera de su propio dominio**. Cero presencia en Google Business Profile indexado, directorios locales, redes sociales o reseñas externas — esto es lo que más limita que un modelo de IA "reconozca" a Telenieto como entidad real y la recomiende.

### Score Breakdown

| Category | Score | Weight | Weighted Score |
|---|---|---|---|
| AI Citability | 80/100 | 25% | 20.0 |
| Brand Authority | 15/100 | 20% | 3.0 |
| Content E-E-A-T | 55/100 | 20% | 11.0 |
| Technical GEO | 80/100 | 15% | 12.0 |
| Schema & Structured Data | 85/100 | 10% | 8.5 |
| Platform Optimization | 10/100 | 10% | 1.0 |
| **Overall GEO Score** | | | **56/100** |

---

## Critical Issues (Fix Immediately)

Ninguno. El sitio es indexable, sin bloqueos de crawler, con HTTPS y sin errores 5xx.

## High Priority Issues

1. **Brand invisible fuera del dominio propio** — búsqueda web de "Telenieto Alcorcón" no devuelve ningún resultado del negocio. Sin Google Business Profile verificable, sin redes sociales, sin directorios locales (Páginas Amarillas, Yelp ES, etc.). Los modelos de IA confían en menciones de terceros para reconocer entidades; ahora mismo Telenieto solo existe según su propia web.
2. **No hay `llms.txt`** (404 en `https://telenieto.es/llms.txt`) — estándar emergente que ayuda a los crawlers de IA a entender la estructura del sitio sin tener que parsear todo el HTML.
3. **`sameAs` del schema LocalBusiness es débil** — solo enlaza a `wa.me/34644391910` (no es una señal de autoridad real). Falta vincular Google Business Profile, Instagram/Facebook si existen.
4. **Sin Review individual schema** — solo hay `AggregateRating` (5/18) pero no reseñas individuales con autor verificable, lo que limita la confianza que un LLM puede depositar en esa cifra.

## Medium Priority Issues

1. **Testimonios con poca verificabilidad** — "Laura G.", "Javier M.", "Carmen R." con solo barrio. Sin enlace a reseña real (Google, etc.), un LLM no puede verificar que existen.
2. **Sin contenido con fecha/frescura** — ninguna página muestra fecha de publicación o última actualización (excepto `lastmod` en sitemap, que es interno). Los blogs/guías sin fecha visible pierden puntos de E-E-A-T.
3. **Adrián (Person schema) sin credenciales verificables** — buena historia de fundador, pero no hay enlace a LinkedIn, certificaciones, ni prensa que lo respalde.
4. **Falta `BreadcrumbList` schema** en las páginas de guías (ya tienen breadcrumb visual en HTML, pero no está marcado con schema).
5. **og-image.jpg pesa 8.7 MB** — no es un problema de citabilidad de IA pero sí de rendimiento al compartir enlaces (lo veníamos arrastrando de la sesión anterior).

## Low Priority Issues

1. Falta `Organization` schema general (se usa `LocalBusiness`, correcto, pero sin entidad separada para casos donde Google prefiere `Organization` + `LocalBusiness` combinados).
2. No hay schema `HowTo` en las 3 páginas de guías (sí en homepage) — sería útil en la guía de Banca/Bizum, por ejemplo "cómo configurar Bizum paso a paso".
3. Sin presencia en YouTube — un vídeo corto "cómo ayudamos a una familia en Alcorcón" tendría alto potencial de citabilidad en Google AI Overviews.

---

## Category Deep Dives

### AI Citability (80/100)
**Fortalezas:**
- FAQ con formato pregunta→respuesta directa y autocontenida (ej: "¿Cuánto cuesta? → La visita a domicilio cuesta 45 €...") — exactamente el formato que ChatGPT/Perplexity citan.
- `HowTo` schema con 3 pasos claros y `estimatedCost`.
- `speakable` schema marcando selectores específicos (`.hero h1`, `.faq-wrap .ans`) — preparado para Google Assistant / AI Overviews por voz.
- Datos concretos y citables: "45 €, hasta 1 hora", "Lunes a viernes 9:00–20:00".

**Mejoras:**
- Las respuestas FAQ podrían ser aún más autocontenidas (algunas asumen contexto de la pregunta).
- Ninguna página de guía tiene tabla comparativa (ej. "qué incluye cada extra") — las tablas son altamente citables.

### Brand Authority (15/100)
- Búsqueda externa "Telenieto Alcorcón" → 0 resultados relevantes del negocio.
- `sameAs` solo apunta a WhatsApp (no es una entidad de terceros).
- Sin Google Business Profile detectable, sin Instagram/Facebook, sin prensa local, sin directorios.
- **Esta es la categoría que más arrastra el score global hacia abajo.**

### Content E-E-A-T (55/100)
- Founder story (Adrián) bien narrada y con `Person` schema + `knowsAbout`.
- Testimonios con nombre+inicial+barrio (nivel medio de verificabilidad).
- Sin fechas de publicación/actualización visibles.
- Sin enlaces externos de respaldo (prensa, asociaciones de mayores, colegios profesionales).

### Technical GEO (80/100)
- robots.txt: `Allow: /` para todos los user-agents — ningún crawler de IA bloqueado (GPTBot, ClaudeBot, PerplexityBot todos permitidos).
- HTML estático puro, sin dependencia de JavaScript para el contenido — ideal para crawlers de IA que no ejecutan JS.
- Headers de seguridad completos: HSTS, CSP, X-Frame-Options, etc.
- CDN con tiempos de respuesta de borde de 10ms.
- **Único gap:** `llms.txt` ausente (404).

### Schema & Structured Data (85/100)
- Homepage tiene 7 bloques de structured data: WebSite, HowTo, Service, LocalBusiness, WebPage+Speakable, Person, FAQPage — cobertura excelente, poco habitual en sitios de este tamaño.
- Las 3 páginas de guías tienen Service + FAQPage.
- `AggregateRating` y `ContactPoint` presentes en LocalBusiness.
- Gaps: sin `BreadcrumbList`, sin `Review` individuales, `sameAs` incompleto.

### Platform Optimization (10/100)
- Sin presencia verificable en ninguna plataforma que los LLMs usan para entity recognition (Google Business Profile, Wikipedia, Reddit, LinkedIn, YouTube).
- Para un negocio local, el Google Business Profile es la señal más importante y probablemente la más fácil de conseguir — es gratis y ya debería existir dado que el negocio opera activamente.

---

## Quick Wins (Implement This Week)

1. **Crear/reclamar Google Business Profile** para Telenieto en Alcorcón — es la señal de autoridad local más citada por IA y gratuita. Pedir a los primeros 5-10 clientes que dejen reseña.
2. **Crear `llms.txt`** en la raíz con un resumen del sitio, enlaces a páginas clave y servicios — 15 minutos de trabajo, usa la skill `geo-llmstxt` disponible.
3. **Reducir `og-image.jpg`** de 8.7 MB a <400 KB (comprimir/recortar a 1200×630).
4. **Añadir `sameAs` con Google Business Profile** en cuanto exista, en el schema LocalBusiness.
5. **Añadir `BreadcrumbList` schema** a las 3 páginas de guías (el breadcrumb visual ya existe, solo falta marcarlo).

## 30-Day Action Plan

### Semana 1: Cimientos de autoridad
- [ ] Crear y verificar Google Business Profile (dirección de servicio en Alcorcón, horario, teléfono, fotos)
- [ ] Pedir reseñas a clientes reales ya atendidos (objetivo: 10 reseñas verificables en Google)
- [ ] Generar `llms.txt`

### Semana 2: Schema y técnica
- [ ] Añadir `BreadcrumbList` a las 3 guías
- [ ] Comprimir `og-image.jpg`
- [ ] Vincular `sameAs` a Google Business Profile + cualquier red social activa

### Semana 3: Contenido y E-E-A-T
- [ ] Añadir fecha de "última actualización" visible en las guías
- [ ] Ampliar testimonios con enlace a reseña real de Google (cuando existan)
- [ ] Considerar perfil de LinkedIn para Adrián, enlazado desde el Person schema

### Semana 4: Expansión de plataforma
- [ ] Crear página de Facebook/Instagram del negocio (si no existe) — refuerza `sameAs` y aparece en búsquedas locales
- [ ] Grabar 1 vídeo corto (testimonio real o "cómo trabajamos") para YouTube — alto potencial de citación en AI Overviews
- [ ] Evaluar inclusión en directorios locales de Alcorcón (ayuntamiento, asociaciones de mayores)

---

## Appendix: Pages Analyzed

| URL | Title | GEO Issues |
|---|---|---|
| / | Telenieto · Ayuda a mayores... | 2 (sameAs débil, sin Review individual) |
| /movil-whatsapp-mayores-alcorcon.html | Configurar Móvil y WhatsApp... | 2 (sin BreadcrumbList, sin fecha) |
| /banca-online-bizum-mayores-alcorcon.html | Ayuda con Banca Online y Bizum... | 2 (sin BreadcrumbList, sin fecha) |
| /television-smart-tv-mayores-alcorcon.html | Configurar Smart TV... | 2 (sin BreadcrumbList, sin fecha) |
| /aviso-legal.html | Aviso Legal | 0 (no requiere optimización GEO) |
| /privacidad.html | Política de Privacidad | 0 (no requiere optimización GEO) |

**Fetch failures:** ninguno. `llms.txt` devuelve 404 (esperado, no existe).
