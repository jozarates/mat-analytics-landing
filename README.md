# Mat Analytics — Landing Page Institucional

Sitio web B2B institucional para **Mat Analytics SAC**, empresa peruana de analítica de datos en alianza con Stamping.io. Targeting: sector corporativo y entidades del Estado.

---

## Stack técnico

| Capa | Tecnología |
|------|-----------|
| Markup | HTML5 semántico |
| Estilos | CSS puro con custom properties (design tokens) |
| Interactividad | Vanilla JS (sin frameworks) |
| Formularios | Formspree (endpoint: `mdavynjy`) |
| Fuente | Inter — Google Fonts |
| Certificación | Stamping.io (`/es/images/` CDN) |
| Analítica BI | Microsoft Power BI CDN |
| Correo | webmail.mat-analytics.com |

> Arquitectura intencional: cero dependencias de build, cero node_modules. Un archivo HTML por página.

---

## Estructura del proyecto

```
mat-analytics-landing/
├── index.html              # Landing principal
├── trusttech.html          # TrustTech & Certificación Digital (Stamping.io)
├── arquitectura.html       # Arquitectura de Datos Enterprise (Oracle)
├── analitica.html          # Inteligencia Analítica Avanzada (OAC + Power BI)
├── reclamaciones.html      # Libro de Reclamaciones Virtual
├── brand-assets/
│   ├── favicon/            # favicon.ico + 16/32/48/180/192/512 px
│   ├── logo-horizontal-*.svg / *.png   # Logo horizontal (color, negativo, rojo, grises)
│   ├── logo-vertical-*.svg / *.png     # Logo vertical (color, negativo, grises)
│   ├── isotipo-*.svg / *.png           # Isotipo M (uso pequeño)
│   └── LEEME.txt           # Especificaciones del kit de logotipos
├── README.md
├── ROADMAP.md
└── docs/
    ├── design-tokens.md    # Variables CSS y paleta de color
    ├── integraciones.md    # Servicios externos y credenciales
    └── contenido.md        # Guía editorial y tono de comunicación
```

---

## Design tokens principales

```css
--red:        #8B0101   /* Rojo MAT — acento principal */
--black:      #1E1E1E   /* Negro corporativo */
--gray-text:  #3A3A3A   /* Gris texto */
--gray-mid:   #757575   /* Barras / triángulo */
--gray-trace: #999999   /* Símbolo conectividad */
--white:      #FFFFFF
--radius:     6px
--radius-lg:  12px
--transition: 0.22s ease
--max-w:      1160px
```

---

## Páginas y contenido

### `index.html` — Landing principal
- Hero con efecto cinematográfico CSS (gradientes animados, orbes, grid, scanline)
- 3 cards glassmorphism: Reporte Financiero, Análisis de Riesgo, Certificación Stamping.io
- Trust bar con badges de tecnología
- 3 pilares de valor (TrustTech, Arquitectura, Analítica)
- Sección TrustTech diferenciador
- Casos de uso por industria
- CTA diagnóstico (formulario Formspree)
- Footer 3 columnas + Libro de Reclamaciones

### `trusttech.html` — TrustTech & Certificación Digital
- Hero con imagen Stamping.io
- 9 tarjetas de funcionalidades blockchain
- Slider auto-avance (6s) con imágenes del diseñador visual Stamping.io
- Tabs con casos: Certificación, Firma Digital, Trazabilidad, Tokenización
- Pricing plans Stamping.io (Free / Pro / Enterprise)

### `arquitectura.html` — Arquitectura de Datos Enterprise
- Productos Oracle: ADW, ODI, GoldenGate, Exadata, OCI, Database 23ai
- Mockup visual CSS de consola Oracle ADW (sin hotlinking — oracle.com bloquea)
- Capacidades: diseño/migración, rendimiento, seguridad
- Casos por industria: banca, seguros, sector público, logística

### `analitica.html` — Inteligencia Analítica Avanzada
- Oracle Analytics Cloud: mockup dashboard CSS + funcionalidades
- Power BI: imágenes vía Microsoft CDN (`cdn-dynmedia-1.microsoft.com`)
- Estadísticas ROI: 321% ROI, 6 meses amortización, $38.48M beneficio
- Casos de uso analítica por sector

### `reclamaciones.html` — Libro de Reclamaciones Virtual
- Formulario conforme Ley 29571 (Código de Consumo peruano)
- Canvas HTML5 para firma manuscrita (mouse + touch)
- Envío vía Formspree endpoint `mdavynjy`
- Campo de recibo con número de ticket autogenerado

---

## Desarrollo local

```bash
# Python (cualquier versión)
python -m http.server 8743

# Luego abrir:
# http://localhost:8743/
```

> No requiere compilación, bundler ni node. Abrir directamente en navegador también funciona para review estático.

---

## Notas de integración

### Stamping.io images
- CDN funcional: `https://stamping.io/es/images/[archivo]`
- CDN bloqueado: `https://stamping.io/images/[archivo]` — retorna 0px (hotlink bloqueado)

### Oracle
- `oracle.com` retorna **403 Forbidden** en todos los recursos
- Solución: mockups CSS puros basados en conocimiento del producto

### Formspree
- Endpoint: `https://formspree.io/f/mdavynjy`
- Formulario de reclamaciones + formulario de diagnóstico (index.html)

---

## Convenciones de código

- Sin comentarios salvo WHY no obvio
- CSS primero en `<style>`, JS al final de `<body>`
- Dropdown JS genérico: `querySelectorAll('.nav-dropdown')` — no IDs específicos
- IntersectionObserver para animaciones `reveal` al scroll
- Clases BEM-like: `.hero__card`, `.nav-dropdown__item`, etc.

---

## Restricciones editoriales

- **Sin razón social de clientes** — usar solo sector + capacidad (ej: "banco regional de 2M clientes")
- Idioma: español, tono institucional B2B
- No incluir precios de licenciamiento de terceros (Power BI, Oracle) en el sitio

---

## Contribución

Branch `master` = producción. Para cambios:
1. Crear branch `feature/[descripcion]`
2. PR con descripción de cambio y captura de pantalla
3. Merge solo con revisión visual en local

---

*Generado con Claude Code — Anthropic*
