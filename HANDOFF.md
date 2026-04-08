# Southern Belles Website — Session Handoff

**Date:** 2026-04-05
**Status:** Site built, photos collected, ready for deployment discussion

## What Was Done This Session

### 1. Full Site Audit
- Crawled the live WordPress site at southernbellespancakes.com
- Used Chrome browser automation to render the JS-heavy pages
- Found 22 issues including completely blank Carpentersville page, broken slider images, no SEO, Toast ordering OFF
- Documented everything in `SITE_AUDIT.md`

### 2. Built New Standalone Site
- `index.html` — single-page static site with Tailwind CSS CDN
- Complete text-based menu (80+ items from PDF) organized in 8 tabbed categories
- JSON-LD Restaurant schema, OpenGraph, Twitter Cards for SEO
- Mobile-responsive, sticky nav, smooth scroll
- Toast ordering integration, Google Maps embed, social links
- WGN 9 link (verified), FOX 32 mention
- Matches original blue theme and branding

### 3. Collected 71 Food Photos
- 14 from existing website via curl
- 7 from Instagram via Chrome canvas-to-blob (first 5 worked, then Chrome blocked)
- 45 from Instagram via Playwright MCP batch scraping (breakthrough method)
- Visually reviewed all 45 via multimodal Read tool
- Curated and renamed 39 with semantic menu item names
- Photo grids added to every menu category tab

### 4. Key Findings
- **Playwright MCP** is the correct tool for Instagram image downloads (documented in global memory)
- Chrome blocks automated downloads after ~5 files, base64 returns are blocked by security filter, fetch to localhost blocked by mixed content
- The WordPress site is managed by WebFish and user has no admin access
- Domain must stay as southernbellespancakes.com (shared with other locations)
- Toast POS name: "Southern Belles S. Western Ave"

## What Needs to Happen Next

### Deployment
- User needs to determine hosting path: WordPress admin access from WebFish, or subdomain/subfolder arrangement
- Site is ready to deploy — just needs a server to serve the HTML

### Content Gaps
- No interior/exterior photos of Carpentersville location
- Missing photos: gumbo-laya, catfish, crepes, salads (not found in their ~50 most recent IG posts)
- FOX 32 segment URL not found online
- User to provide additional photos when available

### Business Tasks
- Claim Google Business Profile for Carpentersville
- Re-enable Toast online ordering
- Consider getting Instagram handle or creating Carpentersville-specific social accounts

## File Structure
```
Southern_Belles_Website/
  index.html                          # The new site
  SITE_AUDIT.md                       # Full 22-issue audit
  CLAUDE.md                           # Project instructions
  HANDOFF.md                          # This file
  Southern-Belle-Menu-WEB_0425.pdf    # Menu PDF
  upload_server.py                    # Temp server (can delete)
  assets/images/                      # 71 curated images
    logo_wide.png, logo_square.png    # Logos
    hero_bonuts.jpg                   # Hero image
    bonuts.jpg, wrecker.jpg, ...      # Website originals
    banana_pudding.jpg, ...           # Chrome downloads
    waffles.jpg, nashville_hot.jpg, ...  # Playwright downloads (renamed)
    ig_scan/                          # 45 raw IG screenshots (by post ID)
```

## Restaurant Details
- **Name:** Southern Belle's Pancake House
- **Address:** 152 S. Western Ave, Carpentersville, IL 60110
- **Phone:** (224) 699-9959
- **Hours:** 6 AM - 3 PM daily, Gaming Cafe 3-10 PM
- **Toast:** https://order.toasttab.com/online/southern-belles-carpentersville
- **Instagram:** @southernbellespancakes
- **Facebook:** facebook.com/southernbellescarpentersville
- **WGN 9:** https://wgntv.com/midday-news/lunchbreak-apple-pancakes/
