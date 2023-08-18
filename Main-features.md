---
title: Main features
---
CogStat is different from other statistical packages in many ways. The main aim was to build a very efficient statistical package. Most of the functions were developed cognitive psychologists in mind, but many of these the methods could be useful for many other scientists as well.

### Main features of CogStat

**CogStat automatically compiles the relevant items and statistics for a task.**
* Why? While analyzing the data, for a specific task, usually a quite well defined set of analyses are used. For example when comparing two groups, one might want to look at the raw data, look for outliers, check normality, compute some descriptive statistics, calculate the effect size, estimate the population parameters, run hypothesis tests, etc. In most statistical packages these functions can be found behind different menus, and takes quite some time to run all these analyses. This is not the most efficient way to run the analysis.
* **In CogStat the menus reflect complete tasks rather than single analysis**, and CogStat runs all the related analysis for those tasks. For example, in group comparison function after setting the grouping and dependent variables, CogStat automatically presents the data graphically, computes the descriptives, runs the hypothesis tests, etc.
* **CogStat chooses the appropriate hypothesis tests automatically** depending on your question and the measurement levels of your variables.
    * Why? There are many useful summaries of hypothesis tests in textbooks and on the Internet that guides students and researchers which test should be used. However, in most cases it is quite straightforward which test should be used in a sense that it could be easily algorithmized, which means that a computer could easily do it. Using CogStat there is no need to look for the appropriate tests and check for their assumption, because CogStat knows how to do it, and depending on the question, the variables, and the measurement level of the data, it chooses the appropriate hypothesis test. CogStat checks for all other relevant information, for example, checking the number of groups/levels/cases, checking the assumptions, and so on.
* **Less known or insufficiently used analysis are more accessible**
    * There are many known problems with the current statistical analysis practice, and there are several remedies proposed in the recent decades. Unfortunately, many of those solutions are not widespread. To promote those solutions, CogStat, for example, computes effect size and confidence intervals (work in progress, these results are available only for some of the analyses), uses specific [hypothesis tests for single case studies](Compare-groups#population-properties), is prepared to run [EZ diffusion analysis](Behavioral-data-diffusion-analysis).

**CogStat presents the results in a more understandable and efficient way.**

* How are the results displayed in other packages? Most of the statistical packages display many details of an analysis, and many of those details are hardly used by the researchers. These details make using the output more difficult. E.g., have you ever made mistakes by coping the ANOVA results to your manuscript converting it to APA format? Do you spend some time to find the appropriate table that includes the relevant data, while the data of some other tables are never used?
* CogStat **displays the information that is most required by researchers**, and CogStat displays these results in a format that is used by researchers, currently **in the [APA format](APA-style)**.
* To find and interpret the results more easily, in most analyses **CogStat displays the results in three sections**: [raw data, sample properties and population properties](https://github.com/cogstat/cogstat/wiki/Common-elements-of-the-analysis-results#raw-data-sample-properties-and-population-properties). In most cases sample and population properties are displayed both in numerical and in graphical forms.
* CogStat uses **informative graphs**. Graphs should help researchers to understand the data and understand statistics. Several rarely used methods are used to support this understanding, for example,
    * [Individual data](Displaying-individual-data) are displayed on graphs to show if there are outliers, or if there are some unexpected patters, or to show hints about the reliability of the data.
    * Repeated measures data are connected between neighboring variables to stress that the data are related.
    * For ordinal variables the [ordinal information](Displaying-ordinal-and-nominal-data#displaying-ordinal-data) is displayed.
    * (See the details in the [technical description](How-to-create-figures%3F) how CogStat graphs are built.)

Further notable features
* Coverage of the analyses
    * So far, CogStat supports several simple tasks, like explore a variable, explore a variable pair, compare variables, compare groups, create pivot tables, **covering most of the analyses methods taught is BA psychology programs**.
    * It covers **more than 25 hypothesis tests** (and counting).
    * In includes **rare and/or not accessible analyses**, such as [hypothesis tests for single case studies](Compare-groups#population-properties), or [EZ diffusion analysis](Behavioral-data-diffusion-analysis).
* It is **free** to use
* It is cross platform, so you can use it on **Windows, Linux and Mac**
* It is localized to **several languages** ([see available languages](https://poeditor.com/join/project/lgpFkIh0FZ))
* If you're a Python coder, CogStat can be used in [Jupyter Notebook](Jupyter-Notebook)
* It is open source, so you can look at the [code](https://github.com/cogstat/cogstat) (if you understand code) and also you can modify it

### Advantages of using CogStat
* It **saves a lot of time**.
    * **Much less clicking** is needed in CogStat than in other analysis software. See [this example](https://docs.google.com/presentation/d/1_rnHhyD3pF9BZuqCkcFLWKhAbX1DfS8T5q-TxogqpZA/edit#slide=id.g5a16674318_0_81).
    * Because the output has similar structure across different tasks, it is **easier to find the appropriate information you need**. Additionally, it is harder to mix up the results and to use some incorrect result based on the statistical package output.
    * Results needs **less reformatting** before inserting them to your manuscript.
        * It is **easier to apply the APA format** more precisely, and there is no need for checking the correct format for a rare hypothesis test.
    * When the analyses are more precise, you might **avoid dead ends and wrong decisions**, saving months in your work.
* The **analyses are more precise**.
    * It decreases the chances that something important aspect of your data is missed. **“Blind” analysis is less likely**, because you can see your data more completely, without additional efforts.
    * Automatic hypothesis test selection decreases the possibility that **assumptions are** not **checked**.
    * You might apply some hypothesis test or other analyses you haven't been aware of before.
* CogStat is a **platform to find consensus about the recommended data analysis pipeline**.
    * Developers and contributors of CogStat can suggest a consensus about the appropriate tests and their use when multiple solutions are available.
    * Methodological and statistical **innovations may spread much faster**.
    * It helps to overcome the [replication crisis](https://docs.google.com/presentation/d/1HmSTPnTxDzW8hYZG7ujHaeHc0mRqqYeY95yKh56z61c/edit?usp=sharing).

Cool? [Download and install CogStat.](Installation)
