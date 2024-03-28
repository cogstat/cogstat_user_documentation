---
title: Common elements of the analysis results
---
# Raw data, sample properties, and population properties

In most analyses, the results are divided into three main sections and further subsections:

1. **Raw data.** 
    1. You'll find the number of **observed and [missing cases](Missing-data)** here. In all analyses, missing cases are removed, and analyses are run only on observed cases.
    2. This part displays the **individual values [graphically](Displaying-the-data-and-results-graphically)** without any further information. This is useful to get an impression of your data without any statistical aid, and check if the data have some [unexpected properties](Displaying-individual-data) (e.g., unexpected distribution, outliers, etc.).

2. **Sample properties.** Strictly speaking, these are [descriptive statistics](https://en.wikipedia.org/wiki/Descriptive_statistics), and in very rare cases, when you measure the whole population, these results show the population properties as well.
    1. **Summary statistics** of your data in numerical forms.
    2. You'll find **[standardized effect sizes](Standardized-effect-sizes)** here.
    3. Summary statistics of your data in **[graphical form](Displaying-the-data-and-results-graphically)**.
3. **Population properties.** Be aware that these results are always speculations because no one really knows what population your sample comes from. These are just some reasonable guesses. Strictly speaking, these are [inferential statistics](https://en.wikipedia.org/wiki/Statistical_inference), and in very rare cases, when you measure the whole population, these results could be just ignored.
    1. You'll find the **population parameters** here (point and interval estimations) in numerical form.
    2. Point and interval estimation of **[standardized effect sizes](Standardized-effect-sizes)**.
    3. Population parameters in **[graphical form](Displaying-the-data-and-results-graphically)**.
    4. **[Hypothesis tests](Hypothesis-tests)** with automatic assumption checks.
    5. In some cases, before a hypothesis test is run, **[sensitivity power analysis](Power-analysis)** is given.

Find some more (technical) information about these parts in the [development documentation](https://github.com/cogstat/cogstat/wiki/How-to-compile-the-results%3F#results-to-compile).

# Rerun the analyses

(New in v2.4.) You can rerun all analyses in the current Results pane with the `Analysis > Rerun all analyses...` menu. This is useful after you [reload your active data file](Handling-data#how-to-edit-your-data).

(New in v2.5) Turn on `Analyses > Rerun all analyses when file reloaded` to rerun all the analyses seen in the results pane whenever the [file is reloaded](Handling-data#how-to-edit-your-data).

When [automatic reloading](Handling-data#how-to-edit-your-data) and automatic reanalysis are turned on, the editor software can be considered as the external data editor of CogStat.
