# 📝 Learning Reflection — Full Stack Web Project

**Course:** Full Stack Web Development  
**Institution:** Kirirom Institute of Technology  
**Author:** Chanratharo Rath  
**Collaborator:** Hour-Meng  

---

## What This Project Is

A multi-page static website built to simulate the Harley-Davidson product site. The assignment covered responsive layout, Bootstrap component usage, CSS custom properties, and multi-page navigation — all core skills in front-end web development.

---

## What Went Well

**Bootstrap grid mastery.** The `row`/`col-*` system clicked for me on this project. Understanding how `col-12 col-md-4` collapses from 3-column to single-column on mobile was the moment responsive design made sense — not just theoretically, but in practice while watching the layout shift in the browser.

**CSS variables.** Using `--hd-orange`, `--hd-dark`, and similar custom properties across all pages meant changing one color in `custom.css` updated the whole site instantly. That's a workflow upgrade I'll carry forward.

**Swiper.js integration.** Wiring up `<swiper-container>` web components with breakpoint configs in vanilla JS was the most challenging part. Getting `slidesPerView` to change responsively — 1.15 on mobile, 1.8 on tablet, 2.4 on desktop — required reading documentation and testing, not just copying code.

**Semantic HTML.** Using `<header>`, `<section>`, `<footer>`, `<address>`, and `<nav>` properly instead of generic `<div>` soup. Small thing, but it matters for accessibility and career-readiness.

---

## What Was Challenging

**Script placement.** I placed Bootstrap's `<script>` tag at the top of `<body>` across all pages, which is technically a render-blocking pattern. The correct approach is to put scripts at the end of `<body>` or add `defer`. This is something I'll fix reflexively in future projects.

**Image path management.** Keeping track of `images/cruiser/`, `images/Touring/`, `images/Trike/` sub-directories and making sure every `src` path was correct across five HTML files was tedious. A templating system or a component-based framework (React, Vue) would eliminate this class of error.

**Non-functional forms.** The newsletter form uses `onsubmit="return false;"` to prevent page reload — it's a UI demo, not a real form. Wiring this to an actual backend (Node.js + Express, or a form service) is the next logical step.

---

## What I'd Do Differently

1. Put all scripts at the end of `<body>` with `defer` from day one
2. Use a shared HTML template or include system to avoid repeating the navbar and footer in every file
3. Replace the real H-D contact info in the footer with clearly marked placeholder data
4. Add `<meta name="description">` to every page for SEO basics
5. Deploy to GitHub Pages from the start, not just at the end

---

## Skills Demonstrated

- HTML5 semantic structure
- CSS3 custom properties and responsive styling
- Bootstrap 5 grid, navbar, utilities, and component classes
- Third-party library integration (Swiper.js)
- Multi-page site architecture with consistent navigation
- Accessibility markup (`aria-*`, `alt`, semantic elements)
- CDN loading with SRI integrity hashes

---

## Next Steps (Personal Roadmap)

- [ ] Add a JavaScript filter to the Parts page (filter by category without page reload)
- [ ] Convert the newsletter form to actually submit via a free service like Formspree
- [ ] Deploy to GitHub Pages
- [ ] Rebuild one page in React to compare the developer experience
