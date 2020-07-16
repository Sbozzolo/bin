<p align="center">
<img width="333" height="204" src="logo.png">
</p>

[![GPLv3
license](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html)

## cleanup_tikz_file

```
LaTeX engines have strong memory limitations, and sometimes it is not possible
to compile TikZ figures. To work around this, one can reduce the density of
points and reduce the precision of their numerical representation.

cleanup_tikz_file takes a file as input, detects lines with two numbers (the data),
and keeps only one every N. All the data is put in scientific notation with
precition of 4.

If the file is not supplied, text is read from STDIO. If N is not provided,
all the data is kept but it is still re-printed in scientific notation.


Usage: cleanup_tikz_file takes {N} {file}
```

## merge_pdfs

```
Concatenate multiple PDF files
Usage: merge_pdfs {first pdf file} {second pdf file} ... {output pdf file}
```
`merge_pdfs` requires Ghostscript.

## pdf_page_extractor

```
Extract a subset of pages from a PDF
Usage: pdf_page_extractor {first page} {last page} {input pdf file} {output pdf file}
```
`pdf_page_extractor` requires Ghostscript.
