# How to Enable GitHub Pages - Step by Step

Your repository is ready on GitHub, but **GitHub Pages is not enabled yet**. That's why Google Search Console says the sitemap is invalid - the site isn't live yet.

Follow these exact steps:

---

## 🔧 Enable GitHub Pages

### Step 1: Log into GitHub
Make sure you're logged into GitHub as **MeMeZ0106**

### Step 2: Go to Repository Settings
Open this URL in your browser:
```
https://github.com/MeMeZ0106/sanzin_landing/settings/general
```

### Step 3: Scroll Down to "Pages"
On the left sidebar, you should see:
- General
- Collaborators  
- **Pages** ← Click this

OR just open directly:
```
https://github.com/MeMeZ0106/sanzin_landing/settings/pages
```

### Step 4: Select "Deploy from a branch"
Under **"Build and deployment"** section:

1. You should see a dropdown labeled **"Source"**
2. Click it and select: **"Deploy from a branch"**

### Step 5: Configure Branch
After selecting "Deploy from a branch", new options appear:

1. **Branch dropdown** - Select: **`gh-pages`**
2. **Folder dropdown** - Select: **`/ (root)`**

### Step 6: Click "Save"
Click the blue **"Save"** button

### Step 7: Wait for Deployment
- The page will refresh
- Wait 1-2 minutes
- You'll see a **blue banner** at the top saying:
  ```
  ✅ Your site is live at https://MeMeZ0106.github.io/sanzin_landing/
  ```

---

## ✅ Verify It Works

Once enabled:

1. **Visit your live site:**
   ```
   https://MeMeZ0106.github.io/sanzin_landing/
   ```
   You should see your landing page!

2. **Check robots.txt:**
   ```
   https://MeMeZ0106.github.io/sanzin_landing/robots.txt
   ```
   Should show sitemap location

3. **Check sitemap.xml:**
   ```
   https://MeMeZ0106.github.io/sanzin_landing/sitemap.xml
   ```
   Should show XML content

---

## 🔍 Then: Retry Sitemap Submission

Once Pages is enabled and the blue banner appears:

1. Go back to Google Search Console
2. Go to **Sitemaps** section
3. Try submitting the sitemap again:
   ```
   https://MeMeZ0106.github.io/sanzin_landing/sitemap.xml
   ```
4. It should now accept it ✅

---

## ⚠️ If You Can't Access Settings Page

If the settings page shows 404 or isn't loading:

1. **Make sure you're logged in**: Click your profile icon (top right) and confirm you're logged in as **MeMeZ0106**

2. **Try this simpler URL first**:
   ```
   https://github.com/MeMeZ0106/sanzin_landing
   ```

3. **Look for Settings link**: On the repo page, there should be a **⚙️ Settings** button in the navigation (usually between "Projects" and "Security")

4. **Click on Pages** in the left sidebar

---

## 📱 Screenshots Reference

The Pages settings should look like:
```
Build and deployment
├─ Source
│  └─ [Dropdown: "Deploy from a branch" selected]
│
├─ Branch
│  └─ [Dropdown: "gh-pages" selected] / (root)
│
└─ [Save button]
```

---

**That's it! Once Pages is enabled, your site goes live and Google can validate your sitemap.** 🚀
