# Complete ACM SIG Proceedings template

`main.tex` is an unchanged, byte-for-byte copy of the complete `sigconf.tex`
source published in the [official Overleaf template](https://www.overleaf.com/latex/templates/association-for-computing-machinery-acm-sig-proceedings-template/bmvfhcdnxfty).
All 852 lines are retained, including sample authors, abstract, body text,
figures, tables, equations, references, acknowledgements, and appendices.

The original document class setting is preserved:

```tex
\documentclass[sigconf]{acmart}
```

No review, anonymous, font, spacing, margin, or metadata overrides have been
added. The sample title is **The Name of the Title Is Hope**. Its sample
metadata and content are part of the original template, not project facts.

## Open in Overleaf

1. Download this repository using **Code → Download ZIP** on GitHub.
2. In Overleaf, select **New Project → Upload Project** and upload the ZIP.
3. Select `main.tex` as the main document and **pdfLaTeX** as the compiler.
4. Compile to view the complete original example.

## Included files

| Path | Contents |
| --- | --- |
| `main.tex` | Complete, unchanged Overleaf SIG Proceedings source |
| `acmart.cls`, `ACM-Reference-Format.bst` | Official class and bibliography style from ACM acmart 2.20 |
| `sample-base.bib` | Original sample bibliography used by `main.tex` |
| `sampleteaser.pdf`, `sample-franklin.png` | Original example graphics used by `main.tex` |
| `template/overleaf/sigconf.tex` | Exact source captured from the Overleaf gallery |
| `template/overleaf/sigconf.pdf` | Original PDF downloaded from the Overleaf gallery |
| `template/acmart-2.20.zip` | Complete, unmodified official CTAN distribution archive |
| `template/acmart/` | Every file from that archive, plus official TeX examples generated with `samples.ins` |
| `template/SOURCE.md` | Source URLs, version distinction, checksums, and font comparison |

The gallery describes acmart 2.19, while this repository's class is the
official CTAN 2.20 release. The gallery's `sigconf.tex` and the 2.20 sample
source were verified to be byte-identical. This is not an authenticated
export of an Overleaf project; the exact public source and preview are
preserved alongside the complete official CTAN distribution.

## Local compilation

With TeX Live or MiKTeX and `latexmk` installed, run from this directory:

```sh
latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
```

The output is `main.pdf`. Generated build files are ignored by Git. The
official PDFs included in the template remain tracked.

## Future UIST submission

The project targets UIST 2027. Keep this template intact until manuscript
editing is requested. Confirm the target year's formatting requirements
before preparing the submission. UIST 2026 specified
`sigconf,review,anonymous` for paper review, but that adaptation is not
enabled in this exact template copy.
