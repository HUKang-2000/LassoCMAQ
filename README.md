# LassoCMAQ
- LassoCMAQ is a computationally efficient reduced-form CMAQ model, developed using the least absolute shrinkage and selection operator (LASSO) together with an adaptive logit transformation of the response variable.
- It estimates ozone and PM₂.₅ concentrations from regional emission-control scenarios in about 30 seconds per scenario. The model computes concentrations for every grid cell at every hour, enabling rapid what-if exploration without running CMAQ.
## Live Server ##
The live server is available at: xxx

## How to use LassoCMAQ
1. Enter a 17 × 7 emission scenario matrix (Region × Emission Sector) specifying emission change ratios (e.g., 0.9 = 10% reduction from the baseline).
2. Select pollutant(s) and click Run to estimate CMAQ-equivalent concentrations for the selected scenario.
3. Inspect maps and summary metrics; click a grid cell to view the top five influential variables for the corresponding region.
4. Download the scenario inputs and the full model results as needed.
   
## Dependencies
LassoCMAQ uses the following software and R packages:
- R                  (>= 3.6)
- base64enc          (>= xxx)
- bslib              (>= xxx)
- dplyr              (>= xxx)
- DT                 (>= xxx)
- filelock           (>= xxx)
- future             (>= xxx)
- ggplot2            (>= xxx)
- leaflet            (>= xxx)
- promises           (>= xxx)
- RColorBrewer       (>= xxx)
- scales             (>= xxx)
- sf                 (>= xxx)
- shiny              (>= xxx)
- shinycssloaders    (>= xxx)
- shinyjs            (>= xxx)
- shinyWidgets       (>= xxx)
- waiter             (>= xxx)

## Copyright & Contact
- Copyright (c) 2026 Lee, D.-B, Kang, H.-U, Seo, G.-E, Kim, J.-S, Kim, B.-M, Woo, J.-H, and and Hwang, K.-B. All rights reserved. The author retains all rights to this software and documentation
- If you have any questions, please feel free to contact me: kbhwang@ssu.ac.kr

## Citation
- D.-B. Lee et al., A LASSO-based reduced-form CMAQ model for predicting ozone and PM2.5 responses to emission changes in South Korea (submitted)
