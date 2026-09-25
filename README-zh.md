[English](README.md) · [日本語](README-ja.md) · [繁體中文](README-zh-TW.md) · 简体中文 · [Deutsch](README-de.md) · [Français](README-fr.md) · [Español](README-es.md)

# Kawaii Hugo Theme

具有可爱（kawaii）风格、深色模式，以及处处细腻动画的 Hugo 主题。

![Kawaii 主题截图](https://raw.githubusercontent.com/didvc/hugo-kawaii/master/images/screenshot.png)

[在线演示](https://didvc.github.io/hugo-kawaii/)可以看到实际效果，`exampleSite` 目录则包含一个完整可运行的网站。

![GitHub stars](https://img.shields.io/github/stars/didvc/hugo-kawaii?style=social)
![GitHub forks](https://img.shields.io/github/forks/didvc/hugo-kawaii?style=social)
![GitHub issues](https://img.shields.io/github/issues/didvc/hugo-kawaii)
![GitHub license](https://img.shields.io/github/license/didvc/hugo-kawaii)

## 功能

布局采用响应式、移动优先的设计，搭配清爽的字体、流畅的动画和细致的交互效果。深色模式会跟随系统设置，也可以手动切换。搜索完全在客户端运行。标记在设计时就考虑了无障碍（包括键盘操作），并以符合 WCAG 为目标。颜色、字体和布局由 CSS 自定义属性控制，因此很容易修改；仓库还附带一个完整的示例网站，可以直接作为起点。

## 快速开始

1. 将主题添加为子模块：
   ```bash
   git submodule add https://github.com/didvc/hugo-kawaii.git themes/kawaii
   ```

2. 在 `hugo.toml` 中设置：
   ```toml
   theme = "kawaii"
   ```

3. 启动网站：
   ```bash
   hugo server
   ```

## 要求

Hugo Extended 0.147.0 或更高版本，以及用于安装主题的 Git。

## 配置

### 基本配置

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

### 社交链接

```toml
[[params.social]]
  name = "github"
  url = "https://github.com/yourusername"

[[params.social]]
  name = "twitter"
  url = "https://twitter.com/yourusername"
```

### 导航菜单

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

### 精选区块

```toml
[[params.featured_sections]]
  title = "Modern Design"
  description = "Clean and beautiful aesthetics"
  icon = "✨"
  link = "about/"
```

## 自定义

### 颜色

覆盖 CSS 变量以更改颜色：

```css
/* assets/css/custom.css */
:root {
  --kawaii-primary: #your-primary-color;
  --kawaii-secondary: #your-secondary-color;
  --kawaii-accent: #your-accent-color;
}
```

### 字体

通过字体变量更改排版：

```css
:root {
  --kawaii-font-family: 'Your Font', sans-serif;
  --kawaii-font-mono: 'Your Mono Font', monospace;
}
```

## 内容结构

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

### 页面结构

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

## 性能

本主题的目标是在 Lighthouse 的性能、无障碍、最佳实践和 SEO 四项中均达到 100 分。CSS 和 JavaScript 合计小于 50 KB，在现代网络连接下可在一秒内加载完成。

## 浏览器支持

Chrome 或 Chromium 88+、Firefox 85+、Safari 14+ 以及 Edge 88+。

## 贡献

欢迎通过[错误报告](https://github.com/didvc/hugo-kawaii/issues/new?template=bug_report.yml)和[功能请求](https://github.com/didvc/hugo-kawaii/issues/new?template=feature_request.yml)模板提交错误报告和功能请求；想法也可以发到 [Discussions](https://github.com/didvc/hugo-kawaii/discussions)。如果要贡献代码，请 fork 仓库，按照现有风格在功能分支上开发，用示例网站测试后，再提交一个说明改动内容的 pull request。改进文档和示例、分享你自己的定制方式，同样非常欢迎。

### 开发环境搭建

1. Fork 并克隆仓库：
   ```bash
   git clone https://github.com/didvc/hugo-kawaii.git
   cd hugo-kawaii
   ```

2. 创建测试网站：
   ```bash
   hugo new site test-site
   cd test-site
   ln -s ../../../hugo-kawaii themes/kawaii
   ```

3. 复制示例配置：
   ```bash
   cp themes/kawaii/exampleSite/hugo.toml .
   cp -r themes/kawaii/exampleSite/content .
   ```

4. 启动开发服务器：
   ```bash
   hugo server --theme kawaii
   ```

## 路线图

计划中：多语言支持（i18n）、更高级的搜索、更多配色方案，以及动画和性能的进一步改进。

## 支持

使用方法请参阅本 README 和示例网站。问题和疑问请提交到 [GitHub Issues](https://github.com/didvc/hugo-kawaii/issues) 或 [GitHub Discussions](https://github.com/didvc/hugo-kawaii/discussions)；一般的 Hugo 问题请参阅 [Hugo 论坛](https://discourse.gohugo.io/)、[Hugo 文档](https://gohugo.io/documentation/) 和 [Hugo 主题目录](https://themes.gohugo.io/)。

## 致谢

基于 [Hugo](https://gohugo.io/) 构建。字体使用 Rasmus Andersson 设计的 Inter 和 JetBrains Mono，图标来自 Feather Icons。

## 许可证

以 [MIT 许可证](LICENSE) 发布。

<!-- BEGIN gh-mutual-linking -->

---

### Related projects

- [astro-html-editor](https://github.com/didvc/astro-html-editor): Self-hosted HTML editor with live preview. Astro SSR + plain JavaScript, server-side file persistence.
- [html-bio-generator](https://github.com/didvc/html-bio-generator): A modern, intuitive tool for creating beautiful HTML bio pages with ease. Built with Next.js, TypeScript, and Tailwind CSS. Perfect for developers, freelancers, and content creators.
- [cf-cache-utils](https://github.com/didvc/cf-cache-utils): CLI to warm and inspect Cloudflare edge cache status across all your URLs; no external dependencies, pure Node.js
- [uptime-mon](https://github.com/didvc/uptime-mon): Lightweight single-binary endpoint uptime monitor. Probes HTTP, keyword, ICMP and TCP targets on a schedule, appends results as zstd-compressed InfluxDB line protocol, and reads them back in a terminal UI. No web server, no database, no alerting.
- [didvc](https://github.com/didvc/didvc): Aesthetic Vulpes, Tokyo | a 20s Japanese fox #arts #music #provenance | 2027 Profile README
<!-- END gh-mutual-linking -->
