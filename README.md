# Claude.do

This is the web repo for Claude.do.

## App

- `apps/site` - the Astro site for `https://claude.do`
- `/` - landing page
- `/blog` - blog index
- `/blog/[slug]` - blog posts

The site is still arranged as an npm workspace so more apps or shared packages can be added later without moving the existing site again.

## Commands

Run all commands from the repo root unless noted otherwise.

| Command | Action |
| :-- | :-- |
| `npm install` | Install workspace dependencies |
| `npm run dev` | Start the site app |
| `npm run build` | Build every workspace |
| `npm run build:site` | Build only `apps/site` |
| `npm run preview` | Preview the site build |

## Content

Blog posts live in `apps/site/src/content/blog`.

Use the file name format:

```text
YYYY-MM-DD-post-title.md
```

The landing page previews the newest posts from the same Astro content collection that powers `/blog`.

## Deployment

The Astro site is configured for static output. Deployment config lives with the app:

- `apps/site/netlify.toml`
- `apps/site/wrangler.toml`

The intended public URL structure is:

- `https://claude.do`
- `https://claude.do/blog`
