# Southern Belles Pancakes — Website

Website for **Southern Belles Pancakes**, a family diner in Carpentersville, IL. Live at [southernbellespancakes.com](https://southernbellespancakes.com/site/carpentersville-il/).

## Project Goals

- Modern, fast, mobile-first website for a local diner
- Strong local SEO (Google Business, Maps, rich results for Carpentersville, IL)
- Accessible to all visitors (WCAG 2.1 AA minimum)
- Menu, hours, location, and contact info front and center
- Optimized for Core Web Vitals and page speed

## Tech Decisions

Pending — discuss stack before building. Candidates: Next.js + Tailwind, static HTML/CSS, or Astro.

## Content Priorities

1. Menu (food items, prices, specials)
2. Location & hours (Carpentersville, IL — embedded map, clear address)
3. About / story (family history, photos, Southern hospitality theme)
4. Contact (phone, email, online ordering link if applicable)
5. Gallery (food photos, interior shots)

## SEO Requirements

- Restaurant schema markup (JSON-LD) for Google rich results
- Local business structured data (Carpentersville, IL address, hours, phone, cuisine type)
- Open Graph and Twitter Card meta tags for social sharing
- Optimized page titles and meta descriptions targeting "pancakes Carpentersville IL", "breakfast Carpentersville", "diner near me"
- XML sitemap
- Mobile-friendly (Google Mobile-First Indexing)
- Local SEO signals: NAP consistency, Google Business Profile integration

## Antigravity Skills
When working on this project, use these skills from antigravity-awesome-skills:
- `frontend-design` — UI aesthetics and design system decisions
- `react-best-practices` — React component performance (if using React/Next.js)
- `react-patterns` — modern React composition patterns
- `nextjs-best-practices` — Next.js App Router, SSR, ISR patterns
- `nextjs-app-router-patterns` — Next.js 14+ architecture
- `tailwind-patterns` — Tailwind CSS v4 utility patterns
- `tailwind-design-system` — design tokens, component variants, responsive system
- `seo-audit` — diagnose and fix SEO issues
- `seo-fundamentals` — core SEO principles for local restaurant
- `schema-markup` — Restaurant and LocalBusiness JSON-LD structured data
- `local-legal-seo-audit` — local business SEO optimization for Carpentersville area
- `seo-content-planner` — content strategy and topic clusters
- `seo-content-writer` — SEO-optimized page copy targeting local keywords
- `seo-structure-architect` — header hierarchy, internal links, site structure
- `seo-content-auditor` — audit content quality and optimization gaps
- `seo-cannibalization-detector` — prevent keyword overlap if multi-location pages exist
- `fixing-metadata` — OG tags, meta descriptions, canonical URLs, Twitter cards
- `accessibility-compliance-accessibility-audit` — WCAG/ADA compliance audit
- `web-performance-optimization` — Core Web Vitals, bundle size, caching
- `progressive-web-app` — offline menu access, installability
- `mobile-design` — mobile-first responsive design for diner customers
- `form-cro` — optimize contact/order forms for conversion
- `landing-page-generator` — high-converting page layouts
- `scroll-experience` — smooth scroll interactions for menu/gallery
- `typescript-expert` — TypeScript patterns (if using TS)
- `javascript-pro` — modern JS best practices
- `nodejs-best-practices` — Node.js patterns for build/deploy
- `clean-code` — code quality and maintainability
- `performance-optimizer` — identify and fix performance bottlenecks
- `error-handling-patterns` — resilient error handling
- `git-advanced-workflows` — git branching and PR workflows
- `github-actions-templates` — CI/CD pipeline for deployment
- `content-creator` — brand voice and marketing copy
- `copy-editing` — polish menu descriptions and page copy

## Image Acquisition

When downloading images from Instagram or social media, use **Playwright MCP** (`mcp__plugin_playwright_playwright__*`), NOT Chrome browser automation. Chrome blocks automated downloads after ~5 files. Playwright can batch-screenshot element-level images directly to disk. See global memory `feedback_playwright_instagram_images.md` for the batch code pattern.

Instagram handle: `@southernbellespancakes` (1,221+ posts). 71 images already downloaded to `assets/images/`. Scanned originals in `assets/images/ig_scan/`.
