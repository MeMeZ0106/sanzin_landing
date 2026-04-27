# Sanzin K-Store — Landing Page

This repository contains a simple static landing page. The project includes basic SEO metadata, a `robots.txt`, and a `sitemap.xml` to help search engines index the site.

Quick steps to publish to GitHub Pages and register with Google Search Console

1. Create a GitHub repository and push this code

```bash
git init
git add .
git commit -m "Initial commit"
# create repo on GitHub (use the website or gh CLI), then:
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git
git branch -M main
git push -u origin main
```

2. Automatic deployment (GitHub Actions)

- This repo includes `.github/workflows/deploy.yml` which will deploy the repository root to the `gh-pages` branch using the `peaceiris/actions-gh-pages` action whenever you push to `main`.
- Make sure Actions are enabled in your repository settings. After the first successful run, your site will be available at:
  `https://YOUR_USERNAME.github.io/REPO_NAME/` (replace placeholders)

3. Update placeholders

- Open `index.html` and replace `https://YOUR_DOMAIN_OR_USERNAME.github.io/REPO_NAME/` in the `og:url`, `canonical`, and JSON-LD with your actual site URL.
- Replace `REPLACE_WITH_GOOGLE_VERIFICATION_CODE` in the `google-site-verification` meta tag with the verification string Google gives you (see next step).

4. Register and verify in Google Search Console

1) Go to https://search.google.com/search-console and add a new property using the "URL prefix" option.
2) Choose HTML tag verification and copy the provided meta tag value (a string). Replace the placeholder in `index.html` (`google-site-verification`).
3) Commit and push the change to `main`, wait for your site to be deployed, then click "Verify" in Search Console.

Alternative verification: upload the verification file or use DNS verification for a custom domain.

5. Submit your sitemap

- In Search Console, open the property, go to "Sitemaps" and add:
  `https://YOUR_DOMAIN_OR_USERNAME.github.io/REPO_NAME/sitemap.xml`

6. Check `robots.txt`

- Visit `https://YOUR_DOMAIN_OR_USERNAME.github.io/REPO_NAME/robots.txt` and confirm it does not contain `Disallow: /` or any `noindex` directives. The included `robots.txt` allows all crawlers and points to the sitemap.

7. Verify indexing meta tag

- Make sure `index.html` does NOT include a `meta name="robots" content="noindex"` tag. This project explicitly sets `meta name="robots" content="index, follow"`.

Notes and next steps

- Replace the placeholder OG image with a real image hosted at your site for improved link previews.
- Consider adding per-page metadata if you add additional pages.
- Optionally connect a custom domain in the repository Pages settings and update canonical/verification accordingly.
