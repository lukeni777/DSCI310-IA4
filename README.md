## DSCI 310 individual assignment on Quarto reproducible reports using R

This is a template repository 
for the individual assignment on Quarto reproducible reports using R
from the DSCI 310 (Trustworthy workflows for data science) course.
Instructions for this assignment can be found on the DSCI 310 course website 
[here](https://ubc-dsci.github.io/dsci-310-student/individual_assignment4).

### Dependencies

To complete this assignment you will need to install:
- GNU Make
- Quarto
- R programming language
- R packages:
  - `knitr`
  - `tidyverse`
  - `tinytex`

### License:
The non-software content of this template repository is licensed under the 
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International (CC BY-NC-SA 4.0) License](https://creativecommons.org/licenses/by-nc-sa/4.0/). 
The software content of this template repository licensed under the [MIT License](https://spdx.org/licenses/MIT.html). See the [license file](LICENSE.md) for more information.

###Terminal history for pdf rendering error
(base) Lukes-MacBook-Air:DSCI310-IA4 lukeni$ make
Rscript source/generate_figures.R --input_dir="data/00030067-eng.csv" \
                --out_dir="results"
── Attaching core tidyverse packages ────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────── tidyverse 2.0.0 ──
✔ dplyr     1.1.4     ✔ readr     2.1.5
✔ forcats   1.0.0     ✔ stringr   1.5.1
✔ ggplot2   3.5.1     ✔ tibble    3.2.1
✔ lubridate 1.9.3     ✔ tidyr     1.3.1
✔ purrr     1.0.4     
── Conflicts ──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────── tidyverse_conflicts() ──
✖ dplyr::combine() masks gridExtra::combine()
✖ dplyr::filter()  masks stats::filter()
✖ dplyr::lag()     masks stats::lag()
ℹ Use the conflicted package (<http://conflicted.r-lib.org/>) to force all conflicts to become errors
Warning message:
package ‘purrr’ was built under R version 4.3.3 
Rows: 1000 Columns: 6
── Column specification ──────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
Delimiter: ","
chr (3): GEO, DATE, Vector
dbl (3): Ref_Date, Coordinate, Value

ℹ Use `spec()` to retrieve the full column specification for this data.
ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.
quarto render reports/qmd_example.qmd --to html


processing file: qmd_example.qmd
1/5                  
2/5 [unnamed-chunk-1]
3/5                  
4/5 [unnamed-chunk-2]
5/5                  
output file: qmd_example.knit.md

pandoc 
  to: html
  output-file: qmd_example.html
  standalone: true
  section-divs: true
  html-math-method: mathjax
  wrap: none
  default-image-extension: png
  toc: true
  number-sections: true
  
metadata
  document-css: false
  link-citations: true
  date-format: long
  lang: en
  title: 'DSCI 310: Historical Horse Population in Canada'
  author: Tiffany Timbers & Jordan Bourak
  bibliography:
    - references.bib
  editor: source
  toc-title: Table of Contents
  fig-cap-location: top
  
Output created: qmd_example.html

quarto render reports/qmd_example.qmd --to pdf


processing file: qmd_example.qmd
1/5                  
2/5 [unnamed-chunk-1]
3/5                  
4/5 [unnamed-chunk-2]
5/5                  
output file: qmd_example.knit.md

pandoc 
  to: latex
  output-file: qmd_example.tex
  standalone: true
  pdf-engine: xelatex
  variables:
    graphics: true
    tables: true
  default-image-extension: pdf
  
metadata
  documentclass: scrartcl
  classoption:
    - DIV=11
    - numbers=noendperiod
  papersize: letter
  header-includes:
    - \KOMAoption{captions}{tableheading}
  block-headings: true
  title: 'DSCI 310: Historical Horse Population in Canada'
  author: Tiffany Timbers & Jordan Bourak
  bibliography:
    - references.bib
  editor: source
  

Rendering PDF
running xelatex - 1
  This is XeTeX, Version 3.141592653-2.6-0.999996 (TeX Live 2024) (preloaded format=xelatex)
   restricted \write18 enabled.
  entering extended mode
  
updating tlmgr

updating existing packages
finding package for scrartcl.cls
ERROR: Your TexLive version is not updated enough to connect to the remote repository and download packages. Please update your installation of TexLive or TinyTex.

Underlying message: Local TeX Live (2024) is older than remote repository (2025).
Cross release updates are only supported with
  update-tlmgr-latest(.sh/.exe) --update
See https://tug.org/texlive/upgrade.html for details.


Stack trace:

Underlying message: Local TeX Live (2024) is older than remote repository (2025).
Cross release updates are only supported with
  update-tlmgr-latest(.sh/.exe) --update
See https://tug.org/texlive/upgrade.html for details.

    at findPackages (file:///Applications/quarto/bin/quarto.js:83966:27)
    at eventLoopTick (ext:core/01_core.js:175:7)
    at async findAndInstallPackages (file:///Applications/quarto/bin/quarto.js:84812:30)
    at async initialCompileLatex (file:///Applications/quarto/bin/quarto.js:84704:39)
    at async generatePdf (file:///Applications/quarto/bin/quarto.js:84647:22)
    at async Object.complete (file:///Applications/quarto/bin/quarto.js:84929:27)
    at async file:///Applications/quarto/bin/quarto.js:78314:31
    at async withTimingAsync (file:///Applications/quarto/bin/quarto.js:16879:25)
    at async Object.complete (file:///Applications/quarto/bin/quarto.js:78307:13)
    at async Object.onPostProcess (file:///Applications/quarto/bin/quarto.js:85808:36)
make: *** [reports/qmd_example.pdf] Error 1
