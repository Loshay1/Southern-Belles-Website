# Southern Belle's Pancake House — Website Audit

**Date**: 2026-04-04
**Location**: Carpentersville, IL (only location owned by client)
**URL**: https://southernbellespancakes.com/site/carpentersville-il/

---

## Restaurant Details

| Field | Value |
|-------|-------|
| **Full Name** | Southern Belle's Pancake House |
| **Address** | 152 S. Western Ave, Carpentersville, IL 60110 |
| **Phone** | (224) 699-9959 |
| **Hours** | Open 7 days/week, 6:00 AM – 3:00 PM |
| **Gaming Cafe** | 3:00 PM – 10:00 PM |
| **Evening Takeout/Delivery** | 3:00 PM – 8:00 PM (Carpentersville only) |
| **Patio** | Open |
| **Facebook** | facebook.com/southernbellescarpentersville |
| **Twitter/X** | @SBPancakes |
| **Toast Ordering URL** | https://order.toasttab.com/online/southern-belles-carpentersville |
| **Toast Name** | Southern Belles S. Western Ave |
| **Menu PDF** | [Southern-Belle-Menu-WEB_0425.pdf](./Southern-Belle-Menu-WEB_0425.pdf) |

### Other Locations (NOT owned by client — shared website only)

| Location | Address | Phone |
|----------|---------|-------|
| Yorkville | 56 E. School House Rd., IL 60560 | (630) 553-9977 |
| Plainfield | 15051 S. Van Dyke Rd., IL 60544 | (815) 267-7800 |
| Barrington | 210 S. Cook St., IL 60010 | (847) 387-4290 |

---

## Current Tech Stack

| Component | Technology |
|-----------|-----------|
| **CMS** | WordPress |
| **Theme** | The7 by Dream-Theme |
| **Page Builder** | Elementor |
| **Slider** | Slider Revolution |
| **Forms** | WPForms |
| **E-commerce** | WooCommerce (inactive?) |
| **POS / Online Ordering** | Toast |
| **Domain** | southernbellespancakes.com (likely GoDaddy registrar) |
| **Built by** | WebFish (webfishis.com) |
| **Analytics** | Google Tag Manager |

---

## Issues Found

### CRITICAL — Site is Broken

| # | Issue | Impact |
|---|-------|--------|
| 1 | **Carpentersville sub-page renders completely blank** — `/site/carpentersville-il/` shows a white page with only navigation and footer. No content visible. | Customers searching for this specific location see nothing. |
| 2 | **Toast online ordering is OFF** — "Online ordering is currently unavailable. Please contact the restaurant to place an order." | Lost revenue. Customers who click "Order Online" hit a dead end. |
| 3 | **Slider/hero images broken on Carpentersville page** — loading `dummy.png` placeholder files instead of real images. | Page looks unprofessional/broken. |
| 4 | **No WordPress admin access** — cannot fix any of the above without wp-admin credentials. | Blocks all improvements to current site. |

### MAJOR — Content & Functionality Gaps

| # | Issue | Impact |
|---|-------|--------|
| 5 | **No address displayed on Carpentersville page** — visitors can't find the restaurant. | Customers leave; bad for local SEO. |
| 6 | **No hours displayed on Carpentersville page** — visitors don't know when you're open. | Customers call instead of visiting; some give up. |
| 7 | **Menu is image-based (not text)** — the menu page renders the PDF as images. | Google can't index menu items. Screen readers can't read it. Terrible on mobile. |
| 8 | **Shared site with 3 other locations** — you only own Carpentersville but the website serves all 4. | Your page is buried; other locations' info may confuse your customers. |
| 9 | **Video Gaming page has no content** — just says "Video Gaming now available at our Carpentersville location!" with no details. | Wasted page; no gaming hours, rules, or descriptions. |
| 10 | **Main page has huge blank space** — scrolling past the hero reveals a large empty area before content appears. | Looks broken; visitors may leave. |

### SEO — Missing Fundamentals

