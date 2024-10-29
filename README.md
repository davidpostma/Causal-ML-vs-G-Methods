# Causal-ML-vs-G-Methods
A longitudinal causal machine learning in Python (random forest from econML package) contrasted with the longitudinal g-methods in R (ipw and gfoRmula packages) using the same simulation that attempted to capture the complexity of real-world observational data. 

The inverse probability treatment weighting was performed in a pooled-logistic regression in a time-varying analysis of continuous exposure. There are 10 yearly observations per id (n=10,000), with treatment adherence modeled with Beta(5,2) distribution, and 5% missing data handled with mean imputation. The simulated dataset included a complex binary outcome generation, including time-varying effects through sin(time/2), treatment-adherence interactions, non-linear covariate effects, and treatment-comorbidity interactions. Competing risks were included in the causal ML, but not in the g-methods yet. Comprehensive diagnostics were made for longitudinal data structure, time-varying patterns, data quality, and causal assumptions.

Methodology Notes:
-Treatment is handled as a continuous variable
-Missing data is addressed through mean imputation
-Time-varying confounding is accounted for in both methods
-Bootstrap is used for confidence intervals in g-formula
-Robust variance estimation is used for IPTW

This R implementation parallels a Python-based Causal Forest analysis with matching:
-Data generation processes
-Variable relationships
-Missing data mechanisms
-Time-varying effects

This independent project is still a work in progress and I have yet to fully interpret the findings or the robustness, and for a full disclaimer, Claude 3.5 Sonnet had greatly helped with my initial exploration of this comparison. 
Please refer to the corresponding package vignettes (EconML, ipw, and gfoRmula) for much more reliable examples of these packages. I was curious to compare the outputs on the same simulation.

Contributions are welcome, please feel free to submit a pull request!
