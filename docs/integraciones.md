# Integraciones y servicios externos

## Formspree

- **Endpoint:** `https://formspree.io/f/mdavynjy`
- **Usado en:** `index.html` (formulario diagnóstico) y `reclamaciones.html` (libro de reclamaciones)
- **Configuración:** Sin backend — envío directo desde el navegador al email configurado en Formspree
- **Dashboard:** https://formspree.io/forms/mdavynjy/submissions

## Stamping.io

Proveedor de certificación blockchain. Mat Analytics es partner.

| Recurso | URL |
|---------|-----|
| CDN imágenes (activo) | `https://stamping.io/es/images/[archivo]` |
| CDN imágenes (bloqueado) | `https://stamping.io/images/[archivo]` — no usar |
| Plataforma admin | `https://stamping.io/admin/` |
| Verificador de sellos | `https://stamping.io/es/scan/` |
| Registro partners | `https://stamping.io/admin/register2.php` |
| Partners page | `https://stamping.io/es/partners.html` |

**Ecosistema Stamping.io** (apps integradas, aparecen en trusttech.html):
- `registrado.org` — certificación de documentos
- `appcuerdo.com` — firma de acuerdos
- `whatsign.com` — firma por WhatsApp
- `rastrar.com` — trazabilidad de cadena de suministro

## Webmail

- **URL:** `https://webmail.mat-analytics.com`
- **Contacto:** `info@mat-analytics.com`
- **Usado en:** icono de mail en navbar de todas las páginas

## Microsoft Power BI (imágenes)

CDN de imágenes de Microsoft para sección Power BI en `analitica.html`:

```
https://cdn-dynmedia-1.microsoft.com/is/image/microsoftcorp/Hero_PBI_opt2?wid=1200&hei=675&fit=crop
https://cdn-dynmedia-1.microsoft.com/is/image/microsoftcorp/ProductOverview_PBICapabilities_1.1?wid=600&hei=400&fit=crop
https://cdn-dynmedia-1.microsoft.com/is/image/microsoftcorp/ProductOverview_WhyPBI_2.2?wid=600&hei=400&fit=crop
https://cdn-dynmedia-1.microsoft.com/is/image/microsoftcorp/ProductOverview_CopilotinPBI_3.1?wid=600&hei=400&fit=crop
```

## Oracle

- **oracle.com** retorna 403 Forbidden en todos los recursos (hotlinking bloqueado + WebFetch bloqueado)
- Solución adoptada: mockups CSS puros (consola ADW, dashboard OAC)
- No usar imágenes de oracle.com — siempre fallarán

## Google Fonts

- **Fuente:** Inter (300, 400, 500, 600, 700, 800)
- **URL:** `https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&display=swap`
- Preconnect a `fonts.googleapis.com` y `fonts.gstatic.com` en todas las páginas

## GitHub

- **Repositorio:** https://github.com/jozarates/mat-analytics-landing (privado)
- **Branch principal:** `master`
- **Remote:** origin (HTTPS, cuenta jozarates)
- **Sincronización:** manual tras cada bloque de cambios significativo
