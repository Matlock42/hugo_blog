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

## Adding article-specific images (Hugo best practices)

You have a few clean options:

1. **Leaf bundle per project (recommended)**
   - Put each project in `content/projects/<slug>/index.md`
   - Store that article's images in the same folder
   - Reference images in markdown with relative paths, e.g. `![alt](photo.jpg "Caption")`

2. **Use `/static/images/...` for shared/global assets**
   - Good for logos/icons reused across multiple pages
   - Less ideal for project-specific build photos

3. **Use a gallery shortcode for grouped image grids**
   - Wrap a block of markdown images with:

```md
{{< gallery >}}
![Alt](photo1.jpg "Caption")
![Alt](photo2.jpg "Caption")
{{< /gallery >}}
```

This repo now supports:
- A markdown image render hook that outputs semantic `<figure>` + optional `<figcaption>`
- A `gallery` shortcode for responsive image grids

## Build production output

```bash
hugo --minify
```

Generated files are written to `public/`.
