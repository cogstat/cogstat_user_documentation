New in v2.4.
# How to run the analysis?

In the `Analysis` menu, choose `Internal consistency reliability analysis...`, select the variables that include items, and check the selected items that are reversed items.

Note that the to-be-reversed items will be reversed independently of each other, and the minimum and maximum will be specified for each item independently, too. This means that if, for an item, some minimum or maximum values were not chosen by any participants (e.g., in a 1-5 scale, only 1–4 values were chosen), then the analysis assumes that the scale is a 1-4 scale. This may cause a bias in the total scores and related statistics. You can check if the intended range was observed for the items in the Sample properties section of the results. If any items were reversed incorrectly, then we recommend reversing the items in your data editor, before using it in the analyses, and those items should not be marked as reversed items in the CogStat analysis. (Note that the same item reversing solution is used by other popular software packages.)

# Components of the results

## Raw data

- The number of observed and missing cases are displayed.
- Scatter plots of the items vs. the total score.

## Sample properties

- Scatter plots of the items vs. the total score with linear regression.
- Cronbach's alpha.
- Cronbach's alpha when individual items are removed, and item-rest correlation.

## Population properties
- Cronbach's alpha and its confidence intervals
- Cronbach's alpha when individual items are removed, and item-rest correlation. Point and interval (confidence interval) estimations.

# See also

See also the similar analysis of [Interrater reliability analysis](Interrater-reliability-analysis) and all the [reliability analyses](Reliability) that are supported by CogStat.
