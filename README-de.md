[English](README.md) · [日本語](README-ja.md) · [繁體中文](README-zh-TW.md) · [简体中文](README-zh.md) · Deutsch · [Français](README-fr.md) · [Español](README-es.md)

# Kawaii Hugo Theme

Ein Hugo-Theme mit Kawaii-Look, Dark Mode und kleinen Animationen überall.

![Screenshot des Kawaii-Themes](https://raw.githubusercontent.com/didvc/hugo-kawaii/master/images/screenshot.png)

Eine [Live-Demo](https://didvc.github.io/hugo-kawaii/) zeigt das Theme im Einsatz, und das Verzeichnis `exampleSite` enthält eine vollständige, lauffähige Website.

![GitHub stars](https://img.shields.io/github/stars/didvc/hugo-kawaii?style=social)
![GitHub forks](https://img.shields.io/github/forks/didvc/hugo-kawaii?style=social)
![GitHub issues](https://img.shields.io/github/issues/didvc/hugo-kawaii)
![GitHub license](https://img.shields.io/github/license/didvc/hugo-kawaii)

## Funktionen

Das Layout ist responsiv und mobile-first, gesetzt in klarer Typografie mit weichen Animationen und Mikrointeraktionen. Der Dark Mode folgt der Systemeinstellung und lässt sich auch von Hand umschalten. Die Suche läuft vollständig im Client. Das Markup ist auf Barrierefreiheit ausgelegt, einschließlich Tastaturbedienung, und das Theme strebt WCAG-Konformität an. Farben, Schriften und Layout werden über CSS Custom Properties gesteuert und sind daher leicht anzupassen; das Repository enthält außerdem eine vollständige Beispielseite als Ausgangspunkt.

## Schnellstart

1. Das Theme als Submodul hinzufügen:
   ```bash
   git submodule add https://github.com/didvc/hugo-kawaii.git themes/kawaii
   ```

2. In der `hugo.toml` eintragen:
   ```toml
   theme = "kawaii"
   ```

3. Die Seite starten:
   ```bash
   hugo server
   ```

## Voraussetzungen

Hugo Extended 0.147.0 oder neuer sowie Git, um das Theme zu installieren.

## Konfiguration

### Grundkonfiguration

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

### Social Links

```toml
[[params.social]]
  name = "github"
  url = "https://github.com/yourusername"

[[params.social]]
  name = "twitter"
  url = "https://twitter.com/yourusername"
```

### Navigationsmenü

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

### Hervorgehobene Bereiche

```toml
[[params.featured_sections]]
  title = "Modern Design"
  description = "Clean and beautiful aesthetics"
  icon = "✨"
  link = "about/"
```

## Anpassung

### Farben

Die CSS-Variablen überschreiben, um die Farben zu ändern:

```css
/* assets/css/custom.css */
:root {
  --kawaii-primary: #your-primary-color;
  --kawaii-secondary: #your-secondary-color;
  --kawaii-accent: #your-accent-color;
}
```

### Schriften

Die Typografie über die Schriftvariablen ändern:

```css
:root {
  --kawaii-font-family: 'Your Font', sans-serif;
  --kawaii-font-mono: 'Your Mono Font', monospace;
}
```

## Inhaltsstruktur

### Front Matter eines Beitrags

```yaml
---
title: "Your Post Title"
date: 2024-01-15T10:00:00Z
description: "Post description for SEO"
tags: ["tag1", "tag2", "tag3"]
featured_image: "/images/featured.jpg"
---
```

### Seitenstruktur

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

## Performance

Das Theme zielt auf einen Lighthouse-Wert von 100 in Performance, Accessibility, Best Practices und SEO. CSS und JavaScript zusammen bleiben unter 50 KB, und Seiten laden über eine moderne Verbindung in weniger als einer Sekunde.

## Browserunterstützung

Chrome oder Chromium 88+, Firefox 85+, Safari 14+ und Edge 88+.

## Mitwirken

Fehlerberichte und Funktionswünsche sind über die Vorlagen für [Fehlerberichte](https://github.com/didvc/hugo-kawaii/issues/new?template=bug_report.yml) und [Funktionswünsche](https://github.com/didvc/hugo-kawaii/issues/new?template=feature_request.yml) willkommen; Ideen können auch in die [Discussions](https://github.com/didvc/hugo-kawaii/discussions). Für Code: das Repository forken, auf einem Feature-Branch im bestehenden Stil arbeiten, mit der Beispielseite testen und einen Pull Request mit einer Beschreibung der Änderung öffnen. Verbesserungen an Dokumentation und Beispielen sowie Berichte über eigene Anpassungen sind ebenso willkommen.

### Entwicklungsumgebung

1. Repository forken und klonen:
   ```bash
   git clone https://github.com/didvc/hugo-kawaii.git
   cd hugo-kawaii
   ```

2. Eine Testseite anlegen:
   ```bash
   hugo new site test-site
   cd test-site
   ln -s ../../../hugo-kawaii themes/kawaii
   ```

3. Die Beispielkonfiguration kopieren:
   ```bash
   cp themes/kawaii/exampleSite/hugo.toml .
   cp -r themes/kawaii/exampleSite/content .
   ```

4. Den Entwicklungsserver starten:
   ```bash
   hugo server --theme kawaii
   ```

## Roadmap

Geplant: Mehrsprachigkeit (i18n), erweiterte Suche, zusätzliche Farbschemata sowie weitere Arbeit an Animationen und Performance.

## Support

Die Nutzung ist in dieser README und der Beispielseite beschrieben. Fragen und Probleme gehören in die [GitHub Issues](https://github.com/didvc/hugo-kawaii/issues) oder die [GitHub Discussions](https://github.com/didvc/hugo-kawaii/discussions); für allgemeine Hugo-Fragen gibt es das [Hugo-Forum](https://discourse.gohugo.io/), die [Hugo-Dokumentation](https://gohugo.io/documentation/) und das [Hugo-Themes-Verzeichnis](https://themes.gohugo.io/).

## Danksagungen

Gebaut auf [Hugo](https://gohugo.io/). Gesetzt in Inter von Rasmus Andersson und JetBrains Mono, mit Icons von Feather Icons.

## Lizenz

Veröffentlicht unter der [MIT-Lizenz](LICENSE).

<!-- BEGIN gh-mutual-linking -->

---

### Related projects

- [astro-html-editor](https://github.com/didvc/astro-html-editor): Self-hosted HTML editor with live preview. Astro SSR + plain JavaScript, server-side file persistence.
- [html-bio-generator](https://github.com/didvc/html-bio-generator): A modern, intuitive tool for creating beautiful HTML bio pages with ease. Built with Next.js, TypeScript, and Tailwind CSS. Perfect for developers, freelancers, and content creators.
- [cf-cache-utils](https://github.com/didvc/cf-cache-utils): CLI to warm and inspect Cloudflare edge cache status across all your URLs; no external dependencies, pure Node.js
- [uptime-mon](https://github.com/didvc/uptime-mon): Lightweight single-binary endpoint uptime monitor. Probes HTTP, keyword, ICMP and TCP targets on a schedule, appends results as zstd-compressed InfluxDB line protocol, and reads them back in a terminal UI. No web server, no database, no alerting.
- [didvc](https://github.com/didvc/didvc): Aesthetic Vulpes, Tokyo | a 20s Japanese fox #arts #music #provenance | 2027 Profile README
<!-- END gh-mutual-linking -->
