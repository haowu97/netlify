---
title: "China Health and Nutrition Survey (CHNS) Study Notes"
date: 2021-02-23T17:59:50+08:00
lastmod: 2021-02-24T17:59:50+08:00
draft: false

description: ""
upd: "The data volume of CHNS is very large, and it merges the data of many years, so it feels very confusing for people who just got started. This article records my experience of processing the CHNS database."

tags: ['Academic', 'Database', 'CHNS']
categories: []
---

CHNS data is stored in different compressed packages according to categories. After downloading to the same path, first use the following Python code to decompress all compressed packages:

```python
import os
import zipfile

# The directory where the compressed package is located
src_dir = r"D:\Workfiles\Academic\Databases\CHNS\Data\RawArchive"
# The destination directory to unzip the compressed package 
dst_dir = r"D:\Workfiles\Academic\Databases\CHNS\Data\Tree"

def unzip_file(zip_src, dst_dir):
    zip_name = zip_src.split("\\")[-1]
    file_name = zip_name.split(".")[0]
    r = zipfile.is_zipfile(zip_src)
    if r:     
        fz = zipfile.ZipFile(zip_src, 'r')
        for file in fz.namelist():
            if len(file.split('/')) == 1:
                # The current file is in the root directory
                fz.extract(file, dst_dir+"\\"+file_name) 
            else:
                # The current file isn't in the root directory
                fz.extract(file, dst_dir) 
        fz.close()
    else:
        print('This is not zip')

for filename in os.listdir(src_dir):
    zip_src = src_dir+ "\\" +filename
    unzip_file(zip_src, dst_dir)
```

The data provided by CHNS is in SAS format. Since SAS is not usually used, in order to facilitate data reading and viewing, the data is uniformly converted to CSV format using Python and placed under the agreed path:

```python
import pandas as pd

def sas7bdat2CSV(path):
    data = pd.read_sas(path)
    dst_path = path.split(".")[0]+".csv"
    data.to_csv(dst_path, index = False)
    
# The destination directory to save csv
dst_dir = r"D:\Workfiles\Academic\Databases\CHNS\Data\DataFlies"
# Traverse folders
for file in os.listdir(dst_dir):
    data_dir = dst_dir+"\\"+file
    # Traverse subfolders
    for sub_file in os.listdir(data_dir):
        # Convert sas7bdat data into CSV format
        if sub_file.endswith(".sas7bdat"):
            print(data_dir+"\\"+sub_file)
            sas7bdat2CSV(data_dir+"\\"+sub_file)
```

The file directory after processing is as follows:

