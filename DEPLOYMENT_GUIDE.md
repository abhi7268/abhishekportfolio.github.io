# Deployment Guide (GitHub-First)

This repository is currently a static website (`index.html`, `styles.css`, `script.js`), so the easiest deployment is **GitHub Pages**.

If you later build the full-stack Next.js + AI app, use the "Full-Stack Path" section below.

---

## 1) Deploy this current static site to GitHub Pages

### Step 1: Push project to GitHub
1. Create a repository on GitHub.
2. In your local project:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<repo-name>.git
   git push -u origin main
   ```

### Step 2: Enable GitHub Pages
1. Open your GitHub repository.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main`
   - **Folder**: `/ (root)`
4. Click **Save**.

### Step 3: Wait for first deploy
- GitHub will generate a URL like:
  `https://<your-username>.github.io/<repo-name>/`
- It can take a few minutes on first deploy.

### Step 4: Verify assets load correctly
- Since this project uses relative file paths, it should work without changes.
- If images/fonts are added later, keep relative paths (or set absolute paths correctly).

### Step 5: Update workflow
For every change:
```bash
git add .
git commit -m "Describe update"
git push
```
GitHub Pages will auto-redeploy.

---

## 2) If you later build the full-stack app (Next.js + DB + AI)

GitHub Pages alone is not enough for server/API features.

Use this setup:
- **Code + CI/CD**: GitHub
- **Frontend + API runtime**: Netlify / Render / Railway
- **Database/Auth**: Supabase

### Minimal flow
1. Push Next.js project to GitHub.
2. Connect repo to Netlify/Render.
3. Add env vars (Supabase keys, AI API key).
4. Deploy and test routes/API.
5. Keep GitHub as source of truth; every push triggers redeploy.

---

## 3) Common issues checklist
- Pages not updating? Check **Actions** tab for failed build.
- 404 on assets? Confirm file paths and case sensitivity.
- Wrong homepage path? Confirm Pages branch/folder settings.
- Custom domain issue? Add `CNAME` and update DNS records.

