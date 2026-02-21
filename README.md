# E SPORT CMS & Static Site

This project is a Jekyll-based static site with a built-in client-side CMS for managing content via the GitHub REST API.

## Features

- **Frontend**: Jekyll-based grid layout for E-Sports news.
- **CMS**: `cms.html` allows you to manage site settings and publish posts directly from the browser.
- **GitHub Integration**: Uses GitHub API to commit files directly to your repository.

## Setup Instructions

1. **Deploy to GitHub**:
   - Push this entire repository to GitHub.
   - Go to **Settings** > **Pages**.
   - Select **Source**: `Deploy from a branch` (main).
   - Click **Save**.

2. **Generate a Personal Access Token (PAT)**:
   - Go to GitHub Settings > Developer settings > Personal access tokens > Tokens (classic).
   - Generate a new token with `repo` scope.
   - Copy the token.

3. **Use the CMS**:
   - Navigate to `https://<your-username>.github.io/<repo-name>/cms.html`.
   - Enter your GitHub Username, Repository Name, and the PAT.
   - Click **Save & Connect**.

4. **Publish Content**:
   - Use the "New Post" section to create content.
   - The CMS will upload images to `assets/images/` and create posts in `_posts/`.
   - GitHub Pages will automatically rebuild your site within seconds.

## Local Development

To preview the CMS locally:
```bash
npm install
npm run dev
```
Open `http://localhost:3000/cms.html`.

*Note: The `index.html` page uses Jekyll Liquid tags and will not render correctly in a local Vite environment. It requires the GitHub Pages Jekyll build process.*
