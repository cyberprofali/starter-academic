# Md Ali's Professional Website

Source code for [alihmd.com](https://alihmd.com), the professional and academic website of Md Ali, Ph.D. The site presents cybersecurity leadership experience, research, teaching, projects, publications, and professional credentials.

## Technology

- [Hugo](https://gohugo.io/) static site generator
- Wowchemy Academic theme
- Go modules for theme dependencies
- Netlify for builds and deployment

This is a legacy Wowchemy project pinned to Hugo 0.79.1. Keep framework upgrades separate from content changes so they can be tested and rolled back cleanly.

## Run locally

Install Go and Hugo Extended 0.79.1, then run:

```bash
go mod download
hugo server --disableFastRender --i18n-warnings
```

Open the local address printed by Hugo. The repository also provides `./view.sh` for the preview command on macOS or Linux.

To check the production build:

```bash
hugo --gc --minify
```

Netlify uses the production command and Hugo version defined in `netlify.toml`.

## Where to make changes

| Area | Location |
| --- | --- |
| Biography and profile links | `content/authors/admin/_index.md` |
| Home-page sections | `content/home/` |
| Projects | `content/project/` |
| Publications | `content/publication/` |
| Events and talks | `content/event/` |
| Navigation and site settings | `config/_default/` |
| Static files and media | `static/`, `assets/`, `images/` |

Do not commit generated output from `public/` or `resources/`.

## Working with Codex

Repository-level instructions live in `AGENTS.md`. Codex reads that file before working in this project, including its build expectations and code-review priorities. Ordered improvement priorities live in [`ROADMAP.md`](ROADMAP.md).

For each change:

1. Create a focused branch.
2. Ask Codex to implement or review the change.
3. Open a pull request into `master`.
4. Confirm the Netlify preview/build and review feedback.
5. Merge only after the result looks correct.

## License

See `LICENSE.md`.
