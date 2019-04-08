# The Indiana Training Program in Public & Population Health Informatics
## Didactic Material
### Introduction

The last decade or so has seen tremendous changes in the healthcare landscape. Most notably, paper records have now been replaced by electronic health records (EHRs). These records capture highly detailed information regarding the care a patient receives. This includes information on medications received, tests performed, diagnoses, hospital stays etc. As you can imagine this data can be highly valuable from a research standpoint. However, due to its sheer volume and granularity, analyzing data derived from an EHR poses challenges related to data analysis and interpretation that make it harder to derive value from this data. 

In addition to generating large amounts of data, EHRs have also made it possible to share health data of entire populations for public health practices. For instance, EHRs have made it possible to monitor population health data in real-time in order to detect outbreaks, or any sudden changes in the health status. This process is known as syndromic surveillance and allows public health agencies to monitor public health and enables the early detection of outbreaks and epidemics. This in turn facilitates public health agencies to  mobilize a swift and appropriate response to any emergencies. 

As part of the the Indiana training program in public and population health informatics, we created excercise sets which focus on these two related but distinct use cases of electronic healthd ata. In the following exercises, we will see some examples of ways in which EHR-derived data can be manipulated and used to answer research questions. In addition to EHR data, the use of publicly available data from online sources such as webpages is also becoming increasingly popular in public health research. As such, we will also explore one such use case which focuses on extracting data from the National Oceaonographic and Atmosphereic Administration website using _web scraping_ methods.


**Note: While the datasets used in these exercises have been derived from real EHR data, for privacy and security purposes they have been deidentified and perturbed. Since individual observations in the data have been modified, spurious associations may be discovered and as such, these findings should \*NOT\* be considered as evidence or as scientific premise for future research.**

## Exercise set I: Type-2 Diabetes Mellitus (T2DM)
### The Premise
You are a researcher who is interested in studying glycemic control in diabetic patients. You have just been given access to EHR-derived data on Type-2 Diabetes Mellitus patients and are looking to use this data to examine the association between glycemic control and body mass index.

### The Tasks
There are several tasks that are involved in answering your research question, from acquiring raw data to actually creating an analytic dataset that will be used to run the final analysis. You need to first clean the data to make it more meaningful. This involves dropping observations, recoding the data, checking for outliers and missingness, and checking validity of observations (e.g. males should not be pregnant) among other things. Additionally, you may need to bring in information from other data sources to add more meaning to the observations in your dataset. Further, it is possible that the "shape" of the data that you receive may not be optimal for your analysis. This may require reshaping your dataset to the strucuture most suitable for your analysis.

In the exercises that follow we will do a little bit of everything that we just discussed. Remember that these are not essentially discrete processes, meaning that you will often do multiple things to achieve the desired result.

To reiterate, our research question focuses on examining the relationship between glycemic control and body mass index. It is also likely that an individual's race and gender may affect this relationship. As such, we need to include this information in the analysis. 

In Exercise 1, we will follow steps that clean the patient data file in our dataset by recoding the race variable. We will recode in two different ways and examine how this affects the variable.

In Exercise 2, we will examine the medications file in our dataset. Specifically, we will make this data more meaningful by merging this file with an external dataset. Finally, we will see how adding this new information helps categorize individual medications into broader categories.

In Exercise 3, we will use the clinical variables file in our dataset to derive information on body mass index. Body mass index is not always present in EHR-derived data, however, since this is our independent variable (x) of interest we will try to maximize the number of observations that we can get for BMI by either finding BMI in the dataset or deriving it from height and weight.

In Exercise 4, we will derive information on glycemic control by extracting information on glycated hemoglobin (hba1c) values. We will then use several variables that we created in Exercises 1-3 to examine our research question. Our final analysis will be a linear regression which examines the relationship between BMI and Hba1c while controlling for gender and race. 

How will these findings change if we also control for medications, specifically anti-diabetic medications? Use the medication categories derived in Exercise 2 to rerun this regression while controlling for medications. What decisions did you have to make regarding choosing the medication categories? Which observations were included in the analytic dataset? What was the rationale for doing so? Finally, how do the findings change when you control for medications?

## Exercise set II: Public Health Emergency Surveillance System
### The Premise
You are a researcher who is interested in investigating the distribution and relation between causes for emergency admissions in the Indiana Health System using the Public Health Emergency Surveillance System (PHESS) data. While new to R, you are interested in learning the tidyverse method for transforming, summarizing, and visualizing data in the R programming language.

### The Tasks
The PHESS data includes duplicated records, which we will deal with as necessary, but also brings up many questions, including the relationship between FLAG variables in the data, and the creation of new relevant FLAG variables using the text fields available in the dataset. Our primary aim is also to become more proficient at transforming and visualizing data using the R programming language, and in specific, the `ggplot2` and `dplyr` libraries, two of the primary choices for data scientists who utilize R in their workflows.

In Exercise 1, we will learn basic `dplyr` commands for selecting, filtering, mutating, and summarizing data. We will also investigate more flexible methods for filtering, selecting, and mutating data based on patterns in the variable names. We will then learn how to group our data and summarize in several manners by categories embedded in the data. Finally, we will learn how to restructure data from so-called “wide” to “long” format, and vice versa.

In Exercise 2, we will learn basic `ggplot2` visualization techniques using the grammar of graphics built into this package. We will learn how to change labels in a plot and also change the presentation of scales in the plots created. We will also learn how to visualize data by groups similar to how we summarized data by group using `dplyr` in exercise 1. Finally, we will learn how one can create new FLAG variables using the R package `stringr`.

In Exercise 3, we will try to put all of our knowledge together and apply a dimension reduction technique to the **PHESS** data with hopes of reducing the number of FLAG variables we need to consider in future analyses. This process includes calculating the Pearson Phi coefficient for binary data and also utilizing the `ggcorrplot` function, which provides aesthetically pleasing visual representations of correlation matrices. Finally, we apply Principal Components Analysis (**PCA**) to the FLAG data. We find that there are insufficient correlations between most FLAG variables, and that the **PCA** identifies components of which the first two are driven by the two most common FLAG variables in the **PHESS** data.

## Exercise set III: Web Scraping Using R  
### The Premise  
You are a public health researcher interested in extracting data from sources on the web with little to no experience with web development or web scraping.

### The Tasks  
This standalone exercise provides an introduction to navigating the document object model (DOM) of a web page in order to write an R script which extracts the desired data in a tabular format using the R package `rvest`. Screenshots are provided to help individuals who are new to web scraping understand how to navigate a page using the DOM, and demonstrations are given for extracting data held in tables from the website https://airquality.weather.gov

This process can easily be scaled up in R using for loops, while loops, etc. to extract data from many different locations over a short period of time.  

****  
We hope you enjoy these exercises and find them useful in your research process. 

Happy Coding!
