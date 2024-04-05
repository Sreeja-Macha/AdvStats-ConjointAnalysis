# TV Product Evaluation: Bootstrapped Willingness-to-Pay Analysis

## Importance

Bootstrapped Willingness-to-Pay Analysis is critical for accurately gauging consumer valuation of product attributes, providing manufacturers with precise, confidence-backed data on customer spending thresholds for specific features. This refined insight supports strategic product and pricing decisions in the consumer electronics market, enhancing competitive positioning and market responsiveness.

## Overview

This project extends the previous conjoint analysis work by focusing on obtaining confidence intervals for willingness to pay (WTP) for TV product attributes using bootstrap regression techniques. It evaluates the WTP based on customer preferences and provides a 95% confidence interval for each non-price attribute level.

## Project Files

- `TV-UserProfilePreferences.xlsx`: Input data file containing the customer preferences and the design matrix used in the analysis.
- `TV-Bootstrapped-WTPAnalysis.Rmd`: The R Markdown script for executing the bootstrap regression analysis.
- `TV-Bootstrapped-WTPAnalysis.html`: The HTML output with the bootstrapped WTP analysis results.
- `TV-Bootstrapped-WTPAnalysis-Report.pdf`: Comprehensive report detailing the findings and interpretations of the bootstrapped WTP analysis.

## Inputs and Outputs

### Inputs

- **Preference Data**: A matrix of customer preferences for 24 TV product profiles, stored in `TV-UserProfilePreferences.xlsx`.
- **Bootstrap Parameters**: Specification for the number of bootstrap samples as set in the R Markdown script.

### Outputs

- **Confidence Intervals for WTP**: For each non-price attribute level, the algorithm will output:
  - Mean WTP estimate.
  - Lower and upper bounds of the 95% confidence interval from residual bootstrap.
  - Lower and upper bounds of the 95% confidence interval from data bootstrap.
- These outputs will be presented in the `TV-Bootstrapped-WTPAnalysis.html` file for each customer.

## Usage

To conduct this analysis:

1. Confirm that R and all required libraries are installed.
2. Open the `TV-Bootstrapped-WTPAnalysis.Rmd` in RStudio to execute the analysis.
3. Set `resampling_trials` to the desired number of bootstrap samples.
4. Run and inspect the bootstrapped WTP results in the generated `TV-Bootstrapped-WTPAnalysis.html`.

## License

This project is released under the "MIT License".

## Acknowledgements

This project was made possible by the contributions and guidance of several individuals:

- Professor Prasad Naik, Co-founder of the MSBA program at UC Davis and professor for Advanced Statistics, whose teachings have been instrumental in the execution of this project.
- Special thanks to my classmates for their collaboration and contributions:

  - Sujai Aditya Muralidaran
  - Kritikka FNU
  - Sushma Niveni Pindiga
  - Ruben Cases
