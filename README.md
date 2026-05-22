# Holly Melone — Portfolio

A hand-built static portfolio site. No frameworks, no build step, no dependencies — just HTML, CSS, and a little JavaScript. Open any `.html` file in a text editor to edit it directly.

Live at **https://hmelone.github.io**

---

## File structure

```
.
├── index.html              Homepage
├── about.html              About + capabilities
├── resume.html             Web resume / CV
├── contact.html            Contact
├── work/
│   ├── index.html          Work index
│   ├── flexera.html        Case study — Flexera knowledge transformation
│   ├── help-center.html    Case study — post-sales help center
│   ├── ai-tool.html        Case study — AI authoring tool
│   ├── twn.html            Case study — TWN knowledge system
│   ├── onboarding.html     Case study — onboarding foundation
│   ├── ai-techcomm.html    Essay — AI in technical communication
│   └── utah-handbook.html  Project — U of Utah handbook redesign
├── css/style.css           The whole design system
├── js/main.js              Scroll-reveal + auto-year script
├── assets/                 Images, diagrams, and downloadable files
│   ├── utah/               Handbook cover images
│   └── files/              Downloadable PDFs
├── .nojekyll               Tells GitHub Pages to serve files as-is
└── README.md
```

---

## Editing

Everything is plain HTML/CSS. To change content, open the relevant `.html` file and edit the text. To change styling, edit `css/style.css` (colors and fonts are defined as CSS variables at the top). The copyright year updates automatically.

## Publishing updates

This site is hosted with GitHub Pages from the `hmelone.github.io` repository. To update the live site, upload changed files to the repo (or commit and push) — Pages rebuilds automatically within a few minutes.

Filenames are case-sensitive on GitHub Pages: keep everything lowercase with hyphens (e.g. `utah-before.pdf`).
