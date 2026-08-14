# Repository guidance

This repository is the source for Md Ali's professional website at https://alihmd.com. It is a Hugo site built with the legacy Wowchemy Academic theme. Keep changes focused, readable, and easy to review.

## Improvement direction

Use `ROADMAP.md` as the ordered improvement backlog. When a request is broad, select the first unchecked item that can be completed safely in one focused pull request.

The roadmap does not authorize automatic merging, deployment, changes to personal facts, credentials, or a framework migration. Stop for owner review whenever one of those decisions is involved.

## Project structure

- `content/authors/admin/_index.md` contains the primary biography, credentials, interests, and profile links.
- `content/home/` controls the home-page sections and their order.
- `content/project/`, `content/publication/`, and `content/event/` contain portfolio entries.
- `config/_default/` contains site, navigation, language, and theme configuration.
- `static/`, `assets/`, and `images/` contain site media and styling assets.
- `netlify.toml` is the source of truth for the production build command and pinned Hugo version.

## Working locally

Match the deployed toolchain whenever possible:

1. Install Go and Hugo 0.79.1.
2. Download module dependencies with `go mod download`.
3. Preview with `hugo server --disableFastRender --i18n-warnings`.
4. Before submitting, run `hugo --gc --minify`.

If the exact legacy Hugo version is unavailable, state that clearly in the pull request and avoid changing dependencies merely to make a newer local version pass.

## Change guidelines

- Preserve existing personal facts, credentials, dates, and external links unless the task explicitly asks to update them.
- Prefer editing Markdown content and TOML configuration over generated HTML.
- Do not commit `public/`, `resources/`, editor metadata, credentials, API keys, or deployment secrets.
- Keep front matter valid and retain Wowchemy widget fields that the current version requires.
- Treat Hugo, Go module, Wowchemy, and deployment upgrades as separate changes with explicit migration and rollback notes.
- Optimize images before adding them, use meaningful alt text where supported, and avoid unnecessary third-party scripts.
- Keep navigation labels and headings concise, professional, and consistent.

## Pull requests

- Use a focused branch and a descriptive title.
- Explain what changed, why it changed, any visible impact, and exactly what was validated.
- Include screenshots for visual changes when a preview is available.
- Do not merge automatically; leave the final review and merge decision to the repository owner.

## Code review rules

During review, prioritize:

- build failures, invalid TOML or front matter, broken internal links, and incompatible Hugo or Wowchemy changes;
- inaccurate or unintentionally removed profile information;
- privacy leaks, secrets, unsafe embedded HTML, and untrusted third-party scripts;
- accessibility regressions such as missing labels, poor heading structure, or unusable keyboard interactions;
- large generated files, editor artifacts, and unrelated formatting churn.

Avoid blocking on subjective wording or visual preference unless it harms clarity, accuracy, accessibility, or the stated goal.
