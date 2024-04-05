# Enhancing TV Product Strategy: Conjoint Analysis Insights Project

## Importance

The application of conjoint analysis in this context addresses a critical need within the consumer electronics sector for empirical, consumer-driven data to guide product development and marketing strategies. In a market characterized by rapid technological advancements and intense competition, understanding and meeting consumer expectations become paramount for any brand striving for relevance and growth. This analysis not only uncovers consumer preferences but also identifies how these preferences stack against the offerings of competitors like Sony and Sharp, offering a clear competitive edge. As a result, manufacturers can more accurately align their products with consumer demands, optimize pricing, and strategically position themselves in the market, significantly boosting their potential for innovation and profitability.

## Overview

This project leverages conjoint analysis to dissect and understand consumer preferences in the TV product category, focusing on the evaluation of how different product attributes influence buyer choices. By dissecting the value placed on various features by consumers, the analysis provides a strategic foundation for TV manufacturers to innovate within their product lines. Insights gained from this study are pivotal in navigating the competitive dynamics of the consumer electronics market, especially against established giants like Sony and Sharp. The project's outcome aims at informing decisions on product design, optimal pricing strategies, and market positioning to enhance market share and profitability.

## Project Structure

- `TV-UserProfilePreferences.xlsx`: Input data file containing the customer preferences and the design matrix used in the analysis.
- `TV-ConjointAnalysis.Rmd`: This R Markdown script contains the function that performs the conjoint analysis.
- `TV-ConjointAnalysis.html`: The HTML output for conjoint analysis.
- `TV-ConjointAnalysis-Report.pdf`: A detailed report on conjoint analysis, methodology, and project findings.

## Functionality

The main function is designed to accept input in the form of preference rankings and produce outputs that include partworths, attribute importance, willingness to pay for each non-price attribute level, optimal price, maximum profit, and associated market share.

### Inputs

To perform the conjoint analysis, the inputs are as follows:

- Preference Rankings: A reverse rank ordered matrix (24 x 1) with rankings from best (24) to worst (1), created through a binary split process based on the profile preferences.

- Cost Estimates: The cost_estimates in the script should be updated to reflect the latest market or production cost information for each attribute level.

- Design Variables: Adjust the attribute values in my_design, sony_design, and sharp_design within the script to match the specific product scenarios being analyzed. This ensures the analysis reflects current market conditions and competitive strategies.

These inputs are crucial for accurately capturing consumer preferences and the cost implications of different product attributes, which are central to the conjoint analysis and the determination of WTP.

#### Binary Split Process

To rank profiles accurately:

1. Split the 24 profiles into good and not-so-good.
2. Apply this binary split process to the set of good profiles and create two sets: very good and good ones.
3. Repeat the binary split process for not-so-good profiles to create average and below average sets. 4. Next, assign points 60-70 to the below average set, 71 to 80 for the average set, 81 to 90 points to the good set, and 91 to 100 to the very good set.
4. Finally, reverse sort all the 24 profiles based on 60 to 100 ratings and assign rank of 24 (highest rating) to 1 (smallest rating). That way we will get the ranked preferences for all the profiles.

### Outputs

1. Partworths for each attribute level.
2. Attribute importance for each attribute.
3. Willingness to pay for each non-price attribute level.
4. Optimal price for the product.
5. Maximum profit that can be obtained.
6. Market share associated with the optimal price.
7. Visual representation of market shares and sales as a function of prices.
8. Profit plotted as a function of prices.

## Usage

To run the conjoint analysis, follow these steps:

1. Ensure that R is installed on your machine.
2. Open the `TV-ConjointAnalysis.Rmd` file in R or RStudio.
3. Install any required libraries that are listed at the start of the script if you haven't already (e g., readxl, dplyr, purrr, stringr, ggplot2).
4. Update your preferences in the `TV-UserProfilePreferences.xlsx` file accordingly.
5. Update the cost associated with each attribute level (cost_estimates) to reflect the latest market or production cost information. This ensures that your profitability and willingness to pay analyses are based on current economic conditions.
6. Design Variables (my_design, sony_design, sharp_design):

   For each of these configurations, you will retain the same attributes (e.g., screen size, resolution, brand, price) but update the values to reflect the new scenarios you wish to analyze. This could involve changing the price level to test different market positions or adjusting the screen size to see how it impacts consumer preferences and competitive advantage.

7. Run the script.

## License

This project is licensed under the "MIT License".

## Acknowledgements

This project was made possible by the contributions and guidance of several individuals:

- Professor Prasad Naik, co-founder of the MSBA program at UC Davis and professor for Advanced Statistics, whose teachings have been instrumental in the execution of this project.
- Special thanks to my classmates for their collaboration and contributions:

  - Sujai Aditya Muralidaran
  - Kritikka FNU
  - Sushma Niveni Pindiga
  - Ruben Cases
