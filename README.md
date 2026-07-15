# Tomás Arias-Vergara — Academic Website

A clean, single-page academic site (plain HTML/CSS, no build step, no dependencies).

```
index.html                 → the website
style.css                  → styling
CV_Tomas_AriasVergara.pdf  → linked from the "Curriculum Vitae" button
assets/                    → put profile.jpg here (optional)
```

The photo: drop a square portrait named `assets/profile.jpg`. If it's missing, the page automatically falls back to your FAU photo, so the site works either way.

---

## How to publish it on GitHub Pages

You have two options. **Option A** puts the site at `https://tariasvergara.github.io` (your main personal page). **Option B** puts it at `https://tariasvergara.github.io/academic-website`. Option A is the natural choice for a personal academic homepage.

### Option A — main personal site (recommended)

1. **Create the repository.** Go to <https://github.com/new> and create a **public** repo named exactly:

   ```
   tariasvergara.github.io
   ```

   (Repo name must match your username `TAriasVergara` + `.github.io`. Don't add a README/license during creation — keep it empty.)

2. **Upload the files.** On the empty repo page, click **"uploading an existing file"**. Drag in `index.html`, `style.css`, `CV_Tomas_AriasVergara.pdf`, and the `assets` folder. Click **Commit changes**.

3. **Done.** GitHub Pages is automatic for `username.github.io` repos. Wait 1–2 minutes, then open:

   ```
   https://tariasvergara.github.io
   ```

### Option B — project site (if you want to keep the name free)

1. Create a public repo, e.g. `academic-website`.
2. Upload the same files.
3. Go to **Settings → Pages**. Under **Build and deployment → Source**, choose **Deploy from a branch**, select branch **`main`** and folder **`/ (root)`**, then **Save**.
4. After ~1 minute the site is live at `https://tariasvergara.github.io/academic-website`.

---

## Using Git from the command line (alternative to drag-and-drop)

If you prefer the terminal, from the folder containing these files:

```bash
git init
git add .
git commit -m "Initial academic website"
git branch -M main
git remote add origin https://github.com/TAriasVergara/tariasvergara.github.io.git
git push -u origin main
```

---

## Updating the site later

Edit `index.html` (all content lives there) and commit again — GitHub Pages redeploys automatically within a minute or so. To add a publication, copy an existing `<li>…</li>` inside the relevant `<div class="year-group">` and edit the text.

## Optional niceties

- **Custom domain** (e.g. `tomasarias.com`): Settings → Pages → Custom domain, then point a CNAME record at `tariasvergara.github.io` with your DNS provider.
- **Google Scholar auto-metrics**: the page already links to your Scholar and ORCID profiles for up-to-date citation counts.
- **Favicon**: add `favicon.ico` to the root and a `<link rel="icon" href="favicon.ico">` line in `index.html`.
