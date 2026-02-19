# Blog - Claude Notes

Hugo blog using the PaperMod theme, deployed to GitHub Pages via GitHub Actions on push to `main`.

## Key commands

```bash
hugo server -D          # local preview with drafts
hugo new content posts/my-post.md  # create a new post
```

## Config

- `hugo.toml` — site config (update `baseURL` to match GitHub Pages URL before first deploy)
- Theme: `themes/PaperMod` (git submodule — run `git submodule update --init --recursive` if missing)

## Content

- Posts go in `content/posts/` as markdown files
- Front matter: `title`, `date`, `draft`, `tags`, `categories`
- Set `draft: false` to publish; `math: true` to enable KaTeX per-post

## Layouts

- `layouts/partials/` — custom partials (e.g. `extend_footer.html` loads Mermaid.js)
- `layouts/_default/_markup/` — render hooks

## Features

- LaTeX math via KaTeX (enabled globally in `hugo.toml` with `math = true`)
- Mermaid diagrams via fenced code blocks ` ```mermaid `
- Syntax highlighting: Monokai, line numbers enabled
