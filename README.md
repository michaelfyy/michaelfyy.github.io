# Personal Website

Minimal one-page academic website for a current undergraduate AI researcher.

## Edit Before Publishing

Update these placeholders in `index.html`:

- `Michael` / page title, if you want your full name displayed.
- University, major, graduation year, and coursework.
- Research vision wording.
- Paper/project titles, collaborators, and links.
- Google Scholar and CV links.
- Replace `assets/profile-placeholder.svg` with a headshot if you have one.

## GitHub Pages Deployment

For a personal GitHub Pages site, create a public repository named:

```text
michaelfyy.github.io
```

Then push this folder to that repository:

```bash
git init
git add .
git commit -m "Present a minimal AI research identity online" \
  -m "The site is intentionally static so GitHub Pages can serve it without a build step. The first version prioritizes a concise research profile, editable placeholder papers, and clear deployment instructions." \
  -m "Constraint: GitHub Pages requires index.html at the deployed artifact root." \
  -m "Confidence: high" \
  -m "Scope-risk: narrow" \
  -m "Tested: Opened through a local static server." \
  -m "Not-tested: Live GitHub Pages deployment before the repository exists on GitHub."
git branch -M main
git remote add origin https://github.com/michaelfyy/michaelfyy.github.io.git
git push -u origin main
```

In GitHub, open the repository and go to:

```text
Settings -> Pages -> Build and deployment
```

Set **Source** to **GitHub Actions**. The workflow in
`.github/workflows/pages.yml` will deploy the static site whenever you push to
`main`.

The site will be available at:

```text
https://michaelfyy.github.io
```

## Local Preview

You can open `index.html` directly in a browser. If you prefer a local server:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.
