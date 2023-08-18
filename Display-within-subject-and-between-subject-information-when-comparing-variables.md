---
title: Display within subject and between subject information when comparing variables
---
New in v2.4.

When comparing repeated measures variables or groups or both, the relevant results can be displayed flexibly.

* First, select the grouping variables or the repeated measures variables factors.
  * For choosing the grouping variables, in the `Analysis > Compare groups...` or in the `Analysis > Compare repeated measures variables and groups...` dialogs, select the grouping variables (Group(s) list).
  * For setting the within-subject factors, in the `Analysis > Compare repeated measures variables...` or in the `Analysis > Compare repeated measures variables and groups...` dialogs, click on the `Factors...` button, and add the required factors and the number of their levels. Then, choose the variables (Selected variables or Dependent variables lists) in line with the factor level combinations.
    * If you choose several variables without adding factor(s), then the factor will be named automatically as "Default factor".
* After you specified the grouping variables and/or the repeated measures factors, you can specify how they'll be displayed. Click on the `Display options...` button, and set which groups and repeated measures factors will be displayed along the x-axis, as colors or in separate panels. Note that only grouping variables can be used in panels, but not repeated measures factors.
  * The order of the grouping variables and repeated measures factors in a display category (x-axis, color, panels) matters. The topmost variable/factor will be displayed as the top level, i.e., it will change less frequently as one moves along the category dimension.
  * Raw data of the neighboring repeated measures variables are connected if they are displayed next to each other along a category dimension. It means that this will happen only if they are at the bottom level within that display category, i.e., there are no grouping variables under the repeated measures factors. We recommend using repeated measures factors this way, otherwise the critical information of the repeated measures variables will not be visible.
