# LassoCMAQ
- LassoCMAQ is a computationally efficient reduced-form CMAQ model, developed using the least absolute shrinkage and selection operator (LASSO) together with an adaptive logit transformation of the response variable.
- It estimates ozone and PM<sub>2.5</sub> concentrations from regional emission-control scenarios in about 30 seconds per scenario. The model computes concentrations for every grid cell at every hour, enabling rapid what-if exploration without running CMAQ.
- The live server is available at: xxx

## How to use LassoCMAQ
1. Enter a 17 × 7 emission scenario matrix (Region × Emission Sector) specifying emission change ratios (e.g., 0.9 = 10% reduction from the baseline).
2. Select pollutant(s) and click Run to estimate CMAQ-equivalent concentrations for the selected scenario.
3. Inspect maps and summary metrics; click a grid cell to view the top five influential variables for the corresponding region.
4. Download the scenario inputs and the full model results as needed.
   
## Dependencies
LassoCMAQ uses the following software and R packages:
- R                  (>= 4.5)
- base64enc          (>= 0.1.3)
- bslib              (>= 0.9.0)
- dplyr              (>= 1.1.4)
- DT                 (>= 0.33)
- filelock           (>= 1.0.3)
- future             (>= 1.67.0)
- ggplot2            (>= 3.5.2)
- leaflet            (>= 2.2.3)
- promises           (>= 1.3.3)
- RColorBrewer       (>= 1.1.3)
- scales             (>= 1.4.0)
- sf                 (>= 1.0.21)
- shiny              (>= 1.11.1)
- shinycssloaders    (>= 1.1.0)
- shinyjs            (>= 2.1.1)
- shinyWidgets       (>= 0.9.0)
- waiter             (>= 0.2.5.1)

## Copyright & Contact
- Copyright (c) 2026 Lee, D.-B, Kang, H.-U, Seo, G.-E, Kim, J.-S, Kim, B.-M, Woo, J.-H, and and Hwang, K.-B. All rights reserved. The author retains all rights to this software and documentation.
- If you have any questions, please feel free to contact me: kbhwang@ssu.ac.kr

## Citation
- D.-B. Lee et al., A LASSO-based reduced-form CMAQ model for predicting ozone and PM<sub>2.5</sub> responses to emission changes in South Korea (submitted)

## Installation
Download the source code and dataset, and place them in the current working directory.
### Source code
```sh
gdown 1UvxVWDeCWfdw7a9Rd1tgwpVvenb449xs -O LassoCMAQ_Source_code.tar.gz
```
### Dataset
```sh
gdown 1e9j8Cx3CPUFFajw28ikqiTwnZJZRBljc -O LassoCMAQ_Data.tar.gz
```

## Usage
1. Create a working directory and extract the downloaded files:
```sh
mkdir LassoCMAQ

tar -xvzf LassoCMAQ_Source_code.tar.gz -C LassoCMAQ
tar -xvzf LassoCMAQ_Data.tar.gz -C LassoCMAQ
```
2. Open LassoCMAQ/LassoCMAQ_Source/app.R and set BASE_DIR to the directory containing the extracted LassoCMAQ folder.
3. Move to the source directory:
'''sh
cd LassoCMAQ/LassoCMAQ_Source/
'''
4. Run the Shiny app
```sh
nohup Rscript app.R> run_log.txt 2>&1 &
```
