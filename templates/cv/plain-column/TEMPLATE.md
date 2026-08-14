# Template: plain-column

- **Type:** CV
- **Engine:** lualatex
- **Page limit:** 2 page(s)
- **Fonts:** system default sans-serif (`\sfdefault` via `\familydefault`) — no bundled fonts, no font files to install
- **Class/packages:** `article` base class + local `resume_style.sty` (geometry, xcolor, hyperref, titlesec, enumitem, tabularx, array, needspace — all standard TeX Live/MiKTeX packages)

## Compile command

    cd <output dir> && lualatex -interaction=nonstopmode <file>.tex

## Style rules

- Single column, plain `article`-class layout — no moderncv/photo/sidebar
- Section headings: bold, `resumeblue` (#2E74B5), with a thin blue rule underneath (`\titleformat{\section}`)
- Body text color: `resumegray` (#444444) for dates/locations, black for bullet text
- Header block (`\cvheader{name}{title}{contact line}`) is centered; contact line uses `\textbullet\ ` as separator between items
- Entry headers (`\cventryhead{left text}{right-aligned date range}`) use a two-column `tabularx` — left-aligned title/company, right-aligned dates
- Bullets: `itemize` with tight spacing (`itemsep=1pt, topsep=1pt`)
- Standard section order: SUMMARY, CORE COMPETENCIES, PROFESSIONAL EXPERIENCE, [OPEN SOURCE PROJECTS if relevant], EDUCATION, TECHNICAL SKILLS, CERTIFICATIONS

## Known pitfalls

- `\cventryhead` already calls `\needspace{3\baselineskip}` internally — do NOT add a second manual `\needspace` before it, it's redundant (unlike the old moderncv template, orphaned entry titles are not a common failure mode here)
- The `TECHNICAL SKILLS`/`skillrow` tabularx pattern can make `pdftotext` extraction slightly reorder row labels vs. content in ATS checks — cosmetic only, the same keywords already appear in `CORE COMPETENCIES` as plain itemize text, so ATS keyword matching is unaffected. Note this in Step 5d of `/apply` rather than treating it as a failure.
- No custom fonts, no `fontspec` — `pdflatex` would likely also compile this cleanly, but `lualatex` is used for consistency with the rest of the repo's CVs (21 existing applications compiled this way) and to sidestep any future `fontawesome`-style font issues if icons are ever added.
