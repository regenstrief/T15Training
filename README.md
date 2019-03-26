# The Indiana Training Program in Public & Population Health Informatics
## Didactic Material
### Introduction

The last decade or so has seen tremendous changes in the healthcare landscape. Most notably, paper records have now been replaced by electronic health records (EHRs). These records capture highly detailed information regarding the care a patient receives. This includes information on medications received, tests performed, diagnoses, hospital stays etc. As you can imagine this data can be highly valuable from a research standpoint. However, due to its sheer volume and granularity, analyzing data derived from an EHR poses challenges related to data analysis and interpretation that make it harder to deriver value from tis data. 

In addition to generating large amounts of data, EHRs have also made it possible to share health data of entire populations for public health practices. For instance, EHRs have made it possible to monitor population health data in real-time in order to detect outbreaks, or any sudden changes in the health status. This process is known as syndromic surveillance and allows public health agencies to monitor public health and if needed mobilize a swift and appropriate response to any emergencies. 

As part of the the Indiana training program in public and population health informatics, we created excercise sets which focus on these two related but distinct use cases of electronic healthd ata. In the following exercises,we will see some examples of ways in which EHR-derived data can be manipulated and used to answer research questions.

**Note: while the datasets used in these exercises have been derived from real EHR data, for privacy and security purposes they have been deidentified and perturbed. Since individual observations in the data have been modified, spurious associations may be discovered and as such, these findings should \*NOT\* be considered as evidence or as scientific premise for future research.**

## Exercise set I: Type-2 Diabetes Melitus (T2DM)
### The Premise
You are a researcher who is interested in studying glycemic control in diabetic patients. You have just been given access to EHR-derived data on Type-2 Diabetes Melitus patients and are looking to use this data to examine the association between glycemic control and body mass index.

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

### The Tasks
