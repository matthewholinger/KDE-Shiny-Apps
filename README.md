# KDE Shiny Apps

This repository contains two R Shiny applications for KDE-based spatial analysis.

## Apps

### KDE_Original
Original workflow for 2D or 3D KDE analysis, including standard depth jitter for 3D data.

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

## Notes:

To run the application locally, users need R and the required package dependencies installed. The application was developed and tested in R version 4.5.2.

After installing the required packages, the user simply sets the working directory to the application folder and launches the Shiny app.

Here is a YouTube Tutorial https://www.youtube.com/watch?v=e_gPvsluPT8 

## How to Run Locally

1. Open RStudio.
2. Open the desired app folder.
3. Set working directory.
Example:
        setwd("~/Desktop/KDE_Manatee")
5. Make sure `app.R` is inside the folder.
6. Set source in console using code below. Once that is set, then run shiny:runApp()

```r
source("app.R")

shiny::runApp()

