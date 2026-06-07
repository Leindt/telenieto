# Architecture — Telenieto

## Stack
- **HTML/CSS/JS puro** — sitio estático, sin frameworks ni build tools
- **Fuente:** Plus Jakarta Sans (Google Fonts, display=swap)
- **Imágenes:** `<img>` estándar + Unsplash CDN para la foto hero
- Sin dependencias npm, sin bundler

## Estructura de archivos
```
Telenieto/
├── index.html          # Única página — toda la landing
├── image-slot.js       # Componente de diseño (NO se usa en producción)
├── adrian.jpg          # Foto del fundador (sección "Sobre")
├── favicon.svg         # Favicon vectorial
├── favicon-32.png      # Favicon rasterizado
├── apple-touch-icon.png
├── robots.txt          # SEO: permite indexación
├── sitemap.xml         # SEO: mapa del sitio
├── _headers            # Headers de seguridad (Netlify/Cloudflare Pages)
├── .htaccess           # Headers + redirects (Apache/cPanel/Hostinger)
├── .gitignore
├── docs/               # Documentación del proyecto
└── uploads/            # Archivos de diseño (ignorados por git)
```

## SEO
- Schema.org: LocalBusiness + FAQPage
- Open Graph completo (Facebook/Instagram Ads)
- Canonical: https://telenieto.es/
- robots.txt + sitemap.xml

## Performance
- LCP image: `fetchpriority="high"` + `<link rel="preload">`
- Fuente con `display=swap` + `preconnect`
- `loading="lazy"` en imágenes below-fold
- Sin JS en critical path (image-slot.js eliminado de producción)
- Compresión gzip via .htaccess

## Seguridad
- X-Content-Type-Options: nosniff
- X-Frame-Options: SAMEORIGIN
- Referrer-Policy: strict-origin-when-cross-origin
- Permissions-Policy restrictivo
- rel="noopener noreferrer" en todos los links externos
- Options -Indexes (sin listado de directorios)

## Hosting previsto
- Hostinger (o similar con Apache/cPanel)
- .htaccess maneja HTTPS redirect + www redirect + telenieto.com → telenieto.es
