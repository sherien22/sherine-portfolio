# Sherine Zarif Farhan — Portfolio Website

Personal portfolio website for **Sherine Zarif Farhan**, Full-Stack Developer.  
Built with pure HTML5, CSS3, and Vanilla JavaScript. No build step. No dependencies to install.

---

## Project Structure

```
portfolio/
├── index.html                        # Single-page entry point
├── robots.txt                        # SEO crawler rules
├── sitemap.xml                       # SEO sitemap
│
├── assets/
│   ├── css/
│   │   ├── style.css                 # Design tokens, reset, base layout
│   │   ├── components.css            # Buttons, cards, forms, skills, etc.
│   │   └── animations.css            # Scroll reveals, keyframes, transitions
│   │
│   ├── js/
│   │   ├── main.js                   # Navbar, theme toggle, typed text, etc.
│   │   ├── animations.js             # IntersectionObserver scroll animations
│   │   └── contact.js                # Formspree form validation & submission
│   │
│   └── images/
│       ├── profile/
│       │   └── sherine-avatar.jpg    # [PLACEHOLDER] Your profile photo
│       ├── projects/
│       │   ├── hospital-website.jpg          # [PLACEHOLDER] Project screenshot
│       │   ├── php-web-project.jpg           # [PLACEHOLDER] Project screenshot
│       │   └── laravel-employee-system.jpg   # [PLACEHOLDER] Project screenshot
│       ├── og-image.jpg              # [PLACEHOLDER] Open Graph image (1200×630)
│       └── favicon/
│           ├── favicon.ico
│           ├── favicon-32x32.png
│           └── apple-touch-icon.png  # [PLACEHOLDER] Favicon set
│
└── cv/
    └── sherine-zarif-farhan-cv.pdf   # [PLACEHOLDER] Your CV / Resume
```

---

## Quick Start (Local Preview)

### Option A — XAMPP (already installed)

1. The project is already at `C:\xampp\htdocs\portfolio`.
2. Start **Apache** in the XAMPP Control Panel.
3. Open your browser and go to: `http://localhost/portfolio`

### Option B — VS Code Live Server

1. Install the [Live Server extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer).
2. Right-click `index.html` → **Open with Live Server**.

### Option C — Any browser (file protocol)

Double-click `index.html`. Most features work; fonts and icons require an internet
connection (they load from Google Fonts and Cloudflare CDNs).

---

## Before You Deploy — Placeholder Checklist

Search the codebase for `[PLACEHOLDER` to find every item that needs your real data.

