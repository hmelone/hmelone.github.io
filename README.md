# Holly Melone — Portfolio

A hand-built static portfolio site. No frameworks, no build step, no
dependencies. Just HTML, CSS, and a tiny bit of JavaScript. Open any
`.html` file in a text editor and edit it directly.

---

## Files in this repo

```
.
├── index.html            ← Homepage
├── about.html            ← About + 10 capabilities
├── resume.html           ← Full record / CV
├── contact.html          ← Contact
├── work/
│   ├── index.html        ← Case-study index
│   ├── flexera.html      ← Case study 01 — fully written
│   ├── ai-tool.html      ← Case study 02 — fully written
│   ├── ia-rhetoric.html  ← Case study 03 — scaffolded (in progress)
│   ├── twn.html          ← Case study 04 — fully written
│   └── onboarding.html   ← Case study 05 — fully written
├── css/
│   └── style.css         ← The whole design system
├── js/
│   └── main.js           ← Tiny scroll-reveal script
├── assets/               ← Drop images here (headshot, diagrams, etc.)
└── README.md
```

---

## Design notes

- **Typeface:** *Instrument Serif* (display, italic-forward),
  *Inter Tight* (body), *IBM Plex Mono* (metadata). All free from
  Google Fonts.
- **Palette:** bone white `#F4F1E8`, ink `#0E0E0C`, acid yellow
  `#E8FF3A`. The yellow is deliberately bright — it's the signature
  move of the site. It appears on hovers, status pills, and a single
  highlighted phrase in the cover lede. Don't add more.
- **No images required.** The whole site works without a single
  photograph. Add a headshot later if you want one — drop it in
  `assets/headshot.jpg` and reference it from `about.html`.

---

## How to put this online with GitHub Pages

These steps assume you don't already have a GitHub account or
familiarity with the tools. If you do, skip ahead.

### 1. Create a free GitHub account

Go to **https://github.com** and sign up. Pick a username you'd be
comfortable showing on a resume — `hollymelone` if it's available is
ideal.

### 2. Create a new repository

Once signed in, click the **+** in the top right of GitHub and choose
**New repository**.

- **Repository name:** `hmelone.github.io`
  (Use this exact format — your username, then `.github.io`. This
  tells GitHub Pages to serve the repo at the matching URL with no
  extra setup.)
- **Public**
- **Don't** check "Add a README" — this folder already has one.
- Click **Create repository**.

### 3. Upload these files

The easiest path that doesn't require installing anything:

1. On the new repository page, click **uploading an existing file**.
2. Drag every file and folder from this folder into the upload area
   (`index.html`, `about.html`, the `css/` folder, the `work/` folder,
   etc.).
3. Scroll to the bottom and click **Commit changes**.

GitHub will automatically detect this as a Pages site within a minute
or two. Visit `https://hmelone.github.io` (replace with your
actual username) and your site will be live.

### 4. Optional but recommended: a custom domain

If you buy `hollymelone.com` (Namecheap, Cloudflare Registrar, and
Porkbun are all good and cost roughly $10–15/year):

1. In your repo, go to **Settings → Pages**.
2. Under **Custom domain**, enter `hollymelone.com` and save.
3. At your domain registrar, point the domain to GitHub by adding
   these DNS records (GitHub's docs walk through this):
   - Four `A` records pointing to `185.199.108.153`,
     `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One `CNAME` record on `www` pointing to
     `hmelone.github.io`
4. Back in GitHub, check **Enforce HTTPS**.

It can take an hour or so for DNS to propagate. After that,
`hollymelone.com` will serve your site with a free SSL certificate.

---

## How to edit content

Every page is a single `.html` file. Open it in any text editor (VS
Code is free and the standard recommendation, but Notepad, TextEdit,
or even GitHub's web editor will work). Edit the visible text between
the tags and save. Push the change to GitHub and the site updates
within a minute.

### Editor notes (the yellow boxes)

Several pages have **bright yellow boxes** that say
**"Editor's note (visible only to you)"**. These are reminders to
yourself about specifics to fill in (metrics, citations, examples,
links). Once you've filled in the surrounding content, **delete the
entire `<div class="editor-note">…</div>` block.** They're visible on
the public site by design — so you can't forget them — but they
need to come out before you share widely.

### Filling in Writing & Projects (homepage)

The homepage has a "Writing & Projects" grid with six placeholder
items (YouTube channel, articles, projects). Each item is a single
`<a class="item">…</a>` block. To customize:

1. Open `index.html` and find the `<!-- WRITING & PROJECTS -->`
   section.
2. For each item, replace the `href="#"` with the real URL, and
   update the `kind`, `h4`, `p`, and `when` text.
3. Add or remove items by copying or deleting whole `<a class="item">`
   blocks. Six fits perfectly in two rows; nine fits in three. Any
   number works — the grid auto-flows.
4. Delete the editor's note above the grid when you're done.

### Adding a new case study

1. Copy `work/flexera.html` to a new file like `work/new-project.html`.
2. Edit the title, kicker (`Case Study / 06 · year`), the meta block,
   and the section content.
3. Add a link to the new file in three places:
   - `work/index.html` (the case-study list)
   - `index.html` (the homepage feed, if you want it featured)
   - The previous and next case study's `cs-nav` block at the bottom

### Swapping the headshot or adding images

Drop image files into the `assets/` folder and reference them in HTML
like `<img src="assets/headshot.jpg" alt="Holly Melone" />`.

### Changing colors

The whole color system is at the top of `css/style.css` under
`:root { ... }`. Change `--accent: #E8FF3A;` to any hex color and the
entire site updates.

---

## Browser support

Tested on current Chrome, Safari, Firefox, and Edge. Uses modern CSS
(custom properties, clamp, grid, sticky) and works on mobile.
Reduced-motion preferences are respected. No trackers, no analytics,
no cookies — just HTML.