```
├─biomarker_09
│      biomarker_09.sas7bdat
│      
├─Master_Agriculture_201804: Agriculture income, work hours, and cost
│      cropt_12.sas7bdat
│      farmg_12.sas7bdat
│      farmh_12.sas7bdat
│      fishh_12.sas7bdat
│      fishi_12.sas7bdat
│      foods_12.sas7bdat
│      gardh_12.sas7bdat
│      
├─Master_Asset_201804: mainly record what they have in home
│      asset_12.sas7bdat
│      
├─Master_Business_201804: Business Income & work hours
│      busi_12.sas7bdat
│      busn_12.sas7bdat
│      
├─Master_Caltrac_201410
│      en_00.sas7bdat: Individual Energy/CALTRAC File 1997-2000
│      
├─Master_Childcare_201804
│      carec_12.sas7bdat: Individual Child Care File 1989-2015
│      careh_12.sas7bdat: Household Child Care 1991-2006
│      
├─Master_Constructed_Income_201804: summary of different kind of income 
│      hhinc_10.sas7bdat
│      indinc_10.sas7bdat
│      
├─Master_Educ_201804
│      educ_12.sas7bdat: Individual Education File 1989-2015
│      
├─Master_EverMarriedWomen_201804
│      birthmast_pub_12.sas7bdat: Birth History Individual ID File through 2015
│      birth_12.sas7bdat: Birth History File 1991-1993, 2000-2015
│      emw_12.sas7bdat: Ever Married Women File 1991-2015
│      preg_12.sas7bdat: Pregnancy History File 1991-2015
│      wed_12.sas7bdat: Marriage History File 1991-2015
│      
├─Master_HealthCare_201804
│      hlth_12.sas7bdat: Individual Health Care File 1989-2015
│      ins_12.sas7bdat: Individual Medical Insurance File 1989-2015
│      
├─Master_ID_201908
│      dataset relationship.pdf
│      mast_pub_12.sas7bdat: Marriage History File (wed_12) 1991-2015
│      rst_12.sas7bdat: Roster File 1989-2015
│      surveys_pub_12.sas7bdat: Survey File 1989-2015
│      
├─Master_Income_Categories_201804: record different categories of income
│      jobs_12.sas7bdat
│      oinc_12.sas7bdat
│      subf_12.sas7bdat
│      subh_12.sas7bdat
│      subi_12.sas7bdat
│      wages_12.sas7bdat
│      
├─Master_InfantFeeding_201410
│      infed_00.sas7bdat: Infant Feeding File 1989-1993
│      infnt_00.sas7bdat: Infant Feeding Survey 1989
│      
├─Master_Livestock_201804
│      liveh_12.sas7bdat: Household Livestock File 1991-2015
│      livei_12.sas7bdat: Individual Livestock Income File 1989-2015
│      livet_12.sas7bdat: Household Livestock Type 1989-2015
│      
├─Master_Macronutrients_201410
│      c12diet.sas7bdat: Household Food Inventory 1989-2011
│      
├─Master_Media_201410
│      media_00.sas7bdat: EMW MASS MEDIA File 2000-2011
│      medsv_00.sas7bdat: Household Medical Facilities 1989-2006
│      
├─Master_PE_PA_201908
│      pact_12.sas7bdat: Physical Activity 1989-2015
│      pexam_pub_12.sas7bdat: Physical Examination 1989-2015
│      pstress_12.sas7bdat: Physical Examination 2015-2015
│      
├─Master_Relationship_201410
│      relationmast_pub_00.sas7bdat: Mast Relationship File (rst_00) 1989-2011
│      
├─Master_TimeUse_201804
│      timea_12.sas7bdat
│      
└─Master_UrbanIndex_201804
        urban_11.sas7bdat
```

`Master_ID_201908/surveys_pub_12` stores the most basic personal data. We use this as the basic individual identification to merge different data sets.

## [ID Variables](https://www.cpc.unc.edu/projects/china/data/documentation/idvar)

### Household ID (HHID)

HHID is a nine-digit numeric variable that uniquely identified each household that had been seven digits in the old cross-sectional files. The variables T1 through T5 (documented in the questionnaire) were concatenated to form the HHID. Each HHID value represented one household. When the unit of analysis for a file/table was household, 1 HHID = 1 row = 1 household = 1 observation. Observations in these files were sorted by HHID and survey year (Wave). Thus the key sort variables for these files were HHID and Wave.

### Individual ID (IDind)

The IDind is a twelve-digit numeric variable that uniquely identified for all participants. Each participant will have the same ID in all datasets and in all survey years. The unique ID will not change over time and will facilitate data merges across datasets and survey years. Each IDind value represented one individual. When the unit of analysis for a file/table was individual, 1 IDind = 1 row = 1 individual = 1 observation. Observations in these files are sorted by IDind, and Wave, i.e., the key sort variables were IDind, and Wave.

### Community ID (COMMID)

A third ID variable, COMMID, is a six-digit numeric variable that uniquely identified each community. The variables T1 through T4 were concatenated to create COMMID. Each COMMID value represented one community. When the unit of analysis for a file was community, 1 COMMID = 1 community = 1 observation. Observations in these files were sorted by COMMID and Wave, i.e., the key sort variables were COMMID and Wave. Although COMMID was not required for most file merges, this variable was included on all data sets to facilitate merges with community-level files.

When the unit of analysis was something other than individual, household or community (e.g., job, livestock type, food item, health facility), a variable that identified this unit was included on the file (e.g., JOB, F11, FOODCODE, Q1). For the files/tables where job was the unit of analysis, for example, each value of the variable JOB represented one occupation. That is, 1 JOB = 1 row = 1 occupation = 1 observation. Observations in these files were sorted by HHID, LINE, and JOB, i.e., the key sort variables were HHID, LINE, and JOB.

