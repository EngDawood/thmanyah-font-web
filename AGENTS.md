# AGENTS.md

Guidance for AI coding agents working in this repository.

## Project overview

`@dawod/thmanyah-font-web` is a **static, community-maintained web font package** for the Thmanyah (ثمانية) Arabic font family — three families (Sans, Serif Display, Serif Text), five weights each (300 / 400 / 500 / 700 / 900).

There is **no build step, no bundler, no framework, and no JavaScript**. The product is plain CSS files whose `@font-face` rules point at woff2 files served through the jsDelivr CDN directly from this GitHub repository. The font is designed and owned by [Thmanyah](https://thmanyah.com); this repo only repackages it for convenient web use.

Key facts:

- npm package name: `@dawod/thmanyah-font-web`, entry points `index.css` (`main` / `style`).
- Published artifact is **CSS only** — see `package.json` `files`: `index.css`, `sans.css`, `serif-display.css`, `serif-text.css`. Font binaries are **not** published to npm; they are fetched at runtime from `https://cdn.jsdelivr.net/gh/engdawood/thmanyah-font-web@<commit>/fonts/...` (URLs are pinned to a specific commit hash, currently `@4266a9d`).
- GitHub Pages serves the repo root as a static site; `index.html` redirects to `examples/demo.html` (the live demo at <https://engdawood.github.io/thmanyah-font-web/>).

## Repository layout

- `index.css` — main entry: 15 `@font-face` declarations (3 families × 5 weights) plus utility classes (`.font-thmanyah-sans`, `.font-thmanyah-serif-display`, `.font-thmanyah-serif-text`, `.font-weight-light` … `.font-weight-black`).
- `sans.css`, `serif-display.css`, `serif-text.css` — per-family subsets containing only that family's 5 `@font-face` blocks (no utility classes).
- `fonts/<family>/{woff2,otf}/` — font binaries. woff2 files are committed to git (jsDelivr serves them from the repo); **otf files are gitignored** (local reference only, kept out of both git and npm).
- `examples/demo.html` — self-contained Arabic (RTL) showcase page; opens directly in a browser, loads `../index.css`.
- `index.html` — meta-refresh redirect to `examples/demo.html` (so GitHub Pages root works).
- `public/image.png` — README banner image.
- `README.md` (Arabic, primary) and `README.en.md` (English) — user docs. Keep both in sync when changing usage, weights, class names, or URLs.
- `.github/workflows/static.yml` — deploys the whole repo to GitHub Pages on every push to `main`.
- `.github/workflows/publish.yml` — runs `npm publish` when a `v*` tag is pushed (uses `secrets.NPM_TOKEN`, Node 20).
- `Thmanyah-Font-Family/`, `Thmanyah-Font-Family1/`, `*.zip`, `tmp/` — source/vendor material from the original font download; gitignored and/or excluded from npm. Do not modify or rely on them.
- `node_modules/@engdawood/` — a local self-install of the published package (used for testing consumption); not a real dependency (`dependencies` is empty).

## Build, test, and release commands

There is no build. Useful commands:

```bash
# Preview the demo — just open the file, no server needed
start examples/demo.html        # Windows
# open examples/demo.html       # macOS

npm test                        # placeholder: prints "No tests — this is a font package"

npm pack --dry-run              # verify exactly what would be published to npm
npm publish                     # manual publish (normally done by CI on v* tags)
```

Release flow: bump `version` in `package.json`, push a `v*` git tag → the publish workflow releases to npm. Pushes to `main` auto-deploy the demo to GitHub Pages.

## Conventions and things to watch

- **Pinned CDN URLs**: every `src: url(...)` in the CSS files points to jsDelivr with a hard-pinned commit (`@4266a9d`). If font binaries change, the new files only reach users after (a) the commit is pushed and (b) the hash in **all four** CSS files is updated to the new commit. Keep the hash identical across `index.css`, `sans.css`, `serif-display.css`, and `serif-text.css`.
- **Duplicated content**: the per-family CSS files are copies of the matching sections of `index.css`. Edit them together — there is no generation step.
- Every `@font-face` block uses `font-display: swap`, `font-style: normal`, and the same `unicode-range` covering Arabic and Latin blocks. Preserve these when adding or editing faces.
- Weight mapping is fixed: Light=300, Regular=400, Medium=500, Bold=700, Black=900. File naming: `thmanyah-<family>-<Weight>.woff2`.
- `.npmignore` additionally excludes `index.html`, `public/`, `examples/`, `CLAUDE.md`, vendor zips/dirs, and `fonts/**/otf/` from the npm tarball (the `files` allowlist already excludes them; the ignore file is belt-and-braces).
- `package-lock.json` is gitignored on purpose.
- Documentation is bilingual: user-facing docs are primarily **Arabic** (`README.md`, RTL HTML), with an English translation (`README.en.md`). Code comments and CSS are English. Match that split when editing.

## Testing

There are no automated tests, linters, or CI checks on the CSS. Manual verification:

1. Open `examples/demo.html` in a browser and confirm all 15 faces render (check devtools Network tab for the jsDelivr woff2 requests).
2. Run `npm pack --dry-run` before publishing to confirm the tarball contains only the four CSS files (+ README/package.json).
3. After changing CDN URLs, verify one URL directly in a browser/curl to ensure the pinned commit resolves on jsDelivr.

## Security and licensing considerations

- **License is restrictive**: the Thmanyah font license (see <https://font.thmanyah.com/licenses>) permits **personal use only** and does not authorize hosting/redistributing the font files. This repo's CDN redistribution is a community effort at the maintainer's own risk — flag any license-sensitive change (e.g. bundling fonts into npm, adding new font files) to the maintainer instead of doing it silently.
- npm publish runs with a token secret in CI; the repo itself contains no secrets.
- Do not commit the gitignored vendor directories (`Thmanyah-Font-Family*/`, `tmp/`, otf files) — they contain the original licensed downloads.
