# Template: plain-column

- **Type:** Cover letter
- **Engine:** xelatex
- **Page limit:** 1 page(s)
- **Fonts:** system default sans-serif (`\sfdefault` via `\familydefault`) — no bundled fonts, no font files to install
- **Class/packages:** `article` base class + local `letter_style.sty` (geometry, xcolor, hyperref, enumitem, parskip — all standard TeX Live/MiKTeX packages)

## Compile command

    cd <output dir> && xelatex -interaction=nonstopmode <file>.tex

## Style rules

- Single column, plain `article`-class layout, matches `plain-column` CV template's color scheme (`resumeblue` #2E74B5, `resumegray` #444444)
- Header (`\letterheader{name}{contact line}`) centered; contact line uses `\textbullet\ ` separator
- Date (`\letterdate{\today}`) right-aligned above the salutation
- Body is plain paragraphs (no `\lettercontent{}` wrapper macro) with an optional `itemize` block for 3-5 concrete proof points tied to the posting's requirements
- Sign-off via `\lettersignoff{closing phrase}{name}` inside `\begin{flushright}...\end{flushright}`
- Target length: opening paragraph, one proof-point paragraph + itemize, optional one-sentence gap acknowledgment, closing line — keep to 1 page

## Known pitfalls

- None recorded. Unlike the old `cover.cls` template, there is no `\lettercontent{}` macro wrapping body text, so the itemize-inside-macro font/line-break bug from the stock template does not apply here — bullets and body already share the same font by construction.
- No `fontspec` calls or bundled font files are actually used, so `pdflatex` would likely compile this too — `xelatex` is used only for consistency with the rest of the repo's cover letters (21 existing applications compiled this way).
