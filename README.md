# Kawaii Hugo Theme

A modern and cool Hugo theme with beautiful kawaii aesthetics, dark mode support, and delightful animations.

## 📸 Preview

![Kawaii Theme Screenshot](https://raw.githubusercontent.com/yuis-ice/hugo-kawaii/master/images/screenshot.png)

Visit the [live demo](https://hugo-kawaii.pages.dev/) to see the theme in action, or check out the `exampleSite` directory for a complete working example.

## ✨ Features

- 🎨 **Modern Design**: Clean, contemporary aesthetics with beautiful typography
- 🌙 **Dark Mode**: Automatic system preference detection with manual toggle
- 📱 **Responsive**: Mobile-first design that looks great on all devices
- ⚡ **Fast**: Optimized for performance with minimal resource overhead
- 🔍 **Search**: Built-in client-side search functionality
- ✨ **Animations**: Smooth animations and delightful micro-interactions
- 🎯 **Accessible**: WCAG compliant with keyboard navigation support
- 🛠️ **Customizable**: Easy to customize colors, fonts, and layout

## 🚀 Quick Start

1. **Install the theme**:
   ```bash
   git submodule add https://github.com/yuis-ice/hugo-kawaii.git themes/kawaii
   ```

2. **Update your `hugo.toml`**:
   ```toml
   theme = "kawaii"
   ```

3. **Start your site**:
   ```bash
   hugo server
   ```

## 📋 Requirements

- Hugo Extended version 0.147.0 or higher
- Git (for theme installation)

## 🎨 Configuration

### Basic Configuration

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
  hero_cta_link = "/posts"
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

### Navigation Menu

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

### Featured Sections

```toml
[[params.featured_sections]]
  title = "Modern Design"
  description = "Clean and beautiful aesthetics"
  icon = "✨"
  link = "/about"
```

## 🎨 Customization

### Colors

Override CSS variables to customize colors:

```css
/* assets/css/custom.css */
:root {
  --kawaii-primary: #your-primary-color;
  --kawaii-secondary: #your-secondary-color;
  --kawaii-accent: #your-accent-color;
}
```

### Fonts

Change typography by updating font variables:

```css
:root {
  --kawaii-font-family: 'Your Font', sans-serif;
  --kawaii-font-mono: 'Your Mono Font', monospace;
}
```

## 📝 Content Structure

### Post Front Matter

```yaml
---
title: "Your Post Title"
date: 2024-01-15T10:00:00Z
description: "Post description for SEO"
tags: ["tag1", "tag2", "tag3"]
featured_image: "/images/featured.jpg"
---
```

### Page Structure

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

## 🎯 Performance

The Kawaii theme is optimized for performance:

- **Lighthouse Score**: 100/100 (Performance, Accessibility, Best Practices, SEO)
- **Page Size**: < 50KB (CSS + JS combined)
- **Load Time**: < 1 second on modern connections
- **Mobile Friendly**: Optimized for mobile devices

## 🌍 Browser Support

- Chrome/Chromium 88+
- Firefox 85+
- Safari 14+
- Edge 88+

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### 🐛 Report Issues
- Found a bug? [Create an issue](https://github.com/yuis-ice/hugo-kawaii/issues/new?template=bug_report.yml)
- Use our detailed bug report template for faster resolution

### ✨ Suggest Features
- Have an idea? [Request a feature](https://github.com/yuis-ice/hugo-kawaii/issues/new?template=feature_request.yml)
- Join our [discussions](https://github.com/yuis-ice/hugo-kawaii/discussions) to brainstorm

### 🔧 Code Contributions
- Fork the repository and create a feature branch
- Follow the existing code style and patterns
- Test your changes with the example site
- Submit a pull request with a clear description

### 📚 Documentation
- Help improve documentation and examples
- Share your customizations and use cases
- Contribute to the community discussions

### Development Setup

1. **Fork and clone the repository**:
   ```bash
   git clone https://github.com/yuis-ice/hugo-kawaii.git
   cd kawaii-theme
   ```

2. **Create a test site**:
   ```bash
   hugo new site test-site
   cd test-site
   ln -s ../../../hugo-kawaii themes/kawaii
   ```

3. **Copy example configuration**:
   ```bash
   cp themes/kawaii/exampleSite/hugo.toml .
   cp -r themes/kawaii/exampleSite/content .
   ```

4. **Start development server**:
   ```bash
   hugo server --theme kawaii
   ```

## 📄 License

This theme is released under the [MIT License](LICENSE).

## 🙏 Credits

- **Hugo**: The world's fastest framework for building websites
- **Inter Font**: Beautiful typography by Rasmus Andersson
- **JetBrains Mono**: Excellent monospace font for code
- **Feather Icons**: Beautiful open source icons

## 📞 Support

- **Documentation**: Check the README and exampleSite for usage instructions
- **Issues**: [GitHub Issues](https://github.com/yuis-ice/hugo-kawaii/issues)
- **Discussions**: [GitHub Discussions](https://github.com/yuis-ice/hugo-kawaii/discussions)
- **Community**: [Hugo Community Forum](https://discourse.gohugo.io/)

## 🚀 What's New

- ✅ Modern CSS with custom properties system
- ✅ Dark mode with system preference detection
- ✅ Responsive mobile-first design
- ✅ Interactive JavaScript features
- ✅ Comprehensive example site
- ✅ Accessibility-focused HTML structure

## 🗺️ Future Plans

- [ ] Multi-language support (i18n)
- [ ] Advanced search functionality
- [ ] Additional color schemes
- [ ] Animation improvements
- [ ] Performance optimizations

---

**Made with ❤️ for the Hugo community**

If you like this theme, please ⭐ star it on GitHub and share it with others!

## 📊 Repository Stats

![GitHub stars](https://img.shields.io/github/stars/yuis-ice/hugo-kawaii?style=social)
![GitHub forks](https://img.shields.io/github/forks/yuis-ice/hugo-kawaii?style=social)
![GitHub issues](https://img.shields.io/github/issues/yuis-ice/hugo-kawaii)
![GitHub license](https://img.shields.io/github/license/yuis-ice/hugo-kawaii)

## 🔗 Links

- **Repository**: [github.com/yuis-ice/hugo-kawaii](https://github.com/yuis-ice/hugo-kawaii)
- **Hugo Themes**: [themes.gohugo.io](https://themes.gohugo.io/)
- **Hugo Documentation**: [gohugo.io/documentation](https://gohugo.io/documentation/)

<!-- BEGIN gh-mutual-linking -->

---

### Related projects

- [**bio**](https://github.com/didvc/bio) — Profile writings and translations of Vulpes (didvc)
- [**didvc**](https://github.com/didvc/didvc) — a little bit about me/vulpes.
- [**astro-html-editor**](https://github.com/didvc/astro-html-editor) — Self-hosted HTML editor with live preview. Astro SSR + plain JavaScript, server-side file persistence.
- [**awesome-template**](https://github.com/didvc/awesome-template)
- [**qiskit-getting-started**](https://github.com/didvc/qiskit-getting-started) — 🚀 Learn quantum computing with Qiskit! Comprehensive tutorials, examples, and algorithms for beginners. Features Bell states, quantum…
- [**vibe-go-image-gallery**](https://github.com/didvc/vibe-go-image-gallery) — 🖼️ Modern image gallery application built with Go and Vue.js featuring SEO optimization, responsive design, and automatic thumbnail generation.
- [**go-filemanager**](https://github.com/didvc/go-filemanager) — 🗂️ Modern web-based file manager built with Go. Features file preview, UTF-8 support, responsive design, and secure file operations.
- [**html-bio-generator**](https://github.com/didvc/html-bio-generator) — A modern, intuitive tool for creating beautiful HTML bio pages with ease. Built with Next.js, TypeScript, and Tailwind CSS. Perfect for…
- [**app**](https://github.com/AI-marriage/app) — AIを使った結婚証明書ジェネレーター - ChatGPTとの特別な瞬間を美しい証明書で記録しましょう
- [**app**](https://github.com/anime-portfolio/app) — 🎌 A stunning developer portfolio template with anime aesthetics and interactive features. Transform your portfolio into an anime-inspired…
- [**text-to-speech**](https://github.com/didvc/text-to-speech) — 🎤 VoiceFlow - Modern text-to-speech web application with real-time word highlighting, customizable voice settings, and content management. Built…
- [**molecular**](https://github.com/didvc/molecular) — 🧬 Interactive web application for visualizing and animating molecular structures. Built with React, TypeScript, and modern web technologies for…
- [**app**](https://github.com/hiroyuki-generator/app)
- [**Kuso-Physics**](https://github.com/KusoGames/Kuso-Physics) — Open-source chaos physics game. Built with Next.js. Easily self-host on GitHub Pages.
- [**yuis-ice**](https://github.com/didvc/yuis-ice)
<!-- END gh-mutual-linking -->
