# Template provenance and verification

Retrieved and checked on 2026-10-05.

## Exact public Overleaf example

- [Official ACM SIG Proceedings gallery page](https://www.overleaf.com/latex/templates/association-for-computing-machinery-acm-sig-proceedings-template/bmvfhcdnxfty)
- [Official gallery PDF](https://www.overleaf.com/latex/templates/association-for-computing-machinery-acm-sig-proceedings-template/bmvfhcdnxfty.pdf)
- The complete source was extracted from the gallery's **View Source** block, decoding HTML entities without changing the source text.
- `main.tex`, `overleaf/sigconf.tex`, and `acmart/samples/sigconf.tex` are byte-identical, at 32,385 bytes and 852 lines.
- Source SHA-256: `af143961b24a34579a05d1a6e5f3ca1d22574a93ed144e1a1d8be314b0ab3aff`.
- The gallery PDF is retained unchanged as `overleaf/sigconf.pdf`.
- Gallery PDF SHA-256: `e34d5a6b950d04378c83e580de9bfe721be8fa2a88641ade67aa05f91863be93`.

The gallery describes acmart 2.19, dated 2026-07-02. No authenticated
Overleaf project was created or exported, so this repository does not claim
to contain a byte-identical export of the gallery's entire project.

## Complete official ACM distribution

- Package: ACM `acmart` 2.20, dated 2026-08-16.
- [ACM template page](https://www.acm.org/publications/proceedings-template)
- [CTAN package metadata](https://ctan.org/pkg/acmart)
- [Actual ZIP download](https://mirrors.ctan.org/macros/latex/contrib/acmart.zip)
- The unmodified download is retained as `acmart-2.20.zip`.
- ZIP SHA-256: `93933ce58fbeffa13e23398bb523fcb68275ecc73369c6bc73b421eeef2c10de`.

Every file in the ZIP is extracted under `acmart/` and retained without
edits or exclusions. `acmart.cls` was generated with the official
`latex acmart.ins` command. All 18 official example `.tex` files were
generated with `latex samples.ins`. The class, bibliography style,
sample bibliography, and required graphics are copied to the repository
root so that the complete example compiles directly as `main.tex`.

The ACM direct ZIP endpoint returned HTTP 403, so CTAN supplied the complete
official distribution. Despite the version difference, its generated
SIG Proceedings source matches the Overleaf gallery source byte for byte.

## Comparison with the supplied paper

Reference: [Textro, arXiv:2608.00294v1](https://arxiv.org/abs/2608.00294).
The public PDF and TeX source were inspected. The paper uses
`\documentclass[sigconf]{acmart}` and explicitly writes its introduction
heading as `\section{INTRODUCTION}`.

PDF font inspection with `pdffonts` and PyMuPDF found the same fonts and
nominal sizes in the paper, official Overleaf preview, and locally built
template:

| Element | Embedded font | Approximate PDF size |
| --- | --- | --- |
| Body | `LinLibertineT` | 9 pt, with small glyph-scaling variations |
| Title | `LinBiolinumTB` | 17.215 PDF pt |
| Section heading | `LinLibertineTB` | 10.909 PDF pt |

Matching font names and sizes establish the typography configuration,
not pixel-identical rendering across TeX/font versions and PDF viewers.
The earlier project starter had review line numbers, anonymous authors,
removed sample content, and changed metadata. Those adaptations have been
removed from `main.tex`; the complete original source is now the default.

## License

Copyright 2016–2026 Association for Computing Machinery. The upstream
template is maintained by Boris Veytsman and distributed under the
LaTeX Project Public License, version 1.3 or later, as stated in
`acmart/acmart.dtx`. Original copyright and maintenance notices are retained.
The license is available at https://www.latex-project.org/lppl/.
