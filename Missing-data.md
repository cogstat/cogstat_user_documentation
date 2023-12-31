---
title: Missing data
---
* CogStat displays the missing cases at the beginning of the analyses, drops them, and uses only the observed cases in that analysis.
* When [filtering outliers](Filter-outliers), cases with missing data are also excluded. In multivariate outlier detection (Mahalanobis distance), when a data is missing in any variables, the case will be excluded.
    * This practice has a clear advantage that only the cases for which we have information can be included. On the other hand, cases can be excluded not only because they are outliers but because we miss some information (this is clearly not an issue when the filtering is based on a single variable but when multiple univariate or a multivariate filtering is used). Based on later considerations, we may modify this rule.
* CogStat uses only a single type of missing data.
    * Various missing values can be analyzed with a workaround: use nominal variables including this information, i.e., observed and various missing values. If the user wants to analyze the missing data together with other values, then, in a nominal variable, a special value should be used for the missing values that is not recognized by CogStat as a missing value.
    * Various missing values should be imported into this single NaN value.
* There is no listwise option to ignore cases that have at least a single missing value in a set of analyses because CogStat handles the analyses independently. A workaround is to filter the data in the data source.
