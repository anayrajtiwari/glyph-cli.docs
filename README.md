# 🌀 Glyph: Zero-Dependency Documentation Compiler & Local Preview Server

**Glyph** is a minimal, blazing-fast, static-site documentation engine designed for developers. It converts directories of raw Markdown and MDX files into premium, responsive developer hubs with client-side search.

---

## 📂 System Architecture

```
                       ┌─────────────────────────┐
                       │   Markdown/MDX Source   │
                       │   (docs/ directory)     │
                       └────────────┬────────────┘
                                    │
                              Compile (V8)
                                    │
                       ┌────────────▼────────────┐
                       │  Static HTML Output     │
                       │  (dist/ directory)      │
                       └────────────┬────────────┘
                                    │
                              Local Hosting
                                    │
                       ┌────────────▼────────────┐
                       │   Glyph Dev Server      │
                       │   (localhost:3000)      │
                       └─────────────────────────┘
```

---

## 🚀 Key Features

1. **Instant Compilation:** Built in vanilla JS with minimal dependency overhead. Compiles documentation pages in under 50ms.
2. **Local Fuzzy Search:** Generates a local search index on-the-fly, giving users instant results without needing external search APIs (like Algolia).
3. **GitHub-Style Alerts:** Supports native `[!NOTE]`, `[!TIP]`, `[!WARNING]`, and `[!IMPORTANT]` blockquotes, rendering them as modern callout cards.
4. **Dev Server & Hot-Reloading:** Watches the source directory for saved edits and automatically triggers builds, instantly updating the local preview.

---

## 🛠️ Quick Start

### 1. Install Dependencies
```bash
npm install
```

### 2. Compile Documentation
```bash
npm run build
```
This compiles the raw documents in `docs/` to static html outputs inside the `dist/` directory.

### 3. Run the Development Preview Server
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) in your browser to view the documentation hub. Saving changes inside `docs/` will trigger automatic rebuilding!

---

## 💻 CLI Commands

Run the compiler CLI locally:

* **Build static documentation:**
  ```bash
  node bin/compiler.js build
  ```
* **Start dev server:**
  ```bash
  node bin/compiler.js dev [port]
  ```

---

## ⚙️ Configuration & Frontmatter

Every page inside `docs/` should start with a YAML frontmatter block to establish ordering, page titles, and meta descriptions.

Example frontmatter block:
```yaml
---
title: "Getting Started"
description: "Learn how to configure your Glyph documentation pipeline."
order: 2
---
```
