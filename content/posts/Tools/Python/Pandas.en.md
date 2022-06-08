---
title: "Pandas Notes"
date: 2021-02-28T13:00:27+08:00
draft: false

description: "Pandas Notes."
upd: "Pandas Notes."

tags: ['Python', 'Notes']
categories: []
---

<!--more-->

Data Indexing / selection

- [pandas.DataFrame.loc](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.loc.html)

The basics of indexing are as follows:

| Operation                      | Syntax          | Result    |
| :----------------------------- | :-------------- | :-------- |
| Select column                  | `df[col]`       | Series    |
| Select row by label            | `df.loc[label]` | Series    |
| Select row by integer location | `df.iloc[loc]`  | Series    |
| Slice rows                     | `df[5:10]`      | DataFrame |
| Select rows by boolean vector  | `df[bool_vec]`  | DataFrame |

Convert float into integer

- [pandas.to_numeric](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.to_numeric.html)
- [pandas.DataFrame.astype](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.astype.html)
- [pandas.DataFrame.round](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.round.html)

Bug solution:

- [Pandas: ValueError: cannot convert float NaN to integer](https://stackoverflow.com/questions/47333227/pandas-valueerror-cannot-convert-float-nan-to-integer)

Merge data

- [Merge, join, concatenate and compare](https://pandas.pydata.org/pandas-docs/stable/user_guide/merging.html)
- [pandas.DataFrame.merge](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.merge.html)

Duplicated value

- [pandas.DataFrame.duplicated](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.duplicated.html): judge whether duplicated
    - E.g. `data[data.duplicated(subset = ["Id"], keep = False)]`
- [pandas.DataFrame.drop_duplicates](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.drop_duplicates.html?highlight=drop_duplicates)

Missing data

- [pandas.DataFrame.dropna](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.dropna.html?highlight=dropna#pandas.DataFrame.dropna)

Reshape:

- [pandas.pivot](https://pandas.pydata.org/docs/reference/api/pandas.pivot.html)