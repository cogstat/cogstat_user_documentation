From the `Analysis` menu choose `Compare groups`, and choose the dependent variable(s) you want to analyze, choose the `Grouping variable`, then hit OK.

In the `Display options...` dialog, [the minimum and maximum of the y-axis](Displaying-the-data-and-results-graphically#range-of-the-axes), and (new in v2.4) [the way groups are displayed](Displaying-the-data-and-results-graphically#displaying-factors-and-groups-in-x-axis-colors-and-panels) can be set.

The following results will be calculated (see also the [common elements of the results](Common-elements-of-the-analysis-results)):

## Raw data

|Result|For interval variables|For ordinal variables|For nominal variables
|---|---|---|---|
|Sample size | Number of observed cases | Number of observed cases | Number of observed cases
|Graphs of the raw data|Plot with individual data|Plot with individual data ([order of the values](Displaying-ordinal-and-nominal-data))|[Mosaic plot](https://en.wikipedia.org/wiki/Mosaic_plot)

## Sample properties

|Result|For interval variables|For ordinal variables|For nominal variables
|---|---|---|---|
|Descriptive data|Means, [Standard deviations](https://en.wikipedia.org/wiki/Standard_deviation), Maximums, [Upper quartiles](https://en.wikipedia.org/wiki/Quartile), [Medians](https://en.wikipedia.org/wiki/Median), Lower quartiles, Minimums|Maximums, [Upper quartiles](https://en.wikipedia.org/wiki/Quartile), [Medians](https://en.wikipedia.org/wiki/Median), Lower quartiles, Minimums|[Variation ratio](https://en.wikipedia.org/wiki/Variation_ratio), [Contingency table](https://en.wikipedia.org/wiki/Contingency_table) (case count), Contingency table (percentage)
|[Standardized effect size](Standardized-effect-sizes)|For two groups Cohen's d and eta-squared| |[Cramér's V](https://en.wikipedia.org/wiki/Cram%C3%A9r%27s_V)
|Graphs of the data|[Box plot](Box-plots) with individual data|[Box plot](Box-plots) with individual data ([order of the values](Displaying-ordinal-and-nominal-data))|

## Population properties

|Result|For interval variables|For ordinal variables|For nominal variables
|---|---|---|---|
|Population parameters numerically|Mean with 95% CI|Median and its confidence interval|Contingency table (confidence interval, multinomial proportions with Goodman method)
|Graphs of the population parameters|Graph with mean and 95% CI of the mean| | 
|[Standardized effect size](Standardized-effect-sizes)|* For two groups, Hedges' g and its confidence interval<br>* If one-way ANOVA was run, then [omega-squared effect size](https://en.wikipedia.org/wiki/Effect_size#Omega-squared_(%CF%892)).| | 
|[Hypothesis test](Hypothesis-tests) for two groups and [sensitivity power analyses](Power-analysis)|When one of the groups includes a [single case](Single-case-analyses), if control group is normal (measured with [Shapiro-Wilk test](https://en.wikipedia.org/wiki/Shapiro%E2%80%93Wilk_test)) then [modified t-test](Single-case-analyses), otherwise [Mann-Whitney test](https://en.wikipedia.org/wiki/Mann%E2%80%93Whitney_U_test). If the `Single case slope` is set, then [slope comparison](Single-case-analyses).<br><br>For comparing two groups if the data are normal (measured with [Shapiro-Wilk test](https://en.wikipedia.org/wiki/Shapiro%E2%80%93Wilk_test)) and [homoscedastic](https://en.wikipedia.org/wiki/Homoscedasticity) (measured with [Levene's test](https://github.com/cogstat/cogstat/wiki/Differences-in-calculations-between-CogStat-and-other-programs#levenes-test)), then [two-sample t-test](https://en.wikipedia.org/wiki/Student%27s_t-test) and (new in v2.3) Bayesian two-samples t-test<br>For non-normal groups, [Mann-Whitney test](https://en.wikipedia.org/wiki/Mann%E2%80%93Whitney_U_test)<br>For normal but heteroscedastic groups, [Welch's t-test](https://en.wikipedia.org/wiki/Welch%27s_t-test)<br>Confidence interval of the difference of the groups<br><br>For two-sample t-test [sensitivity power analyses](Power-analysis)|[Mann-Whitney test](https://en.wikipedia.org/wiki/Mann%E2%80%93Whitney_U_test)|[Chi-squared test](https://en.wikipedia.org/wiki/Pearson%27s_chi-squared_test) and [sensitivity power analyses](Power-analysis)
|[Hypothesis test](Hypothesis-tests) for more than two groups and [sensitivity power analyses](Power-analysis)|If the data are normal (measured with [Shapiro-Wilk test](https://en.wikipedia.org/wiki/Shapiro%E2%80%93Wilk_test)) and [homoscedastic](https://en.wikipedia.org/wiki/Homoscedasticity) (measured with [Levene's test](https://github.com/cogstat/cogstat/wiki/Differences-in-calculations-between-CogStat-and-other-programs#levenes-test)) [one-way ANOVA](https://en.wikipedia.org/wiki/One-way_analysis_of_variance)<br>If ANOVA is significant, post hoc [Tukey's HSD tests](https://en.wikipedia.org/wiki/Tukey%27s_range_test)<br><br>Otherwise, [Kruskal-Wallis test](https://en.wikipedia.org/wiki/Kruskal%E2%80%93Wallis_one-way_analysis_of_variance)<br>If the Kruskal-Wallis test is significant, post hoc [Dunn's test](https://en.wikipedia.org/wiki/Kruskal%E2%80%93Wallis_one-way_analysis_of_variance)<br><br>For one-way ANOVA [sensitivity power analyses](Power-analysis) displayed as eta-square and as f.|[Kruskal-Wallis test](https://en.wikipedia.org/wiki/Kruskal%E2%80%93Wallis_one-way_analysis_of_variance)<br><br>If the Kruskal-Wallis test is significant, post hoc [Dunn's test](https://en.wikipedia.org/wiki/Kruskal%E2%80%93Wallis_one-way_analysis_of_variance)|[Chi-squared test](https://en.wikipedia.org/wiki/Pearson%27s_chi-squared_test) and [sensitivity power analyses](Power-analysis)
|[Hypothesis test](Hypothesis-tests) for two or more grouping variables|[Two-way ANOVA](https://en.wikipedia.org/wiki/Two-way_analysis_of_variance) or multi-way ANOVA ||
