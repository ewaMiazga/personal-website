# Ewa Miazga Website

This repository contains two related static pages:

- `index.html` - the personal homepage.
- `projects/3dgstream/index.html` - the 3DGStream project page.

The root `index.html` stays at the top level so GitHub Pages and similar static hosts can serve it as the homepage.

## Editing Guide

### Personal Website

Edit:

- Homepage content: `index.html`
- Homepage styling: `static/css/personal-site.css`
- Homepage navigation behavior: `static/js/personal-site.js`
- Personal images, CV, logos, and thumbnails: `assets/`

Useful homepage sections in `index.html`:

- Hero/profile: search for `personal-hero`
- News: search for `id="news"`
- Publications: search for `id="publications"`
- Education: search for `id="education"`
- Experience: search for `id="experience"`
- Former projects: search for `id="projects"`

### 3DGStream Project Page

Edit:

- Project page content: `projects/3dgstream/index.html`
- Project page styling: `static/css/project-page.css`
- Project images: `projects/3dgstream/results/`
- Project teaser videos: `projects/3dgstream/teaser-videos/`
- Project comparison videos: `projects/3dgstream/carousel-videos/`
- Project banner image: `projects/3dgstream/banner/`
- Local project report copy: `projects/3dgstream/CV_lab_Report-3.pdf`

The project page uses paths relative to `projects/3dgstream/index.html`, so files inside the same project folder can be referenced directly, for example:

```html
<img src="results/eval-graphs.png" alt="Quantitative Evaluation Graph">
<source src="teaser-videos/example.mp4" type="video/mp4">
```

Shared files from the repository root need `../../`, for example:

```html
<link rel="stylesheet" href="../../static/css/project-page.css">
<img src="../../assets/epfl-logo.png" alt="EPFL Logo">
```

## Project Structure

```text
.
├── index.html
├── assets/
├── docs/
├── projects/
│   └── 3dgstream/
│       ├── index.html
│       ├── banner/
│       ├── carousel-videos/
│       ├── results/
│       ├── teaser-videos/
│       └── unused-videos/
└── static/
    ├── css/
    └── js/
```

## Visitor Analytics

See `docs/visitor-analytics.md` for notes on collecting visitor counts.
