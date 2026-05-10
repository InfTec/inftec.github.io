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
├── _layouts/
│   └── default.html                  # custom layout (logo header, footer)
├── assets/
│   ├── css/style.scss                # InfTec brand overrides on top of cayman
│   └── img/
│       ├── inftec-logo.png           # white-on-dark-gray logo (header band)
│       └── favicon.ico               # matches the one served by inftec.ch
├── doodle-poodle/
│   └── privacy/
│       └── index.md                  # → https://inftec.github.io/doodle-poodle/privacy/
└── (future: other-app/<doc-type>/index.md)
```

Each app gets its own top-level directory; each document type
gets a sub-directory with an `index.md` so the URL slug is
clean (`/<app>/<doc>/`, not `/<app>/<doc>.html`).

## Branding

The site's look matches the InfTec corporate styleguide:

- **Header band** is `#4D4D4D` (styleguide dark-gray) with the
  authorised "icon-orange + wordmark-white on dark gray" logo
  variant.
- **Body links** use the brand orange `#F18D0D`, hovering to the
  brand red `#ED1C24` (the two endpoints of the brand gradient).
- **Type** is the system sans stack — the styleguide authorises
  Helvetica / Arial as substitutes for the commercial ARS
  Maquette Pro, and a system stack avoids a webfont round-trip.

Brand tokens are centralised at the top of
[`assets/css/style.scss`](assets/css/style.scss) so a styleguide
revision touches one file. The custom layout
[`_layouts/default.html`](_layouts/default.html) overrides
cayman's default to inject the logo and the InfTec footer.

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

## Local preview

GitHub Pages rebuilds the site on every push to `main` (~1 min).
For most colour or typography tweaks, pushing and refreshing
the live URL is the fastest iteration loop. If you expect to
iterate a lot — or you're touching `_layouts/` or
`assets/css/style.scss` and want to catch SCSS syntax errors
interactively — set up Jekyll locally.

### Option 1 — Push and refresh (fastest, no setup)

```bash
git push origin main
# wait ~1 min, then refresh https://inftec.github.io/
```

Trade-off: a SCSS or layout error makes the Pages build fail
silently (GitHub emails the repo owner; no interactive
feedback). Fine for low-risk colour or text tweaks; switch to
a local setup if you're touching the layout.

### Option 2 — Local Jekyll via Bundler

The "official" preview path. GitHub publishes a `github-pages`
meta-gem that pins Jekyll + plugins to whatever Pages currently
runs:

```bash
# One-time setup: a Gemfile with the github-pages gem.
cat > Gemfile <<'EOF'
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
EOF

bundle install
bundle exec jekyll serve --livereload
# preview at http://localhost:4000/
```

Saving any source file triggers a browser reload via
`--livereload`. The `Gemfile` and `Gemfile.lock` are already
listed in `_config.yml`'s `exclude:` block, so they don't
become served URLs even though they're in the repo.

**Heads-up for Arch Linux:** if `bundle install` fails with
`uninitialized constant` errors (Bundler 4 + Ruby 3.4
incompatibilities — same shape as the fastlane breakage in the
Doodle-Poodle dev box), fall back to option 3.

### Option 3 — Docker (no host Ruby needed)

```bash
docker run --rm -it \
  -v "$PWD:/srv/jekyll" \
  -p 4000:4000 \
  jekyll/jekyll:latest \
  jekyll serve --host 0.0.0.0
# preview at http://localhost:4000/
```

The official `jekyll/jekyll` image isn't `github-pages`-pinned,
so an exotic plugin might render differently. For a vanilla
theme + static markdown like this site, output is identical to
Pages.

## Contact

[`info@inftec.ch`](mailto:info@inftec.ch).
