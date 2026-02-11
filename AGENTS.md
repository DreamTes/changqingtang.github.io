# Repository Guidelines

## Project Structure & Module Organization
This repository is a Jekyll-based academic site template. Core configuration is in `_config.yml`.
- Content collections: `_pages/`, `_posts/`, `_publications/`, `_talks/`, `_teaching/`, `_portfolio/`
- Layout and reusable templates: `_layouts/`, `_includes/`
- Data files: `_data/` (for navigation, authors, CV JSON, UI strings)
- Styling and scripts: `_sass/`, `assets/css/`, `assets/js/`
- Static downloads and media: `files/`, `images/`
- Utilities: `scripts/` (for CV conversion helpers)

## Build, Test, and Development Commands
- `bundle install`: install Ruby/Jekyll dependencies from `Gemfile`.
- `bundle exec jekyll serve -l -H localhost`: run local dev server at `http://localhost:4000` with live reload.
- `bundle exec jekyll build`: production-style site build to verify templates/content compile.
- `npm install`: install JS dependencies used for front-end bundling.
- `npm run build:js`: rebuild `assets/js/main.min.js` from source files.
- `npm run watch:js`: watch JS sources and rebuild on change.

## Coding Style & Naming Conventions
- Use 2-space indentation for YAML, Markdown front matter, HTML/Liquid, and SCSS.
- Keep Markdown content files named by collection conventions, e.g. `_posts/YYYY-MM-DD-title.md` and `_talks/YYYY-MM-DD-title.md`.
- Prefer lowercase, hyphenated filenames (`paper-title-number-5.md`).
- Keep front matter keys consistent with existing files (for example `title`, `permalink`, `date`, `collection`).

## Testing Guidelines
There is no dedicated unit-test framework in this repository. Use build verification:
- Run `bundle exec jekyll build` before opening a PR.
- If JS changes were made, run `npm run build:js` and confirm no unexpected diffs in `assets/js/main.min.js`.
- Manually check affected pages locally with `bundle exec jekyll serve`.

## Commit & Pull Request Guidelines
Git history in this copy is minimal (`init`), so follow a clear, conventional style:
- Commit messages: short imperative subject, optional scope (example: `talks: add 2026 keynote entry`).
- Keep commits focused (content, style, and config changes separated when practical).
- PRs should include: purpose summary, key files changed, preview screenshots for UI/content layout changes, and linked issue(s) when applicable.

## Security & Configuration Tips
- Do not commit secrets or private tokens in `_config.yml` or data files.
- Validate external links and uploaded files in `files/` before publishing.
