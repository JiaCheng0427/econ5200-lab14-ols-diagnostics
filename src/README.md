# OLS Diagnostics: Robust and Clustered Standard Errors

## Objective

I checked how different standard errors affect OLS confidence intervals and how unusual observations can change the slope.

## Methodology

- I simulated data with unequal error variances and data with shocks shared within 40 firms.
- I checked how often the 95% confidence intervals contained the true slope.
- I used leverage, studentized residuals, and Cook’s distance to examine the three added observations.
- I asked AI to write a standard error table function and checked its results against statsmodels.

## Key Findings

- With unequal error variances, coverage was 92.4% with classical standard errors and 94.4% with HC3.
- With errors shared within firms, coverage was 50.3% with HC3 and 93.7% when I clustered by firm.
- One of the added observations pulled the slope from 1.4927 down to 1.4468.
- All 18 standard errors matched statsmodels in Round 1, including after I renamed the columns.
