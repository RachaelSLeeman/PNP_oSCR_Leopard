
# oSCR Analysis for Tourist Image Data with Non-Viable Habitat Exclusion

This README documents the R script for analyzing tourist image data using the oSCR package with a focus on excluding non-viable habitats. The analysis is based on a 2 km² grid over a reserve area, with each grid having a central centroid location. This script was developed by Dr. Rob Davis from Nelson Mandela University & Nottingham Trent University, and the analysis was conducted by Rachael Leeman from Nottingham Trent University. The Pilanesberg shapefiles were provided by Dr. Richard Yarnell, also from Nottingham Trent University.

## Software Requirements
- RStudio 2023.09.1+494 "Desert Sunflower" Release for macOS.
- The script was last run on 13th December 2023.

## Installation
Before running the script, ensure you have the required packages installed. The script uses `githubinstall` and `devtools` to install the `oSCR` package directly from GitHub.

```r
install.packages("githubinstall")
install.packages("devtools")
library(githubinstall)
library(devtools)
install_github("jaroyle/oSCR")
```

## Data Preparation
1. **Capture History & Trap Detection Files**: The script reads in capture history and trap detection data from CSV files. It performs data cleaning and checks on the data.

2. **Setting Up the Analysis Environment**: Specifies the working directory and checks its location.

## Analysis Steps
1. **Data Formatting & State Space Creation**: Formats the data for oSCR analysis, creates an oSCR data object, and generates a state space. It includes setting up session-specific information and making a buffer in GIS for the analysis.

2. **Model Fitting**: Fits various SCR models to the data to explore factors such as sex-specific space use, detection, and session-specific density.

3. **Model Comparison**: Evaluates and compares the fitted models using model selection criteria such as AIC (Akaike Information Criterion).

4. **Model Inference**: Selects a top model based on comparison results and conducts further inference to estimate parameters related to detection, density, and sex-specific behavior.

5. **Data Visualization**: Creates visualizations to display the results, including density maps and plots illustrating sex-specific estimates and session-specific density.

## Outputs
The script outputs an HTML notebook detailing the analysis process and results.

For more information on the methodology and findings, refer to the associated publications and the comments within the script.
