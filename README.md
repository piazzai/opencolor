<!--
opencolor v1.0.1
Author: Michele Piazzai
Contact: michele.piazzai@uc3m.es
License: MIT
-->

# opencolor

This is a simple LaTeX package that provides hexadecimal color definitions of the 130 colors included in the [Open Color](https://yeun.github.io/open-color/) library (v1.9.1). Open Color's goal is to provide a selection of colors optimized for UI design. Although LaTeX is a typesetting system primarily intended for print, many of the documents it produces never get printed, in which case it makes sense to use colors suitable for on-screen reading.

Open Colors are organized according to 13 hues (gray, red, pink, grape, violet, indigo, blue, cyan, teal, green, lime, yellow, orange) and 10 brightness levels (0–9). The naming convention is `oc-(color)-(number)`. At the same brightness level, the perceived brightness of different hues aims to be constant.

The package's only dependency is [xcolor](https://www.ctan.org/pkg/xcolor), which is included in most LaTeX distributions.

## Demo

![](https://github.com/piazzai/opencolor/blob/master/demo-opencolor.png)

## Installation

The package is hosted on CTAN and distributed as part of MikTeX and TeXLive. It can also be installed manually by cloning this repository in your `$HOME/texmf/tex/latex` folder. If you do not have this folder, [you can create it](https://www.ias.edu/math/computing/faq/local-latex-style-files).

## Usage

The choice of colors for a document is a responsibility of the author, but UI design principles can provide helpful guidelines. For example, in a beamer presentation, `oc-gray-1` could be used instead of white and `oc-gray-9` instead of black in order to reduce eye strain. If a color like `oc-teal-6` is used for a plot, then it would be best for other plots to use colors at the same brightness level, like `oc-orange-6`, for visual consistency.

## Minimal working example

```tex
\documentclass{article}

\usepackage{opencolor}

\begin{document}
    \textcolor{oc-red-8}{Hello}
    \textcolor{oc-blue-6}{,}
    \textcolor{oc-lime-9}{world}
    \textcolor{oc-grape-7}{!}
\end{document}
```

## Bugs

The package merely loads xcolor and then provides color definitions, so any error or warning is most likely due to xcolor. Nonetheless, if you encounter any problem using this package, please [open an issue](https://github.com/piazzai/opencolor-latex/issues).
