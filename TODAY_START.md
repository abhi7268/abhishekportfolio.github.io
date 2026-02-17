# Start Today (GitHub Deployment)

Use this checklist to get your site live **today** in about 30–45 minutes.

## 0) Prerequisites
- A GitHub account
- Git installed on your laptop
- This project opened in your terminal

## 1) Initialize and push to GitHub

Create an empty repository on GitHub first (for example: `abhishekportfolio`).

Then run:

```bash
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## 2) Turn on GitHub Pages

1. Open your repository on GitHub.
2. Go to **Settings → Pages**.
3. Set:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main`
   - **Folder**: `/ (root)`
4. Click **Save**.

## 3) Open your live link

After ~1–5 minutes, your site should be available at:

```text
https://<your-username>.github.io/<repo-name>/
```

## 4) Quick verification checklist

- Home page loads correctly.
- CSS styles are applied.
- JavaScript interactions in `script.js` work.
- No missing assets (404 errors in browser console).

## 5) Daily update workflow (from now on)

Whenever you change the site:

```bash
git add .
git commit -m "Update portfolio section"
git push
```

GitHub Pages will redeploy automatically.

## 6) Today’s finish line

You are done for today when all three are true:
- Code is pushed to GitHub main branch.
- GitHub Pages is enabled.
- Your public URL opens successfully on mobile + desktop.

---

If you want, tomorrow you can add:
- custom domain (`CNAME`)
- SEO meta tags
- GitHub Actions checks (HTML/CSS lint)
