# plagouanelle.github.io

Paul Lagouanelle's personal/academic site, built on [al-folio](https://github.com/alshedivat/al-folio) (Jekyll).

## Local development

```bash
bundle install
bundle exec jekyll serve
```

Site is served at `http://localhost:4000/`.

## Structure

- `_pages/` — About, Publications, Teaching, Misc, CV, News
- `_bibliography/papers.bib` — publications, rendered by jekyll-scholar
- `_data/cv.yml` — structured CV data (rendered at `/cv/`)
- `_data/socials.yml` — contact/social links
- `_news/` — items shown on the About page and at `/news/`
- `assets/pdf/CV_LAGOUANELLE.pdf` — downloadable CV

Pushing to `main` deploys automatically via `.github/workflows/deploy.yml`.

See `AGENTS.md` / `CLAUDE.md` for notes on how this starter is organized (most
of the theme's layouts/styling live in the `al_folio_core` gem, not in this
repo).
