# Website Visitor Analytics

This static website cannot know how many people visit it by itself. To collect visit counts, the deployed site needs either hosting analytics or a small analytics script.

## What You Can Measure

- Page views: how many times pages are loaded.
- Unique visitors: an estimate of how many distinct people visited.
- Referrers: where visitors came from, such as Google, GitHub, LinkedIn, or direct links.
- Countries or regions: approximate location, depending on the analytics provider.
- Popular pages: useful if both the personal homepage and project pages are deployed.

## Recommended Options

### 1. Hosting Analytics

Use this if the website is hosted somewhere that already provides traffic stats.

- GitHub Pages: repository traffic can show views and referrers, but the data is limited and only visible to repository collaborators.
- Cloudflare Pages: includes privacy-friendly web analytics if enabled.
- Vercel or Netlify: can provide analytics depending on the plan and settings.

Best for: a quick overview without editing the site much.

### 2. Privacy-Friendly Analytics Script

Use this if you want a dashboard with clear visitor counts.

Good choices for a personal academic site:

- Plausible Analytics
- GoatCounter
- Umami
- Statcounter

Best for: seeing visits, referrers, countries, and popular pages in one place.

### 3. Google Analytics

Use this only if you specifically need Google Analytics. It is powerful, but heavier and less privacy-friendly than the simpler options above.

Best for: detailed marketing-style analytics.

## Where the Script Goes

Most analytics services give you a small `<script>` tag. Add it inside the `<head>` of each page you want to track, usually near the other scripts:

```html
<!-- Analytics script goes here after choosing a provider. -->
```

For this repository, the main pages to track are:

- `index.html`
- `projects/3dgstream/index.html`

## Suggested Setup

For this site, I would use a privacy-friendly tracker such as Plausible, GoatCounter, or Umami. After creating an account/project, copy the script they provide into the `<head>` of `index.html` and `projects/3dgstream/index.html`.

Then check the analytics dashboard after sharing the website link on:

- GitHub profile
- LinkedIn
- CV
- paper/project pages
- email signature

## Important Note

Analytics starts collecting data only after the tracker is added and the updated site is deployed. It cannot recover exact historical visitor counts from before tracking was enabled.
