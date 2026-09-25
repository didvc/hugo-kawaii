[English](README.md) · [日本語](README-ja.md) · [繁體中文](README-zh-TW.md) · [简体中文](README-zh.md) · [Deutsch](README-de.md) · [Français](README-fr.md) · Español

# Kawaii Hugo Theme

Un tema de Hugo con estética kawaii, modo oscuro y pequeñas animaciones por todas partes.

![Captura de pantalla del tema Kawaii](https://raw.githubusercontent.com/didvc/hugo-kawaii/master/images/screenshot.png)

Una [demo en vivo](https://didvc.github.io/hugo-kawaii/) muestra el tema en uso, y el directorio `exampleSite` contiene un sitio completo y funcional.

![GitHub stars](https://img.shields.io/github/stars/didvc/hugo-kawaii?style=social)
![GitHub forks](https://img.shields.io/github/forks/didvc/hugo-kawaii?style=social)
![GitHub issues](https://img.shields.io/github/issues/didvc/hugo-kawaii)
![GitHub license](https://img.shields.io/github/license/didvc/hugo-kawaii)

## Características

El diseño es responsive y mobile-first, con una tipografía limpia, animaciones suaves y microinteracciones. El modo oscuro sigue la preferencia del sistema y también se puede cambiar a mano. La búsqueda se ejecuta por completo en el cliente. El marcado está pensado para la accesibilidad, incluida la navegación con teclado, y el tema aspira a cumplir WCAG. Los colores, las fuentes y el diseño se controlan con propiedades personalizadas de CSS, así que son fáciles de cambiar, y el repositorio incluye un sitio de ejemplo completo para empezar.

## Inicio rápido

1. Añade el tema como submódulo:
   ```bash
   git submodule add https://github.com/didvc/hugo-kawaii.git themes/kawaii
   ```

2. Configúralo en tu `hugo.toml`:
   ```toml
   theme = "kawaii"
   ```

3. Inicia el sitio:
   ```bash
   hugo server
   ```

## Requisitos

Hugo Extended 0.147.0 o posterior, y Git para instalar el tema.

## Configuración

### Configuración básica

```toml
baseURL = "https://yoursite.com"
locale = "en-us"
title = "Your Site Title"
theme = "kawaii"

[params]
  description = "Your site description"
  author = "Your Name"

  # Theme features
  theme_toggle = true    # Enable dark mode toggle
  search = true         # Enable search functionality

  # Hero section
  hero_cta = "Get Started"
  hero_cta_link = "posts/"
```

### Enlaces sociales

```toml
[[params.social]]
  name = "github"
  url = "https://github.com/yourusername"

[[params.social]]
  name = "twitter"
  url = "https://twitter.com/yourusername"
```

### Menú de navegación

```toml
[menu]
  [[menu.main]]
    name = "Home"
    url = "/"
    weight = 10

  [[menu.main]]
    name = "Posts"
    url = "/posts"
    weight = 20
```

### Secciones destacadas

```toml
[[params.featured_sections]]
  title = "Modern Design"
  description = "Clean and beautiful aesthetics"
  icon = "✨"
  link = "about/"
```

## Personalización

### Colores

Sobrescribe las variables CSS para cambiar los colores:

```css
/* assets/css/custom.css */
:root {
  --kawaii-primary: #your-primary-color;
  --kawaii-secondary: #your-secondary-color;
  --kawaii-accent: #your-accent-color;
}
```

### Fuentes

Cambia la tipografía mediante las variables de fuente:

```css
:root {
  --kawaii-font-family: 'Your Font', sans-serif;
  --kawaii-font-mono: 'Your Mono Font', monospace;
}
```

## Estructura del contenido

### Front matter de una entrada

```yaml
---
title: "Your Post Title"
date: 2024-01-15T10:00:00Z
description: "Post description for SEO"
tags: ["tag1", "tag2", "tag3"]
featured_image: "/images/featured.jpg"
---
```

### Estructura de páginas

```
content/
├── _index.md          # Homepage content
├── about/
│   └── _index.md      # About page
├── posts/
│   ├── _index.md      # Posts listing page
│   ├── post-1.md      # Individual posts
│   └── post-2.md
└── contact/
    └── _index.md      # Contact page
```

## Rendimiento

El tema apunta a una puntuación de 100 en Lighthouse en Rendimiento, Accesibilidad, Prácticas recomendadas y SEO. El CSS y el JavaScript juntos pesan menos de 50 KB, y las páginas cargan en menos de un segundo con una conexión moderna.

## Navegadores compatibles

Chrome o Chromium 88+, Firefox 85+, Safari 14+ y Edge 88+.

## Contribuir

Los informes de errores y las solicitudes de funciones son bienvenidos a través de las plantillas de [informe de error](https://github.com/didvc/hugo-kawaii/issues/new?template=bug_report.yml) y [solicitud de función](https://github.com/didvc/hugo-kawaii/issues/new?template=feature_request.yml); las ideas también pueden ir a [Discussions](https://github.com/didvc/hugo-kawaii/discussions). Para contribuir código, haz un fork del repositorio, trabaja en una rama siguiendo el estilo existente, prueba con el sitio de ejemplo y abre un pull request que describa el cambio. Las mejoras en la documentación y los ejemplos, y las reseñas de tus propias personalizaciones, son igual de bienvenidas.

### Entorno de desarrollo

1. Haz un fork y clona el repositorio:
   ```bash
   git clone https://github.com/didvc/hugo-kawaii.git
   cd hugo-kawaii
   ```

2. Crea un sitio de prueba:
   ```bash
   hugo new site test-site
   cd test-site
   ln -s ../../../hugo-kawaii themes/kawaii
   ```

3. Copia la configuración de ejemplo:
   ```bash
   cp themes/kawaii/exampleSite/hugo.toml .
   cp -r themes/kawaii/exampleSite/content .
   ```

4. Inicia el servidor de desarrollo:
   ```bash
   hugo server --theme kawaii
   ```

## Hoja de ruta

Previsto: soporte multilingüe (i18n), búsqueda más avanzada, esquemas de color adicionales y más trabajo en animaciones y rendimiento.

## Soporte

El uso se explica en este README y en el sitio de ejemplo. Las preguntas y los problemas van a [GitHub Issues](https://github.com/didvc/hugo-kawaii/issues) o a [GitHub Discussions](https://github.com/didvc/hugo-kawaii/discussions); para dudas generales sobre Hugo, consulta el [foro de Hugo](https://discourse.gohugo.io/), la [documentación de Hugo](https://gohugo.io/documentation/) y el [directorio de temas de Hugo](https://themes.gohugo.io/).

## Créditos

Construido sobre [Hugo](https://gohugo.io/). Tipografía en Inter, de Rasmus Andersson, y JetBrains Mono, con iconos de Feather Icons.

## Licencia

Publicado bajo la [licencia MIT](LICENSE).

<!-- BEGIN gh-mutual-linking -->

---

### Related projects

- [astro-html-editor](https://github.com/didvc/astro-html-editor): Self-hosted HTML editor with live preview. Astro SSR + plain JavaScript, server-side file persistence.
- [html-bio-generator](https://github.com/didvc/html-bio-generator): A modern, intuitive tool for creating beautiful HTML bio pages with ease. Built with Next.js, TypeScript, and Tailwind CSS. Perfect for developers, freelancers, and content creators.
- [cf-cache-utils](https://github.com/didvc/cf-cache-utils): CLI to warm and inspect Cloudflare edge cache status across all your URLs; no external dependencies, pure Node.js
- [uptime-mon](https://github.com/didvc/uptime-mon): Lightweight single-binary endpoint uptime monitor. Probes HTTP, keyword, ICMP and TCP targets on a schedule, appends results as zstd-compressed InfluxDB line protocol, and reads them back in a terminal UI. No web server, no database, no alerting.
- [didvc](https://github.com/didvc/didvc): Aesthetic Vulpes, Tokyo | a 20s Japanese fox #arts #music #provenance | 2027 Profile README
<!-- END gh-mutual-linking -->
