# Yellowstone 1-Day Itinerary

A shareable web page for a 1-day Yellowstone itinerary based out of West Yellowstone.

Every push to `main` automatically deploys to GitHub Pages via the included Actions workflow.

## Deploy to GitHub Pages

### 1. Create a new GitHub repository

Go to [github.com/new](https://github.com/new) and create a new **public** repository (e.g. `yellowstone-trip`). Leave it empty — don't initialize with a README.

### 2. Push these files

```bash
git init
git add .
git commit -m "Add Yellowstone itinerary"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```

Replace `YOUR_USERNAME` and `YOUR_REPO_NAME` with your GitHub username and repository name.

### 3. Set Pages source to GitHub Actions

1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (in the left sidebar)
3. Under **Source**, select **GitHub Actions** (not "Deploy from a branch")
4. Click **Save**

The workflow at `.github/workflows/deploy.yml` will now run on every push to `main` and deploy the site automatically.

### 4. Share the link

After the first workflow run completes (check the **Actions** tab), your site will be live at:

```
https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/
```

## Files

| File | Purpose |
|------|---------|
| `index.html` | The itinerary page |
| `.nojekyll` | Tells GitHub not to process the site with Jekyll |
| `.github/workflows/deploy.yml` | GitHub Actions workflow — deploys on every push to `main` |
| `README.md` | This file |
