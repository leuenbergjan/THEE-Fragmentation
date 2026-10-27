# Evolutionary rescue under the influence of habitat fragmentation
## THEE Research Practical 2026

**Authors:** Jan Leuenberger & Safeeya Ramis  
**Date:** October 27, 2026

## Overview

This project analyzes the probability of evolutionary rescue under habitat 
fragmentation and was conducted as part of the Theoretical Research Practical.

In this scenario, the main habitat, containing a population with wild-type 
allele and a beneficial mutant allele will be divided into two separate habitats 
at a certain time point. The simulations are then used to assess whether the 
populations in the new habitats will experience evolutionary rescue, and also 
whether only one or both of the habitats will be rescued.

The Base code for this project was provided by THEE Lab.

## Main Questions

The main questions we want to answer regarding evolutionary rescue under 
habitat fragmentation are:

- Is evolutionary rescue possible in the Fragmented habitats?
- What is the impact of split_time on ER?
- What is the impact of the habitat proportions on ER?

## Variables & Parameters

Following you will find a table containing the most important variables and parameters:

| Name | Meaning |
|---|---|
| `N_a`, `N_A` | current size of the wild-type / mutant population (change over time) |
| `N_init_a`, `N_init_A` | initial sizes of wild type (positive integer) and mutant (non-negative integer) |
| `decay_rate` | detrimental effect of the environment on the wild type (> 0 so that extinction is possible) |
| `sel_coeff` | selective advantage of the mutant (should be > `decay_rate` to allow rescue) |
| `mut_rate` | mutation rate from wild type to mutant (> 0 and small) |
| `t_max` | maximum number of generations simulated (a setting, not a model parameter) |
| `split_time` | generation at which the fragmentation happens (integer > 0) |
| `split_ratio` | probability with which each individual is assigned to habitat B at the split (between 0 and 1) |
| `habitat_prop` | share of the total carrying capacity given to habitat B (between 0 and 1); habitat C gets `1 - habitat_prop` |
| `K` | carrying capacity of the original (unsplit) habitat; limits growth and is divided among B and C in the same proportions as the habitats |

## Steps to make the code run



