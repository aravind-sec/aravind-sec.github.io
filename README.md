# Aravind A — Portfolio

Static HTML/CSS/JS portfolio. No frameworks, no build tools. Open `index.html` in a browser and you're live.

---

## Files

```
portfolio/
├── index.html   ← All content lives here
├── style.css    ← All styles & design tokens
├── script.js    ← Interactions (nav, scroll reveal)
└── README.md
```

---

## How to Edit Content (no deep-dive needed)

### 1. Your Photo
In `index.html`, find:
```html
src="https://placehold.co/480x580/..."
```
Replace with your photo filename, e.g.:
```html
src="photo.jpg"
```
Drop `photo.jpg` into the same folder as `index.html`.

---

### 2. Your Bio / About Me Text
Search for `EDIT: Your bio` in `index.html`.
The three `<p class="about__para">` blocks are your bio paragraphs. Replace them freely.

---

### 3. Your Skill Tags
Find `<div class="about__skills">`. Each `<span class="skill-tag">` is one chip.
Add, remove, or rename them.

---

### 4. Adding / Editing a Project
Find the `<!-- PROJECT 01 -->` block.  
Each project card has these clearly labelled fields:
- `.proj__category` — badge (e.g. "Security Automation")
- `.proj__title` — project name
- `.proj__desc` — 2–3 sentence summary
- `.proj__tag` items — tech stack
- `img src` — screenshot image
- `.btn` href — GitHub or live demo URL

**To add a new project:** Copy a full `<article class="proj-card">` block and paste it inside `.projects__grid`. Fill in the fields.

---

### 5. Contact Links
Find the `<!-- EDIT: Update all href -->` comment in the contact section.
Update each `href="..."` with your actual links (email, LinkedIn, GitHub, HTB).

---

### 6. Resume Download
Find:
```html
<a href="#" class="btn btn--primary" download>Download Resume ↓</a>
```
Replace `#` with the path to your PDF, e.g. `href="Aravind_Resume.pdf"`.
Drop the PDF into the same folder.

---

## Changing Colours

All colours are CSS variables in `style.css` under `:root`:

```css
:root {
  --bg:      #0b0d12;   /* main background */
  --accent:  #4ade80;   /* green — swap this for any colour */
  --text-1:  #f0f2f5;   /* headlines */
  --text-2:  #8b9199;   /* body text */
}
```

Change `--accent` to any hex and the entire site updates.

---

## Deployment (3 options)

### Option A — GitHub Pages (free, recommended)
1. Push this folder to a GitHub repo.
2. Go to Settings → Pages → Source: `main` branch, `/ (root)`.
3. Your site is live at `https://yourusername.github.io/repo-name`.

### Option B — Netlify (drag & drop)
1. Go to [netlify.com](https://netlify.com) → "Add new site" → "Deploy manually".
2. Drag the entire `portfolio/` folder onto the page.
3. Live in 10 seconds.

### Option C — Vercel
1. `npm i -g vercel` then `vercel` inside the folder.
2. Follow the prompts. Done.

---

## Scroll Reveal Animations
Add `class="reveal"` to any HTML element and it will fade up when scrolled into view.
Add `class="reveal reveal-delay-1"` (or `-2`, `-3`) for staggered effects.
