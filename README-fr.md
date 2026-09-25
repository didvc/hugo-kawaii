[English](README.md) · [日本語](README-ja.md) · [繁體中文](README-zh-TW.md) · [简体中文](README-zh.md) · [Deutsch](README-de.md) · Français · [Español](README-es.md)

# Kawaii Hugo Theme

Un thème Hugo au style kawaii, avec un mode sombre et de petites animations un peu partout.

![Capture d’écran du thème Kawaii](https://raw.githubusercontent.com/didvc/hugo-kawaii/master/images/screenshot.png)

Une [démo en ligne](https://didvc.github.io/hugo-kawaii/) montre le thème en situation, et le répertoire `exampleSite` contient un site complet et fonctionnel.

![GitHub stars](https://img.shields.io/github/stars/didvc/hugo-kawaii?style=social)
![GitHub forks](https://img.shields.io/github/forks/didvc/hugo-kawaii?style=social)
![GitHub issues](https://img.shields.io/github/issues/didvc/hugo-kawaii)
![GitHub license](https://img.shields.io/github/license/didvc/hugo-kawaii)

## Fonctionnalités

La mise en page est responsive et pensée d’abord pour le mobile, avec une typographie nette, des animations fluides et des micro-interactions. Le mode sombre suit la préférence du système et peut aussi être basculé à la main. La recherche s’exécute entièrement côté client. Le balisage est conçu pour l’accessibilité, navigation au clavier comprise, et le thème vise la conformité WCAG. Les couleurs, les polices et la mise en page reposent sur des propriétés personnalisées CSS, ce qui les rend faciles à modifier, et le dépôt fournit un site d’exemple complet pour démarrer.

## Démarrage rapide

1. Ajouter le thème comme sous-module :
   ```bash
   git submodule add https://github.com/didvc/hugo-kawaii.git themes/kawaii
   ```

2. Le déclarer dans votre `hugo.toml` :
   ```toml
   theme = "kawaii"
   ```

3. Lancer le site :
   ```bash
   hugo server
   ```

## Prérequis

Hugo Extended 0.147.0 ou plus récent, et Git pour installer le thème.

## Configuration

### Configuration de base

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

### Liens sociaux

```toml
[[params.social]]
  name = "github"
  url = "https://github.com/yourusername"

[[params.social]]
  name = "twitter"
  url = "https://twitter.com/yourusername"
```

### Menu de navigation

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

### Sections mises en avant

```toml
[[params.featured_sections]]
  title = "Modern Design"
  description = "Clean and beautiful aesthetics"
  icon = "✨"
  link = "about/"
```

## Personnalisation

### Couleurs

Redéfinissez les variables CSS pour changer les couleurs :

```css
/* assets/css/custom.css */
:root {
  --kawaii-primary: #your-primary-color;
  --kawaii-secondary: #your-secondary-color;
  --kawaii-accent: #your-accent-color;
}
```

### Polices

Modifiez la typographie via les variables de police :

```css
:root {
  --kawaii-font-family: 'Your Font', sans-serif;
  --kawaii-font-mono: 'Your Mono Font', monospace;
}
```

## Structure du contenu

### Front matter d’un article

```yaml
---
title: "Your Post Title"
date: 2024-01-15T10:00:00Z
description: "Post description for SEO"
tags: ["tag1", "tag2", "tag3"]
featured_image: "/images/featured.jpg"
---
```

### Structure des pages

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

## Performances

Le thème vise un score Lighthouse de 100 en Performance, Accessibilité, Bonnes pratiques et SEO. Le CSS et le JavaScript réunis pèsent moins de 50 Ko, et les pages se chargent en moins d’une seconde sur une connexion moderne.

## Navigateurs pris en charge

Chrome ou Chromium 88+, Firefox 85+, Safari 14+ et Edge 88+.

## Contribuer

Les signalements de bugs et les demandes de fonctionnalités sont les bienvenus via les modèles [signalement de bug](https://github.com/didvc/hugo-kawaii/issues/new?template=bug_report.yml) et [demande de fonctionnalité](https://github.com/didvc/hugo-kawaii/issues/new?template=feature_request.yml) ; les idées peuvent aussi aller dans les [Discussions](https://github.com/didvc/hugo-kawaii/discussions). Pour le code : forkez le dépôt, travaillez sur une branche dédiée en suivant le style existant, testez avec le site d’exemple, puis ouvrez une pull request qui décrit la modification. Les améliorations de la documentation et des exemples, ainsi que les retours sur vos propres personnalisations, sont tout aussi bienvenus.

### Environnement de développement

1. Forker et cloner le dépôt :
   ```bash
   git clone https://github.com/didvc/hugo-kawaii.git
   cd hugo-kawaii
   ```

2. Créer un site de test :
   ```bash
   hugo new site test-site
   cd test-site
   ln -s ../../../hugo-kawaii themes/kawaii
   ```

3. Copier la configuration d’exemple :
   ```bash
   cp themes/kawaii/exampleSite/hugo.toml .
   cp -r themes/kawaii/exampleSite/content .
   ```

4. Lancer le serveur de développement :
   ```bash
   hugo server --theme kawaii
   ```

## Feuille de route

Prévu : prise en charge multilingue (i18n), recherche plus avancée, schémas de couleurs supplémentaires, et poursuite du travail sur les animations et les performances.

## Support

L’utilisation est décrite dans ce README et dans le site d’exemple. Les questions et les problèmes vont dans les [GitHub Issues](https://github.com/didvc/hugo-kawaii/issues) ou les [GitHub Discussions](https://github.com/didvc/hugo-kawaii/discussions) ; pour les questions générales sur Hugo, consultez le [forum Hugo](https://discourse.gohugo.io/), la [documentation Hugo](https://gohugo.io/documentation/) et le [répertoire des thèmes Hugo](https://themes.gohugo.io/).

## Remerciements

Construit sur [Hugo](https://gohugo.io/). Composé en Inter de Rasmus Andersson et en JetBrains Mono, avec des icônes de Feather Icons.

## Licence

Publié sous [licence MIT](LICENSE).

<!-- BEGIN gh-mutual-linking -->

---

### Related projects

- [astro-html-editor](https://github.com/didvc/astro-html-editor): Self-hosted HTML editor with live preview. Astro SSR + plain JavaScript, server-side file persistence.
- [html-bio-generator](https://github.com/didvc/html-bio-generator): A modern, intuitive tool for creating beautiful HTML bio pages with ease. Built with Next.js, TypeScript, and Tailwind CSS. Perfect for developers, freelancers, and content creators.
- [cf-cache-utils](https://github.com/didvc/cf-cache-utils): CLI to warm and inspect Cloudflare edge cache status across all your URLs; no external dependencies, pure Node.js
- [uptime-mon](https://github.com/didvc/uptime-mon): Lightweight single-binary endpoint uptime monitor. Probes HTTP, keyword, ICMP and TCP targets on a schedule, appends results as zstd-compressed InfluxDB line protocol, and reads them back in a terminal UI. No web server, no database, no alerting.
- [didvc](https://github.com/didvc/didvc): Aesthetic Vulpes, Tokyo | a 20s Japanese fox #arts #music #provenance | 2027 Profile README
<!-- END gh-mutual-linking -->