| # | Issue | Impact |
|---|-------|--------|
| 11 | **No Restaurant/LocalBusiness structured data** (JSON-LD schema) | No rich results in Google (hours, rating, menu, address). |
| 12 | **No meta descriptions** on location pages | Google generates its own snippets, usually poorly. |
| 13 | **Menu not crawlable** — images, not HTML text | Google can't index "BoNuts", "Morning Wrecker", etc. |
| 14 | **No Open Graph / Twitter Card meta tags** | Links shared on social media look plain. |
| 15 | **NAP inconsistency** — address not shown on Carpentersville page but appears elsewhere | Hurts local search ranking. |
| 16 | **Hours typo** — "3:oo p.m" (lowercase 'o' instead of zero) in the about section | Looks unprofessional; may confuse search engines. |

### UX / Design

| # | Issue | Impact |
|---|-------|--------|
| 17 | **Contact form serves all 4 locations** — dropdown includes Yorkville, Barrington, Plainfield | Confusing for Carpentersville-only customers. |
| 18 | **"All locations" messaging everywhere** — "Our Patios at Barrington, Yorkville, Carpentersville, and Plainfield are open!" | Your customers don't care about other locations. |
| 19 | **Footer credits "Powered by WebFish"** | Takes space from your brand. |
| 20 | **No Google Maps embed** on Carpentersville page | Customers can't get directions easily. |
| 21 | **No Instagram link** — only Facebook and Twitter/X | Missing the most important social platform for restaurants. |
| 22 | **Credit card processing fee note on menu** — "additional % fee for credit card processing" | May deter customers; also may violate card network rules depending on implementation. |

---

## Menu Summary (from PDF, dated April 2025)

### Page 1 — Breakfast

| Category | Items |
|----------|-------|
| **Crepes** | Crepes, Cobbler, Nutella, Blintz |
| **Waffles** | "The Original", Sugared Pecan, Waffle Breakfast, Hot Honey Chicken & Waffle |
| **French Toast** | Plain & Simple, French Lady, Cinnamon Swirl, Caramelized Bread Pudding, Stuffed Strawberry, French Toast Overload |
| **Biscuit Craze** | BoNuts, Basket of Biscuits, Morning Wrecker, Stacked Biscuit, Country Style Biscuits & Gravy, The Dirty Bird, "Un-Porking Believable" Biscuit, Belly Buster Biscuit |
| **Pancakes** | Buttermilk, CinnaBomb, Belle's Bliss, Strawberry Cheesecake, The Woodsman, Banana Puddin' Brulee, 2x2x2, Camp-Fire |
| **Signature Skillets** | Garden, "The Debutante", Irishman's, Skirt Steak, Southern Belle's, Pork Popper, Pork Belly, Spanish, Hotlanta, Farmer's, Country-Time |
| **Omelettes** | Chicken, Salsa, Southern Belle's, Grumpy Goat, The Biscuit, Gouda, Vegetable |
| **Benedicts** | Country, Avocado Smashed Benny, Shamrock, Crabby, Green Acres, Eggs Benedict, Pimento |
| **Eggs & More** | 2 Eggs Any Style, Corned Beef Hash, Breakfast Sandwich, Belly Up, Corn Bread Sliders, Steak & Eggs, Fried Chicken & Eggs, Country Fried Steak & Eggs |

### Page 2 — Lunch, Specialties, Sandwiches

