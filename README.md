# Voxen Landing

Sitio publico de [voxenvisuals.com](https://voxenvisuals.com). Es HTML estatico exportado de Framer + varios bloques inyectados por script (equipo, sistema, portfolio, testimonios, FAQ).

## Que hay aca

- `agencia/index.html` — la landing entera (~1.2 MB de HTML minificado con todos los estilos y scripts inline).
- `agencia/images/`, `agencia/videos/`, `agencia/fonts/`, `agencia/sistema/`, `agencia/swiper/`, `agencia/js/` — los assets.
- `terminos/index.html`, `privacidad/index.html`, `legal/legal.css` — paginas legales enlazadas desde el footer.
- `robots.txt`, `sitemap.xml`, `icon-180.png`, `icon-512.png`, `logo-voxen.svg`, `logo.png`.
- `vercel.json` — rewrite `/` → `/agencia/index.html` y cache largo para los assets.

## Como se despliega

Auto-deploy con Vercel al pushear a `main`. El proyecto sirve estatico sin build, sin dependencias.

## Hero 3D y nav kinetico

La V roja 3D del hero y el menu kinetico corren en la plataforma (`voxenvisuals.app/agencia-clon-hero` y `/agencia-clon-nav`) y se embeben aca como iframes cross-origin. Si algun dia se rompen: el CSP `frame-ancestors` de la plataforma tiene que permitir a `https://voxenvisuals.com`.
