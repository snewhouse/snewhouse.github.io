# snewhouse.github.io

Personal site of [Stephen J Newhouse](https://github.com/snewhouse), built with [Quarto](https://quarto.org).

Live at <https://snewhouse.github.io>.

## Structure

```
.
├── _quarto.yml           # site config (theme, navbar, SEO, OG, twitter-card)
├── index.qmd             # homepage (about-trestles)
├── about.qmd             # extended bio
├── cv.qmd                # CV (template — fill in real entries)
├── projects.qmd          # project listing
├── posts.qmd             # blog listing
├── archive.qmd           # links into /archive
├── projects/             # one .qmd per featured project
├── posts/                # one folder per blog post
├── archive/              # legacy 2016–2019 content (preserved as-is)
├── assets/               # favicon, OG image, project images, avatar
├── includes/head.html    # SEO meta + JSON-LD Person + WebSite
├── styles.scss           # theme overrides (sass)
├── styles.css            # extra css
├── robots.txt            # crawler directives
├── llms.txt              # plain-text bio for LLM agents (agent-optimised)
├── .well-known/security.txt
└── .github/workflows/publish.yml   # build + deploy to gh-pages on push to master
```

## Local development

```bash
# install Quarto >= 1.5  →  https://quarto.org/docs/get-started/
quarto preview            # live-reloading dev server
quarto render             # one-shot build into _site/
```

## Deployment

The GitHub Action in `.github/workflows/publish.yml` renders on every push to `master` (or `main`) and publishes to the **`gh-pages`** branch.

**One-time setup in GitHub:**

1. Repo → **Settings → Pages** → set source to **Deploy from a branch**, branch **`gh-pages`**, folder **`/ (root)`**.
2. Repo → **Settings → Actions → General** → under "Workflow permissions" select **Read and write permissions**.

The first push will create the `gh-pages` branch automatically.

## What's in the box

- **SEO:** meta description/keywords, canonical URL, Open Graph, Twitter Card, sitemap (auto by Quarto), robots.txt.
- **Agent / LLM optimisation:** JSON-LD `Person` and `WebSite` schemas (`includes/head.html`), `rel=me` profile links (see `includes/head.html` for the current list), plain-text `llms.txt` summary at the site root.
- **Recruiter-friendly:** clear CV page, prominent LinkedIn link, Open-to-Work callout, contact email.
- **Blog:** Quarto listing with RSS feed.
- **Projects:** grid listing with categories.
- **Archive:** old 2016–2019 homepage, CVs, talks, and the NGS workshop preserved at stable URLs.

## Gaps still to fill in

These are still placeholders — the build won't fail without them, but you'll want to populate:

- [ ] **Avatar:** drop a square headshot at `assets/avatar.jpg` and switch `index.qmd` `image:` from `assets/favicon.svg` back to `assets/avatar.jpg`.
- [ ] **OG image:** add `assets/og-image.png` (1200×630). Referenced by JSON-LD.
- [ ] **CV PDF:** drop `assets/cv.pdf` to enable the download button on `cv.qmd`.
- [ ] **Selected publications:** `cv.qmd` currently links out to Scholar / KCL Pure / Impactstory. Add 3–5 hand-picked highlights if you want them surfaced.
- [x] **Google Scholar profile ID:** `t3faIVoAAAAJ`. Verified by Stephen and applied site-wide (`index.qmd`, `about.qmd`, `cv.qmd`, `includes/head.html`, `llms.txt`).
- [ ] **Google Analytics / Plausible** *(optional)*: `_quarto.yml` `google-analytics:` is empty; add an ID if you want stats.
- [ ] **Custom domain** *(optional)*: add a `CNAME` file at the repo root, then configure DNS.

### Already filled in from the LinkedIn export

- ✅ Current role: Head of Professional Services & Senior Bioinformatician, Biorelate Ltd.
- ✅ Location: Manchester, UK
- ✅ Full work history (Biorelate → Grid Edge → Mindwave → UCL → KCL × 4 roles → 3 postdocs)
- ✅ Education: PhD QMUL, MSc KCL, BSc Liverpool
- ✅ Certifications + MHFA Champion
- ✅ Email: stephen.j.newhouse@gmail.com
- ✅ KCL Pure profile link
- ✅ Bio voice / tone lifted from LinkedIn summary

## Migrating from the old site

The old pandoc-rendered `index.html`, `cv/`, `git_intro/`, and `ngs_workshop/2019/` are preserved under `archive/`. URLs from old papers/talks should keep working via:

- `/archive/homepage-legacy.html`
- `/archive/cv-legacy/`
- `/archive/git-intro-2018/`
- `/archive/ngs-workshop-2019/files/`
