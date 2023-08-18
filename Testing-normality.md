## Available methods
There are several possible methods to [test normality](https://en.wikipedia.org/wiki/Normality_test) of a variable.

* Graphical methods
  * See, for example, Schucany & Tony Ng (2006) or Wilkinson (1999) arguing for its use.
  * Cons
    * The decision based on it is subjective.
    * Cannot be automatic, which is important in a software with automatic decisions.
* Numerical methods with descriptives
  * E.g., skewness and kurtosis
  * Cons
    * It cannot consider the sampling error.
    * It cannot capture some unexpected assumption violation.
* Hypothesis tests
  * See a few of them [here](https://en.wikipedia.org/wiki/Normality_test#Frequentist_tests). There are more than 40 hypothesis tests for normality test.
  * A few studies are investigating the power of normality tests, e.g., Razali & Wah, 2011; Noughabi & Arghami, 2011; Farrell & Rogers-Stewart, 2006; Romão, Delgado & Costa, 2010; Yap & Sim, 2011
    * [Shapiro-Wilk test](https://en.wikipedia.org/wiki/Shapiro%E2%80%93Wilk_test) is the most recommended test.
    * [Jarque-Bera test](https://en.wikipedia.org/wiki/Jarque%E2%80%93Bera_test), [Anderson-Darling test](https://en.wikipedia.org/wiki/Anderson%E2%80%93Darling_test) and [D'Agostino test](https://en.wikipedia.org/wiki/D%27Agostino%27s_K-squared_test) also perform well.
    * Use of [Kolmogorov-Smirnov test](https://en.wikipedia.org/wiki/Kolmogorov%E2%80%93Smirnov_test) is mostly discouraged.
    * Power of the specific tests depends on the distribution, therefore in some cases it is impossible to tell which test is the best choice.
    * (Thanks Ákos Laczkó for the summary.)
  * Cons
    * Lack of power for small samples. E.g., see the referred simulation studies how the specific tests perform for specific sample sizes and specific distributions.
    * As an assumption test, it could influence the overall alpha level of the main test.
    * It cannot capture some unexpected assumption violation.

## Chosen method for CogStat
* Graphical methods are subjective, which is not in line with the idea of use of consensual methods in CogStat. Still, CogStat displays data and the result of the analyses. Therefore, histograms with normal distribution and Q-Q plots are displayed, but the decision (e.g., for assumption check) is not based on them.
* It is hard to tell whether numerical methods or hypothesis tests would cause more problems. Because hypothesis tests seem to be more accepted, CogStat uses hypothesis tests.
* Simulations demonstrate that Shapiro-Wilk test shows the highest power in most cases.

Therefore, CogStat uses (1) [Shapiro-Wilk test](https://en.wikipedia.org/wiki/Shapiro%E2%80%93Wilk_test) test for the decision about assumptions, and additionally displays (2a) the histogram with normal distribution and (2b) the [Q-Q plot](https://en.wikipedia.org/wiki/Q%E2%80%93Q_plot). Therefore, if the user sees that the hypothesis test couldn't capture some critical violation of the assumption, the rest of the analysis can be rerun in a classic statistical software. (Our experience so far shows that this would rarely be needed.)

## References
Farrell, P. J., & Rogers-Stewart, K. (2006). Comprehensive study of tests for normality and symmetry: extending the Spiegelhalter test. Journal of Statistical Computation and Simulation, 76(9), 803–816. <https://doi.org/10.1080/10629360500109023>

Noughabi, H. A., & Arghami, N. R. (2011). Monte Carlo comparison of seven normality tests. Journal of Statistical Computation and Simulation, 81(8), 965–972. <https://doi.org/10.1080/00949650903580047>

Razali, N. M. & Wah, Y. B. (2011) Power comparisons of Shapiro-Wilk, Kolmogorov-Smirnov, Lilliefors and Anderson-Darling tests, Journal of Statistical Modeling and Analytics, Vol. 2, pp. 21-33.

Romão, X., Delgado, R., & Costa, A. (2010). An empirical power comparison of univariate goodness-of-fit tests for normality. Journal of Statistical Computation and Simulation, 80(5), 545–591. <https://doi.org/10.1080/00949650902740824>

Schucany, W. R., & Tony Ng, H. K. (2006). Preliminary Goodness-of-Fit Tests for Normality do not Validate the One-Sample Student t. Communications in Statistics - Theory and Methods, 35(12), 2275–2286. <https://doi.org/10.1080/03610920600853308>

Wilkinson, L. (1999). Statistical methods in psychology journals: Guidelines and explanations. American Psychologist, 54(8), 594–604. <https://doi.org/10.1037/0003-066X.54.8.594>

Yap, B. W., & Sim, C. H. (2011). Comparisons of various types of normality tests. Journal of Statistical Computation and Simulation, 81(12), 2141–2155. <https://doi.org/10.1080/00949655.2010.520163>
