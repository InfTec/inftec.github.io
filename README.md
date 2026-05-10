# inftec.github.io

Org-level GitHub Pages site for **InfTec GmbH**. Holds public
documents (privacy policies, terms of service, support pages,
etc.) for InfTec apps. Served at:

**https://inftec.github.io/**

## Structure

```
.
├── index.md                          # landing page
├── _config.yml                       # Jekyll config (theme, site title)
├── doodle-poodle/
│   └── privacy/
│       └── index.md                  # → https://inftec.github.io/doodle-poodle/privacy/
└── (future: other-app/<doc-type>/index.md)
```

Each app gets its own top-level directory; each document type
gets a sub-directory with an `index.md` so the URL slug is
clean (`/<app>/<doc>/`, not `/<app>/<doc>.html`).

## Per-document source of truth

Document content is drafted and reviewed in the relevant app's
private repository (e.g. Doodle-Poodle's policy lives at
`docs/privacy-policy.md` in the app repo). The copy here is a
clean derivative — drafting notes and internal checklists
stripped — and must be kept in sync on every revision. The
HTML comment at the top of each `index.md` flags this.

When a document changes:

1. Edit the source in the app repository.
2. Bump the **Last updated** date in both copies.
3. Copy the body across, preserving the HTML comment header.
4. Commit & push. Pages rebuilds automatically (~1 min).

## Adding a new app

1. Create `<app-slug>/<doc-type>/index.md` with the document
   content and a per-page front-matter `title` / `description`.
2. Add a link to the new document from the root `index.md`.
3. Commit, push, verify the URL.

## Contact

[`info@inftec.ch`](mailto:info@inftec.ch).
