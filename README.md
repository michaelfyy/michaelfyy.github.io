# Personal Website

Minimal one-page academic website for a current undergraduate AI researcher.

## Edit

Update these details in `index.html` as they change:

- Research vision wording.
- Publication titles, venues, and paper links.
- Education details, GPA, and honors.
- Profile links and CV file.

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

Set **Source** to **Deploy from a branch**, then choose:

```text
Branch: main
Folder: / (root)
```

GitHub Pages will publish the root `index.html` file whenever you push to
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
