---
title: If you are coming from another software
---
It is worth to use (even partially) CogStat because automatic analysis is fast, and less error prone and optimized output is easier to understand, review, and copy to a report. Also, you may find additional relevant and important details about your data that you would not have checked for otherwise.

It is easy to start using CogStat because there's a chance that your former data file format is supported, so you can start using your previous data and because, technically, CogStat is quite simple to use.

However, in an automatic analysis software, things may work a bit differently. Here, we briefly summarize the essential differences between CogStat and individual analysis software packages. If you understand these few key differences, then you're ready to use CogStat for analyzing your data.

## Storing your data

CogStat does not have its own data editor.

* You can use either a **spreadsheet software** or **other statistical packages** to store and handle your data.
* Using these data sources is pretty simple. You can **either drag and drop your data file**, **or you can copy and paste your data**, and you're good to go. Because [CogStat supports a series of data file formats](Handling-data#available-file-formats), there's a chance that you can use your former data files in their current forms.

Find more information on the [Handling data](Handling-data) page.

## Setting the measurement level in your data

Because CogStat analyzes the data automatically, you have to set the measurement levels of your data.

* If you store your data **in a spreadsheet file**, **add a second row**, and add `int`, `ord` or `nom` words to denote the measurement level.
- If you store your data **in a statistical package** that can save the measurement level in your data file (such as SPSS, jamovi, JASP), **set the measurement level in that software**, and CogStat will automatically import that information.

If you don't set the measurement level, CogStat assumes that numerical variables are interval variables and string variables are nominal variables.

Find more information on the [Handling data](Handling-data) page.

## Choosing a task instead of individual statistical functions

Because CogStat chooses the to-be-run analyses automatically, you cannot choose a specific analysis independent of other analyses. For example, you cannot run a hypothesis test where the assumptions are violated.

Instead, **in the `Analysis` menu, choose the appropriate task**, and after choosing the relevant variables, the appropriate analyses will be run automatically.

What if you need a specific individual analysis? We propose that first the recommended analyses that are implemented in the automatic pipeline should be run. If for any reason you decide that other analyses should be run, and you have a reasonable justification why standard procedures are not appropriate for you, then choose a classic statistical package and run your analyses there. It would be convenient to run both automatic and individual analyses in the same software, but we focus on the automatic part, and there are excellent individual analysis software packages, so at the moment automatic and individual analyses should be run in different software. Still, you'll save a lot of time with the automatic analyses even if you need to use different software because automatic analysis saves you more time compared to the extra time of software switch.

## Finding the result you need

The results have a similar structure across different analysis tasks.

The output usually has three main sections:
1. **Raw data** Check your data with your own eyes, see if there are unexpected patterns that the following analyses cannot handle, and have a common sense estimation of what results you'll get.
2. **Sample properties** Descriptive statistics are summarized in numerical and graphical forms.
3. **Population properties** Inferential statistics are presented, including point and interval estimations, hypothesis tests, related power analyses, etc.

As most methodological descriptions propose, you may need all of that information because they present different aspects of your data.

Find more information on the [Common elements of the analysis results](Common-elements-of-the-analysis-results) page.

## APA style

When relevant, CogStat usually presents the results in APA style, so instead of hunting for appropriate df values, etc., in large tables, you can **simply copy and paste the results to your report**.

## Optional need for additional individual analysis

While automatic analysis can provide appropriate results in most cases, in some other cases, you may spot some peculiar details about your data, and you may decide that additional specific analyses are needed. In these cases, you can use your favorite individual analysis software to run some follow-up analyses. See more details about how [automatic and individual analysis software packages can be used together](Using-automatic-and-individual-analysis-software-packages). 

## Saving the results

Because automatic analysis is really fast in terms of user interaction, you don't always need to save your results: **Rerunning an analysis may be faster than finding a saved result file**.

Still, if you want to save the results, you can save them to a pdf file.

Find more information on the [Handling output](Handling-output) page.

## All set

Now you're ready to give CogStat a try. If you're familiar with statistical terms and with other statistical software packages, based on these differences it should be easy to use CogStat.
