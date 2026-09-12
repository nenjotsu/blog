# Trading Blog

Trading articles and instructions for running a Hugo website locally and publishing it on GitHub Pages (`github.io`).

**Current state:** this repository contains `less-is-more-trading.md`. A Hugo application, theme, and deployment workflow have not been created yet. Follow the one-time setup below to create the application in `blog/`.

## Install the tools

On Windows, install Git and Hugo Extended from PowerShell:

```powershell
winget install --id Git.Git -e
winget install --id Hugo.Hugo.Extended -e
```

Restart your terminal, then verify:

```powershell
git --version
hugo version
```

Use a recent Hugo release (0.158.0 or later for the project command below). Record the installed version so you can use the same version in the deployment workflow. For other platforms, see [Hugo installation](https://gohugo.io/installation/). The Windows package command is documented in [Hugo's Windows guide](https://gohugo.io/installation/windows/).

## One-time Hugo setup

Run these commands from this repository's root directory. Skip this section if `blog/hugo.toml` already exists; use the existing configuration and theme instead.

```powershell
hugo new project blog
git submodule add https://github.com/gohugo-ananke/ananke.git blog/themes/ananke
```

The repository already has Git initialized. Keep `blog/` inside this repository rather than initializing another Git repository there.

Edit the generated `blog/hugo.toml` to contain:

```toml
baseURL = 'https://YOUR_USERNAME.github.io/YOUR_REPOSITORY/'
locale = 'en-us'
title = 'Trading Blog'
theme = 'ananke'

[caches.images]
dir = ':cacheDir/images'
```

Replace the URL placeholders with your GitHub account and repository names. See the deployment section for the account-site URL option. This setup uses Ananke, the theme in the [official Hugo quick start](https://gohugo.io/getting-started/quick-start/).

Add these entries to a `.gitignore` file at the repository root:

```gitignore
/blog/public/
/blog/resources/_gen/
/blog/.hugo_build.lock
```

Keep the theme submodule and `.gitmodules` tracked. For an existing clone, download its recorded theme version with:

```powershell
git submodule update --init --recursive
```

## Add the article

From the repository root:

```powershell
Copy-Item -LiteralPath ./less-is-more-trading.md -Destination ./blog/content/posts/less-is-more-trading.md
```

Create `blog/content/posts/` first if it does not exist. At the very beginning of the copied file, insert:

```toml
+++
title = 'Less Is More: How I Learned to Simplify My Trading'
date = 2026-09-12T12:00:00+08:00
draft = true
+++
```

Remove the copied article's first `# Less Is More...` heading because the theme displays the title from front matter. Keep the original article at the repository root as the source document.

When ready to publish, change `draft` to `false`. A future publication date also prevents normal publication until that date is reached.

For subsequent articles, run from `blog/`:

```powershell
hugo new content content/posts/my-next-article.md
```


## Run locally

From the repository root:

```powershell
cd blog
hugo server -D
```

Open [http://localhost:1313/](http://localhost:1313/). Hugo reloads the page when content changes. `-D` includes drafts. Press **Ctrl+C** to stop the server.

Preview published content only:

```powershell
hugo server
```

Build production files locally, while still in `blog/`:

```powershell
hugo --gc --minify
```

The output is `blog/public/`. Confirm the home page and published article appear, and check navigation and styling. This command builds the site; it does not deploy it.

## Deploy to GitHub Pages

### 1. Create and connect the GitHub repository

Choose the address you want:

| Repository name | Website URL / `baseURL` |
| --- | --- |
| `YOUR_USERNAME.github.io` | `https://YOUR_USERNAME.github.io/` |
| `trading-blog` or another project name | `https://YOUR_USERNAME.github.io/YOUR_REPOSITORY/` |

Use the matching URL in `blog/hugo.toml`, including its trailing slash. The local `blog/` directory does **not** add `/blog/` to the published URL.

Create an empty public GitHub repository. From the local repository root, connect it if `origin` is not already configured:

```powershell
git remote -v
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

If `origin` already points to the intended repository, skip the add command.

### 2. Configure automated publishing

In the GitHub repository, open **Settings → Pages** and select **GitHub Actions** as the source.

Use the workflow from [Hugo's official GitHub Pages deployment guide](https://gohugo.io/host-and-deploy/host-on-github-pages/), saving it locally as `.github/workflows/hugo.yaml` at the **repository root**, alongside `blog/`. Make these adjustments before committing:

- Set `HUGO_VERSION` to the version used locally, without the leading `v`. If the theme requires Extended, use the matching `hugo_extended_${HUGO_VERSION}_linux-amd64.tar.gz` release archive in both download and extraction commands.
- Set `TZ` to `Asia/Manila`.
- Keep recursive submodule checkout so the Ananke theme is available.
- Set the push trigger to your publishing branch; the example uses `main`.
- Replace the build command with the following so Hugo reads the nested application:

```bash
hugo --source blog --gc --minify \
  --baseURL "${{ steps.pages.outputs.base_url }}/" \
  --cacheDir "${{ runner.temp }}/.cache/hugo"
```

- Set the upload-artifact step's `path` to `./blog/public` instead of `./public`.
- If you later add Hugo modules or Node dependencies inside `blog/`, update the workflow's dependency-file checks and installation directories to that folder too.

Keep the official workflow's Pages permissions, deployment job, and `github-pages` environment. The Pages-provided base URL handles account sites and project sites. Do not select branch-folder publishing or upload the Markdown source as the website.

### 3. Commit and publish

From the repository root, review the changes and commit the site, theme reference, and workflow:

```powershell
git status
git add README.md .gitignore .gitmodules blog .github/workflows/hugo.yaml less-is-more-trading.md
git commit -m "Set up Hugo trading blog and GitHub Pages deployment"
git push -u origin HEAD
```

Ensure the branch being pushed matches the workflow trigger. In GitHub's **Actions** tab, open the workflow run. After deployment succeeds, follow its deployment URL and verify the article, styling, and navigation.

Future commits pushed to that branch rebuild and publish the site automatically. Generated `blog/public/` files should remain untracked.

## Troubleshooting

| Problem | Check |
| --- | --- |
| `hugo` is not recognized | Restart the terminal after installation and check that Hugo is on `PATH`. |
| Missing configuration or blank site | Run from `blog/`, complete the one-time setup, and confirm the theme setting. |
| Theme not found | Run `git submodule update --init --recursive` at the repository root. |
| Article missing | Check its front matter, `draft` flag, date, and location under `blog/content/posts/`. |
| Port 1313 is occupied | Use `hugo server -D --port 1314` and visit the displayed URL. |
| Pages build cannot find the site | Confirm the build uses `--source blog` and uploads `./blog/public`. |
| Published styles or links fail | Check the project-name segment and trailing slash in the production base URL. |
| No deployment starts | Check the workflow branch trigger and that Pages uses GitHub Actions. |

These are setup instructions, not a record of a completed deployment. Run the local build and the GitHub workflow to validate your configured site.