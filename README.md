# OReilly_R_Tidyverse_Core_Competencies_Pre-work
Pre-work exercises for the O'Reilly live online learning course 

Course web-site: [O'Reilly](https://learning.oreilly.com/live-training/courses/data-analysis-paradigms-in-the-tidyverse/0636920292555/)
Next Session: July 30, 2019 - 6:00pm – 9:00pm CEST

## Pre-work assignment

This course serves as an introduction to the R Tidyverse. To give you an idea of the analytical problems we'll address, let's take a look at the data sets we'll use in the course. 

In the data folder you'll find four sub-folders containing data files. Below I give a brief description of the data and some analytical questions we'd like to answer.

Take a look at the files, and for each exercise, write at least pseudo code describing how you would tackle the solution. If you're motivated, try to execute your analysis in R (base, or if you're already familiary with the Tidyverse).

### Dataset 1: plants

In these data files we have the dry weight of 30 plants evenly split among 3 treatment groups -- control, treatment 1 and treatment 2.

#### Exercises

For PlantGrowth.txt:

A) Plot the weight of each plant, described by it's group

B) Calculate a linear model of the weight described by the group

C) Calculate descriptive statistics of each group

D) Calculate a transformation statistics of each group

For PlantGrowth_2weeks.txt

E) Calculate the mean and standard deviation for each group (ctrl, trt1, and trt2) for each week

F) Perform a z-score transformation on each group (ctrl, trt1, and trt2, disregarding week)

### Dataset 2: science

This file contains over 1200 proteins and their abundances identified using mass spectometry.

#### Exercises

A.1) Calculate a log2 transformation on: Ratio.H.M, Ratio.M.L, and Ratio.H.L

A.2) Calculate a z-score transformation on the transformed ratio columns

B) Calculate a log10 transformation on: Intensity.H, Intensity.M, and Intensity.L

C) Return a table of proteins that have the a z-score and log2 transformed ratio above 2

D) Return a table of proteins that have the 10 highest Intensity.H

Using text:

A) Extract only the Ratio columns for the Uniprot IDs GOGA7_MOUSE and PSA6_MOUSE proteins

B) Keep only the first Uniprot ID (i.e. delete everything after the _)

C) Keep only protein descriptions that contain the phrase "Ubiquitin"

D) Does capitalization make a difference in the answer to C, above?

### Dataset 3: weather 

These four files contain the average daily temperatures from from 1995 - 2015 for four major world cities: Paris, New York, London and Reykjavik.

#### Exercises

A.1) Beginning with New York (NYNEWYOR.txt) calculate the average temperature for each month of each year and plot that against the month. The plot should have multiple lines, one for each year.

A.2) let all the lines be black, except for 2015, which is red.

B) Read all four temperature data sets into one large data frame. 

C) Produce one plot with for sub-plots at once, one for each city.

C) Automatically create individual plots for each city, save them to your hard drive with an appropriate name. 

### Dataset 4: meditation

This is the result of an experiment to measure the relative gene expression level (we'll refer to this as "value") of 6 pro-inflammatory genes (RIPK2, COX2, CCR7, CXCR1, IL-6 & TNF) in two groups of individuals (i.e. "treatment"): those with a history of meditation (Meditation) and those without (Control). Measurements were taken in the morning (time 1) and in the afternoon (time 2) after a full day of mediating (experimental group) or liesure (control). 

#### Exercises

A) Calculate each of the following statistics for each of the unique 24 combinations of gene, treatment and time:
- average: the mean of the value
- n: the number of observations in each group
- SEM: The standard error of the mean (standard deviation divided by the square root of n)
- lower95: The upper 95% CI limit
- upper95: The upper 95% CI limit

B) Plot the raw values as such:
- time on the x-axis
- value on the y-axis
- points colored according to treatment, on
- 6 sub-plots, one for each gene

C) Calculate an ANCOVA using the following formula: value ~ treatment + time for for each gene.
