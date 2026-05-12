# KDE Shiny Apps

This repository contains two R Shiny applications for KDE-based spatial analysis.

## Apps

### KDE_Original
Original workflow for 2D/3D KDE analysis, including standard depth jitter for 3D data.

### KDE_Manatee
Manatee-specific 3D workflow using habitat-depth-based jitter. Surface and floor points are not jittered. The water column is divided into:
- shallow: top quarter
- middle: middle half
- deep: bottom quarter

## Required packages
install.packages(c(
  "shiny", "readxl", "ks", "rgl", "misc3d", "dplyr",
  "htmlwidgets", "ggplot2", "rjson", "shinyFiles",
  "zip", "shinyWidgets"
))

## How to Run Locally

1. Open RStudio.
2. Open the desired app folder.
3. Make sure `app.R` is inside the folder.
4. Run:

```r
shiny::runApp()

