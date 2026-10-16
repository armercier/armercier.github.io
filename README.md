# Arnaud Mercier — personal academic website

Built with [Hugo](https://gohugo.io) from Pascal Michaillat's
[hugo-website](https://github.com/pmichaillat/hugo-website) template (PaperMod-based),
deployed to GitHub Pages by `.github/workflows/hugo.yml`.

## Run locally

```console
hugo server        # http://localhost:1313
```

## Structure

| Path | What |
|---|---|
| `config.yml` | name, intro text, menu, homepage buttons, social icons |
| `content/research.md` | research overview |
| `content/publications/<slug>/index.md` | one folder per paper (put PDF and figure next to it) |
| `content/talks/*.md` | conference talks |
| `content/software/*.md` | software and hardware projects |
| `content/teaching/*.md` | courses and supervision |
| `content/contact.md` | contact / office |
| `static/cv.pdf`, `static/picture.jpeg` | CV and portrait |

New paper: `hugo new content/publications/my-paper/index.md --kind publication`

Search for `PLACEHOLDER` and `TODO` to find what still needs writing.

## Colour palette

Derived from a dusk landscape photograph, sampled top to bottom
(`assets/css/core/theme-vars.css`, accents in `assets/css/extended/dusk.css`):

| Token | Hex | Use |
|---|---|---|
| sky lavender | `#857399` | top of gradient band, favicon |
| dusk mauve | `#846282` | horizon glow |
| twilight plum | `#6f547b` | links, underlines (`--darkcolor`) |
| night blue | `#454a6f` | headings; text `#2f3350` |
| lavender tint | `#d9cde2` | button hover (`--lightcolor`) |

## Deploy

In the GitHub repo: **Settings → Pages → Source: GitHub Actions**. Each push to `main` rebuilds the site.
Set `baseURL` in `config.yml` to the final URL.
