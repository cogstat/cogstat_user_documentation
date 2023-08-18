CogStat can handle comparisons when a single case (e.g., a patient) is compared to a group (e.g., a control group). The single case hypothesis tests are based on the solution proposed by John R. Crawford and his colleagues.

At the moment, CogStat supports the following hypothesis tests:
* Compare the performance of a single case to a control group (i.e., extremity of a task), as introduced in [Crawford & Howell (1998)](https://doi.org/10.1076/clin.12.4.482.7241).
* Compare the performance of a single case to a control group when the performance is measured as a slope (i.e., extremity of a task expressed as a slope), as introduced in [Crawford & Garthwaite (2004)](https://doi.org/10.1016/S0010-9452(08)70145-X).

To perform other single-case hypothesis tests not supported by CogStat yet, you might use [the single-case study statistic packages](http://homepages.abdn.ac.uk/j.crawford/pages/dept/SingleCaseMethodology.htm) by John R Crawford.

## How to run a single-case analysis in CogStat?
**Preparing the data.** Load your data, where a grouping variable will tell whether a case is a single case or a member of the control group, and where there is a dependent variable. In a slope comparison analysis you also need a slope standard error variable.

Your data should look like this:

Group|Dependent variable|
---|---|
nom|int|
Single case|3
Control group|3
Control group|4
Control group|2

Or if you compare slope data, your data should look like this:

Group|Slope|Slope SE|
---|---|---|
nom|int|int|
Single case|3|0.2
Control group|3|0.3
Control group|4|0.4
Control group|2|0.3

**Performing the analysis.** Then choose `Analysis > Compare groups`, and set the appropriate grouping variable and dependent variable. To run a slope analysis, beyond setting the grouping variable and setting the slope values as the dependent variable, click on the `Single case slope...` button, and set the Slope SE variable, and set the number of trials per participant.

If the grouping variable includes two groups and one of the groups includes a single case (such as in the data sources above), the single-case hypothesis tests will be chosen automatically.

Note that the modified t-test will be run only if the control group is normally distributed.