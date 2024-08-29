---
title: Compare repeated measures variables
---
From the `Analysis` menu choose `Compare repeated measures variables`, and choose the variables you want to compare, then hit OK.

To use several factors, click on `Factors...` and set the names and the levels of the factors, and click OK. Then, you can select the variables for the factor level combinations.

* Only the cases where all variables are available are used.
* Variables to be compared have to have the same measurement levels.

In the `Display options...` dialog, [the minimum and maximum of the y-axis](Displaying-the-data-and-results-graphically#range-of-the-axes), and (new in v2.4) [the way factors are displayed](Displaying-the-data-and-results-graphically#displaying-factors-and-groups-in-x-axis-colors-and-panels) can be set.

The following results will be calculated (see also the [common elements of the results](Common-elements-of-the-analysis-results)):

## Raw data

|Result|For interval variables|For ordinal variables|For nominal variables
|---|---|---|---|
|Sample size | Number of observed cases | Number of observed cases | Number of observed cases
|Graphs of the raw data|Spaghetti plot showing individual data|Spaghetti plot showing individual data|[Mosaic plot](https://en.wikipedia.org/wiki/Mosaic_plot)

For individual data plots, [values of a single case are connected](Displaying-individual-data-in-repeated-measures-variables).

## Sample properties

|Result|For interval variables|For ordinal variables|For nominal variables
|---|---|---|---|
|Descriptive data|Means, [Standard deviations](https://en.wikipedia.org/wiki/Standard_deviation), Maximums, [Upper quartiles](https://en.wikipedia.org/wiki/Quartile), [Medians](https://en.wikipedia.org/wiki/Median), Lower quartiles, Minimums|Maximums, [Upper quartiles](https://en.wikipedia.org/wiki/Quartile), [Medians](https://en.wikipedia.org/wiki/Median), Lower quartiles, Minimums|[Variation ratio](https://en.wikipedia.org/wiki/Variation_ratio), [Contingency table](https://en.wikipedia.org/wiki/Contingency_table) (case count), Contingency table (percentage)
|[Standardized effect size](Standardized-effect-sizes)|For two groups Cohen's d and eta-squared
|Graphs of the data|Box plot showing quartiles with spaghetti plot showing individual data|Box plot showing quartiles with spaghetti plot showing individual data|

For individual data plots, [values of a single case are connected](Displaying-individual-data-in-repeated-measures-variables).

## Population properties

|Result|For interval variables|For ordinal variables|For nominal variables
|---|---|---|---|
|Population parameters numerically|Mean with 95% CI|Median and its confidence interval|Contingency table (confidence interval, multinomial proportions with Goodman method)
|[Standardized effect size](Standardized-effect-sizes)|For two groups, Hedges' g and its confidence interval
|Graphs of the population parameters|Graph with mean and 95% CI of the mean| | 
|[Hypothesis test](Hypothesis-tests) for two variables and [sensitivity power analyses](Power-analysis)|If the data are normal (measured with [Shapiro-Wilk test](https://en.wikipedia.org/wiki/Shapiro%E2%80%93Wilk_test)), then [paired t-test](https://en.wikipedia.org/wiki/Student%27s_t-test) and (new in v2.3) Bayesian paired t-test<br><br>Otherwise, [paired Wilcoxon test](https://en.wikipedia.org/wiki/Wilcoxon_signed-rank_test) (see [CogStat specific](Differences-in-calculations-between-CogStat-and-other-programs#wilcoxon-signed-rank-test) details)<br><br>For paired t-test [sensitivity power analyses](Power-analysis)|[Paired Wilcoxon test](https://en.wikipedia.org/wiki/Wilcoxon_signed-rank_test) (see [CogStat specific](Differences-in-calculations-between-CogStat-and-other-programs#wilcoxon-signed-rank-test) details)|If the variables are dichotomous, then [McNemar's test](https://en.wikipedia.org/wiki/McNemar%27s_test)<br><br>Otherwise, no test is provided by CogStat
|[Hypothesis test](Hypothesis-tests) for more than two variables|If the data are normal (measured with [Shapiro-Wilk test](https://en.wikipedia.org/wiki/Shapiro%E2%80%93Wilk_test)) [repeated measures ANOVA](https://en.wikipedia.org/wiki/Repeated_measures_design#Repeated_measures_ANOVA)<br>For ANOVA, sphericity is checked with [Mauchly's sphericity test](https://en.wikipedia.org/wiki/Mauchly%27s_sphericity_test). If sphericity is violated, [Greenhouse-Geisser correction](https://en.wikipedia.org/wiki/Mauchly%27s_sphericity_test#Violations_of_sphericity) is applied.<br>If ANOVA is significant, [Holm-Bonferroni corrected](https://en.wikipedia.org/wiki/Holm%E2%80%93Bonferroni_method) post-hoc tests are run.<br><br>For non-normal variables [Friedman test](https://en.wikipedia.org/wiki/Friedman_test)<br>(New in v2.3) If the Friedman test is significant, post hoc Durbin-Conover test|[Friedman test](https://en.wikipedia.org/wiki/Friedman_test)<br>(New in v2.3) If the Friedman test is significant, post hoc Durbin-Conover test|If the variables are dichotomous, then [Cochran Q-test](https://en.wikipedia.org/wiki/Cochran%27s_Q_test)<br><br>Otherwise, no test is provided by CogStat
|[Hypothesis test](Hypothesis-tests) for two factors|[Repeated measures ANOVA](https://en.wikipedia.org/wiki/Repeated_measures_design#Repeated_measures_ANOVA)||
