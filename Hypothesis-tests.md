---
title: Hypothesis tests
---
CogStat supports a series of hypothesis tests.

* For the Bayesian tests, CogStat uses the default priors as in [JASP](https://jasp-stats.org/), so that the two software gives the same result (unless you modify the priors in JASP).
* See more details about the special version of some hypothesis tests on the [Differences in calculations between CogStat and other programs](Differences-in-calculations-between-CogStat-and-other-programs) page.

## Available tests

Currently CogStat supports the following hypothesis tests (tests in parenthesis are included in several analysis):

[Explore a variable](Explore-variable):
1. Shapiro-Wilk test
1. One-sample t-test
    - with Bayesian one-sample t-test
1. Wilcoxon signed-rank test

[Explore relation of a variable pair](Explore-relation-of-variable-pair):
1. Pearson correlation hypothesis test
    - with Bayes Factor for Pearson correlation
1. Spearman correlation hypothesis test
1. Chi-squared test

[Compare repeated measures variables](Compare-repeated-measures-variables):
1. (Shapiro-Wilk test)
1. paired t-test
    - with Bayesian paired t-test
1. paired Wilcoxon test
1. repeated measures ANOVA
1. Mauchly's sphericity test (assumption)
1. Holm-Bonferroni corrected post-hoc tests
1. Friedman test
1. Durbin-Conover test
1. McNemar's test
1. Cochran Q-test

[Compare groups](Compare-groups):
1. (Shapiro-Wilk test)
1. modified t-test
1. Mann-Whitney test
1. Levene's test (assumption)
1. two-samples t-test
    - with Bayesian two-samples t-test
1. Welch's t-test
1. one-way ANOVA
1. post hoc Tukey's HSD tests
1. Kruskal-Wallis test
1. post hoc Dunn's test
1. Two-way ANOVA
1. (Chi-squared test)
