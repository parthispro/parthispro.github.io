# portfolio-static

Hyper-minimalist static portfolio. Pure HTML + CSS. No JavaScript, no frameworks,
no build step, no external requests.

## Structure

```
portfolio-static/
├── index.html                       # /whoami  (home)
├── writeups/
│   └── index.html                   # /writeups archive (links to disclosure repos)
├── projects/
│   └── index.html                   # /projects
├── styles.css                       # single shared stylesheet
├── favicon.svg                      # inline SVG, no image request
├── .nojekyll                        # serve files verbatim on GitHub Pages
└── README.md
```

## Deploy (GitHub Pages)

1. Create a repository and push the contents of this folder to its root.
2. Settings → Pages → Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. No build step runs; `.nojekyll` keeps every file path intact.

Add a writeup by adding one `<li>` to `writeups/index.html` pointing at its
disclosure repository.

## Constraints honored

- No JS frameworks, no CSS frameworks, no build step.
- No animations, transitions, or scroll effects.
- No analytics, tracking, cookies, or external fonts/requests.
- System monospace stack only; dark default; semantic HTML5; skip link and
  `aria-current` for accessibility; a restrictive Content-Security-Policy meta tag
  on every page.
