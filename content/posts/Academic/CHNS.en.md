---
weight: 5
title: "China Health and Nutrition Survey (CHNS) Documentation"
date: 2021-02-22T15:23:33+08:00
draft: false

description: "sky description"

upd: "A document summary of CHNS"

tags: ['Academic', 'Database']
categories: []
---

A document summary of CHNS

<!--more-->

The China Health and Nutrition Survey (CHNS), an ongoing open cohort, international collaborative project between the Carolina Population Center at the University of North Carolina at Chapel Hill and the National Institute for Nutrition and Health (NINH, former National Institute of Nutrition and Food Safety) at the Chinese Center for Disease Control and Prevention (CCDC), was designed to examine the effects of the health, nutrition, and family planning policies and programs implemented by national and local governments and to see how the social and economic transformation of Chinese society is affecting the health and nutritional status of its population. The impact on nutrition and health behaviors and outcomes is gauged by changes in community organizations and programs as well as by changes in sets of household and individual economic, demographic, and social factors.

The survey was conducted by an international team of researchers whose backgrounds include nutrition, public health, economics, sociology, Chinese studies, and demography. The survey took place over a 7-day period using a multistage, random cluster process to draw a sample of about 7,200 households with over 30,000 individuals in 15 provinces and municipal cities that vary substantially in geography, economic development, public resources, and health indicators. In addition, detailed community data were collected in surveys of food markets, health facilities, family planning officials, and other social services and community leaders.

Following are official documentation of CHNS. A careful review of these materials will help you:

- Navigate the questionnaires and data files more efficiently
- Determine which files should be combined to create the analyses files you need
- Alert you to features and problems in the data that may affect your analysis.

## ID Variables - case identifiers, how to merge files across survey years.

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

## Special LINE Numbers

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