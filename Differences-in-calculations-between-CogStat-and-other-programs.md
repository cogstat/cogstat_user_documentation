Sometimes different programs use different solutions (e.g., different hypothesis tests) for the same question, or sometimes they use a different version of the same solution ([see some examples](https://www.pharmasug.org/proceedings/2017/QT/PharmaSUG-2017-QT12.pdf)).

Here we list some of the differences in the calculations between CogStat and other statistical programs.

## Confidence interval of the mean

Different methods can be used to calculate the CI of the mean: z-value-based solution (when SD is known and the sample is large (>30), and t-value-based solution, when SD is not known, and the sample is potentially small (see more details [here](https://en.wikipedia.org/wiki/Confidence_interval#Basic_steps)). CogStat uses the t-value-based solution, while other software packages (e.g., jamovi) may use the z-value-based solution.

## Standard deviation of the sample and the population

For the standard deviation of the sample the [Bessel's correction](https://en.wikipedia.org/wiki/Bessel%27s_correction) shouldn't be used, so CogStat doesn't use it for sample properties. Find more information about the methods [here](https://en.wikipedia.org/wiki/Standard_deviation#Estimation).

Software packages (e.g., SPSS Descriptives, or spreadsheet software [STDEV](https://support.office.com/en-us/article/STDEV-function-51fecaaa-231e-4bbb-9230-33650a72c9b0) or [STDEV.S](https://support.office.com/en-us/article/STDEV-S-function-7d69cf97-0c1f-4acf-be27-f3e83904cc23?ui=en-US&rs=en-US&ad=US) function) often suppose that you're interested in the population estimation, and the Bessel's correction is used (e.g., even if, in SPSS, the menu "Descriptives" refers to the sample). In spreadsheet software, for an uncorrected sample standard deviation use the [STDEV.P](https://support.microsoft.com/en-us/help/826406/excel-statistical-functions-stdevp) function.

## Lack of range for ordinal variables

Range is the difference of the smallest and the largest value. Sometimes it is recommended as a dispersion measure for ordinal variables. However, in ordinal variables the difference of two values is not known, and subtraction is meaningless. In Explore variable, CogStat displays only the minimum and maximum values, but not the range.

## Wilcoxon signed-rank test
Many times statistical programs report W (e.g., jamovi) or Z as the test statistic. On the other hand, CogStat reports T because the supporting function from [scipy calculates T](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.wilcoxon.html). Independent of those statistics, the p value should be the same.

See for example, the Wikipedia about the differences between [W or Z](https://en.wikipedia.org/wiki/Wilcoxon_signed-rank_test#Test_procedure) and [T](https://en.wikipedia.org/wiki/Wilcoxon_signed-rank_test#Original_test).

## Chi-squared test
CogStat uses the [Yates's correction for continuity](https://en.wikipedia.org/wiki/Yates%27s_correction_for_continuity), which is the default version in Python scipy.stats, similar to R. In SPSS and jamovi you'll find this version in the Continuity Correction line. See also [this description](https://www.pharmasug.org/proceedings/2017/QT/PharmaSUG-2017-QT12.pdf).

## Cramer's V
CogStat calculates the Cramer's V with the continuity correction, which is the default version both in scipy.stats and pingouin modules. You'll find the version without the continuity correction in jamovi.

## Levene's test
Various versions of the Levene's test are available. CogStat uses the Brown–Forsythe version where median instead of mean is used to calculate the spread. (Mean is used e.g., in jamovi 2.2.) Sometimes this version is termed as the Brown–Forsythe test. See more information in our [issue tracker](https://github.com/cogstat/cogstat/issues/56) and in the [Wikipedia article](https://en.wikipedia.org/wiki/Levene%27s_test).

## Confidence interval of the Spearman correlation
JASP relies on a bootstrapping-based solution, while CogStat [calculates CI with the Fisher transformation](https://en.wikipedia.org/wiki/Pearson_correlation_coefficient#Using_the_Fisher_transformation).

## Additional differences
There could be other differences between some implementations of the same tests, because different versions of the same tests could be used. See some background about [Wilcoxon signed-rank test](https://github.com/cogstat/cogstat/issues/31) and [McNemar test](https://github.com/cogstat/cogstat/issues/55).

CogStat also uses special solutions to display the data and results graphically. See more details in the [chart help page](Displaying-the-data-and-results-graphically).