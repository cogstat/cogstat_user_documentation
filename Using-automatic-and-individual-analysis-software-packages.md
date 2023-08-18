---
title: Using automatic and individual analysis software packages
---
## Automatic vs individual analysis software packages

Most statistical packages are **individual analysis software**, i.e., you have to choose individually which analyses (such as specific hypothesis tests, descriptive statistics, confidence interval) to run. In an **automatic analysis software**, you choose the task/question and the specific analyses are chosen by the software.

Both types of analyses have their advantages and drawbacks.

* In an automatic analyses software, it is fast to run the typical analyses, the analysis can be more precise, and the computer may help the user to chose more appropriate methods than the user have chosen otherwise. However, there may be special scenarios that the computer does not recognize, e.g., the data violates some assumption but the procedure that is used to detect the violation misses it.
* Contrarily, in an individual analysis software, the user can control all the details. This provides more possibilities, but at the same time, it comes with more responsibility, too. Also, in an individual analysis software, the data analysis takes more time.

## Which type of software to use?

We recommend using both. In most cases, automatic analysis should be sufficient. In a few cases (like with any other software packages), you need additional packages for your analyses needs.

* Use **automatic analysis software** by default. For a first check of your data, you can quickly run the typical analysis. In most cases, this may be the final check of your data as well: If all goes well, then the typical analysis pipeline is appropriate, and you may not see any sign of unhandled properties of the data. You may be happy with the results, and you can use them.
* However, in some other cases, you may discover some features in the results that are not handled by the automatic pipeline, such as a special pattern in your data distribution. In those cases, use your favorite **individual analysis software**, and check the details in a more traditional way. See our recommendations for [additional statistical packages](Other-useful-statistical-programs).
  * Since CogStat knows a [lot of data file formats](Handling-data#available-file-formats), you can store your data in your favorite individual analysis software, and drag and drop the file to CogStat to analyze the data automatically. Then, if an individual analysis is needed, use the same file in your individual analysis software.
