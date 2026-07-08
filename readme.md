# my-dev-blog

Personal dev notes blog, hosted on GitHub Pages.

## Setup (one-time)

1. Create a new repo on GitHub — name it anything (e.g. `dev-blog`)
2. Push this folder to it:
   ```bash
   git init
   git add .
   git commit -m "init blog"
   git remote add origin https://github.com/YOUR_USERNAME/dev-blog.git
   git push -u origin main
   ```
3. Go to the repo on GitHub → **Settings → Pages**
4. Under **Source**, select `Deploy from a branch` → branch: `main` → folder: `/ (root)`
5. Hit **Save** — your site will be live at:
   ```
   https://YOUR_USERNAME.github.io/dev-blog/
   ```

## Adding a new post

1. Copy `posts/claude-code-artifacts.html` as a template
2. Rename it to `posts/your-post-slug.html`
3. Update the title, content, and meta description inside the file
4. Add a new `<a class="post-card">` block in `index.html` pointing to `posts/your-post-slug.html`
5. Commit and push — GitHub Pages auto-deploys in ~30 seconds

## Structure

```
dev-blog/
├── index.html              # Homepage — lists all posts
├── assets/
│   └── style.css           # Shared styles (fonts, header, footer, tokens)
├── posts/
│   └── claude-code-artifacts.html   # Post 1
└── README.md
```

## Updating styles

All visual design lives in `assets/style.css`. Every post links to it via `../assets/style.css` so a single edit updates the whole site.
