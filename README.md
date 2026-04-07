# Huddon Petroleum Consulting — Website

Premium informational website for Huddon Petroleum Consulting.

## Deploy to Vercel

### Option A: Vercel CLI (fastest)

```bash
# 1. Install Vercel CLI (if not already)
npm i -g vercel

# 2. From this project directory, run:
vercel

# 3. Follow the prompts:
#    - Link to existing project? → No (first time) or Yes (updates)
#    - Project name? → huddon-consulting
#    - Framework? → Other
#    - Build command? → (leave empty, press Enter)
#    - Output directory? → . (just a dot)

# 4. Deploy to production:
vercel --prod
```

### Option B: Vercel Dashboard (GitHub)

1. Push this folder to a GitHub repository
2. Go to [vercel.com/new](https://vercel.com/new)
3. Import the GitHub repo
4. Settings will auto-detect from `vercel.json`:
   - **Framework Preset**: Other
   - **Build Command**: (empty)
   - **Output Directory**: `.`
5. Click **Deploy**

### Option C: Drag & Drop

1. Go to [vercel.com/new](https://vercel.com/new)
2. Drag this entire project folder onto the page
3. Vercel will detect `vercel.json` and deploy

## Custom Domain Setup

After deploying:

1. Go to your Vercel project → **Settings** → **Domains**
2. Add `huddonconsulting.com` and `www.huddonconsulting.com`
3. Vercel will give you DNS records to set:
   - **A record**: `76.76.21.21` for `huddonconsulting.com`
   - **CNAME record**: `cname.vercel-dns.com` for `www.huddonconsulting.com`
4. Update these DNS records at your domain registrar
5. Vercel auto-provisions SSL certificates

## File Structure

```
huddon-site/
├── index.html          ← Main page (all sections)
├── base.css            ← CSS reset & foundation
├── style.css           ← Design tokens & components
├── vercel.json         ← Vercel deployment config
├── robots.txt          ← Search engine crawl rules
├── sitemap.xml         ← Sitemap for SEO
├── .gitignore
├── README.md
└── assets/
    ├── favicon-32.png
    ├── favicon-192.png
    ├── apple-touch-icon.png
    ├── og-image.png    ← Social sharing image (1200x630)
    └── og-image.svg    ← Source for OG image
```

## SEO Configuration

All SEO settings from the current Wix site have been preserved:
- Title tag (same format)
- Meta description (same copy)
- Open Graph tags (og:title, og:description, og:url, og:site_name, og:type)
- Twitter Card tags (summary_large_image)
- Google Search Console verification
- Bing Webmaster verification
- Canonical URL
- robots.txt (same crawl rules)
- Sitemap

**Improvements over the current Wix site:**
- Added `og:image` and `twitter:image` (was missing)
- Added `ProfessionalService` JSON-LD schema (was only generic `WebSite`)
- Includes address, phone, email, service areas in structured data