| Category | Items |
|----------|-------|
| **Lunchtime** | Half & Half, Country Platter, Roscoe's Catfish, Gumbo-laya (Spicy Stew) |
| **SB House Specialties** | Eggy-Waffle Sandwich, Georgia Catfish & Jalapeno Cheddar Grits, Chilaquiles, "South of the Border" Fried Chicken, Banana Pudding Parfait, Shrimp & Grits, Breakfast Tacos, Ranchero Breakfast Burrito, Brisket Bowl |
| **Between the Bread** | Cali Club, Fried Chicken, Reuben, Fried Green Pimento BLT, "Not Your Mom's Grilled Cheese", Honey Butter Chicken Sandwich, The Cubano, Avondale Chicken Sandwich, Tuna Melt, Hot Honey Chicken Thigh Sandwich, Nashville Hot Chicken Sandwich |
| **Burgers** | House Burger, The Melt |
| **Salads** | Blackened Chicken, Chopped Greek Chicken, Sugared Pecan, Texas Roadhouse, Country Cobb, Southern Shrimp, Autumn Bliss |
| **Wraps** | Baja, Goat Cheese, Sriracha Chicken, Crispy Chicken, Pesto Caprese |
| **Gluten Free** | GF Ancient Grain French Toast, GF Johnny Cakes, GF Gluten Free Crepes |
| **Vegan** | V GF Vegan Salsa Scrambler, V Vegan Oatmeal Pancakes |
| **Healthy** | Lo-Cal Scrambler, Avocado Toast, Best Bowl Oatmeal |
| **Sides** | Hash Browns, House Hash Browns, Corned Beef Hash, Fruit, Canadian Bacon, Ham off the Bone, Turkey Links, Sausage Links, Sausage Patties, Chicken Apple Cherry Links, Bacon, Fried Green Tomatoes, Bowl of Soup, Corn Bread, Toast (multiple types), Fries |

### Menu Notes
- Gratuity may be added to parties of 8+
- On weekends/holidays, seating limited to 90 minutes
- Additional % fee for credit card processing
- Inform server of allergies prior to ordering

---

## Media Mentions

- **WGN 9** — Lunchbreak: Apple Pancakes
- **FOX 32** — Breakfast Comfort Food

---

## Key Assets Found

| Asset | URL |
|-------|-----|
| Logo (blue, wide) | wp-content/uploads/2021/01/logo_350x86_blue.png |
| Logo (blue, square) | wp-content/uploads/2021/01/logo_406x100_blue.png |
| BoNuts hero slide | wp-content/uploads/revslider/intro-02-11/bonuts_slide-1024x8201.jpg |
| Benedict photo | wp-content/uploads/2020/12/benedict.jpg |
| Morning Wrecker photo | wp-content/uploads/2020/12/wrecker_raw-800x800.jpg |
| Skillet photo | wp-content/uploads/2020/12/skillet_01-800x800.jpg |
| Avocado Toast photo | wp-content/uploads/2020/12/avocado_toast-800x800.jpg |
| BoNuts photo | wp-content/uploads/2020/12/bonuts-780x780.jpg |
| Pancakes photo | wp-content/uploads/2020/12/pancakes-800x800.jpg |
| Menu PDF | wp-content/uploads/2025/04/Southern-Belle-Menu-WEB_0425.pdf |

---

## About Section Text (from main site)

> Here at Southern Belle's, we strive to provide you a wholesome breakfast & lunch. We promise to do our best to prepare your meal just the way you like it using the freshest ingredients seasonally available. Sit back and let us do the dishes!

---

## Recommendation

The current WordPress site is a shared multi-location site that you don't have admin access to. The Carpentersville page is broken. Toast ordering is off. The menu is images, not text.

**Recommended path: Build a standalone Carpentersville-only website** that you fully control, with:

1. Your menu as searchable HTML text (not images)
2. Toast ordering widget embedded and working
3. Google Maps, hours, address front and center
4. Restaurant schema markup for rich Google results
5. Mobile-first design optimized for local diners
6. Your own domain or subdomain you control

This gives you independence from the other locations and the WebFish-managed WordPress site.

---

## Open Questions for Client

1. **Millie's Pancakes** — you had milliespancakes.com open in a browser tab. What's the connection? Is this a rebrand, a sister restaurant, or unrelated?
2. **Toast admin** — you appear to be logged into Toast admin. Can you enable online ordering, or is there an issue with the Toast account?
3. **Domain** — do you want to keep using southernbellespancakes.com (shared with other locations) or get your own domain?
4. **WordPress admin** — can you get wp-admin credentials from WebFish or whoever manages the site?
5. **Photos** — do you have additional food/interior photos beyond what's on the current site?
6. **Instagram** — does the restaurant have an Instagram account?
7. **Google Business Profile** — is the Carpentersville listing claimed and managed?
