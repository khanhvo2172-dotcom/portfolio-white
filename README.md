# Portfolio White

Vo Van Khanh’s portfolio with two themes in one shared page: white and blue (`#1268d5`) in light mode, and the original blue gradient design in dark mode.

The navigation includes a keyboard-accessible theme button. First visits follow the device color preference; a manual selection is remembered in local storage. The chosen theme is applied before the page renders. Theme switching does not reset project filters, expanded details, or the SEO workflow.

This version preserves the approved content, typing effect, section and project animations, company logo carousel, project filters, and automatic SEO workflow tour.

## Files

- `index.html` — complete website, including styles, component logic, and bundled runtime/fonts.
- `assets/` — local illustrations and company/tool logos.
- `vercel.json` — caching configuration for Vercel.

## Run locally

From the repository root:

```sh
python -m http.server 8767
```

Open http://localhost:8767/.

## Hosting

This is a static site. Serve the repository root; no build command or dependency installation is required. It can be imported as a separate Vercel project.

## Editing

The page template is JSON encoded inside the `script[type="__bundler/template"]` element in `index.html`. Decode it before editing, then encode it back. Theme colors use CSS custom properties on `:root` and `:root[data-theme="dark"]`, with scoped light-theme refinements. Assets use relative paths, so this repository runs independently of the original portfolio.
