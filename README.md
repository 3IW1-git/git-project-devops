# Demo Buttons Site

A tiny demo website showcasing a simple HTML page styled with CSS and interactive buttons (hover/active states). Ideal as a starting point for static demos or UI experiments.

## Features

- Plain HTML5 structure (`index.html`).
- Minimal CSS styling for consistent typography and spacing (`style.css`).
- A styled button with hover and active states (easy to duplicate to create more buttons).
- No build step or dependencies — just open the file in a browser.

## Quick Start

Option 1 — Open directly:
- Double‑click `index.html` to open it in your default browser.

## Project Structure

```
.
├─ index.html   # Main HTML page containing the buttons
├─ style.css    # Button styles, layout, and basic typography
└─ CODE_OF_CONDUCT.md  # Community guidelines for contributions and interactions
```

## Customize

- Change button text: edit the `<button>...</button>` labels in `index.html`.
- Add more buttons: duplicate the existing `<button>` element.
- Adjust colors/sizing: edit the `button` rules in `style.css` (e.g., `background-color`, `padding`, `font-size`).
- Page content: add your own sections, headers, or components directly in `index.html`.

## Development Notes

- This project is intentionally dependency‑free. If you add tooling (bundlers, preprocessors, etc.), document it here.
- Keep HTML/CSS simple and readable for demo purposes.

## Contributing

Contributions are welcome. Please first read our [Code of Conduct](./CODE_OF_CONDUCT.md) to understand expected behavior.

## License

No license specified yet. If you plan to publish or reuse this code, consider adding a suitable open‑source license.

## Lint & CI

- Linter: ESLint is configured via `eslint.config.mjs`.
- Local script: `npm run lint` (and `npm run lint:fix`).
- CI: a GitHub Actions workflow automatically runs ESLint on each push/PR (`.github/workflows/eslint.yml`).

### Local Git hook (without Husky)

A simple `pre-commit` hook is provided in `.github/.githooks/pre-commit` and runs `npm run lint`.

To enable it locally (once per repo):

```
git config core.hooksPath .github/.githooks
```

Then make sure the hook is executable (Git usually keeps the mode from the repo; if not):

```
chmod +x .github/.githooks/pre-commit
```

On every `git commit`, ESLint will run. The CI will also fail PRs with ESLint errors.
