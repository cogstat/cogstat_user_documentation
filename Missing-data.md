---
title: Missing data
---
* When importing the data, CogStat displays missing values as NaN or, occasionally, as NA.
* In an analysis, CogStat displays the number of missing cases at the beginning of the analyses, drops them, and uses only the observed cases in that analysis.
* When [filtering outliers](Filter-outliers), cases with missing data are also excluded. In multivariate outlier detection, when data is missing in any variables, the case will be excluded.
    * This practice has a clear advantage that only the cases for which we have information can be included. On the other hand, cases can be excluded not only because they are outliers but because we miss some information (this is clearly not an issue when the filtering is based on a single variable but when multiple univariate or multivariate filtering is used). Based on later considerations, we may modify this rule.
* CogStat uses only a single type of missing data.
    * Various missing values can be analyzed with a workaround: use nominal variables, including the observed and various missing values. If you want to analyze the missing data together with other values, then, in a nominal variable, special values/codes should be used for the missing values.
* There is no listwise option to ignore cases that have at least a single missing value in a set of analyses because CogStat handles the analyses independently. A workaround is to filter the data in the data source file.