| # | Placeholder | Where | What to Replace With |
|---|-------------|-------|----------------------|
| 1 | `[PLACEHOLDER: your-domain.com]` | `index.html`, `robots.txt`, `sitemap.xml` | Your live domain, e.g. `sherinezarif.dev` |
| 2 | `[PLACEHOLDER: your-formspree-form-id]` | `index.html` (form `action`) | Your Formspree form ID — see **Formspree Setup** below |
| 3 | `[PLACEHOLDER: https://github.com/your-github-username]` | `index.html` (multiple) | Your GitHub profile URL |
| 4 | `[PLACEHOLDER: https://linkedin.com/in/your-linkedin-username]` | `index.html` (multiple) | Your LinkedIn profile URL |
| 5 | `[PLACEHOLDER: your@email.com]` | `index.html` (multiple) | Your email address |
| 6 | `[PLACEHOLDER: cv-pdf]` | `index.html` (Download CV button) | Confirm path matches `cv/sherine-zarif-farhan-cv.pdf` |
| 7 | `[PLACEHOLDER: profile-photo]` | `index.html` (hero `<img>`) | Replace `assets/images/profile/sherine-avatar.jpg` with your photo |
| 8 | `[PLACEHOLDER: project-N-screenshot]` | `index.html` (3 project cards) | Replace the 3 project images in `assets/images/projects/` |
| 9 | `[PLACEHOLDER: project-N-description]` | `index.html` (3 project cards) | Write a real description for each project |
| 10 | `[PLACEHOLDER: live-demo-url]` | `index.html` (3 project cards) | Live demo URLs, or remove the Live Demo buttons |
| 11 | `[PLACEHOLDER: https://github.com/.../project]` | `index.html` (3 project cards) | GitHub repo URLs for each project |
| 12 | `[PLACEHOLDER: Company / Organization Name]` | `index.html` (internship timeline) | Your internship company name |
| 13 | `[PLACEHOLDER: Duration — e.g., Jun 2024 – Aug 2024]` | `index.html` (internship timeline) | Your internship dates |
| 14 | `[PLACEHOLDER: og-image]` | `assets/images/og-image.jpg` | A 1200×630 image for social sharing previews |
| 15 | Favicon set | `assets/images/favicon/` | Generate at [favicon.io](https://favicon.io) or [realfavicongenerator.net](https://realfavicongenerator.net) |

---

## Formspree Setup (Contact Form)

1. Go to [https://formspree.io](https://formspree.io) and create a free account.
2. Click **+ New Form** → give it a name (e.g. *Portfolio Contact*).
3. Copy your form endpoint — it looks like: `https://formspree.io/f/xyzabcde`
4. In `index.html`, find the `<form>` tag in the Contact section and replace:
   ```html
   action="https://formspree.io/f/[PLACEHOLDER: your-formspree-form-id]"
   ```
   with your real endpoint:
   ```html
   action="https://formspree.io/f/xyzabcde"
   ```
5. Deploy the site — Formspree will send submissions directly to your email.

> The free Formspree plan allows **50 submissions/month**, which is plenty for a personal portfolio.

---

## Deployment Options

### GitHub Pages (free)

```bash
# 1. Create a new GitHub repository (e.g. "portfolio")
# 2. Push the portfolio folder contents to the repo root
git init
git add .
git commit -m "Initial portfolio deployment"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/portfolio.git
git push -u origin main

# 3. In the repo on GitHub:
#    Settings → Pages → Source: Deploy from branch → main / (root) → Save
# 4. Your site will be live at: https://YOUR_USERNAME.github.io/portfolio
```

### Netlify (free — recommended for custom domain)

1. Go to [https://netlify.com](https://netlify.com) → **Add new site** → **Deploy manually**.
2. Drag and drop the entire `portfolio/` folder onto the Netlify deploy area.
3. Done — Netlify gives you a live URL instantly.
4. To connect a custom domain: **Site settings → Domain management → Add custom domain**.

### Vercel (free)

1. Go to [https://vercel.com](https://vercel.com) → **Add New Project**.
2. Import your GitHub repository or drag-drop the folder.
3. Vercel auto-detects a static site — click **Deploy**.

### Traditional Hosting (cPanel / Shared Hosting)

1. Zip the `portfolio/` folder contents (not the folder itself).
2. Upload to `public_html/` via cPanel File Manager or FTP.
3. If deploying to a subdirectory (e.g. `public_html/portfolio/`), update all
   `[PLACEHOLDER: your-domain.com]` references to `your-domain.com/portfolio`.

---

## Customisation Guide

### Changing Colors

All colors are CSS custom properties in `assets/css/style.css` under the `:root` and
`[data-theme="light"]` blocks. Change `--accent-primary` and `--accent-secondary` to
update the entire site's color scheme instantly.

```css
:root {
  --accent-primary:   #6366f1;  /* Change this — used for CTAs, links, highlights */
  --accent-secondary: #06b6d4;  /* Change this — used for badges, accents */
}
```

### Adding a New Project

1. Add a project screenshot to `assets/images/projects/`.
2. Copy one of the existing `<article class="project-card">` blocks in `index.html`.
3. Update the title, description, tech tags, image path, and links.

### Adding a New Skill

In the Skills section of `index.html`, add a new `<li class="skill-item">` to the
appropriate `<ul class="skill-list">`, following the same pattern as the existing items.

### Changing Typed Text Phrases

In `assets/js/main.js`, find the `phrases` array in `initTypedText()` and update it:

```js
const phrases = [
  'Full-Stack Applications.',
  'Backend Systems.',
  // Add or change phrases here
];
```

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Markup | HTML5 (semantic) |
| Styling | CSS3 (Custom Properties, Grid, Flexbox) |
| Scripting | Vanilla JavaScript (ES2020, no frameworks) |
| Icons | Font Awesome 6 (CDN) |
| Fonts | Google Fonts — Inter + Fira Code |
| Contact | Formspree (no backend required) |
| SEO | Semantic HTML, Open Graph, JSON-LD, sitemap |
| Hosting | Static — any platform |

---

## Accessibility Notes

- Skip navigation link for keyboard users
- All images have `alt` attributes
- Form fields have associated `<label>` elements
- ARIA roles and `aria-label` on interactive elements
- `prefers-reduced-motion` is respected throughout
- Keyboard-navigable (logical Tab order)
- Color contrast targets WCAG 2.1 AA

> Full WCAG compliance requires manual testing with assistive technologies
> and should be validated with a screen reader before final deployment.

---

## License

This portfolio is personal work. All content belongs to **Sherine Zarif Farhan**.
