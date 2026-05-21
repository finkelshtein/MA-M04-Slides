# Probability & Statistics for Data Science — Slides

Quarto website + Reveal.js slide decks using the [dtslides](https://data-wise.github.io/dtslides/) Academic theme.

## Project structure

```
prob-stats-slides/
├── _quarto.yml          # website config (format: html)
├── index.qmd            # homepage with lecture cards
├── custom.css           # website styling
└── slides/
    ├── custom.scss      # dtslides theme overrides (SCSS)
    ├── lecture01.qmd    # Introduction to Probability
    ├── lecture02.qmd    # Random Variables
    └── lecture03.qmd    # Key Distributions
```

Each `slides/lectureXX.qmd` uses `format: dtslides-revealjs`.  
The root `_quarto.yml` sets `format: html` for the website wrapper.

## First-time setup

Requires [Quarto](https://quarto.org) >= 1.6.0.

```bash
# 1. Install the dtslides extension (once per project)
quarto add Data-Wise/dtslides

# 2. Render the full website
quarto render

# 3. Preview locally
quarto preview
```

The rendered site lands in `_site/`.

## Updating dtslides

```bash
quarto update Data-Wise/dtslides
```

## Adding a new lecture

1. Copy `slides/lecture03.qmd` → `slides/lecture04.qmd`
2. Update the YAML `title` / `subtitle`
3. Add a card to `index.qmd` and a menu entry in `_quarto.yml`
4. Run `quarto render`

## Customising the theme

Edit `slides/custom.scss`:

- Change `$primary` / `$accent` for different colours
- Adjust `$font-size-root` (default 32 px) for larger/smaller text
- Use `$font-family-heading` / `$font-family-sans-serif` to swap fonts

See the [dtslides Getting Started](https://data-wise.github.io/dtslides/getting-started.html) page for the full list of SCSS variables.
