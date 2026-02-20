# TankPro Kenya — Claude Code Project Guide

## Project Overview
A static, SEO-optimized website for **TankPro Kenya**, a professional water tank cleaning company operating across Nairobi and Kenya. The site is built as a single-page HTML file with inline CSS and JS — no frameworks, no build tools.

---

## Brand Colors (from logo)
| Token | Hex | Usage |
|-------|-----|-------|
| `--navy` | `#0B2545` | Primary text, dark sections, footer |
| `--blue` | `#0077C8` | Primary accent, buttons, links |
| `--blue-light` | `#5DADE2` | Gradients, secondary accents |
| `--blue-pale` | `#E8F4FD` | Backgrounds, icon containers |
| `--orange` | `#F5841F` | CTA buttons, highlights, badges |
| `--green` | `#2D7D3A` | Success indicators, eco-messaging |

---

## File Structure
```
tankpro-kenya/
├── index.html          # Main website (all-in-one HTML/CSS/JS)
├── assets/
│   ├── logo.png        # TankPro Kenya logo
│   ├── og-image.jpg    # Open Graph social sharing image (1200x630)
│   └── favicon.ico     # Favicon
├── sitemap.xml         # SEO sitemap
├── robots.txt          # Search engine crawl rules
└── CLAUDE_CODE.md      # This file
```

---

## Tech Stack & Tools Needed

### Core
- **HTML5** — Semantic markup with ARIA attributes
- **CSS3** — Custom properties, Grid, Flexbox, animations, `@media` queries
- **Vanilla JS** — Intersection Observer, scroll effects, FAQ accordion

### Fonts
- **Playfair Display** (headings) — via Google Fonts
- **DM Sans** (body) — via Google Fonts

### No Dependencies
This is a zero-dependency static site. No npm, no build tools, no frameworks.

---

## SEO Implementation Checklist

### On-Page SEO (Already Done)
- [x] Semantic HTML5 (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`)
- [x] Single H1 tag with target keyword
- [x] Descriptive H2/H3 hierarchy
- [x] Meta title (under 60 chars, includes primary keyword)
- [x] Meta description (under 160 chars, includes CTA)
- [x] Canonical URL
- [x] Open Graph & Twitter Card meta tags
- [x] Geo-targeting meta tags for Kenya
- [x] `lang="en"` on `<html>`
- [x] ARIA labels on navigation and interactive elements

### Structured Data (Already Done)
- [x] `LocalBusiness` schema with address, phone, hours, geo
- [x] `FAQPage` schema for FAQ section
- [x] `areaServed` covering major Kenyan cities

### Still Needed
- [ ] **Create `sitemap.xml`** — Submit to Google Search Console
- [ ] **Create `robots.txt`** — Allow all crawlers
- [ ] **Create `favicon.ico`** and touch icons from logo
- [ ] **Create OG image** (1200x630) for social sharing
- [ ] **Add actual logo image** to replace emoji placeholder in nav
- [ ] **Google Analytics / Tag Manager** — Add tracking snippet
- [ ] **Google Search Console** verification meta tag
- [ ] **Google Business Profile** — Set up and link

---

## Content Keywords (Kenya Market)

### Primary Keywords
- water tank cleaning Kenya
- tank cleaning Nairobi
- water tank cleaning services
- professional tank cleaning Kenya

### Secondary Keywords
- water tank disinfection Nairobi
- tank cleaning cost Kenya
- water storage cleaning
- tank sanitization services
- water tank maintenance Kenya
- clean water tank Nairobi

### Long-Tail Keywords
- how much does tank cleaning cost in Nairobi
- best water tank cleaning company Kenya
- water tank cleaning near me
- how often to clean water tank Kenya
- water tank cleaning services Westlands
- commercial water tank cleaning Nairobi

### Local SEO Targets
Include area names throughout content: Karen, Westlands, Kilimani, Kileleshwa, Lavington, Runda, Langata, South B, Eastlands, Mombasa, Kisumu, Nakuru, Eldoret, Thika, Machakos

---

## Deployment Options

### Option 1: GitHub Pages (Free)
```bash
git init
git add .
git commit -m "Initial TankPro Kenya website"
git remote add origin https://github.com/username/tankpro-kenya.git
git push -u origin main
# Enable GitHub Pages in repo settings → Source: main branch
```

### Option 2: Netlify (Free)
```bash
# Drag and drop the folder to netlify.com/drop
# Or connect GitHub repo for auto-deploy
```

### Option 3: Vercel (Free)
```bash
npx vercel --prod
```

### Option 4: Kenyan Hosting (Recommended for .co.ke domain)
- **Truehost Kenya** — Local hosting with .co.ke domain
- **Safaricom Cloud** — Enterprise hosting
- **Kenya Web Experts** — Budget-friendly local host

---

## Post-Launch SEO Tasks

1. **Submit sitemap** to Google Search Console
2. **Create Google Business Profile** with consistent NAP (Name, Address, Phone)
3. **List on Kenyan directories**: Yellow Pages Kenya, Business List Kenya, Mocality
4. **Build backlinks** from: Kenyan business directories, local blogs, real estate sites
5. **Set up Google Analytics 4** for tracking
6. **Add blog section** for content marketing (e.g., "Signs Your Water Tank Needs Cleaning", "Water Tank Cleaning Cost in Kenya 2026")
7. **Enable HTTPS** (SSL certificate) — critical for SEO ranking
8. **Optimize for mobile Core Web Vitals** — already lightweight, verify with PageSpeed Insights
9. **Set up WhatsApp Business** with auto-replies
10. **Create social media accounts** and link back to website

---

## Customization Guide

### To update contact info:
Search and replace these dummy values in `index.html`:
- Phone: `0712 345 678` / `+254712345678`
- Email: `info@tankprokenya.co.ke`
- Address: `Moi Avenue, Suite 12, Nairobi`
- WhatsApp link: `https://wa.me/254712345678`
- Domain: `www.tankprokenya.co.ke`

### To add the real logo:
1. Place logo file in `assets/logo.png`
2. Replace the `.logo-icon` div in nav with: `<img src="assets/logo.png" alt="TankPro Kenya Logo" width="40" height="40">`

### To add Google Analytics:
```html
<!-- Add before closing </head> tag -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## Supporting Files to Create

### robots.txt
```
User-agent: *
Allow: /
Sitemap: https://www.tankprokenya.co.ke/sitemap.xml
```

### sitemap.xml
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemapindex.org/schemas/sitemap/0.9">
  <url>
    <loc>https://www.tankprokenya.co.ke/</loc>
    <lastmod>2026-02-20</lastmod>
    <changefreq>monthly</changefreq>
    <priority>1.0</priority>
  </url>
</urlset>
```

---

## Performance Notes
- **No external JS frameworks** — fastest possible load
- **Inline CSS** — single HTTP request, no render-blocking
- **Google Fonts** with `preconnect` — optimized font loading
- **Intersection Observer** for scroll animations — no scroll event listeners
- **CSS-only animations** where possible — GPU-accelerated
- **Responsive images** — use `loading="lazy"` when adding images
- Target: **95+ PageSpeed score** on mobile and desktop
