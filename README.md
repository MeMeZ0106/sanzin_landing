# Sanzin K-Store — Landing Page

This repository contains a simple static landing page. The project includes basic SEO metadata, a `robots.txt`, and a `sitemap.xml` to help search engines index the site.

Quick steps to publish to GitHub Pages and register with Google Search Console

1. Repository pushed to GitHub

- Your repository is at: `https://github.com/MeMeZ0106/sanzin_landing`
- The code has been committed and pushed to the `main` branch

2. Automatic deployment (GitHub Actions)

- This repo includes `.github/workflows/deploy.yml` which will deploy the repository root to the `gh-pages` branch using the `peaceiris/actions-gh-pages` action whenever you push to `main`.
- Make sure Actions are enabled in your repository settings. After the first successful run, your site will be available at:
  `https://MeMeZ0106.github.io/sanzin_landing/`

3. Update verification code

- Open `index.html` and find the line: `<meta name="google-site-verification" content="REPLACE_WITH_GOOGLE_VERIFICATION_CODE">`
- Replace `REPLACE_WITH_GOOGLE_VERIFICATION_CODE` with the verification string Google gives you (see next step).

4. Register and verify in Google Search Console

1) Go to https://search.google.com/search-console and add a new property
2) Choose **URL prefix** and paste: `https://MeMeZ0106.github.io/sanzin_landing/`
3) Choose **HTML tag** verification and copy the provided `content` value
4) Open `index.html`, find the `google-site-verification` meta tag, and replace `REPLACE_WITH_GOOGLE_VERIFICATION_CODE` with the code from step 3
5) Commit and push the change to `main`:
   ```bash
   git add index.html
   git commit -m "Add Google Search Console verification"
   git push
   ```
6) Wait ~30 seconds for deployment, then click **Verify** in Search Console

5. Submit your sitemap

- In Search Console, open your property, go to **Sitemaps** (left menu)
- Click **Add/Test sitemaps** and enter: `https://MeMeZ0106.github.io/sanzin_landing/sitemap.xml`
- Click **Submit**

6. Verify robots.txt and SEO

- Visit `https://MeMeZ0106.github.io/sanzin_landing/robots.txt` → confirm it shows `User-agent: *` with no `Disallow` rules
- Visit `https://MeMeZ0106.github.io/sanzin_landing/` and check the page source → confirm `<meta name="robots" content="index, follow">`
- Your canonical URL, OG tags, and JSON-LD are set and ready for indexing

Notes and next steps

- Replace the placeholder OG image with a real image hosted at your site for improved link previews.
- Consider adding per-page metadata if you add additional pages.
- Optionally connect a custom domain in the repository Pages settings and update canonical/verification accordingly.
