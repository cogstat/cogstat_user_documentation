From the `Analysis` menu choose `Explore variable`, and choose the variable(s) you want to analyze, then hit OK.

* Optionally, uncheck the Frequencies, if you want to skip that analysis.
* Optionally, change the central tendency value, if your hypothesis is a different value.

The following values and graphs will be displayed (see also the [common elements of the results](Common-elements-of-the-analysis-results)):

## Raw data

|Results|For interval data|For ordinal data|For nominal data
|-----|-----|------|-----
|Sample size|Number of observed and missing cases | Number of observed and missing cases | Number of observed and missing cases
|Raw data|[Dot plot](https://en.wikipedia.org/wiki/Dot_plot_(statistics))|[Dot plot](https://en.wikipedia.org/wiki/Dot_plot_(statistics)) of [the order of the values](Displaying-ordinal-and-nominal-data)|[Histogram](https://en.wikipedia.org/wiki/Histogram)

## Sample properties

|Results|For interval data|For ordinal data|For nominal data
|-----|-----|------|-----
|Frequencies|Table of all values in the variable with the following details:<br>* Value<br>* Frequency<br>* Relative frequency (percentage of that value of all cases)<br>* Cumulative frequency<br>* Cumulative relative frequency|Table of all values in the variable with the following details:<br>* Value<br>* Frequency<br>* Relative frequency (percentage of that value of all cases)<br>* Cumulative frequency<br>* Cumulative relative frequency|Table of all values in the variable with the following details:<br>* Value<br>* Frequency<br>* Relative frequency (percentage of that value of all cases)
|Descriptive statistics|Mean<br>[Standard deviation](Differences-in-calculations-between-CogStat-and-other-programs#standard-deviation-of-the-sample-and-the-population)<br>[Skewness](https://en.wikipedia.org/wiki/Skewness)<br>[Kurtosis](https://en.wikipedia.org/wiki/Kurtosis)<br>[Range](https://en.wikipedia.org/wiki/Range_(statistics))<br>Maximum<br>[Upper quartile](https://en.wikipedia.org/wiki/Quartile)<br>[Median](https://en.wikipedia.org/wiki/Median)<br>Lower quartile<br>Minimum|Maximum<br>[Upper quartile](https://en.wikipedia.org/wiki/Quartile)<br>[Median](https://en.wikipedia.org/wiki/Median)<br>Lower quartile<br>Minimum|[Variation ratio](https://en.wikipedia.org/wiki/Variation_ratio)
|Graphs of the data |Combined graph of histogram, individual data on x axes and [box plot](Box-plots)|Combined graph of histogram, individual data on x axes and [box plot](Box-plots) of [the order of the values](Displaying-ordinal-and-nominal-data)|

## Population properties

|Results|For interval data|For ordinal data|For nominal data
|-----|-----|------|-----
|Normality|* [Shapiro-Wilk test](https://en.wikipedia.org/wiki/Shapiro%E2%80%93Wilk_test)<br>* Histogram with normal distribution (normal distribution has the same average and standard deviation as the data)<br>* [Q-Q plot](https://en.wikipedia.org/wiki/Q%E2%80%93Q_plot) |(Only for interval variables)|(Only for interval variables)
|Parameter estimation|* Mean and its [confidence interval](https://github.com/cogstat/cogstat/wiki/Differences-in-calculations-between-CogStat-and-other-programs#confidence-interval-of-the-mean)<br>* Standard deviation and its confidence interval|Median and its confidence interval|Confidence interval of the relative frequencies (multinomial proportions with Goodman method)
|Graphs of the population parameters|Graph with mean and confidence interval or median for non-normal variable|Graph with median
|[Hypothesis test](Hypothesis-tests) and [sensitivity power analyses](Power-analysis)|If the data are normal (measured with [Shapiro-Wilk test](https://en.wikipedia.org/wiki/Shapiro%E2%80%93Wilk_test)), then [one-sample t-test](https://en.wikipedia.org/wiki/Student%27s_t-test#One-sample_t-test) and (new in v2.3) Bayesian one-sample t-test, otherwise [Wilcoxon signed-rank test](https://en.wikipedia.org/wiki/Wilcoxon_signed-rank_test) (see [CogStat specific](Differences-in-calculations-between-CogStat-and-other-programs#wilcoxon-signed-rank-test) details)<br><br>For one-sample t-test [sensitivity power analyses](Power-analysis)|[Wilcoxon signed-rank test](https://en.wikipedia.org/wiki/Wilcoxon_signed-rank_test) (see [CogStat specific](Differences-in-calculations-between-CogStat-and-other-programs#wilcoxon-signed-rank-test) details)|
