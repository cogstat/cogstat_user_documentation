---
title: Filter outliers
---
How to set outlier-based filtering? 
* To filter outliers, from the `Data` menu, choose `Filter outliers...`, and choose the variable(s) you want to use to remove outliers. Then, (new v2.4) choose whether you want to use the univariate or the multivariate method, then hit OK.
     * CogStat will display the threshold values for being outliers, list the cases that are excluded, and (new in v2.3) display the excluded and included cases graphically together with the thresholds. (New in v2.4) The filtered cases are displayed with gray text in the Data view.
* To remove filtering, choose `Filter outliers...`, remove all variables from the `Selected variables` list, and hit OK.

How does outlier-based filtering work in CogStat?
* In the univariate method,
    * Outliers will be detected in each selected variable, independent of other variables.
    * All cases that are identified as outliers in any of the selected variables will be removed from the following analyses.
    * A value is an outlier if it is more extreme than the median ± 2.5 × MAD. ([See details below.](#information-about-the-mad-method))
        * Before CogStat version 2.2, a value was an outlier if it was more extreme than the mean ± 2 × SD.
* (New in v2.4) In the multivariate method,
    * Mahalanobis-MCD distance will be calculated, and cases beyond the .05 chi-squared cut-off will be excluded. ([See details below.](#information-about-the-Mahalanobis-distance))
* In addition, the cases that have a [missing value](Missing-data) in the selected variables will be excluded too.
* In the following analyses, the filtered cases will be ignored unless a new filtering criterion is set. When the outlier filtering is active, there is a short message about the variables the filtering is based on at the top of the output of all analyses.

## Information about the MAD method

[Median absolute deviation (MAD)](https://en.wikipedia.org/wiki/Median_absolute_deviation) is a robust measure of variability. While the often-used mean ± 2 × SD method is sensitive to the outliers (yes, the method with which we filter the outlier is sensitive to those outliers), the median-based solution is not. For this reason, CogStat uses the MAD method.

In CogStat, MAD is calculated as `median(abs(values - median(sample))) / 0.6744897501960817`. (In some other descriptions, the median is not divided by 0.6745, but it is multiplied by 1.4826. Note that the two solutions are mathematically equivalent.) (Also note that some descriptions define MAD without the division or the multiplication, i.e., only the median distance of the values from the sample median is considered.)

A rejection criterion value of 2.5 was chosen following the recommendation of Leys et al. (2013).

See more details in the [MAD Wikipedia article](https://en.wikipedia.org/wiki/Median_absolute_deviation) and in [Leys et al. (2013)](https://doi.org/10.1016/j.jesp.2013.03.013).

## Information about the Mahalanobis distance

A natural extension of the mean ± 2 × SD method in the case of multiple variables is the Mahalanobis distance. The Mahalanobis distance metric measures distances in multiple dimensions while also taking into account the shape of the distribution (as opposed to Euclidean distance). However, as the SD in the case of univariate analyses, the Mahalanobis distance is also sensitive to outliers. 

A robust way to calculate the Mahalanobis distance is the Minimum Covariance Determinant (MCD) approach. Using the Mahalanobis-MCD distance (MMCD distance for short) distance, CogStat excludes cases that fall outside a criterion specified using the 95th percentile of a chi-squared distribution. This technique is a natural extension of the MAD-median approach, according to Leys et al. (2018), and provides a robust way to estimate multivariate outliers.

See more details in the [Mahalanobis distance Wikipedia article](https://en.wikipedia.org/wiki/Mahalanobis_distance) and in [Leys et al. (2018)](https://doi.org/10.1016/j.jesp.2017.09.011).

## References
Leys, C., Ley, C., Klein, O., Bernard, P., & Licata, L. (2013). Detecting outliers: Do not use standard deviation around the mean, use absolute deviation around the median. Journal of Experimental Social Psychology, 49(4), 764–766. <https://doi.org/10.1016/j.jesp.2013.03.013>

Leys, C., Klein, O., Dominicy, Y., & Ley, C. (2018). Detecting multivariate outliers: Use a robust variant of the Mahalanobis distance. Journal of Experimental Social Psychology, 74, 150–156. <https://doi.org/10.1016/j.jesp.2017.09.011>
