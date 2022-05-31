---
title: "中国健康与营养调查(CHNS)使用笔记"
date: 2021-03-06T19:17:54+08:00
draft: false

upd: "CHNS的数据量非常庞大，并且它将多年的数据合并到一起，因此刚上手的给人感觉非常混乱，本文记录了我的CHNS数据库的处理心得。"

tags: ['学术', '数据库', 'CHNS']
categories: []
---

CHNS的数据按照类别分别存储在不同的压缩包，下载到同一路径之后，首先使用以下Python代码解压所有的压缩包：

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

CHNS提供的数据为SAS格式，由于平时不用SAS，为了方便数据读取与查看，使用Python统一将数据转换为CSV格式并放在同意路径下：

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

处理完成之后的文件目录如下：

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

`Master_ID_201908/surveys_pub_12`存放了最基本的个人数据，我们以此为基本的个体标识来合并不同的数据集。

## [ID 变量](https://www.cpc.unc.edu/projects/china/data/documentation/idvar)

CHNS数据档案中使用了两个ID变量系统：2004年以前调查使用的原始系统，以及此后使用的修订系统。所有旧 ID 已更改为所有文件中的新 ID。

### 家庭身份证（HHID）

HHID 是一个九位数的数字变量，它唯一地识别了旧横截面文件中每个七位数的家庭。T1 到 T5 的变量（记录在调查问卷中）是连在一起形成 HHID 的。每个 HHID 值代表一个家庭。当文件/表的分析单元为家庭时，1 HHID = 1 行 = 1 个家庭 = 1 个观察。这些文件中的观察结果由 HHID 和调查年（波浪）排序。因此，这些文件的关键排序变量是 HHID 和波。

### 个人身份证（Idind）

IDind 是一个十二位数的数字变量，为所有参与者唯一识别。在所有数据集和所有调查年份中，每个参与者都将拥有相同的 ID。唯一 ID 不会随着时间的推移而更改，并且将促进数据集和调查年的数据合并。每个 IDind 值代表一个个体。当文件/表的分析单元是单独的时，1 IDind = 1 行 = 1 个单个 = 1 个观察。这些文件中的观察由 IDind 排序，波（即关键排序变量为 IDind）和 Wave 进行排序。

### 社区 ID （COMMID）

第三个 ID 变量 COMMID 是一个六位数的数字变量，可唯一识别每个社区。T1 到 T4 的变量是连在一起创建 COMMID 的。每个 COMMID 值代表一个社区。当文件分析单元为社区时，1 COMMID = 1 个社区 = 1 个观察。这些文件中的观测结果由COMMID和Wave进行排序，即关键类型的变量是COMMID和波浪。虽然大多数文件合并不需要 COMMID，但此变量已包含在所有数据集中，以方便与社区级文件合并。

当分析单位不是个人、家庭或社区（例如工作、牲畜类型、食品项目、保健设施）之外，文件中包括了确定该单位的变量（例如，JOB、F11、食品代码、第 1 季度）。例如，对于工作是分析单位的文件/表，可变 JOB 的每个值代表一个职业。即1作业=1行=1个职业=1个观察。这些文件中的观察结果由 HHID、LINE 和 JOB 进行排序，即关键类型的变量是 HHID、LINE 和 JOB。

### 调查年（WAVE）

WAVE 是一个四位数的数字变量，确定了调查年份（即 1989 年、1991 年、1993 年、1997 年、2000 年、2004 年、2006 年、2009 年、2011 年、2015 年）。此变量仅用于主纵向文件。

## `biomarker_09`生物标志物数据

2009年在CHNS收集的生物标志物数据涉及对7岁及以上的个人发布26项禁食血液措施。这包括主要的心血管生物标志物（脂质、糖尿病，如HbA1c、葡萄糖、胰岛素、甘油三酯、CRP）和重要的营养生物标志物（转移素、血红蛋白和铁蛋白）。部分主要研究结果概述发表在：严、盛凯、李杰、李丽、张B、S.杜、P.戈登-拉森、L.Adair、B.M.波普金（2012）中国心脏代谢风险负担的扩大：中国健康与营养调查。[肥胖评论 13 （9）： 810-21.](http://onlinelibrary.wiley.com/doi/10.1111/j.1467-789X.2012.01016.x/pdf)PMCID：PMC3429648。

收集和实验室测量的完整文档也作为文档在线放置：

- 收集和处理血液样本的协议[可在此处](https://www.cpc.unc.edu/projects/china/data/datasets/Blood Collection Protocol_English.pdf)获得。
- [这里](https://www.cpc.unc.edu/projects/china/data/datasets/Biomarker_Methods.pdf)提供了用于测量生物标志物和方法的列表。
- 生物标志物数据集的编解码本[可在此处](https://www.cpc.unc.edu/projects/china/data/datasets/C10BIOMARKER.pdf)找到。

## 经济相关数据

Master_Asset_201804：记录家庭资产

Master_Agriculture_201804：农业收入，工作时间和成本 

Master_Business_201804：营业收入和工作时间 

Master_Income_Categories_201804：记录不同类别的收入 

Master_Constructed_Income_201804：各种收入汇总 