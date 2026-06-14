# Roadmap — Mat Analytics Landing Page

Historial de versiones y planificación de desarrollo.

---

## Versiones lanzadas

### v1.0.0 — Lanzamiento inicial `[2026-06-13]`

**Páginas creadas:**
- `index.html` — landing principal completa
- `trusttech.html` — TrustTech & Certificación Digital con slider Stamping.io
- `arquitectura.html` — Arquitectura de Datos Enterprise (Oracle, CSS mockups)
- `analitica.html` — Inteligencia Analítica Avanzada (OAC + Power BI)
- `reclamaciones.html` — Libro de Reclamaciones Virtual con firma canvas

**Funcionalidades:**
- Navbar fija con dropdowns animados (Líneas de Negocio, TrustTech)
- Hero cinematográfico CSS: gradientes animados, orbes, grid, scanline
- Cards glassmorphism en hero
- Slider auto-avance 6s con thumbnails y barra de progreso (trusttech.html)
- Tabs interactivos con imágenes Stamping.io
- IntersectionObserver reveal animations
- Canvas firma manuscrita (mouse + touch)
- Formulario Formspree con validación
- Footer 3 columnas consistente en todas las páginas
- Diseño 100% responsive
- Kit de logotipos SVG vectorizados + favicons completos

**Repositorio:** https://github.com/jozarates/mat-analytics-landing (privado)

---

## Pendiente — Links sin página propia

Los siguientes ítems del navbar apuntan a secciones de `index.html` sin página dedicada:

| Ítem | Estado actual | Acción sugerida |
|------|--------------|----------------|
| Casos de Uso | `index.html#casos` | Crear `casos.html` o mantener ancla |
| Nosotros | `index.html#nosotros` | Crear `nosotros.html` o mantener ancla |
| Política de Privacidad | `href="#"` (muerto) | Crear `privacidad.html` |

---

## v1.1.0 — Páginas de contenido adicional `[PLANIFICADO]`

**Páginas nuevas:**
- [ ] `nosotros.html` — Equipo, historia, visión, partners
- [ ] `casos.html` — Casos de uso detallados por industria (banca, seguros, Estado, logística)
- [ ] `privacidad.html` — Política de Privacidad y Tratamiento de Datos

**Mejoras:**
- [ ] Formulario de diagnóstico mejorado (multi-step con selección de servicio)
- [ ] Meta OG tags con imagen preview por página
- [ ] Sitemap XML

---

## v1.2.0 — SEO y performance `[PLANIFICADO]`

- [ ] Imágenes propias en `/images/` (eliminar dependencia de CDNs externos donde sea posible)
- [ ] `robots.txt` y `sitemap.xml`
- [ ] Schema.org markup (Organization, Service)
- [ ] Lazy loading en imágenes
- [ ] Preload de fuentes críticas
- [ ] Google Analytics / Tag Manager

---

## v1.3.0 — Contenido dinámico `[FUTURO]`

- [ ] Blog / Insights (artículos sobre analítica, Oracle, Stamping.io)
- [ ] Casos de éxito ampliados (sin razón social de cliente — sector + capacidad)
- [ ] Calculadora ROI interactiva

---

## Deuda técnica conocida

| Issue | Archivo | Prioridad |
|-------|---------|-----------|
| `href="#"` Política de Privacidad | reclamaciones.html:729 | Alta |
| Oracle mockups CSS (sin imágenes reales) | arquitectura.html | Media |
| No existe `casos.html` ni `nosotros.html` | navbar todas las páginas | Media |
| LF→CRLF warnings en git (Windows) | todos los archivos | Baja |

---

## Convención de versiones

`MAJOR.MINOR.PATCH`
- MAJOR: rediseño completo o cambio de arquitectura
- MINOR: página nueva o funcionalidad significativa
- PATCH: correcciones, ajustes de contenido, hotfixes
