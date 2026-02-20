# hugo_blog

Hugo-based static site for publishing project writeups to a personal website.

## What changed

This repository now contains a working Hugo content and layout structure using a custom in-repo theme approach (no external theme dependency).

### Implemented

- Hugo config with project-specific permalink style:
  - Project detail pages build to `/projects/<slug>.html`
  - Project list page is `/projects/`
- Reusable template architecture:
  - Global base template
  - Navbar and footer partials
  - Reusable project card partial
  - Home page, projects list page, and project single page templates
- Project content model:
  - Standardized front matter fields (summary, description, cover image, tech stack, status)
  - `archetypes/projects.md` for quickly creating new project posts
- Starter content:
  - Home page content
  - Projects section intro
  - Example migrated project post (`Custom Mechanical Keyboard`)
- Basic custom styling and placeholder cover assets.

## Local development

1. Install Hugo (extended recommended).
2. Run:

```bash
hugo server -D
```

3. Open `http://localhost:1313`.

## Create a new project post

```bash
hugo new projects/my-new-project.md
```

Then fill in the generated front matter and content sections.

## Build production output

```bash
hugo --minify
```

Generated files are written to `public/`.