## Biomarker Data

The biomarker data collected in CHNS 2009 involves the release of 26 fasting blood measures on individuals aged 7 and older. This included major cardiovascular biomarkers (lipids, diabetes such as HbA1c, glucose, insulin, triglycerides, CRP) and important nutrition biomarkers (transferrin, hemoglobin, and ferritin).  An overview of some of the key results was published in: Yan, Shengkai, J. Li, S. Li, B. Zhang, S. Du, P. Gordon-Larsen, L. Adair, B.M. Popkin (2012) The expanding burden of cardiometabolic risk in China: the China Health and Nutrition Survey. [Obesity Reviews 13 (9): 810-21. ](http://onlinelibrary.wiley.com/doi/10.1111/j.1467-789X.2012.01016.x/pdf)PMCID: PMC3429648. 

The full documentation of the collection and laboratory measurement are also placed as documents online:

- Protocols used to collect and process blood samples are available [here](https://www.cpc.unc.edu/projects/china/data/datasets/Blood Collection Protocol_English.pdf).
- A list of biomarkers and methods used to measure them is available [here](https://www.cpc.unc.edu/projects/china/data/datasets/Biomarker_Methods.pdf).
- Codebook of the biomarker dataset is available [here](https://www.cpc.unc.edu/projects/china/data/datasets/C10BIOMARKER.pdf).

## Economic related data

Master_Asset_201804: mainly record what they have in home

Master_Agriculture_201804: Agriculture income, work hours, and cost

Master_Business_201804:  Business Income & work hours

Master_Income_Categories_201804: record different categories of income

Master_Constructed_Income_201804: summary of different kind of income 

## Appendix: some variable frequency statistics

### Province

| ID   | Province                 | Frequency | Percent |
| ---- | ------------------------ | --------- | ------- |
| 11   | Beijing, Added 2011      | 2607      | 1.82    |
| 21   | Liaoning, Missed 1997    | 12327     | 8.59    |
| 23   | Heilongjiang, Added 1997 | 9012      | 6.28    |
| 31   | Shanghai, Added 2011     | 2860      | 1.99    |
| 32   | Jiangsu                  | 14823     | 10.33   |
| 37   | Shandong                 | 14474     | 10.08   |
| 41   | Henan                    | 16982     | 11.83   |
| 42   | Hubei                    | 15906     | 11.08   |
| 43   | Hunan                    | 15449     | 10.76   |
| 45   | Guangxi                  | 19030     | 13.26   |
| 52   | Guizhou                  | 17311     | 12.06   |
| 55   | Chongqing, Added 2011    | 2783      | 1.94    |

### NATIONALITY

| ID   | NATIONALITY | Frequency | Percent |
| ---- | ----------- | --------- | ------- |
| -9   | Unknown     | 7         | 0.02    |
| .    | Missing     | 1853      | 4.17    |
| 1    | Han         | 37853     | 85.15   |
| 2    | Mongolian   | 36        | 0.08    |
| 3    | Hui         | 99        | 0.22    |
| 4    | Tibetian    | 2         | 0       |
| 5    | Vaguer      | 3         | 0.01    |
| 6    | Miao        | 1116      | 2.51    |
| 7    | Yi          | 3         | 0.01    |
| 8    | Zhuang      | 310       | 0.7     |
| 9    | Buyi        | 854       | 1.92    |
| 10   | Korean      | 44        | 0.1     |
| 11   | Man         | 890       | 2       |
| 12   | Dong        | 14        | 0.03    |

### Education

| ID   | Education                      | Frequency | Percent |
| ---- | ------------------------------ | --------- | ------- |
| .    | Missing                        | 6185      | 4.61    |
| 0    | None                           | 33411     | 24.89   |
| 1    | Grad from primary              | 28137     | 20.96   |
| 2    | Lower middle school degree     | 38815     | 28.91   |
| 3    | Upper middle school degree     | 14935     | 11.12   |
| 4    | Technical or vocational degree | 6234      | 4.64    |
| 5    | University or college degree   | 6195      | 4.61    |
| 6    | Master's degree or higher      | 192       | 0.14    |
| 9    | Unknown                        | 152       | 0.11    |

### MARITAL STATUS

| ID        | MARITAL STATUS              | Frequency | Percent |
| --------- | --------------------------- | --------- | ------- |
| .         | Missing                     | 49183     | 27.24   |
| **OTHER** | Unknown or Invalid Response | 275       | 0.15    |
| 1         | Never married               | 34895     | 19.32   |
| 2         | Married                     | 87597     | 48.51   |
| 3         | Divorced                    | 1015      | 0.56    |
| 4         | Widowed                     | 7269      | 4.03    |
| 5         | Separated                   | 348       | 0.19    |

### DOCTOR'S DIAGNOSIS OF ILLENESS/INJURY

| ID   | Disease                           | Frequency | Percent |
| ---- | --------------------------------- | --------- | ------- |
| -9   | Unknown                           | 596       | 0.47    |
| -32  | 23                                | 464       | 0.36    |
| .    | Missing                           | 115370    | 90.3    |
| 0    | No diagnosis                      | 913       | 0.71    |
| 1    | Infectious/parasitic disease      | 162       | 0.13    |
| 2    | Heart disease                     | 678       | 0.53    |
| 3    | Tumor                             | 95        | 0.07    |
| 4    | Respiratory disease               | 3555      | 2.78    |
| 5    | Injury                            | 257       | 0.2     |
| 6    | Alcohol poisoning                 | 10        | 0.01    |
| 7    | Endocrine disorder                | 213       | 0.17    |
| 8    | Hematological disease             | 152       | 0.12    |
| 9    | Mental/psychiatric disorder       | 95        | 0.07    |
| 10   | Mental retardation                | 9         | 0.01    |
| 11   | Neurological disorder             | 255       | 0.2     |
| 12   | Eye/ear/nose/throat/teeth disease | 360       | 0.28    |
| 13   | Digestive disease                 | 1199      | 0.94    |
| 14   | Urinary disease                   | 222       | 0.17    |
| 15   | Sexual dysfunction                | 3         | 0       |
| 16   | Obstetrical/gynecological disease | 133       | 0.1     |
| 17   | Neonatal disease                  | 44        | 0.03    |
| 18   | Dermatological disease            | 246       | 0.19    |
| 19   | Muscular/rheumatological disease  | 489       | 0.38    |
| 20   | Genetic disease                   | 65        | 0.05    |
| 21   | Old age/mid-life syndrome         | 361       | 0.28    |
| 22   | Other                             | 1815      | 1.42    |

### Disease

| ID   | Disease                           |
| ---- | --------------------------------- |
| -9   | Unknown                           |
| -32  | 23                                |
| .    | Missing                           |
| 0    | No diagnosis                      |
| 1    | Infectious/parasitic disease      |
| 2    | Heart disease                     |
| 3    | Tumor                             |
| 4    | Respiratory disease               |
| 5    | Injury                            |
| 6    | Alcohol poisoning                 |
| 7    | Endocrine disorder                |
| 8    | Hematological disease             |
| 9    | Mental/psychiatric disorder       |
| 10   | Mental retardation                |
| 11   | Neurological disorder             |
| 12   | Eye/ear/nose/throat/teeth disease |
| 13   | Digestive disease                 |
| 14   | Urinary disease                   |
| 15   | Sexual dysfunction                |
| 16   | Obstetrical/gynecological disease |
| 17   | Neonatal disease                  |
| 18   | Dermatological disease            |
| 19   | Muscular/rheumatological disease  |
| 20   | Genetic disease                   |
| 21   | Old age/mid-life syndrome         |
| 22   | Other                             |

### CURRENT HEALTH STATUS (SELF-REPORT)

| ID   | Type      | Frequency | Percent |
| ---- | --------- | --------- | ------- |
| .    | Missing   | 52644     | 45.7    |
| 1    | Excellent | 8815      | 7.65    |
| 2    | Good      | 30217     | 26.23   |
| 3    | Fair      | 19463     | 16.89   |
| 4    | Poor      | 3604      | 3.13    |
| 5    | Very Poor | 157       | 0.14    |
| 9    | Unknown   | 301       | 0.26    |