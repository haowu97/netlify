---
title: "China Health and Nutrition Survey (CHNS) Documentation"
date: 2021-02-22T15:23:33+08:00
draft: false

description: "A document summary of CHNS"
upd: "A document summary of CHNS"

tags: ['Academic', 'Database', 'CHNS']
categories: []
---

<!--more-->

The China Health and Nutrition Survey (CHNS), an ongoing open cohort, international collaborative project between the Carolina Population Center at the University of North Carolina at Chapel Hill and the National Institute for Nutrition and Health (NINH, former National Institute of Nutrition and Food Safety) at the Chinese Center for Disease Control and Prevention (CCDC), was designed to examine the effects of the health, nutrition, and family planning policies and programs implemented by national and local governments and to see how the social and economic transformation of Chinese society is affecting the health and nutritional status of its population. The impact on nutrition and health behaviors and outcomes is gauged by changes in community organizations and programs as well as by changes in sets of household and individual economic, demographic, and social factors.

The survey was conducted by an international team of researchers whose backgrounds include nutrition, public health, economics, sociology, Chinese studies, and demography. The survey took place over a 7-day period using a multistage, random cluster process to draw a sample of about 7,200 households with over 30,000 individuals in 15 provinces and municipal cities that vary substantially in geography, economic development, public resources, and health indicators. In addition, detailed community data were collected in surveys of food markets, health facilities, family planning officials, and other social services and community leaders.

