---
title: "Getting Started"
description: "Learn how to configure your DocFlow documentation pipeline."
order: 2
---

# Getting Started 🚀

This guide will walk you through setting up and customizing your documentation project directory.

> [!TIP]
> Ensure your markdown filenames use hyphens instead of spaces (e.g. `getting-started.md`) for cleaner website URLs.

## 📄 Document Frontmatter
Every documentation page should start with a YAML frontmatter block. This block defines the metadata used for navigation page ordering, search engines, and browser page titles.

```yaml
---
title: "Getting Started"
description: "Learn how to configure your DocFlow project."
order: 2
---
```

## 💾 Code & Highlight Syntax
Here is an example code snippet block to demonstrate built-in syntax styling:

```javascript
// bin/compiler.js snippet
import fs from 'fs';
import path from 'path';

export const buildDocs = () => {
  console.log("Compiling markdown directory...");
};
```

---

## 🎨 Layout Alerts
Here is an example of an important warnings callout box:

> [!WARNING]
> Do not expose sensitive environment credentials or secret access tokens inside your public documentation directories!
