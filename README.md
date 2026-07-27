# CV

Source for my personal CV / résumé — built with LaTeX.

<div align="left">
  <a href="https://yuemya.de/cv">
    <img src="https://img.shields.io/badge/Preview-yuemya.de%2Fcv-blue?style=for-the-badge&logo=adobe-acrobat-reader" alt="Preview CV">
  </a>
</div>

## Overview

A clean, single-column developer CV rendered with `pdflatex`.
Styling is fully separated from content:

- `tex/cvstyle.sty` — page layout, colors, fonts, section/entry macros
- `tex/main.tex` — personal data, section content, optional look overrides

Edit the HEADER block in `main.tex` to reuse the template for your own CV.

## Features

- **Two-row contact header** — direct contact (email, phone, location) on one
  line, web links (website, GitHub, LinkedIn) on the next, so nothing
  overflows the margin.
- **Section macros** — `\cvsection`, `\cventry`, `\cvproject`, `\cvskill`,
  `\cvtech`, `\cvpub`, and a `cvitems` list for bullet points.
- **First-entry spacing** — the first item under every section skips the
  top gap, so all sections start at exactly the same distance from their
  rule.
- **Override-friendly palette** — swap the accent color and margins from
  `main.tex` without touching the style file.
- **Optional sections** — Awards, Languages, Publications, etc. ship as
  commented-out templates you can drop in.

## Getting Started

### Prerequisites

A `pdflatex` distribution — TeX Live, MiKTeX, or the default Overleaf image
all work. The template needs the `fontawesome5` and `sourcesanspro` packages.

### Usage

1. Open `tex/main.tex` in your editor.
2. Fill in the **HEADER** block (`\name`, `\tagline`, `\email`, `\website`,
   `\github`, `\linkedin`, …). The placeholders show you what each macro
   expects.
3. Edit the **PROFILE**, **EXPERIENCE**, **PROJECTS**, **EDUCATION**, and
   **SKILLS** sections to match your background.
4. (Optional) Uncomment the extra sections at the bottom of `main.tex`
   (Awards, Languages) if you want them.
5. (Optional) Adjust the accent color or geometry by uncommenting one of
   the override lines near the top of `main.tex`.
6. Compile:

   ```sh
   cd tex && pdflatex main.tex
   ```

### Template Overview

The default layout covers:

- **Header** — name, tagline, two-row contact info with icons.
- **Profile** — short summary of who you are and what you do.
- **Experience** — `\cventry{role}{company}{location}{dates}` plus a
  `cvitems` list of responsibilities and achievements.
- **Selected Projects** — `\cvproject{name}{stack}{year}` with bullets
  describing the work.
- **Education** — degrees, institutions, dates, and an optional thesis
  description.
- **Skills** — grouped `\cvskill{category}{list}` rows that align
  consistently across wrapped lines.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE)
file for details.
