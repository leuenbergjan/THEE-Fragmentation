------------------------------------------------------------------------

editor_options: markdown: wrap: 72 ---

# Evolutionary rescue under the influence of habitat fragmentation

## THEE Research Practical 2026

**Authors:** Jan Leuenberger & Safeeya Ramis\
**Date:** October 28, 2026

### Overview

This project analyzes the probability of evolutionary rescue under habitat fragmentation and was conducted as part of the Theoretical Research Practical at the University of Bern.

In this scenario, the main habitat, containing a population with wild-type allele and a beneficial mutant allele will be divided into two separate habitats at a certain time point. The simulations are then used to assess whether the populations in the new habitats will experience evolutionary rescue, and also whether only one or both of the habitats will be rescued.

The Base code for this project was provided by the [banklab](https://github.com/banklab/THEErp2025).

### Main Questions

The main questions we want to answer regarding evolutionary rescue under habitat fragmentation are:

- Is evolutionary rescue possible in the fragmented habitats?
- What is the impact of the splitting time on evolutionary rescue?
- What is the impact of the habitat proportion on evolutionary rescue?

### Variables & Parameters

Following you will find a table containing the most important variables and parameters used in our model:

| Name | Meaning |
|------------------------------------|------------------------------------|
| `N_a`, `N_A` | current size of the wild-type / mutant population (change over time) |
| `N_init_a`, `N_init_A` | initial sizes of wild type (positive integer) and mutant (non-negative integer) |
| `decay_rate` | detrimental effect of the environment on the wild type (\> 0 so that extinction is possible) |
| `sel_coeff` | selective advantage of the mutant (should be \> `decay_rate` to allow rescue) |
| `mut_rate` | mutation rate from wild type to mutant (\> 0 and small) |
| `t_max` | maximum number of generations simulated (a setting, not a model parameter) |
| `split_time` | generation at which the fragmentation happens (integer \> 0) |
| `split_ratio` | probability with which each individual is assigned to habitat B at the split (between 0 and 1) |
| `habitat_prop` | share of the total carrying capacity given to habitat B (between 0 and 1); habitat C gets `1 - habitat_prop` |
| `K` | carrying capacity of the original (unsplitted) habitat; limits growth and is divided after the splitting time point among B and C in the same proportions as the habitats |

### Packages needed

To run the code, the following packages are required.

\- ggplot2

\- tidyr

\- dplyr

If they have not been installed yet, you can do this as follows by using the command `install.packages(...)`:

\- `install.packages("ggplot2")`

\- `install.packages("tidyr")`

\- `install.packages("dplyr")`

### Files and functions

To provide an overview of the various files in the repository, they are briefly listed and explained below:

| Name | Meaning |
|------------------------------------|------------------------------------|
| `.gitignore` | Files which are not needed and not important for the project, they can be ignored. |
| `Base Model.Rmd` | Base model provided from the [banklab](https://github.com/banklab/THEErp2025) which can be knitted to get an .html or .pdf format of it. |
| `README.md` | Md file creating this explanation for the repository. |
| `THEE_fragmentation.Rmd` | The report notebook of our project which runs the simulations and include the actual code used for the project. |
| `AI promts.pdf` | This file should give transparency of the use of AI during our project, showing all the AI prompts. |
| `THEE_fragmentation.pdf` | The knitted pdf version of our report. |
| `Habitat fragmentation.pptx` | Might be not uploaded yet, but will show the presentation for the project. |

### Structure overview of the code

The report notebook is broadly organized into the following sections:

- Title
- Authors
- Abstract
- Introduction
- Model & Methods
- Results
- Discussion
- References

The actual code can be found in the Model & Methods section and contains four rough junks:

1\. Calculations for one generation of the population

2\. Trajectory of the population over time

3\. Generation of plots showing the trajectory

4\. Analysis with varying model parameters

### Help

For further questions and explanations you are welcome to contact the authors via e-mail:

- [safeeya.mohamedramis\@students.unibe.ch](mailto:safeeya.mohamedramis@students.unibe.ch){.email}
- [jan.leuenberger1\@students.unibe.ch](mailto:jan.leuenberger1@students.unibe.ch){.email}
