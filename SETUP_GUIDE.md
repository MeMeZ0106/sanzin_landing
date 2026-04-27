# Sanzin K-Store — Quick Setup & Deployment Guide

## ✅ What's Done Locally

Your repo is initialized with:
- ✅ SEO meta tags (description, robots, og tags, canonical)
- ✅ `robots.txt` (allows crawling, points to sitemap)
- ✅ `sitemap.xml` (ready for Search Console)
- ✅ GitHub Pages workflow (auto-deploys on push to `main`)
- ✅ All placeholders updated to: `https://MeMeZ0106.github.io/sanzin-landing/`
- ✅ Git initialized & first commit ready

---

## 🚀 Step 1: Push to GitHub

**Option A: Using GitHub CLI** (recommended, quickest)
```bash
gh repo create sanzin-landing --public --source=. --remote=origin --push
```

**Option B: Create repo manually, then push**
1. Go to https://github.com/new
2. Create a repository named `sanzin-landing`
3. Copy the HTTPS URL
4. Run these commands:

```bash
cd "c:\Users\user\Downloads\landingpage"
git remote add origin https://github.com/MeMeZ0106/sanzin-landing.git
git branch -M main
git push -u origin main
```

---

## 🔄 Step 2: Enable GitHub Pages (Auto-Deploy)

1. Go to `https://github.com/MeMeZ0106/sanzin-landing/settings/pages`
2. Under **Source**, select **Deploy from a branch**
3. Select **Branch: `gh-pages`** (the workflow creates this automatically)
4. Click **Save**
5. Wait ~1–2 minutes for the site to build
6. Your site will be live at: `https://MeMeZ0106.github.io/sanzin_landing/`

---

## 🔍 Step 3: Verify in Google Search Console

1. Go to https://search.google.com/search-console
2. Click **+ Create property**
3. Choose **URL prefix**, paste: `https://MeMeZ0106.github.io/sanzin_landing/`
4. Choose **HTML tag** verification method
5. Copy the `content` value from the provided meta tag (looks like: `abc123def456xyz789`)
6. Open `index.html` and replace:
   ```html
   <meta name="google-site-verification" content="REPLACE_WITH_GOOGLE_VERIFICATION_CODE">
   ```
   with:
   ```html
   <meta name="google-site-verification" content="abc123def456xyz789">
   ```
   (use your actual verification code)
7. Commit & push the change:
   ```bash
   git add index.html
   git commit -m "Add Google Search Console verification"
   git push
   ```
8. Wait ~30 seconds for deployment, then click **Verify** in Search Console

---

## 📋 Step 4: Submit Sitemap

1. In Search Console, open your property
2. Go to **Sitemaps** (left menu)
3. Enter: `https://MeMeZ0106.github.io/sanzin_landing/sitemap.xml`
4. Click **Submit**

---

## ✨ Step 5: Verify robots.txt & SEO

- Visit `https://MeMeZ0106.github.io/sanzin-landing/robots.txt` → should show "User-agent: *" with no "Disallow" rules
- Visit `https://MeMeZ0106.github.io/sanzin-landing/` and view source → confirm `<meta name="robots" content="index, follow">`
- Your canonical, OG tags, and JSON-LD are ready

---

## 📦 What You Have

| File | Purpose |
|------|---------|
| `index.html` | Landing page with SEO tags, verification placeholder |
| `robots.txt` | Allows crawling, points to sitemap |
| `sitemap.xml` | Indexed by Google |
| `script.js` | Interactivity (smooth scroll, button effects) |
| `styles.css` | Responsive design |
| `.github/workflows/deploy.yml` | Auto-deploys to gh-pages on push |
| `README.md` | Manual setup reference |
| `.gitignore` | Prevents OS/IDE files from being committed |

---

## 🎯 Summary

Once you push to GitHub:
1. **Site goes live** at `https://MeMeZ0106.github.io/sanzin-landing/` within ~1 min
2. **Google crawls** after Search Console verification
3. **Sitemap submitted** = faster indexing

No `noindex` tag, `robots.txt` allows crawling, canonical & OG tags present → ready for SEO! 🚀
