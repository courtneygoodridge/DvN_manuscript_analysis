# Contrasting symbolic and non-symbolic numerical representations in a joint classification task: code and analysis

## Reference
Prpic, V., Basamh, Y. A., Goodridge, C. M., Agostini, T., & Murgia, M. (2023). Contrasting symbolic and non-symbolic numerical representations in a joint classification task. Psychonomic Bulletin & Review, 1-9.

## Overview: experimental design 
Many studies highlight that people represent numbers on mental number lines. Evidence of this occurs in the SNARC (spatial–numerical association of response codes) effect, whereby people are faster to respond with left key pressses for small numbers and faster right key presses for large numbers. The experiment highlighted in this repository aimed to understand whether symbolic (digits) and non-symbolic (dots) numerals interacted with the SNARC effect. 

The experiment was conducted online. Participants were instructed to place their left index finger on the "A" key and their right finger on the "L" key. All participants completed two tasks - symbolic, and non-symbolic. Participants were presented with the following stimuli (Figure taken from Prpic et al, 2023):

<img width="465" alt="image" src="https://github.com/courtneygoodridge/DvN_manuscript_analysis/assets/44811378/07c39a2c-ff15-4eaf-a3ba-a2aa9592eb11">

For the first block of the symbolic task, participants were asked to judge the symbolic numerals (digits) and ignore non-symbolic numerals (the numerosity of the dots). Specifically, participants were asked to determine whether the digit was larger ("L" key press) or smaller ("A key press) than 3. For the second block the keys were switched for indicating smaller ("L key press) or larger ("A" key press). Instructions were the same for the non-symbolic task; participants had to determine whether there were more or less than 3 digits (non-symbolic numeral/numerosity) while ignoring the digits’ magnitude (symbolic numerals). Response keys for the second block of the non-symbolic task were also switched. More details on the procedure can be found within the manuscript. 

## Code and analysis
The `Dice_SNARC2.zip` file contains the [PsychoPy](https://www.psychopy.org/) script that runs the experiment. PsychoPy is a free software tool that allows researchers to run Psychology experiments using open source software. The `.xlsx` files are used by the PsychoPy scripts to render the stimuli for the experiment. The block files specify the stimuli, their positions, the condition, and the correct key to press. Group A and B files are instructions for counterbalancing.  

Within the Analysis_script folder, there are 3 analysis scripts. `Run DvN_SNARC.Rmd` contains code for the inferential analysis and manuscript figures. Inferential analysis comprises of a Repeated Measures ANOVA. The data for this analysis script is `dat_main.csv`. The `DvN_SNARC_cleaning.Rmd` script contains code to for preprocessing session 1 (`Session1.xlsx`) and 2 (`Session2_combine.xlsx`) data. These were the two sessions of data collection, and thus need to be cleaned and combined for formal analysis. `DvN_SNARC_additional_analysis.Rmd` contains code for additional analysis. In certain [SNARC effect analyses](https://link.springer.com/article/10.1007/s00426-018-1125-1), a linear regression model is fitted on the difference between left and right hand responses for each number; a negative slope being indicative of a SNARC effect. We computed this for the current analysis, but did not include it in the final manuscript. Whilst the manuscript drafts can be found in the Manscripts folder, the appendices for the published manuscript can be found on [Open Science Framework](https://osf.io/e7rj3/).

To run these scripts, clone the `DvN_manuscript_analysis` repository into your working directory (you can find this by running the `here::here()` function in the R command line). For more information on using the `here::here()`, see the [documentation](https://here.r-lib.org/). Once the repository is in your working directory, run each chunk of code to run the models and analysis. Session information is provided below in case of package dependency issues.

## Session info
`sessionInfo()`

<img width="664" alt="image" src="https://github.com/courtneygoodridge/DvN_manuscript_analysis/assets/44811378/90f66773-6066-4871-8f13-3134aab1870c">




 
