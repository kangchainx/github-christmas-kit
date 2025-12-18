# GitHub Profile Christmas Kit

[中文](README.zh-CN.md) | English

Christmas-only SVG icons for decorating your GitHub Profile README.  
This kit does not generate full profile designs or README layouts.

Live demo: https://kangchainx.github.io/github-christmas-kit/

## What’s inside

- `index.html`: single-file SPA (React 18 + Tailwind via CDN)
- `assets/svg/`: animated SVG icons (`viewBox="0 0 64 64"`)

## Use the icons

1. Open the demo and pick an icon.
2. Click `Markdown` / `URL` / `HTML` on the icon card to copy.
3. Paste into your GitHub Profile README (repo named `<username>/<username>`), commit, then refresh your profile.

### Base URL

- GitHub Pages base URL: https://kangchainx.github.io/github-christmas-kit/assets/svg/
- Example (Markdown):

```md
[![Santa Hat](https://kangchainx.github.io/github-christmas-kit/assets/svg/santa-hat.svg)](https://kangchainx.github.io/github-christmas-kit/)
```

## Run locally

### Option A: Open the single file

Open `index.html` directly in your browser (requires network access to load CDN assets).

Note: opening via `file://` may block clipboard access. For the best experience, use a local server:

```bash
python3 -m http.server 5173
# open http://localhost:5173/
```

### Option B: Vite (optional)

```bash
npm install
npm run dev
```

## Contributing guide

### Quick start

1. Create an SVG icon (keep it readable at small sizes), with a looping animation (`repeatCount="indefinite"`).
2. Put it into `assets/svg/` (kebab-case filename, e.g. `santa-hat.svg`).
3. Open a Pull Request.
   - Optional: add the icon entry to the `assets/icons.json` (icon manifest).

Tip: You can preview your SVG in the website’s “Contributor Lab” section before submitting.

### AI prompt template

```text
Create an animated SVG icon of a Santa Hat with viewBox="0 0 64 64" (transparent background). Style: bold, cute, and readable on a dark background.

Colors & structure:
- Red cap with a subtle vertical gradient (top #fb7185 → bottom #ef4444), use a linearGradient id="hatRed"
- Soft white brim (rounded rect/path), optional light gray highlight line
- White pom-pom (circle) on the tip

Looping animations (repeatCount="indefinite"):
- Float the whole hat up/down with animateTransform translate: "0 0; 0 -2; 0 0" dur="1.6s"
- Slight tilt with animateTransform rotate around (32,44): "-3 32 44; 3 32 44; -3 32 44" dur="1.6s"
- Pom-pom bounce by animating its radius: "6; 6.6; 6" dur="1.6s"

Return only the SVG code (no markdown). Keep it self-contained (no external assets). To create other icons in the same style, replace “Santa Hat” with another Christmas item.
```

### Icon guidelines

- Format: SVG
- Size: `viewBox="0 0 64 64"`
- Background: transparent
- Colors: prefer red (`#ef4444`, `#dc2626`), green (`#22c55e`, `#15803d`), white

## License

MIT — see `LICENSE`.
