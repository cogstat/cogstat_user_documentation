## What are diffusion models?

Diffusion models of behavioral data assume that evidence is accumulated within a trial until a specific threshold is reached, and then the response is chosen. Diffusion models assume several parameters in the background influencing the responses, and these parameters can be recovered analyzing the behavioral data.

Find more more details about the diffusion models, for example, in 
- Voss, A., Nagler, M., & Lerche, V. (2013). Diffusion Models in Experimental Psychology. Experimental Psychology, 60(6), 385–402. <https://doi.org/10.1027/1618-3169/a000218>
- Smith, P. L., & Ratcliff, R. (2004). Psychology and neurobiology of simple decisions. Trends in Neurosciences, 27(3), 161–168. <https://doi.org/10.1016/j.tins.2004.01.006>
- Alexandrowicz, R. W. (2020). The diffusion model visualizer: An interactive tool to understand the diffusion model parameters. Psychological Research, 84(4), 1157–1165. <https://doi.org/10.1007/s00426-018-1112-6>

## Diffusion analysis in CogStat

Currently, CogStat implements the EZ-diffusion model recovery method. See more details in Wagenmakers, E.-J., van der Maas, H. L. J., & Grasman, R. P. P. P. (2007). An EZ-diffusion model for response time and accuracy. Psychonomic Bulletin & Review, 14(1), 3–22. <https://doi.org/10.3758/BF03194023>.

There are other software packages with advanced features that can recover diffusion model parameters, although they require more conceptual knowledge about the diffusion models and more technical knowledge to perform the analysis compared to the easy-to-run solution provided in CogStat. Find alternative analysis methods in [fast-dm](https://www.psychologie.uni-heidelberg.de/ae/meth/fast-dm/), [DMAT](https://ppw.kuleuven.be/okp/software/dmat/), [HDDM](http://ski.clps.brown.edu/hddm_docs/), [PyDDM](https://pyddm.readthedocs.io/), [EZ2](http://purl.oclc.org/net/rgrasman/jscript/ez2) (alternative [R version of EZ2](https://rdrr.io/rforge/EZ2/man/EZ2-package.html), [Excel version of EZ2](http://purl.oclc.org/net/rgrasman/excel/ez2)).

### How are the parameters recovered?
Based on the reaction time and error data, drift rate, threshold, and nondecision time parameters are calculated.

* In CogStat, (new in v2.4) first, trials with slower than 2.5 sec are removed. 
* Then, the mean error rates, mean of correct RTs and variance of the correct RTs are calculated. For the mean error rates, the edge correction is applied (see Wagenmakers et al. (2007), p. 11).
* Finally, the drift rate, threshold and nondecision time parameters are calculated as described in Wagenmakers et al. (2007).
  * For the parameter _s_ (noise within the trial as evidence is accumulated; a scaling parameter) 0.1 value or (new in v2.4) value 1 is used.


## How to run a diffusion analysis in CogStat?

You can try these steps with the [demo data](Demo-data) in the `diffusion model` folder.

### Preconditions of running a diffusion analysis

Run the analysis only if these preconditions apply:
- The task is a two-choice task
- The core decision of the task is most probably solved in a single step, not with two or more parallel processes or not with sequential steps.

The EZ-diffusion model recovery can be applied only if these additional preconditions apply:
- The starting point is equidistant from the two thresholds
- Across trial variability of the parameters are not of interest

If the latter EZ-diffusion model-specific preconditions do not apply, you may consider using other software listed above.

### Preparing the data
The data should include the trials, i.e., each row should include a single trial.

All rows should include the following variables:
- Optionally, ID of the participant
- Optionally, one or more condition variables
- Error
  - Either erroneous trials should be coded as 1, and correct trials should be coded as 0, or (new in v2.4) erroneous trials should be coded as 0, and correct trials should be coded as 1.
- Reaction time
  - It is critical that the time should be measured in seconds, or (new in v2.4) in milliseconds, but not in other units, otherwise the recovered parameters will be incorrect.
  - (Up to v2.3) It is recommended to remove trials with outliers. (New in v2.4) Trials with longer than 2.5 sec responses are removed before the analysis.

For example, the data should look like this:

Participant id| Condition| Error| Reaction time 
---|---|---|---
nom| nom| nom| int
p01|	word|	1| 1.132
p01|	word|	0| 0.974
p01|	nonword|	0| 1.243
p01|	word|	1| 1.086
p01|	nonword|	0| 0.712

### Running the analysis
* Choose `Analysis > Behavioral data diffusion analysis`
* Set the variables that include the error, reaction time, participant and condition(s).
  * One or more condition variables can be set. For each other input parameter, a single variable should be chosen.
  * Reaction time and response correctness variables are mandatory, participant and condition(s) are optional.
  * (New in v2.4) Make sure that response coding and reaction time units are set correctly.
  * (New in v2.4) Optionally, you may change the default scaling parameter from 0.1 to 1.
* Find the intermediate descriptive statistics (number of trials (new in v2.4), mean error, mean RT of correct responses, variance of RT of correct responses - first three tables) and the recovered parameters (drift rate, threshold and nondecision time - next three tables) for all participants (rows) and conditions (columns) in the output.
  * (New in v2.4) You'll find the number of trials in each cell. Note that if the cell sizes differ considerably, then the recovered parameters may be biased because the edge correction uses different size of corrections with different cell size; therefore, the recovered parameters will partly correlate with your cell sizes.
  * You will find NaN values in cells where there are no data in that condition.
  * Note that when the results are copied to a spreadsheet, it may depend on the spreadsheet software whether the table headers are handled correctly. For example, Google Spreadsheet (as of 2020 January) handles the headers correctly, ONLYOFFICE (version 5.4) may miss some condition name rows, and LibreOffice (version 6.3) may mess up the table if the headers are also included.
