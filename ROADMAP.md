# Roadmap — Mat Analytics Landing Page

Historial de versiones y planificación de desarrollo.

---

## Versiones lanzadas

### v1.1.2 — Unificación visual de arquitecturas `[2026-06-15]`

**Arquitecturas de Referencia:**
- Se actualizaron las 7 imágenes iniciales con el mismo contexto visual de "Lakehouse e Inteligencia Artificial Empresarial".
- Todas las arquitecturas usan una línea visual consistente: fondo claro, paneles técnicos, acentos rojo MAT, naranja y teal.
- Las imágenes se enfocan en explicar componentes y flujos de arquitectura, sin marcas ni afirmaciones de implementación.

**Assets:**
- Se reemplazaron los WebP anteriores por nuevas imágenes PNG en `assets/arquitecturas/`.
- Se retiraron assets obsoletos para mantener limpia la carpeta de producción.

### v1.1.1 — Imagen IA Empresarial y ajuste de despliegue `[2026-06-15]`

**Arquitecturas de Referencia:**
- Se agregó imagen de referencia para "Lakehouse e Inteligencia Artificial Empresarial".
- La tarjeta 08 ahora muestra imagen y diagrama con el mismo patrón visual de las demás arquitecturas.
- Se compactó el flujo de 7 capas para mantener lectura rápida en desktop.

**Calidad visual:**
- Validación responsive en desktop y móvil.
- Corrección de overflow móvil en la banda editorial de la página.
- Limpieza de artefactos locales de pruebas visuales antes de despliegue.

### v1.1.0 — Arquitecturas de Referencia y navegación `[2026-06-15]`

**Páginas y contenido:**
- `arquitecturas-referencia.html` — nueva página de arquitecturas de referencia.
- Nueva arquitectura: Lakehouse Empresarial.
- Sección "Evolución de las Plataformas de Datos": Data Warehouse → Data Lake → Lakehouse → Data Fabric → IA Empresarial.
- Disclaimer editorial para presentar las arquitecturas como patrones de referencia, no como implementaciones de MAT Analytics.

**UX y visuales:**
- Hero visual propio para Arquitecturas de Referencia.
- 7 imágenes WebP de referencia en `assets/arquitecturas/`.
- Diagramas compactos por arquitectura.
- Layout desktop optimizado para ver componentes, beneficios, imagen y diagrama en una sola vista.
- Animación sobria al expandir cada arquitectura, con soporte para `prefers-reduced-motion`.

**Navegación:**
- Menú superior "Arquitectura" convertido en dropdown:
  - `arquitectura.html`
  - `arquitecturas-referencia.html`
- Menú móvil con enlaces separados para Arquitectura y Arquitecturas de Referencia.

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