Following are [official documentation of CHNS](https://www.cpc.unc.edu/projects/china/data/documentation). A careful review of these materials will help you:

- Navigate the questionnaires and data files more efficiently
- Determine which files should be combined to create the analyses files you need
- Alert you to features and problems in the data that may affect your analysis.

## [ID Variables](https://www.cpc.unc.edu/projects/china/data/documentation/idvar) - case identifiers, how to merge files across survey years

Two systems of ID variables have been employed in CHNS data files: the original system used in surveys before 2004, and a revised system used thereafter. All old IDs have been changed to new IDs in all files.

### Household ID (HHID)

HHID is a nine-digit numeric variable that uniquely identified each household that had been seven digits in the old cross-sectional files. The variables T1 through T5 (documented in the questionnaire) were concatenated to form the HHID. Each HHID value represented one household. When the unit of analysis for a file/table was household, 1 HHID = 1 row = 1 household = 1 observation. Observations in these files were sorted by HHID and survey year (Wave). Thus the key sort variables for these files were HHID and Wave.

### Individual ID (IDind)

The IDind is a twelve-digit numeric variable that uniquely identified for all participants. Each participant will have the same ID in all datasets and in all survey years. The unique ID will not change over time and will facilitate data merges across datasets and survey years. Each IDind value represented one individual. When the unit of analysis for a file/table was individual, 1 IDind = 1 row = 1 individual = 1 observation. Observations in these files are sorted by IDind, and Wave, i.e., the key sort variables were IDind, and Wave.

### Community ID (COMMID)

A third ID variable, COMMID, is a six-digit numeric variable that uniquely identified each community. The variables T1 through T4 were concatenated to create COMMID. Each COMMID value represented one community. When the unit of analysis for a file was community, 1 COMMID = 1 community = 1 observation. Observations in these files were sorted by COMMID and Wave, i.e., the key sort variables were COMMID and Wave. Although COMMID was not required for most file merges, this variable was included on all data sets to facilitate merges with community-level files.

When the unit of analysis was something other than individual, household or community (e.g., job, livestock type, food item, health facility), a variable that identified this unit was included on the file (e.g., JOB, F11, FOODCODE, Q1). For the files/tables where job was the unit of analysis, for example, each value of the variable JOB represented one occupation. That is, 1 JOB = 1 row = 1 occupation = 1 observation. Observations in these files were sorted by HHID, LINE, and JOB, i.e., the key sort variables were HHID, LINE, and JOB.

### Survey Year (WAVE)

The WAVE is a four-digit numeric variable that identified survey year (i.e, 1989, 1991, 1993, 1997, 2000, 2004, 2006, 2009, 2011, 2015). This variable was used in master longitudinal files only.

## [Special LINE Numbers](https://www.cpc.unc.edu/projects/china/data/documentation/lineno) - important LINE numbers

Some special LINE numbers used in the data files are:

21 = first new household member added to the roster in 1991
22 = second new household member added to the roster in 1991, and so on
31 = first new household member added to the roster in 1993
32 = second new household member added to the roster in 1993, and so on
41 = first new household member added to the roster in 1997
42 = second new household member added to the roster in 1997, and so on
61 = first new household member added to the roster in 2000
62 = second new household member added to the roster in 2000, and so on
77 = grandparent
88 = uncle/aunt
99 = other
-2 = guest

For LINE numbers 21, 22, 31, 32, 41, 42, 61, 62, etc., the first digit identifies the round in which the individual first appeared in the Household Member Roster (2=1991, 3=1993, 4 & 5=1997, 6=2000).

LINE numbers 77, 88, and 99 are used in the Childcare section of the Household Survey.

LINE number -2 is used in the Nutrition Survey.

## [Unit of Analysis](https://www.cpc.unc.edu/projects/china/data/documentation/unit) - critical concept for analysis of multi-level data

The CHNS data have been collected at many different levels: community, household, individual, job, food item, etc. The unit of analysis for a file can often be determined by a careful review of the appropriate questionnaire section.

Because of the multi-level nature of the data and the large number of files, most users of the CHNS data must perform complex file merges on a regular basis. A thorough understanding of complex file structures is critical to the successful use of these data. To merge CHNS files properly, users must know the unit of analysis for each data file, be familiar with the case identifiers ([ID Variables](https://www.cpc.unc.edu/projects/china/data/documentation/idvar)), and understand exactly how to use their software to combine files.

## [Variable Names](https://www.cpc.unc.edu/projects/china/data/documentation/varnames) - variable-naming system

Most CHNS variable names consist of an alphabetic prefix (A, B, etc.) followed by a number. Each table/section of the questionnaire employs a different prefix. Variable names are normally printed below or to the right of the corresponding question on the questionnaire.

Some variables were renamed to facilitate use of the data. For example, variables that identify line numbers in tables were renamed "LINE" (see [ID Variables](https://www.cpc.unc.edu/projects/china/data/documentation/idvar)). The suffix "_91" was added to the 1991 variables to distinguish them from similarly named 1989 variables, and "_93" was added to the 1993 variables. However, "_97" and "_00" suffixes were not added to the 1997 and 2000 variables. Suffixes are not indicated in the questionnaires.

Note that some variables documented in the questionnaires do not appear in the data files, particularly in 1989 data sets. Many of these variables were never entered into a computer file. Also note that variables T1 through T5 were dropped from 1989, 1991 and 1993 files since they were combined to form household and community identifiers (see [ID Variables](https://www.cpc.unc.edu/projects/china/data/documentation/idvar)). The variables T1 through T5 were *not* dropped from 1997 and 2000 files. Finally the variables in the data files are not necessarily in the same order that they appear in the documentation.

## [Missing Values](https://www.cpc.unc.edu/projects/china/data/documentation/missing) - missing value indicators

Negative numbers (-9, -99, -999, -8, -88, -888, etc.) are typically used to identify missing values. Large positive numbers (88, 888, 99, 999, etc.) are also used for some variables. Many missing values are not documented in the questionnaire.

## [Date Variables](https://www.cpc.unc.edu/projects/china/data/documentation/datevar) - how date variables are handled

Date information was originally entered using separate date variables (year, month, day). In 1989, 1991, and 1993 files, these variables were concatenated to form 4- and 6-digit variables of the form YYMM and YYMMDD, where YY=year, MM=month, and DD=day. Although they are documented in the questionnaires, the original year, month, and day variables have been deleted from 1989, 1991, and 1993 data files.

Separate date variables (year, month, day) still exist in 1997 and 2000 files. The 1997 and 2000 year variables have the form YYYYS dates are used in the Master File.

## [Data Cleaning](https://www.cpc.unc.edu/projects/china/data/documentation/cleaning) - general cleanup effort

Basic data cleaning has included:

- Corrections to ID variables
- Corrections to the household roster
- Deletion of duplicate records
- Deletion of blank records
- Recoding out-of-range values to missing status.

Note that only values that were clearly **impossible** were recoded to missing. The significance of extreme values still remaining in the files is left to the discretion of individual researchers.

## [Notes / Data Problems](https://www.cpc.unc.edu/projects/china/data/documentation/notes) - important data features and problems

### Sampling-Unit Variables (T1-T5)

The original sampling-unit variables T1 through T5 were concatenated to form community and household ID variables (COMMID, HHID). They are still kept in master longitudinal files, although they contribute no unique information.

### Area of Residence Variables

Area of residence variables (STRATUM and URBAN) can be constructed from the original sampling-unit variables. The short SAS program that constructed these variables is available upon request by sending an email message to [chns@unc.edu](mailto:chns@unc.edu).

### Incorrect Variable Names

Several variables were named incorrectly in the original 1997 and 2000 Chinese questionnaires. The translated English questionnaires include the original name, with the corrected name as it appears in the data file enclosed in [brackets] to the right or below the original name.

## Biomarker Data

The biomarker data collected in CHNS 2009 involves the release of 26 fasting blood measures on individuals aged 7 and older. This included major cardiovascular biomarkers (lipids, diabetes such as HbA1c, glucose, insulin, triglycerides, CRP) and important nutrition biomarkers (transferrin, hemoglobin, and ferritin).  An overview of some of the key results was published in: Yan, Shengkai, J. Li, S. Li, B. Zhang, S. Du, P. Gordon-Larsen, L. Adair, B.M. Popkin (2012) The expanding burden of cardiometabolic risk in China: the China Health and Nutrition Survey. [Obesity Reviews 13 (9): 810-21. ](http://onlinelibrary.wiley.com/doi/10.1111/j.1467-789X.2012.01016.x/pdf)PMCID: PMC3429648. 

 The full documentation of the collection and laboratory measurement are also placed as documents online:

- Protocols used to collect and process blood samples are available [here](https://www.cpc.unc.edu/projects/china/data/datasets/Blood Collection Protocol_English.pdf).
- A list of biomarkers and methods used to measure them is available [here](https://www.cpc.unc.edu/projects/china/data/datasets/Biomarker_Methods.pdf).
- Codebook of the biomarker dataset is available [here](https://www.cpc.unc.edu/projects/china/data/datasets/C10BIOMARKER.pdf).

## Constructed Variables

### Income Measures

 The constructed household income variables have been completely revised in 2011, and individual income variables have been constructed as well. These measures are fully documented below in PDF format:

- [Household Income Variable Construction](https://www.cpc.unc.edu/projects/china/data/datasets/Household%20Income%20Variable%20Construction.pdf), *92 KB*
- [Individual Income Variable Construction](https://www.cpc.unc.edu/projects/china/data/datasets/Individual%20Income%20Variable%20Construction.pdf), *44 KB*

These files are longitudinal, with one observation per household or individual per wave. Income measures include:

#### Household Income (HHINC_10.sas7bdat)

Total Annual Household Income, Nominal
     Total Annual Household Income, Inflated to 2015
     Per Capita Household Income
     Components of Household Income (Business, Wages, etc.)

 Click [here](https://www.cpc.unc.edu/projects/china/data/datasets/longitudinal/codebook/HHINC_10.pdf) to review the codebook.

#### **Individual Income (INDINC_10.sas7bdat)**

​     Total Annual Individual Income, Nominal
​     Total Annual Individual Income, inflated to 2015
​     Components of individual income (business, wages, etc.)

Click [here](https://www.cpc.unc.edu/projects/china/data/datasets/longitudinal/codebook/INDINC_10.pdf) to review the codebook.

Follow the link below to "Download Constructed Variables" and select "Longitudinal" to find the constructed income files.

### Nutrient Intake Variables (C12DIET.sas7bdat)

Nutrient intake variables are constructed. The unit of analysis for these files is *individual*.

Nutrient intake variables include:

Average Daily Calorie Intake (in kilocalories) for Each Survey YearAverage Daily Protein Intake (in grams) for Each Survey YearAverage Daily Fat Intake (in grams) for Each Survey YearAverage Percent Calories From Fat for Each Survey Year

Click [here](https://www.cpc.unc.edu/projects/china/data/datasets/longitudinal/codebook/c12diet.pdf) to review the codebook.

[**Download Constructed Variables**](https://www.cpc.unc.edu/projects/china/data/datasets/data_downloads)

## Longitudinal Data Master Files

by chns@unc.edu — last modified Jun 12, 2018 11:13 AM

**General Description**

These pages:

- Describe the longitudinal data
- Allow users to [download data](https://www.cpc.unc.edu/projects/china/data/datasets/data_downloads) directly from the Website

Researchers can now download datasets known as CHNS Longitudinal Master Files. These new Master Files are designed to make longitudinal analysis of the CHNS Survey data much easier. The new Master Files consolidate and standardize data from multiple survey years into a select number of Master Files, and they address the following problems:

- ID (identification numbers) problems are corrected and consistent across all survey years. In addition, individuals who have lived in multiple households and had multiple IDs, now have all their data stored under their most current ID. Their previous IDs have been saved in the Master ID file.

- Birth dates are corrected and stored only in the Master ID File. And birth dates are now stored as both Western and Lunar dates.

- Gender has been corrected as needed and is stored only in the Master ID File and the Master PE File.

- Household Interview Dates are determined for all longitudinal files that may need to calculate age. Age is generally calculated as ((Household Interview Date - Western DOB) / 365.25).

- Variable names are standardized across all survey years when they represent the same survey question. With a few exceptions, they are standardized to the 2000 variable name.

- Data formatting is standardized across all survey years. All dates are now stored in the YYYYMMDD format.

Click [here](https://www.cpc.unc.edu/projects/china/data/datasets/longitudinal/codebook/mast_pub_12.pdf) to obtain a detailed pdf file that provides a full layout of the contents and organization of these files.

[**Download the Data**](https://www.cpc.unc.edu/projects/china/data/datasets/data_downloads)