---
title: Explore relation of variable pair
---
Choose the `Analysis > Explore relation of variable pair` menu or the `Analysis > Explore relation of variables` menu, and choose the variables you want to analyze, then hit OK.

Differences between the `relation of variable pair` and the `relation of variables` menus:
* In the `relation of variable pair` menu, if you choose more than two variables, all possible pairs will be explored. In a variable pair, the first one will be the predictor and the second one is the predicted variable. If you want to have more than one predictor variables, use the `relation of variables menu`.
    * If the two variables in a pair have different measurement level, then lower measurement level will be used for both variables. For example, for an interval-ordinal pair, CogStat handles them if both variables were ordinal.
* In the `relation of variables` menu, you can choose one or more predictor variables. If you want to see the relation of the variable pairs of the chosen set of variables, use the `relation of variable pair` menu.

In the `Display options...` dialog, the [minimum and maximum of the x and y axes](Displaying-the-data-and-results-graphically#range-of-the-axes) can be set.

The analyses can be used for test-retest reliability analysis. See all the other [reliability analyses](Reliability) that are supported by CogStat.

The following values and graphs will be displayed (see also the [common elements of the results](Common-elements-of-the-analysis-results) for more details):

## Raw data

|Results|For interval data - one predictor|For interval data - several predictors (New in v2.4)|For ordinal data|For nominal data
|-----|-----|------|-----|-----
|Sample size|Number of observed and missing cases | Number of observed and missing cases | Number of observed and missing cases | Number of observed and missing cases
|Raw data|[Scatter plot](https://en.wikipedia.org/wiki/Scatter_plot) of the raw data|[Scatter plot](https://en.wikipedia.org/wiki/Scatter_plot) matrix of the predicted and predictor variables|[Scatter plot](https://en.wikipedia.org/wiki/Scatter_plot) of the raw [order](Displaying-ordinal-and-nominal-data) data|[Mosaic plot](https://en.wikipedia.org/wiki/Mosaic_plot)

On scatter plots, the size of a dot is proportional with the number of cases with that value pair.

## Sample properties

|Results|For interval data - one predictor|For interval data - several predictors (New in v2.4)|For ordinal data|For nominal data
|-----|-----|------|-----|-----
|Descriptive data|Equation of the linear regression line|Equation of the linear regression line| |[Contingency table](https://en.wikipedia.org/wiki/Contingency_table) (case count)<br>Contingency table (percentage)
|Graphs of the data|[Scatter plot](https://en.wikipedia.org/wiki/Scatter_plot) with regression line|[Scatter plot](https://en.wikipedia.org/wiki/Scatter_plot) with regression line<br>[Partial regression plots](https://en.wikipedia.org/wiki/Partial_regression_plot) with regression line| |
|[Standardized effect sizes](Standardized-effect-sizes)|[Pearson](https://en.wikipedia.org/wiki/Pearson_product-moment_correlation_coefficient) and [Spearman](https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient) correlation coefficient|R<sup>2</sup>, Log-likelihood, [AIC](https://en.wikipedia.org/wiki/Akaike_information_criterion), [BIC](https://en.wikipedia.org/wiki/Bayesian_information_criterion), and Pearson's partial correlations|[Spearman correlation coefficient](https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient)|[Cramér's V](https://en.wikipedia.org/wiki/Cram%C3%A9r%27s_V)
|[Residual analysis](https://en.wikipedia.org/wiki/Errors_and_residuals)|(New in v2.3) Residual plot and histogram of residuals|Residual plot and histogram of residuals| |

On scatter plots the size of a dot is proportional with the number of cases with that value pair.

## Population properties

|Results|For interval data - one predictor|For interval data - several predictors (New in v2.4)|For ordinal data|For nominal data
|-----|-----|------|-----|-----
|Assumptions of inferential methods|(New in v2.3) Henze-Zirkler test of [multivariate normality](https://en.wikipedia.org/wiki/Multivariate_normal_distribution)<br><br>(New in v2.3) Koenker's test and [White's test](https://en.wikipedia.org/wiki/White_test) of [homoscedasticity](https://en.wikipedia.org/wiki/Homoscedasticity_and_heteroscedasticity)|Henze-Zirkler test of [multivariate normality](https://en.wikipedia.org/wiki/Multivariate_normal_distribution)<br><br>Koenker's test and [White's test](https://en.wikipedia.org/wiki/White_test) of [homoscedasticity](https://en.wikipedia.org/wiki/Homoscedasticity_and_heteroscedasticity)<br><br>[Variance inflation factors](https://en.wikipedia.org/wiki/Variance_inflation_factor) (VIF) to test [multicollinearity](https://en.wikipedia.org/wiki/Multicollinearity)<br><br>If VIF is larger than 10 for a variable, then (a) betas of the other regressors predicting that variable, and (b) correlations of the predictors are also displayed.| |
|Population parameters|(New in v2.3) Slope and intercept point estimations with 95% confidence intervals|Slopes and intercept point estimations with 95% confidence intervals| |Contingency table (confidence interval, multinomial proportions with Goodman method)
|Graphs of the population parameters|(New in v2.3) Linear regression line with 95% confidence interval| | |
|[Standardized effect sizes](Standardized-effect-sizes)|[Pearson](https://en.wikipedia.org/wiki/Pearson_product-moment_correlation_coefficient) and [Spearman](https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient) correlation coefficient, and their confidence intervals|[Adjusted R<sup>2</sup>](https://en.wikipedia.org/wiki/Coefficient_of_determination#Adjusted_R2), Pearson's partial correlations, and their confidence intervals|[Spearman correlation coefficient](https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient) and its confidence interval|
|[Hypothesis test](Hypothesis-tests) and [sensitivity power analyses](Power-analysis)|p values for correlation coefficients<br><br>(New in v2.3) Bayesian hypothesis test for Pearson correlation|Model F-test and test for the regressor slopes|p value for correlation coefficient|[Chi-squared test](https://en.wikipedia.org/wiki/Pearson%27s_chi-squared_test) and [sensitivity power analyses](Power-analysis)
