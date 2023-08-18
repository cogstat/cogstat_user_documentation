New in v2.4.

From the `Analysis` menu choose `Compare repeated measures variables and groups`, and choose the variables you want to compare and the `Grouping variable`, then hit OK.

To use several factors, click on `Factors...` and set the names and the levels of the factors, and click OK. Then you can select the variables for the factor level combinations.

* Only the cases where all variables are available are used.
* Variables to be compared have to have the same measurement levels.

In the `Display options...` dialog, [the minimum and maximum of the y-axis](Displaying-the-data-and-results-graphically#range-of-the-axes), and [the way factors are displayed](Displaying-the-data-and-results-graphically#displaying-factors-and-groups-in-x-axis-colors-and-panels) can be set.

* If no `Grouping variable` is chosen, then the results mostly show the same results as in [Compare repeated measures variables](Compare-repeated-measures-variables). (Depending on the specific implementation in the background, some results may be missing.)
* If there is only a single `Dependent variable(s)`, then the results mostly show the same results as in [Compare groups](Compare-groups). (Depending on the specific implementation in the background, some results may be missing.)

The following results will be calculated (see also the [common elements of the results](Common-elements-of-the-analysis-results)):

## Raw data

|Result|For interval variables|For ordinal variables|For nominal variables
|---|---|---|---|
|Sample size | Number of observed cases | Number of observed cases | 
|Graphs of the raw data|Plot with individual data|Plot with individual data|

For repeated measures individual data plots, [values of a single case are connected](Displaying-individual-data-in-repeated-measures-variables).

## Sample properties

|Result|For interval variables|For ordinal variables|For nominal variables
|---|---|---|---|
|Descriptive data|Means, [Standard deviations](https://en.wikipedia.org/wiki/Standard_deviation), Maximums, [Upper quartiles](https://en.wikipedia.org/wiki/Quartile), [Medians](https://en.wikipedia.org/wiki/Median), Lower quartiles, Minimums|Maximums, [Upper quartiles](https://en.wikipedia.org/wiki/Quartile), [Medians](https://en.wikipedia.org/wiki/Median), Lower quartiles, Minimums|
|[Standardized effect size](Standardized-effect-sizes)|
|Graphs of the data|Box plot with individual data|Box plot with individual data |

For individual data plots, [values of a single case are connected](Displaying-individual-data-in-repeated-measures-variables).

## Population properties

|Result|For interval variables|For ordinal variables|For nominal variables
|---|---|---|---|
|Population parameters numerically|Mean with 95% CI|Median with 95% CI|
|[Standardized effect size](Standardized-effect-sizes)|
|Graphs of the population parameters|Graph with mean and 95% CI of the mean|Graph with median| 
|[Hypothesis test](Hypothesis-tests) and [sensitivity power analyses](Power-analysis)|||
