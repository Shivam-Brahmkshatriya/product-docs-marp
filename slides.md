---

marp: true
title: "Product X — Technical Documentation"
author: "Shivam Brahmkshatriya"
theme: default
paginate: true
\_class: lead
-------------

<!-- Custom theme (inline) -->

<style>
/* ===== Custom Theme Overrides ===== */
section {
  font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, "Noto Sans";
}
section h1, section h2, section h3 { letter-spacing: 0.3px; }
section.lead h1 { font-size: 2.4em; }
/* Page number badge styling */
footer { color: #6b7280; font-size: 0.8rem; }
/* Accent utility */
.accent { color: #2563eb; }
/* Code block tweaks */
pre code { border-radius: 12px; padding: 0.75rem 1rem; }
/* Card-like container */
.card { background: #ffffffcc; border: 1px solid #e5e7eb; border-radius: 16px; padding: 16px; }
</style>

<!-- _header: **Product X Docs** -->

<!-- _footer: _v1 • docs generated with Marp_ -->

# Product X — Technical Documentation

**Contact:** [23ds3000034@ds.study.iitm.ac.in](mailto:23ds3000034@ds.study.iitm.ac.in)
Version-controlled Markdown → HTML/PDF/PPTX with **Marp**

---

<!-- _class: lead -->

## Why Marp for Product Docs?

* **Single source** of truth in Git
* Export to **HTML / PDF / PPTX / PNG**
* Works with **CI/CD** for docs
* Developer‑friendly: **Markdown**, KaTeX, code highlighting

---

<!-- Demonstrate custom background image -->

<!-- _backgroundImage: url('images/bg-architecture.jpg') -->

<!-- _backgroundSize: cover -->

<!-- _color: #ffffff -->

<!-- _footer: _Background image demo_ -->

# System Architecture Overview

* Microservices: Auth, API, Billing, Analytics
* Event bus: Kafka
* Storage: Postgres + S3

> Tip: Replace `[images/bg-architecture.jpg](https://github.com/Shivam-Brahmkshatriya/product-docs-marp/blob/main/images/bg-architecture.jpg)` with your own diagram.

---

## Installation & Quickstart

```bash
# Local preview
npx @marp-team/marp-cli@latest -s .

# Build HTML (for GitHub Pages or docs portal)
marp slides.md -o dist/slides.html

# Export PDF / PPTX
marp slides.md --pdf --allow-local-files
marp slides.md --pptx
```

---

## Configuration (package.json)

```json
{
  "name": "product-docs-marp",
  "private": true,
  "devDependencies": { "@marp-team/marp-cli": "^4" },
  "scripts": {
    "start": "marp -s .",
    "build": "marp slides.md -o dist/slides.html",
    "pdf": "marp slides.md --pdf --allow-local-files",
    "pptx": "marp slides.md --pptx"
  }
}
```

---

<!-- Custom styling via directives -->

<!-- _backgroundColor: #0b1020 -->

<!-- _color: #e5e7eb -->

## API Surface — Summary

<div class="card">

**Core Endpoints**

* `POST /v1/auth/login` — token minting
* `GET /v1/users/{id}` — user profile
* `POST /v1/billing/invoice` — create invoice

</div>

---

## Code Snippets

```python
from typing import TypedDict

class Invoice(TypedDict):
    id: str
    amount: float
    currency: str

# O(n log n) billing sort for reporting
invoices = sorted(invoices, key=lambda x: (x['amount'], x['id']))
```

```javascript
// Client SDK initialization
import { Client } from '@productx/sdk'
const client = new Client({ apiKey: process.env.PX_KEY })
```

---

## Mathematical Notes (Complexity)

Inline: Sorting uses \$O(n \log n)\$ comparisons.
Block:

$$
T(n) =
\begin{cases}
  c, & n \le 1 \\
  2\,T\!\left(\frac{n}{2}\right) + O(n), & n > 1
\end{cases}
$$

> We use Master Theorem: \$T(n) = O(n \log n)\$.

---

## Release Process (CI/CD)

1. Commit Markdown changes to `main`
2. GitHub Action runs `marp slides.md -o dist/slides.html`
3. Publish `dist/` via Pages or copy to product portal
4. Tag release and attach `slides.pdf`

---

## Assets & Structure

```
presentation/
├── slides.md
├── images/
│   └── bg-architecture.jpg
├── themes/
│   └── custom.css
└── package.json
```

**Email for queries:** [23ds3000034@ds.study.iitm.ac.in](mailto:23ds3000034@ds.study.iitm.ac.in)

---

## Appendix / Links

* Developer Portal
* Changelog
* Incident Handbook

**Contact:** [23ds3000034@ds.study.iitm.ac.in](mailto:23ds3000034@ds.study.iitm.ac.in)
*End of document*
