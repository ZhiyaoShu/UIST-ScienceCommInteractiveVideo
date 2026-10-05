# UIST – Science Communication through Interactive Video

用于后续项目写作的 ACM LaTeX / Overleaf 起始项目。当前只有占位内容，主文件为 `main.tex`。

## Overleaf 使用

1. 在 GitHub 选择 **Code → Download ZIP**。
2. 在 Overleaf 选择 **New Project → Upload Project**，上传该 ZIP。
3. 将主文件设为 `main.tex`，编译器选择 **pdfLaTeX**。建议使用最新可用的 TeX Live。
4. 编辑标题和正文；向 `references.bib` 添加文献，首次引用后取消 `main.tex` 中 `\bibliography{references}` 的注释。

## 默认投稿格式

```tex
\documentclass[sigconf,review,anonymous]{acmart}
```

这对应 [UIST 2026 Papers 官方指南](https://uist.acm.org/2026/cfp/)规定的双栏匿名审稿格式。通用 ACM / Overleaf 模板中的单栏审稿说明不覆盖 UIST 的具体要求。尚未指定本项目的投稿年份，后续请以目标年份和 track 的指南为准。

接受后，根据当届指南改为 `\documentclass[sigconf]{acmart}`，补充作者、CCS 分类、关键词及 ACM 提供的会议和版权元数据，并移除草稿用的 `\setcopyright{none}`、`\settopmatter{printacmref=false}` 和空元数据设置。

## 文件

| 路径 | 用途 |
| --- | --- |
| `main.tex` | 项目写作入口，已配置 UIST 双栏匿名审稿格式 |
| `references.bib` | 项目参考文献 |
| `acmart.cls` | 官方 ACM 文档类，版本 2.20 |
| `ACM-Reference-Format.bst` | 官方 BibTeX 样式 |
| `template/acmart/samples/sigconf.tex` | 未修改的官方 SIG proceedings 示例 |
| `template/acmart/samples/sigconf.pdf` | 上游提供的示例 PDF |
| `template/acmart/acmguide.pdf` | 官方使用指南 |
| `template/acmart/acmart.pdf` | 官方完整文档 |
| `template/SOURCE.md` | 下载来源、版本及许可证说明 |

`template/acmart/` 中的文件用于参考；默认编译 `main.tex`。原始示例中的姓名、会议、DOI 和 CCS 分类均为演示值。

## 本地编译

安装包含 ACM 所需字体和宏包的 TeX Live / MiKTeX，以及 `latexmk`，在仓库根目录执行：

```sh
latexmk -pdf -interaction=nonstopmode -halt-on-error main.tex
```

生成的 `main.pdf` 和中间文件已加入 `.gitignore`，图片及官方参考 PDF 仍可正常提交。

如需编译原始示例，可在仓库根目录执行：

```sh
TEXINPUTS="$PWD/:$PWD/template/acmart/samples/:" \
  BIBINPUTS="$PWD/template/acmart/samples/:" \
  BSTINPUTS="$PWD/:" \
  latexmk -pdf -outdir=build/sample -interaction=nonstopmode -halt-on-error template/acmart/samples/sigconf.tex
```

## 官方来源

- [ACM Proceedings Template](https://www.acm.org/publications/proceedings-template)
- [ACM 官方 Overleaf SIG Proceedings 模板](https://www.overleaf.com/latex/templates/association-for-computing-machinery-acm-sig-proceedings-template/bmvfhcdnxfty)
- [CTAN acmart 稳定版](https://ctan.org/pkg/acmart)

ACM 直接下载地址在准备本项目时返回 HTTP 403，因此实际模板文件取自 CTAN 的官方稳定发行包。它与 Overleaf 官方模板使用相同的 `acmart` 文档类；不是从已登录的 Overleaf 项目导出的副本。
