---
title: Publishing
---

# Publishing with GitHub Pages

This repository is ready for GitHub Pages. It uses Jekyll-compatible Markdown and a small custom layout.

## Create the GitHub Repository

The GitHub CLI is not installed on this machine, so create the remote repository through the GitHub website when ready.

Recommended repository name:

```text
SFA_Documentation
```

Recommended visibility:

```text
Public
```

Public is simplest for a free documentation site.

## Push From This Folder

From `P:\SFA_Documentation`, run:

```powershell
git remote add origin https://github.com/YOUR_USERNAME/SFA_Documentation.git
git branch -M main
git push -u origin main
```

Replace `YOUR_USERNAME` with the GitHub account or organization name.

## Enable Pages

Option A: Use GitHub Actions

1. Open the repository on GitHub.
2. Go to `Settings`.
3. Go to `Pages`.
4. Under `Build and deployment`, choose `GitHub Actions`.
5. The included workflow will publish the site after pushes to `main`.

Option B: Deploy from branch

1. Open the repository on GitHub.
2. Go to `Settings`.
3. Go to `Pages`.
4. Set source to `Deploy from a branch`.
5. Choose `main` and `/root`.

## Editing Directly on GitHub

Most content is plain Markdown. To edit a page:

1. Open the file in GitHub.
2. Click the pencil icon.
3. Make changes.
4. Commit changes.
5. Wait for Pages to rebuild.

## Custom Domain Later

If SFA gets a domain later, add it in GitHub Pages settings. GitHub will tell you what DNS records to create.
