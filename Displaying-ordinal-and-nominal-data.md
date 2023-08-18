---
title: Displaying ordinal and nominal data
---
# Displaying ordinal data
When the data of an ordinal scale is displayed, usually the values are depicted. However, this is misleading, because for an ordinal variable only the order of those values that is considered in the analysis. For example, Spearman's correlation is in fact a Pearson's correlation on the order of the original values ([find more information here](https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient#Definition_and_calculation)). When it is possible, it is more appropriate to display the order information for an ordinal variable, because this is the information the analyses rely on.

### Chosen method in CogStat
#### Dashed axis
In an ordinal scale the distance between two neighboring values (or between any two values) are not defined. This is similar to the charts when the scale is broken:

![Broken axis](https://upload.wikimedia.org/wikipedia/commons/thumb/b/b5/Y-axis_break.svg/203px-Y-axis_break.svg.png)

In a similar way, one can imagine an ordinal scale when the axis is broken between all neighboring values. To follow this idea, in CogStat a dashed axes is used for ordinal scales, indicating that the distance between the values are not defined, instead, it is the order that is utilized in the analysis.

#### Axis values
Additionally, the axis values denote the order, and the original values are displayed in parenthesis.

# Displaying nominal data
#### Dotted axis
In a nominal variable, the values do not have order. To highlight this feature in CogStat, the axes of the nominal values are denoted with dotted style.

This can be used not only for nominal variables, but in any cases when the data are handled as nominal variables, e.g., when non-nominal variables are used as grouping variables.
