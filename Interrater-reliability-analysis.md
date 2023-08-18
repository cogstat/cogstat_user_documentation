New in v2.4.
# How to run the analysis?

In the `Analysis` menu, choose `Interrater reliability analysis...`, select the variables that include the raters' scores, and choose if the mean of the raters' scores/measurements will be used (`Ratings are averaged`).

# Components of the results

## Raw data

- The number of observed and missing cases are displayed.
- The raters' scores/measurements for all cases are displayed in a chart. On the x-axis, the raters/measurements are displayed, and every line is a case.

## Sample properties

- The individual data of the raw data together with the related box plots are displayed.
- The intraclass correlation (ICC) values (see below) of the sample are shown.

## Population properties

- Assumptions of the inferential methods are checked. If assumptions are not met, then the parameter estimations and the hypothesis tests may be biased.
- Parameter estimations of the ICC values (see below) are shown.
- Hypothesis tests showing whether the ICCs differ from zero are displayed.

# ICC values

In CogStat, ICC terms follow the suggestion McGraw and Wong (1996). See the meaning of these indexes in the table below.

In some other packages, and in many papers, the terms of Shrout and Fleiss (1979) are used. It is recommended to use the McGraw and Wong (1996) terms. Still, for having CogStat results comparable with other packages, the table below displays the related Shrout and Fleiss (1979) terms.

McGraw and Wong (1996) terms|Description of the index|Shrout and Fleiss (1979) terms
----|----|----
ICC(1)|No role for the raters/measurements.<br>Single rater/measurement.|ICC(1,1)
ICC(A,1)|Absolute agreement between raters/measurements.<br>Single rater/measurement.|ICC(2,1)
ICC(C,1)|Consistency (relative agreement) between raters/measurements.<br>Single rater/measurement.|ICC(3,1)
ICC(k)|No role for the raters/measurements.<br>Ratings/measurements averaged.|ICC(1,k)
ICC(A,k)|Absolute agreement between raters/measurements.<br>Ratings/measurements averaged.|ICC(2,k)
ICC(C,k)|Consistency (relative agreement) between raters/measurements.<br>Ratings/measurements averaged.<br>(Cronbach's alpha)|ICC(3,k)

While, in some other software packages, the user chooses the assumed variances of raters/measurements, CogStat follows a different logic.
- Instead of relying on the often unjustifiable variance assumptions, CogStat relies on the McGraw and Wong (1996) terms, and ICC indexes are interpreted as different properties of the ratings/measurements.
- CogStat follows the strategy proposed by Liljequist et al. (2019): All the three ICC indexes are calculated. If the index assuming no role of raters/measurements and the C/A indexes do not differ, then the raters/measurements have no role, and the ICC(1)/(k) index can be reported. If the indexes differ, then ICC(1)/(k) index makes no sense, and both the C and the A indexes should be reported (they are sensitive to different properties of the ratings).

# See also

See also the similar analysis of the [internal consistency reliability analysis](Internal-consistency-reliability-analysis) and all the [reliability analyses](Reliability) that are supported by CogStat.

# References
Liljequist, D., Elfving, B., & Roaldsen, K. S. (2019). Intraclass correlation – A discussion and demonstration of basic features. PLOS ONE, 14(7), e0219854. <https://doi.org/10.1371/journal.pone.0219854>

McGraw, K. O., & Wong, S. P. (1996). Forming inferences about some intraclass correlation coefficients. Psychological Methods, 1, 30–46. <https://doi.org/10.1037/1082-989X.1.1.30>

Shrout, P. E., & Fleiss, J. L. (1979). Intraclass correlations: Uses in assessing rater reliability. Psychological Bulletin, 86, 420–428. <https://doi.org/10.1037/0033-2909.86.2.420>
