---
title: Missing data
---
* In CogStat, only a single type of missing value is used.
   * If you need to use various types of missing values for your analysis, then you can use a workaround: use nominal variables, including the observed and various missing values. If you want to analyze the missing data together with other values, then, in a nominal variable, special values/codes should be used for the missing values.
* Missing values are displayed as NaN (occasionally, they are displayed as NA, but they work the same way).
* In an analysis, CogStat displays the number of missing cases at the beginning of the analyses, drops them, and uses only the observed cases in that analysis.
   * There is no listwise option to ignore cases that have at least a single missing value in a set of analyses because CogStat handles the analyses independently. A workaround is to filter the data in the data source file.
* When [filtering outliers](Filter-outliers), cases with missing data are also excluded. In multivariate outlier detection, when data is missing in any variables, the case will be excluded.
    * This practice has a clear advantage that only the cases for which we have information can be included. On the other hand, cases can be excluded not only because they are outliers but because we miss some information (this is clearly not an issue when the filtering is based on a single variable but when multiple univariate or multivariate filtering is used).
