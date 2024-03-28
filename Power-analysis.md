---
title: Power analysis
---
CogStat supports **sensitivity power analysis**. In a sensitivity power analysis, the question is what is the minimal effect size that would provide appropriate power with the given alpha level and sample size. In other words, in the current analysis, what is the minimal effect size that can be shown with appropriate power? Yet, in other words, what is the minimal effect size where the null hypothesis probably can be rejected (i.e., the test will be significant) if the effect is present.

CogStat will calculate the effect size given 95% and (new in v2.5) 80% power, 5% alpha, and the actual sample size.

Note that, in some cases, the modules that CogStat uses to get the power analysis done are occasionally unable to calculate the results. In those cases, CogStat informs the user that the power analysis could not be calculated.

Sensitivity power analysis is available for the following hypothesis tests (see also [here](https://github.com/cogstat/cogstat/issues/120#issuecomment-602016775)):

- One-sample t-test (effect size in d)
- Chi-squared test (effect size in w ([see the description of Phi φ for the w index](http://www.real-statistics.com/chi-square-and-f-distributions/effect-size-chi-square/)))
- Paired t-test (effect size in d)
- Two-sample t-test (effect size in d)
- One-way ANOVA (effect size in eta-square and optionally in f)
