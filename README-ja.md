[English](README.md) · 日本語 · [繁體中文](README-zh-TW.md) · [简体中文](README-zh.md) · [Deutsch](README-de.md) · [Français](README-fr.md) · [Español](README-es.md)

# Kawaii Hugo Theme

かわいい見た目、ダークモード、随所の小さなアニメーションを備えたHugoテーマです。

![Kawaiiテーマのスクリーンショット](https://raw.githubusercontent.com/didvc/hugo-kawaii/master/images/screenshot.png)

[ライブデモ](https://didvc.github.io/hugo-kawaii/)で実際の表示を確認できます。`exampleSite` ディレクトリには、そのまま動くサイト一式が入っています。

![GitHub stars](https://img.shields.io/github/stars/didvc/hugo-kawaii?style=social)
![GitHub forks](https://img.shields.io/github/forks/didvc/hugo-kawaii?style=social)
![GitHub issues](https://img.shields.io/github/issues/didvc/hugo-kawaii)
![GitHub license](https://img.shields.io/github/license/didvc/hugo-kawaii)

## 機能

レイアウトはレスポンシブかつモバイルファーストで、すっきりとした書体に、なめらかなアニメーションと細やかなインタラクションを組み合わせています。ダークモードはシステムの設定に従い、手動でも切り替えられます。検索はすべてクライアント側で動作します。マークアップはキーボード操作を含むアクセシビリティを考慮して作られており、WCAGへの準拠を目指しています。色、フォント、レイアウトはCSSカスタムプロパティで制御しているので変更が簡単で、リポジトリには出発点として使える完全なサンプルサイトが含まれています。

## クイックスタート

1. テーマをサブモジュールとして追加します:
   ```bash
   git submodule add https://github.com/didvc/hugo-kawaii.git themes/kawaii
   ```

2. `hugo.toml` で指定します:
   ```toml
   theme = "kawaii"
   ```

3. サイトを起動します:
   ```bash
   hugo server
   ```

## 動作要件

Hugo Extended 0.147.0以降と、テーマのインストールに使うGit。

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

### ソーシャルリンク

```toml
[[params.social]]
  name = "github"
  url = "https://github.com/yourusername"

[[params.social]]
  name = "twitter"
  url = "https://twitter.com/yourusername"
```

### ナビゲーションメニュー

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

### 注目セクション

```toml
[[params.featured_sections]]
  title = "Modern Design"
  description = "Clean and beautiful aesthetics"
  icon = "✨"
  link = "about/"
```

## カスタマイズ

### 色

CSS変数を上書きして色を変更します:

```css
/* assets/css/custom.css */
:root {
  --kawaii-primary: #your-primary-color;
  --kawaii-secondary: #your-secondary-color;
  --kawaii-accent: #your-accent-color;
}
```

### フォント

フォント変数で書体を変更します:

```css
:root {
  --kawaii-font-family: 'Your Font', sans-serif;
  --kawaii-font-mono: 'Your Mono Font', monospace;
}
```

## コンテンツ構成

### 記事のフロントマター

```yaml
---
title: "Your Post Title"
date: 2024-01-15T10:00:00Z
description: "Post description for SEO"
tags: ["tag1", "tag2", "tag3"]
featured_image: "/images/featured.jpg"
---
```

### ページ構成

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

## パフォーマンス

Performance、Accessibility、Best Practices、SEOのすべてでLighthouseスコア100を目標にしています。CSSとJavaScriptを合わせて50 KB未満で、最近の回線なら1秒未満で読み込まれます。

## 対応ブラウザ

Chrome／Chromium 88以降、Firefox 85以降、Safari 14以降、Edge 88以降。

## コントリビュート

バグ報告と機能要望は、[バグ報告](https://github.com/didvc/hugo-kawaii/issues/new?template=bug_report.yml)と[機能要望](https://github.com/didvc/hugo-kawaii/issues/new?template=feature_request.yml)のテンプレートから受け付けています。アイデアは[Discussions](https://github.com/didvc/hugo-kawaii/discussions)にもどうぞ。コードの場合は、リポジトリをフォークし、既存のスタイルに沿ってフィーチャーブランチで作業し、サンプルサイトで動作を確かめてから、変更内容を説明したプルリクエストを送ってください。ドキュメントやサンプルの改善、独自のカスタマイズの紹介も同じく歓迎します。

### 開発環境のセットアップ

1. リポジトリをフォークしてクローンします:
   ```bash
   git clone https://github.com/didvc/hugo-kawaii.git
   cd hugo-kawaii
   ```

2. テスト用のサイトを作成します:
   ```bash
   hugo new site test-site
   cd test-site
   ln -s ../../../hugo-kawaii themes/kawaii
   ```

3. サンプルの設定をコピーします:
   ```bash
   cp themes/kawaii/exampleSite/hugo.toml .
   cp -r themes/kawaii/exampleSite/content .
   ```

4. 開発サーバーを起動します:
   ```bash
   hugo server --theme kawaii
   ```

## ロードマップ

予定: 多言語対応（i18n）、より高度な検索、配色の追加、アニメーションとパフォーマンスのさらなる改善。

## サポート

使い方はこのREADMEとサンプルサイトで説明しています。質問や問題は[GitHub Issues](https://github.com/didvc/hugo-kawaii/issues)または[GitHub Discussions](https://github.com/didvc/hugo-kawaii/discussions)へ。Hugo全般の質問については、[Hugoフォーラム](https://discourse.gohugo.io/)、[Hugoドキュメント](https://gohugo.io/documentation/)、[Hugoテーマ一覧](https://themes.gohugo.io/)を参照してください。

## クレジット

[Hugo](https://gohugo.io/)をベースにしています。書体はRasmus AnderssonによるInterとJetBrains Mono、アイコンはFeather Iconsを使用しています。

## ライセンス

[MITライセンス](LICENSE)で公開しています。

<!-- BEGIN gh-mutual-linking -->

---

### Related projects

- [astro-html-editor](https://github.com/didvc/astro-html-editor): Self-hosted HTML editor with live preview. Astro SSR + plain JavaScript, server-side file persistence.
- [html-bio-generator](https://github.com/didvc/html-bio-generator): A modern, intuitive tool for creating beautiful HTML bio pages with ease. Built with Next.js, TypeScript, and Tailwind CSS. Perfect for developers, freelancers, and content creators.
- [cf-cache-utils](https://github.com/didvc/cf-cache-utils): CLI to warm and inspect Cloudflare edge cache status across all your URLs; no external dependencies, pure Node.js
- [uptime-mon](https://github.com/didvc/uptime-mon): Lightweight single-binary endpoint uptime monitor. Probes HTTP, keyword, ICMP and TCP targets on a schedule, appends results as zstd-compressed InfluxDB line protocol, and reads them back in a terminal UI. No web server, no database, no alerting.
- [didvc](https://github.com/didvc/didvc): Aesthetic Vulpes, Tokyo | a 20s Japanese fox #arts #music #provenance | 2027 Profile README
<!-- END gh-mutual-linking -->
