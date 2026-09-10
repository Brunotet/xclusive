# Xclusive Luxury — coming soon site

## What's in here
- `index.html` — the coming soon page
- `404.html` — matching not-found page
- `robots.txt` / `sitemap.xml` — so Google can crawl and index the site
- `site.webmanifest`, `favicon.svg`, `favicon.ico`, `apple-touch-icon.png`, `icons/` — icons for browser tabs, bookmarks and home-screen shortcuts
- `og-image.png` — the image shown when the link is shared on WhatsApp/socials
- `CNAME` — tells GitHub Pages to serve this on xclusiveluxury.co.za

## Before you push
Edit `hello@xclusiveluxury.co.za` in `index.html` to your real inbox if that address isn't live yet.

## Push to Brunotet/xclusive
```bash
cd xclusive-site
git init
git add .
git commit -m "coming soon page"
git branch -M main
git remote add origin https://github.com/Brunotet/xclusive.git
git push -u origin main
```

## GitHub Pages settings
Repo → Settings → Pages → Source: `main` branch, `/ (root)` folder → set custom domain to `xclusiveluxury.co.za` → wait for DNS check to pass → tick "Enforce HTTPS".

## Cloudflare DNS (dash.cloudflare.com → xclusiveluxury.co.za → DNS → Records)
Delete the current A record (185.27.134.225), then add:

| Name | Type | Content | Proxy |
|---|---|---|---|
| xclusiveluxury.co.za | A | 185.199.108.153 | DNS only |
| xclusiveluxury.co.za | A | 185.199.109.153 | DNS only |
| xclusiveluxury.co.za | A | 185.199.110.153 | DNS only |
| xclusiveluxury.co.za | A | 185.199.111.153 | DNS only |
| www | CNAME | Brunotet.github.io | DNS only |

Leave the MX, TXT and verification records untouched — mail flow isn't affected.

## Once you have real content
Swap out the copy and images in `index.html`, and update `sitemap.xml` if you add more pages (e.g. `/shop`, `/about`).
