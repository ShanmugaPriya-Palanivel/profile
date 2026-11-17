# Shanmugapriya Palanivel — Profile Website

> Personal single-page profile website built with **pure HTML5, CSS3 and Vanilla JavaScript** (zero frameworks, zero libraries). Deployed automatically to GitHub Pages via GitHub Actions.

---

## 🌐 Live Site

`https://<your-github-username>.github.io/profile-website/`

---

## 📋 Sections

| # | Section | Description |
|---|---------|-------------|
| 1 | Hero | Full-screen intro with name, tagline, skill badges & CTA |
| 2 | Professional Journey | Vertical timeline of milestones & projects |
| 3 | Personal Likings | Card grid — music, movies, food, books, travel, tech |
| 4 | Family | CSS flip-cards with warm palette |
| 5 | Hobbies & Passions | Masonry gallery — Doodling, Art, Painting, Mandala |
| 6 | Footer | Social links, build credit, back-to-top |

---

## 🗂️ Folder Structure

```
profile-website/
├── index.html                 ← Single-page application
├── css/
│   ├── theme.css              ← CSS variables ONLY (edit this to retheme)
│   └── style.css              ← All layout & components (uses var() everywhere)
├── js/
│   └── main.js                ← Navigation, scroll FX, lightbox, interactions
├── images/
│   ├── hero/
│   ├── journey/
│   ├── interests/
│   ├── family/
│   └── hobbies/
├── .github/
│   └── workflows/
│       ├── validate.yml       ← Workflow 1: HTML & CSS linting
│       ├── deploy.yml         ← Workflow 2: Auto-deploy to GitHub Pages
│       ├── pr-checks.yml      ← Workflow 3: PR quality gates
│       ├── lighthouse.yml     ← Workflow 4: Performance audit
│       └── notify.yml         ← Workflow 5: Deployment notifications
├── .htmlhintrc
├── .gitignore
└── README.md
```

---

## 🎨 Theming System

The **entire visual identity** lives in one file: `css/theme.css`.

Change only that file → commit → push → pipeline rebuilds and redeploys automatically.

### Available Themes (branches)

| Branch | Theme |
|--------|-------|
| `main` | Light (default) |
| `theme/dark-mode` | Dark (teal + navy) |
| `theme/warm-tones` | Warm (amber + sand) |

---

## 🌿 Branching Strategy

```
main                        ← Production (auto-deploys)
└── develop                 ← Integration
    ├── feature/hero-section
    ├── feature/journey-timeline
    ├── feature/interests-cards
    ├── feature/family-section
    ├── feature/hobbies-gallery
    ├── theme/dark-mode
    ├── theme/warm-tones
    ├── ci/setup-validation
    ├── ci/setup-deploy
    ├── ci/setup-pr-checks
    ├── ci/setup-lighthouse
    └── ci/setup-notifications
```

**Rules:**
- No direct commits to `main`
- Every change goes through a PR
- At least 1 peer review before merging

---

## ⚙️ CI/CD Pipeline

| Workflow | File | Trigger |
|----------|------|---------|
| HTML & CSS Validation | `validate.yml` | Push / PR |
| Auto-Deploy | `deploy.yml` | Merge to `main` |
| PR Quality Checks | `pr-checks.yml` | PR opened |
| Lighthouse Audit | `lighthouse.yml` | After deploy + weekly Monday 9 AM |
| Deployment Notification | `notify.yml` | After deploy |

---

## 🚀 Getting Started

```bash
# 1. Clone the repo
git clone https://github.com/<username>/profile-website.git
cd profile-website

# 2. Open locally (no build step needed!)
open index.html   # macOS
# or just drag index.html into your browser

# 3. Push to GitHub and enable Pages:
#    Repo Settings → Pages → Source: GitHub Actions
```

---

## 📦 Tech Stack

- **HTML5** — Semantic tags (header, nav, main, section, article, footer)
- **CSS3** — Flexbox, Grid, Custom Properties, Animations, Transitions
- **Vanilla JS** — ES6+, IntersectionObserver, focus management
- **GitHub Actions** — CI/CD pipeline (5 workflows)
- **GitHub Pages** — Deployment target

---

Built with ❤️ HTML, CSS & JS | Deployed via GitHub Actions

