<div align="center">

# 🏍️ Harley-Davidson — Full Stack Web Project

### HTML · CSS · Bootstrap 5 · Swiper.js

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![Bootstrap](https://img.shields.io/badge/Bootstrap_5-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)](https://getbootstrap.com/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Complete-brightgreen?style=for-the-badge)]()

> **Class assignment — Full Stack Web Development**  
> Kirirom Institute of Technology · Software Engineering Program  
> **Author: Chanratharo Rath (`ratharo-gitty`)** · Collaborator: Hour-Meng

</div>

---

## 📖 Table of Contents

- [About the Project](#-about-the-project)
- [Pages & Features](#-pages--features)
- [Tech Stack](#️-tech-stack)
- [What I Learned](#-what-i-learned)
- [Known Issues & Bugs](#-known-issues--bugs)
- [How to Run](#-how-to-run)
- [Project Structure](#-project-structure)
- [Disclaimer](#️-disclaimer)
- [Author](#-author)

---

## 🔍 About the Project

This is a **multi-page front-end website** built as a class assignment for the Full Stack Development course at Kirirom Institute of Technology. The site recreates a Harley-Davidson product showcase using only HTML, CSS, and Bootstrap — no frameworks, no back-end, no JavaScript libraries beyond Bootstrap and Swiper.

**The goal:** demonstrate proficiency with responsive layout, component-based design using Bootstrap 5, custom CSS styling, and clean multi-page navigation.

> ⚠️ This is an educational project. It is NOT affiliated with or endorsed by Harley-Davidson Motor Company. All brand names, logos, and product names used are property of Harley-Davidson, Inc. and are used here for educational demonstration purposes only.

---

## 📄 Pages & Features

| Page | File | Description |
|---|---|---|
| **Home** | `index.html` | Hero banner, model family cards, featured model split-layout, newsletter signup CTA |
| **Motorcycles** | `Motorcycles.html` | Three model families (Cruiser, Touring, Trike) with Swiper.js touch carousels |
| **Parts** | `Parts.html` | Accessories catalog with filterable product grid |
| **Goods & Gifts** | `GoodsGifts.html` | Merchandise catalog with category layout |
| **Discover H-D** | `Discover.html` | Event listings, museum, H.O.G. community section, Riding Academy |

### Key Features Implemented

- ✅ **Responsive navbar** — collapses to hamburger on mobile (Bootstrap)
- ✅ **Hero section** with full-bleed image and overlay text
- ✅ **Swiper.js carousels** — touch/drag, keyboard, breakpoints for 1/2/3 visible slides
- ✅ **Product card grid** — Bootstrap row/col with gap utilities
- ✅ **Sticky navigation** — stays at top on scroll
- ✅ **Custom CSS variables** — consistent color theming via `--hd-orange`, `--hd-dark`, etc.
- ✅ **Custom font** — loaded from `CustomFonts/custom.css`
- ✅ **Fully responsive** — works on mobile, tablet, and desktop
- ✅ **Accessible markup** — `aria-label`, `alt` text, semantic HTML5 elements
- ✅ **Footer** — multi-column links, social icons via Bootstrap Icons, address block

---

## 🛠️ Tech Stack

| Technology | Version | Purpose |
|---|---|---|
| **HTML5** | — | Page structure and semantic markup |
| **CSS3** | — | Custom styles, CSS variables, layout |
| **Bootstrap** | 5.3.8 | Responsive grid, navbar, utilities, components |
| **Bootstrap Icons** | 1.11.3 | Social and UI icons |
| **Swiper.js** | 12.x | Touch-friendly product carousels (Motorcycles page) |

All libraries are loaded via **CDN** — no npm, no build step. Open any `.html` file directly in a browser and it just works.

---

## 🎓 What I Learned

This project was hands-on practice with real concepts taught in the Full Stack course:

**Bootstrap 5**
- Grid system (`container`, `row`, `col-*`, `g-*` gutters)
- Navbar component with responsive collapse
- Utility classes for spacing, typography, flexbox, and color

**CSS**
- CSS custom properties (variables) for consistent theming
- `object-fit: cover` for responsive image cropping
- Overlay positioning with `position: absolute` and z-index
- `clamp()` for fluid, responsive sizing
- Sticky headers with `position: sticky`

**HTML5**
- Semantic sectioning elements (`<header>`, `<section>`, `<footer>`, `<address>`)
- Accessibility: `aria-label`, `aria-controls`, `aria-expanded`, `alt` attributes
- `<form>` with `onsubmit="return false;"` for non-functional UI demo

**Third-party integration**
- Loading and initializing Swiper.js web components (`<swiper-container>`, `<swiper-slide>`)
- Configuring Swiper with breakpoints for responsive behavior
- CDN integrity hashes (SRI — Subresource Integrity) for security

---

## 🐛 Known Issues & Bugs

Identified during code review — documented for learning purposes:

| # | File | Issue | Severity |
|---|---|---|---|
| 1 | `Motorcycles.html` | `<script>` for Swiper placed in `<body>` before it is needed — should be at end of `<body>` or use `defer` | Low |
| 2 | All pages | Bootstrap `<script>` tag placed at **top** of `<body>` instead of end — can delay page rendering | Low |
| 3 | All pages | Footer contact info (`support@harley-davidson.com`, `1-800-258-1525`) references the **real** H-D company — should be replaced with placeholder data for a student project | Informational |
| 4 | All pages | Social icon links use `href="#"` — would 404 or scroll to top in production | Low |
| 5 | `index.html` | Newsletter `<form>` has `onsubmit="return false;"` — acceptable for demo, but should be noted as non-functional | Informational |
| 6 | All pages | No `<meta name="description">` tag — important for SEO and accessibility | Low |
| 7 | `Discover.html` | Event dates (e.g. Sturgis Aug 2026) are hardcoded — will become stale | Informational |

> None of these are security vulnerabilities. They are common beginner-to-intermediate improvements to work through in future iterations.

---

## 🚀 How to Run

No installation needed. This is a pure static site.

**Option 1 — Open directly:**
```
Clone or download this repo → open index.html in any browser
```

**Option 2 — VS Code Live Server:**
1. Install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension
2. Right-click `index.html` → **Open with Live Server**

**Option 3 — GitHub Pages:**
1. Push to a GitHub repo
2. Go to **Settings → Pages → Branch: main → / (root)**
3. Site will be live at `https://yourusername.github.io/repo-name/`

---

## 📁 Project Structure

```
fullstack-hd-project/
│
├── index.html              ← Home page
├── Motorcycles.html        ← Motorcycle lineup with carousels
├── Parts.html              ← Parts & accessories catalog
├── GoodsGifts.html         ← Merchandise catalog
├── Discover.html           ← Events, museum, community
│
├── CustomFonts/
│   └── custom.css          ← Custom fonts + shared CSS variables & component styles
│
├── images/
│   ├── image.png           ← Hero banner
│   ├── GrandAmerica.png
│   ├── Cruiser.png
│   ├── Trike.png
│   ├── cruiser/            ← Cruiser model images
│   ├── Touring/            ← Touring model images
│   ├── Trike/              ← Trike model images
│   ├── parts/              ← Parts & accessories images
│   ├── goods/              ← Merchandise images
│   └── discover/           ← Events & community images
│
├── docs/
│   └── REFLECTION.md       ← Personal learning reflection
│
├── .github/
│   └── workflows/
│       └── lint.yml        ← CI: validates all HTML files exist
│
├── .gitignore
├── LICENSE
└── README.md               ← You are here
```

---

## ⚠️ Disclaimer

This project is a **student class assignment** created for educational purposes at Kirirom Institute of Technology. It is **not affiliated with, endorsed by, or connected to** Harley-Davidson Motor Company in any way.

All Harley-Davidson brand names, logos, trademarks, product names, and images referenced are the property of H-D U.S.A., LLC. They are used here solely for educational and demonstrative purposes under the context of a web development course.

---

## 👤 Author

<div align="center">

**Chanratharo Rath** · `ratharo-gitty`

🎓 Software Engineering @ Kirirom Institute of Technology 🇰🇭  
⚡ Vibecoder — build fast, ship often, iterate always

[![Email](https://img.shields.io/badge/Email-rathchanratharo%40gmail.com-red?style=flat-square&logo=gmail)](mailto:rathchanratharo@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Chanratharo%20Rath-blue?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/chanratharo-rath-5a4502360)
[![Instagram](https://img.shields.io/badge/Instagram-th9ro__onit4riel-purple?style=flat-square&logo=instagram)](https://www.instagram.com/th9ro_onit4riel)
[![GitHub](https://img.shields.io/badge/GitHub-ratharo--gitty-black?style=flat-square&logo=github)](https://github.com/ratharo-gitty)

---

*"He Who Makes No Mistakes, Makes Nothing."*

</div>
