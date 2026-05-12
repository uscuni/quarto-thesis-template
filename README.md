# Quarto thesis template for Faculty of Science, Charles University

Write the thesis body in `thesis.qmd` using Markdown. Render the PDF with:

```sh
quarto render thesis.qmd --to pdf
```

The generated PDF is `thesis.pdf`.

## Where things live

- `_quarto.yml` configures Quarto's PDF output to match the original LaTeX template:
  `article`, 12 pt, A4 paper, Czech language support, `natbib`, `achemso`, PDF/A,
  margins, figure/table caption placement, and the custom LaTeX includes.
- `_quarto.yml` also contains the thesis metadata used by the title page and front
  matter: titles, author, university, faculty, study programme, supervisor, abstracts,
  keywords, and abbreviations.
- `thesis.qmd` is the Markdown thesis body. Use headings for sections,
  `[@citation-key]` for citations, and Quarto cross-reference labels such as
  `{#fig-name}`, `{#tbl-name}`, and `{#eq-name}`.
- `tex/template.tex` is the Quarto/Pandoc LaTeX template that turns the metadata in
  `_quarto.yml` into the title page and front matter.
- `tex/preamble.tex` contains the LaTeX packages and layout settings copied from the
  original template.
- `tex/after-body.tex` contains the optional appendix block from the original template.
- `reference.bib` remains the BibTeX bibliography file.
- `figures/` remains the image directory.

Only the LaTeX fragments under `tex/` are part of the source project. Quarto may
generate `thesis.tex` during rendering because `keep-tex: true` is enabled; it is an
output file and can be deleted.

Converted from a[ LaTeX template](https://www.overleaf.com/latex/templates/univerzita-karlova-v-praze-prirodovedecke-fakulta-sablona-pro-zaverecne-prace/fwjqdvrwpfmn) by Daniel Willimetz, licensed under Creative Commons CC BY 4.0.