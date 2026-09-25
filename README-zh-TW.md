[English](README.md) · [日本語](README-ja.md) · 繁體中文 · [简体中文](README-zh.md) · [Deutsch](README-de.md) · [Français](README-fr.md) · [Español](README-es.md)

# Kawaii Hugo Theme

具有可愛（kawaii）風格、深色模式，以及各處細緻動畫的 Hugo 佈景主題。

![Kawaii 佈景主題螢幕截圖](https://raw.githubusercontent.com/didvc/hugo-kawaii/master/images/screenshot.png)

[線上展示](https://didvc.github.io/hugo-kawaii/)可以看到實際效果，`exampleSite` 目錄則包含一個完整可運作的網站。

![GitHub stars](https://img.shields.io/github/stars/didvc/hugo-kawaii?style=social)
![GitHub forks](https://img.shields.io/github/forks/didvc/hugo-kawaii?style=social)
![GitHub issues](https://img.shields.io/github/issues/didvc/hugo-kawaii)
![GitHub license](https://img.shields.io/github/license/didvc/hugo-kawaii)

## 功能

版面採用響應式、行動優先的設計，搭配清爽的字體、流暢的動畫與細緻的互動效果。深色模式會跟隨系統設定，也可以手動切換。搜尋完全在用戶端執行。標記在設計時就考量了無障礙性（包含鍵盤操作），並以符合 WCAG 為目標。顏色、字型與版面由 CSS 自訂屬性控制，因此很容易修改；儲存庫也附有一個完整的範例網站，可以直接拿來起步。

## 快速開始

1. 將佈景主題加入為子模組：
   ```bash
   git submodule add https://github.com/didvc/hugo-kawaii.git themes/kawaii
   ```

2. 在 `hugo.toml` 中設定：
   ```toml
   theme = "kawaii"
   ```

3. 啟動網站：
   ```bash
   hugo server
   ```

## 需求

Hugo Extended 0.147.0 以上，以及用於安裝佈景主題的 Git。

## 設定

### 基本設定

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

### 社群連結

```toml
[[params.social]]
  name = "github"
  url = "https://github.com/yourusername"

[[params.social]]
  name = "twitter"
  url = "https://twitter.com/yourusername"
```

### 導覽選單

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

### 精選區塊

```toml
[[params.featured_sections]]
  title = "Modern Design"
  description = "Clean and beautiful aesthetics"
  icon = "✨"
  link = "about/"
```

## 自訂

### 顏色

覆寫 CSS 變數以變更顏色：

```css
/* assets/css/custom.css */
:root {
  --kawaii-primary: #your-primary-color;
  --kawaii-secondary: #your-secondary-color;
  --kawaii-accent: #your-accent-color;
}
```

### 字型

透過字型變數變更字體：

```css
:root {
  --kawaii-font-family: 'Your Font', sans-serif;
  --kawaii-font-mono: 'Your Mono Font', monospace;
}
```

## 內容結構

### 文章 Front Matter

```yaml
---
title: "Your Post Title"
date: 2024-01-15T10:00:00Z
description: "Post description for SEO"
tags: ["tag1", "tag2", "tag3"]
featured_image: "/images/featured.jpg"
---
```

### 頁面結構

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

## 效能

本佈景主題以 Lighthouse 在效能、無障礙、最佳做法與 SEO 四項皆達 100 分為目標。CSS 與 JavaScript 合計小於 50 KB，在現代網路連線下可於一秒內載入。

## 瀏覽器支援

Chrome 或 Chromium 88 以上、Firefox 85 以上、Safari 14 以上，以及 Edge 88 以上。

## 貢獻

歡迎透過[錯誤回報](https://github.com/didvc/hugo-kawaii/issues/new?template=bug_report.yml)與[功能請求](https://github.com/didvc/hugo-kawaii/issues/new?template=feature_request.yml)範本提出錯誤回報與功能請求；想法也可以發表在 [Discussions](https://github.com/didvc/hugo-kawaii/discussions)。若要貢獻程式碼，請 fork 儲存庫，依照既有風格在功能分支上開發，用範例網站測試後，再提交說明變更內容的 pull request。改善文件與範例、分享你自己的自訂方式，也同樣歡迎。

### 開發環境設定

1. Fork 並 clone 儲存庫：
   ```bash
   git clone https://github.com/didvc/hugo-kawaii.git
   cd hugo-kawaii
   ```

2. 建立測試網站：
   ```bash
   hugo new site test-site
   cd test-site
   ln -s ../../../hugo-kawaii themes/kawaii
   ```

3. 複製範例設定：
   ```bash
   cp themes/kawaii/exampleSite/hugo.toml .
   cp -r themes/kawaii/exampleSite/content .
   ```

4. 啟動開發伺服器：
   ```bash
   hugo server --theme kawaii
   ```

## 未來規劃

規劃中：多語言支援（i18n）、更進階的搜尋、更多配色，以及動畫與效能的持續改進。

## 支援

使用方式請參閱本 README 與範例網站。問題與疑問請到 [GitHub Issues](https://github.com/didvc/hugo-kawaii/issues) 或 [GitHub Discussions](https://github.com/didvc/hugo-kawaii/discussions)；一般的 Hugo 問題請參閱 [Hugo 論壇](https://discourse.gohugo.io/)、[Hugo 文件](https://gohugo.io/documentation/) 與 [Hugo 佈景主題目錄](https://themes.gohugo.io/)。

## 致謝

以 [Hugo](https://gohugo.io/) 為基礎。字型使用 Rasmus Andersson 設計的 Inter 與 JetBrains Mono，圖示來自 Feather Icons。

## 授權

以 [MIT 授權](LICENSE) 釋出。

<!-- BEGIN gh-mutual-linking -->

---

### Related projects

- [astro-html-editor](https://github.com/didvc/astro-html-editor): Self-hosted HTML editor with live preview. Astro SSR + plain JavaScript, server-side file persistence.
- [html-bio-generator](https://github.com/didvc/html-bio-generator): A modern, intuitive tool for creating beautiful HTML bio pages with ease. Built with Next.js, TypeScript, and Tailwind CSS. Perfect for developers, freelancers, and content creators.
- [cf-cache-utils](https://github.com/didvc/cf-cache-utils): CLI to warm and inspect Cloudflare edge cache status across all your URLs; no external dependencies, pure Node.js
- [uptime-mon](https://github.com/didvc/uptime-mon): Lightweight single-binary endpoint uptime monitor. Probes HTTP, keyword, ICMP and TCP targets on a schedule, appends results as zstd-compressed InfluxDB line protocol, and reads them back in a terminal UI. No web server, no database, no alerting.
- [didvc](https://github.com/didvc/didvc): Aesthetic Vulpes, Tokyo | a 20s Japanese fox #arts #music #provenance | 2027 Profile README
<!-- END gh-mutual-linking -->
