# Getting Started — Southern Belles Website

Welcome to the Southern Belle's Pancake House website project. This guide covers everything you need to set up your development environment, including Claude Code and the plugins/skills we use.

## Project Overview

This is a static HTML website for **Southern Belle's Pancake House** in Carpentersville, IL. It consists of:

- **`index.html`** — Main website (menu, hours, location, about, gallery, contact)
- **`catering.html`** — Catering landing page (packages, quote form, service area, FAQ)
- **`assets/images/`** — 71+ curated food photos from Instagram (@southernbellespancakes)
- **`SITE_AUDIT.md`** — Audit of the original WordPress site we're replacing
- **`CLAUDE.md`** — Project-specific instructions for Claude Code

### Tech Stack

- Static HTML + Tailwind CSS (via CDN)
- Fonts: Playfair Display (headings) + Inter (body)
- No build step — just open HTML files in a browser
- Brand colors: `#3b8ced` (blue), `#1a3a6b` (dark blue), `#fdf8f0` (cream), `#c8943e` (gold)

### Run Locally

```bash
cd Southern-Belles-Website
python3 -m http.server 8888
# Open http://localhost:8888 in your browser
```

---

## Installing Claude Code

Claude Code is Anthropic's AI coding assistant that runs in your terminal. It was used to build this entire project.

### Prerequisites

- macOS, Linux, or Windows (WSL2)
- Node.js 18+ (check with `node --version`)

### Install

```bash
npm install -g @anthropic-ai/claude-code
```

### First Run

```bash
cd Southern-Belles-Website
claude
```

On first launch, it will ask you to authenticate with your Anthropic account. Follow the browser prompt.

### Quick Reference

| Command | What it does |
|---------|-------------|
| `claude` | Start Claude Code in current directory |
| `/help` | Show all available commands |
| `/clear` | Clear conversation context |
| `Ctrl+C` | Cancel current operation |
| `Escape` | Exit Claude Code |

Claude Code reads the `CLAUDE.md` file in the project root automatically, so it already knows the project context, brand guidelines, and conventions.

---

## Plugins We Use

Plugins extend Claude Code with extra capabilities. Install them from inside Claude Code.

### 1. Superpowers (Core Workflow)

Our primary workflow plugin — provides structured planning, brainstorming, code review, TDD, and skill management.

```bash
# Inside Claude Code, run:
/install-plugin superpowers
```

**Key skills from superpowers:**
- `brainstorming` — Structured ideation before building features
- `writing-plans` — Create step-by-step implementation plans
- `executing-plans` — Execute plans with review checkpoints
- `verification-before-completion` — Verify work before claiming it's done
- `requesting-code-review` — Get code reviewed before merging

### 2. Claude-Mem (Memory System)

Gives Claude persistent memory across conversations — remembers what was built, decisions made, and lessons learned.

```bash
/install-plugin claude-mem
```

### 3. Episodic Memory

Searchable conversation history — lets Claude recall exact prompts and decisions from past sessions.

```bash
/install-plugin episodic-memory
```

### 4. Playwright (Browser Automation)

Used for downloading images from Instagram and testing the site in a browser.

```bash
/install-plugin playwright
```

---

## Skills Used on This Project

Skills are specialized prompts that guide Claude's behavior for specific tasks. These are the ones relevant to this project — listed in the project's `CLAUDE.md`. You don't need to install them separately; they come with the plugins above.

### Design & Frontend
| Skill | Purpose |
|-------|---------|
| `frontend-design` | UI aesthetics and design system decisions |
| `mobile-design` | Mobile-first responsive design |
| `tailwind-patterns` | Tailwind CSS v4 utility patterns |
| `tailwind-design-system` | Design tokens, component variants, responsive system |
| `scroll-experience` | Smooth scroll interactions for menu/gallery |
| `landing-page-generator` | High-converting page layouts |
| `form-cro` | Optimize contact/order forms for conversion |

### SEO & Content
| Skill | Purpose |
|-------|---------|
| `seo-fundamentals` | Core SEO principles for local restaurant |
| `seo-audit` | Diagnose and fix SEO issues |
| `schema-markup` | Restaurant and LocalBusiness JSON-LD structured data |
| `local-legal-seo-audit` | Local business SEO optimization |
| `seo-content-writer` | SEO-optimized page copy targeting local keywords |
| `seo-structure-architect` | Header hierarchy, internal links, site structure |
| `fixing-metadata` | OG tags, meta descriptions, canonical URLs |
| `content-creator` | Brand voice and marketing copy |
| `copy-editing` | Polish menu descriptions and page copy |

### Quality & Accessibility
| Skill | Purpose |
|-------|---------|
| `accessibility-compliance-accessibility-audit` | WCAG/ADA compliance audit |
| `web-performance-optimization` | Core Web Vitals, bundle size, caching |
| `progressive-web-app` | Offline menu access, installability |
| `clean-code` | Code quality and maintainability |

### Code & DevOps
| Skill | Purpose |
|-------|---------|
| `javascript-pro` | Modern JS best practices |
| `git-advanced-workflows` | Git branching and PR workflows |
| `github-actions-templates` | CI/CD pipeline for deployment |

### How to Use Skills

Just describe what you want and Claude will use the right skill automatically. You can also reference them directly:

```
# Example prompts that trigger skills:
"Audit the SEO on catering.html"
"Check accessibility on the main page"
"Optimize the images for web performance"
"Review the schema markup"
```

---

## Git Workflow

We use a simple branching model:

```bash
# Always work on a feature branch
git checkout -b feature/your-feature-name

# Make changes, then commit
git add -A
git commit -m "feat: description of what you did"

# Push and create a PR
git push -u origin feature/your-feature-name
# Then create a Pull Request on GitHub
```

### Commit Message Convention

We use conventional commits:
- `feat:` — New feature or section
- `fix:` — Bug fix
- `style:` — Visual/CSS changes
- `content:` — Menu or text content updates
- `docs:` — Documentation changes
- `refactor:` — Code restructuring without behavior change

---

## Key Files Reference

| File | Purpose |
|------|---------|
| `index.html` | Main website — menu, hours, location, about |
| `catering.html` | Catering landing page — packages, quote form |
| `CLAUDE.md` | Project instructions Claude reads automatically |
| `GETTING-STARTED.md` | This file — setup and onboarding guide |
| `SITE_AUDIT.md` | Audit of the old WordPress site |
| `assets/images/` | All food photos and logos |
| `assets/images/ig_scan/` | Raw Instagram post screenshots |
| `Southern-Belle-Menu-WEB_0425.pdf` | Current menu PDF from the restaurant |

---

## Current Status & What Needs Work

### Done
- Main site with full text-based menu (80+ items, 8 tabbed categories)
- Catering landing page with quote form, packages, FAQ, service area
- 71 curated food photos from Instagram
- JSON-LD schema markup (Restaurant, CateringService, FAQPage)
- Mobile-responsive design with sticky header

### In Progress / TODO
- Replace placeholder catering packages with actual catering menu
- Wire up the quote form to a real backend (currently simulated)
- Replace placeholder testimonials with real ones
- Claim Google Business Profile for Carpentersville
- Add interior/exterior photos of the restaurant
- Deploy to southernbellespancakes.com (pending WordPress admin access)
- Set up CI/CD for automatic deployment

---

## Need Help?

- Ask Claude Code — it has full context of this project via `CLAUDE.md`
- Check `SITE_AUDIT.md` for background on the original site issues
- The menu PDF (`Southern-Belle-Menu-WEB_0425.pdf`) is the source of truth for menu items and prices
