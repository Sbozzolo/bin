<p align="center">
<img width="333" height="204" src="logo.png">
</p>

[![GPLv3
license](https://img.shields.io/badge/License-GPLv3-blue.svg)](http://perso.crans.org/besson/LICENSE.html)

# Installation

Clone this repository and add the folder to your `PATH` environmental variable.
Alternatively, select those scripts you are interested in and move them in your
`bin` folder.

# Scripts

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

## file_or_stdin

```
Check if the argument is an existing file.
If yes, print the input argument, if not, print - (for STDIN).
This utility is meant to be used as part of other scripts,
so that they can handle file and STDIN inputs.
Usage: file_or_stdin {arg}"
```

## merge_pdfs

```
Concatenate multiple PDF files
Usage: merge_pdfs {first pdf file} {second pdf file} ... {output pdf file}
```
`merge_pdfs` requires Ghostscript.

## pick

`pick` is a wrapper around `gawk` to easily select columns from a file
or from standard input. For example, to select the 2nd and 4th column 
of file `file`:
```
pick 2 4 file
```
as opposed to 
```
awk '{print $2, $4}' file
```
or 

```
cut -d" " -f2,4 file
```
`pick` is meant to be low-friction.
```
Select columns from a file or STDIN
Usage: pick {column number 1} {column number 2} ... {file}
```

## pdf_page_extractor

```
Extract a subset of pages from a PDF
Usage: pdf_page_extractor {first page} {last page} {input pdf file} {output pdf file}
```
`pdf_page_extractor` requires Ghostscript.
