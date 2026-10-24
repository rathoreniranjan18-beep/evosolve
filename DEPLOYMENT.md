# Deploy EvoSolve with GitHub Pages

This repository is a static website, so you do not need a backend, domain, package manager, or build command.

## 1. Create the GitHub repository

1. Sign in to GitHub.
2. Click **New repository**.
3. Set the repository name to `evosolve`.
4. Choose **Public** if you want the project to be visible to recruiters and classmates.
5. Create the repository. If you are uploading the prepared project, do not initialize it with a README because this project already includes one.

## 2. Upload the files (beginner-friendly route)

1. Unzip `evosolve-github-ready.zip` on your computer.
2. Open the new `evosolve` folder.
3. In your GitHub repository, choose **Add file → Upload files**.
4. Upload the *contents* of the folder, including `index.html`, `README.md`, `.github`, and `docs`. Do not upload only the ZIP file.
5. Enter a commit message such as `Initial commit: publish EvoSolve`.
6. Click **Commit changes**.

## 3. Enable GitHub Pages

1. Open the repository's **Settings**.
2. Select **Pages** from the left menu.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select branch `main` and folder `/ (root)`.
5. Click **Save**.
6. Wait for the Pages deployment to complete. Refresh the Pages settings if needed; GitHub will show the published URL.

The URL normally looks like:

`https://YOUR-GITHUB-USERNAME.github.io/evosolve/`

The username and repository name in the URL must match your own account/repository.

## 4. Verify the live demo

- Open the published URL in a private/incognito window.
- Confirm the page loads and that Run, Pause, Step, Reset, objective selection, parameter controls, comparison, and CSV export work.
- Try it on a phone-sized viewport as well as desktop.
- Check the **Actions** tab if a workflow fails.
- Replace the placeholder live-demo URL in `README.md` with the real URL.

## 5. Recommended Git workflow (optional)

After installing Git, run these commands inside the project folder:

```bash
git init
git add .
git commit -m "Initial commit: EvoSolve genetic algorithm studio"
git branch -M main
git remote add origin https://github.com/YOUR-GITHUB-USERNAME/evosolve.git
git push -u origin main
```

Replace `YOUR-GITHUB-USERNAME` with your actual GitHub username. If Git says the remote already exists, inspect it with `git remote -v` instead of adding it a second time.

## Updating the live website

Edit the files, test locally, then commit and push:

```bash
git add .
git commit -m "Improve experiment controls"
git push
```

GitHub Pages will publish the new version after the deployment finishes.
