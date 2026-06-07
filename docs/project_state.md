# Project State — Telenieto

## Estado actual (2026-06-07)
Landing page completamente optimizada para producción y subida a GitHub.

## Última sesión
- Importado ZIP del diseño (Claude Design)
- Eliminado `image-slot.js` del HTML (era un componente de canvas, no de producción)
- Convertidos `<image-slot>` a `<img>` estándar con `fetchpriority` y `loading=lazy`
- Añadidos headers de seguridad: `_headers` (Netlify/CF) y `.htaccess` (Apache)
- Corregido canonical de `telenieto.com` → `telenieto.es`
- Añadidos `robots.txt` y `sitemap.xml`
- `preload` + `dns-prefetch` para LCP y recursos externos
- `noreferrer` en todos los links externos
- Repo GitHub creado: github.com/Leindt/telenieto

## Pendiente antes de ir a producción
- Crear og-image.jpg (1200×630) para Meta Ads y compartir en redes
- Subir `adrian.jpg` real (foto del fundador) si aún no está en el repo
- Configurar DNS en Hostinger apuntando a hosting elegido
- Verificar que .htaccess funciona en el hosting (redirects HTTPS + dominio)
- Añadir Pixel de Meta si se van a usar anuncios de Facebook/Instagram

## Próximo paso inmediato
Crear og-image.jpg (1200×630px) con branding de Telenieto para Meta Ads.
