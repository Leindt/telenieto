# Decisiones técnicas — Telenieto

## HTML/CSS/JS puro (sin framework)
**Decisión:** No usar React, Vue, ni ningún framework JS.
**Motivo:** Landing page estática de una sola página. Sin framework = cero tiempo de hidratación, máximo rendimiento en LCP, despliegue trivial en cualquier hosting.
**Alternativa descartada:** Next.js/Astro — innecesario para este caso de uso.

## Imagen hero desde Unsplash CDN
**Decisión:** Mantener la URL de Unsplash mientras no haya foto real del servicio.
**Motivo:** Unsplash tiene CDN global y la URL ya incluye parámetros de optimización (w=1100, q=80, auto=format).
**Pendiente:** Reemplazar por foto real cuando esté disponible.

## Eliminación de image-slot.js en producción
**Decisión:** Reemplazar `<image-slot>` por `<img>` estándar y no cargar image-slot.js.
**Motivo:** `image-slot.js` es un componente del canvas de diseño de Claude — no aporta valor en producción y añade carga de script innecesaria al critical path.

## Dominio principal: telenieto.es
**Decisión:** telenieto.es es el canonical; telenieto.com redirige permanentemente (301).
**Motivo:** El negocio está en España; .es refuerza la confianza local y el SEO geográfico.
**Implementación:** .htaccess con RewriteRule + canonical en el `<head>`.

## Seguridad via archivos de servidor (no meta tags)
**Decisión:** Usar `_headers` (Netlify/CF) y `.htaccess` (Apache) para headers de seguridad, no `<meta http-equiv>`.
**Motivo:** Los headers HTTP son más robustos, aplican a todos los recursos (no solo HTML), y no pueden ser ignorados por el cliente.

## Sin cookie banner en el lanzamiento
**Decisión:** No añadir banner de cookies hasta implementar analítica.
**Motivo:** El sitio en su estado actual no instala cookies propias ni de terceros (no hay analytics, no hay pixel). Añadir el banner antes sería confuso para el usuario.
**Actualizar:** Cuando se añada Pixel de Meta o Analytics, implementar el banner antes del deploy.
