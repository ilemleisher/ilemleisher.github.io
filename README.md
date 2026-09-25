# Site scaffold

Static site: `index.html` (research/resume), `blog/`, `art/`. No build step —
just HTML/CSS. Edit the placeholder text/links directly in each file.

## File map
```
index.html          Homepage (bio, publications, projects, experience)
blog/index.html      Blog post list
blog/post-template.html   Copy this for each new post
art/index.html        Image gallery
css/style.css        All styling — colors/fonts/spacing are CSS variables at the top
assets/              Put images here
```

## Publish on GitHub Pages

1. **Create the repo.** On GitHub, click "New repository."
   - If you want it at `https://yourusername.github.io` (root of your account), name the repo exactly `yourusername.github.io`.
   - If you want it at `https://yourusername.github.io/some-name`, name the repo `some-name` — anything works.

2. **Push these files.** From this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/yourusername/REPO-NAME.git
   git push -u origin main
   ```

3. **Turn on Pages.** In the repo on GitHub: Settings → Pages → under
   "Build and deployment," set Source to "Deploy from a branch," branch
   `main`, folder `/ (root)`. Save.

4. **Wait ~1 minute**, then visit the URL GitHub shows on that same Pages
   settings page (it'll be `yourusername.github.io` or
   `yourusername.github.io/REPO-NAME`).

Any future push to `main` redeploys automatically — no extra steps.

## Custom domain (optional)

If you own a domain: add a `CNAME` file at the repo root containing just
your domain (e.g. `yourname.com`), then point your domain's DNS at GitHub
per [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).
