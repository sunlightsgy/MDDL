# MDDL
Dataset for "Depression Detection via Harvesting Social Media: A Multimodal Dictionary Learning Solution" in IJCAI 17.

## Dataset

To make depression detection via social media, we need to get a batch of well-labeled data to train the models. We employed heuristical rule-based methods to construct two benchmark well-labeled depression and non-depression datasets on Twitter, which has mature APIs and is prevalent around the world. We obtain the personal information on social media and a piece of anchor tweet for one user. Besides, as people should be observed for a period of time according to clinical experience, all the other tweets published within one month from the anchor tweet are also obtained.

- Depression Dataset D1. Based on the tweets between 2009 and 2016, we constructed a depression dataset D1, where users were labeled as depressed if their anchor tweets satisfied the strict pattern "(I'm/ I was/ I am/ I've been) diagnosed depression".

- Non-Depression Dataset D2. We constructed a non-depression dataset D2, where users were labeled as non-depressed if they had never posted any tweet containing the character string "depress". We select the tweets on December 2016.

Although D1 and D2 are well-labeled, the depressed users on D1 are too few so we constructed a larger dataset D3 for depression behaviors discovery.

- Depression-candidate Dataset D3. Based on the tweets on December 2016, we constructed a unlabeled depression-candidate dataset D3, where users were obtained if their anchor tweets loosely contained the character string "depress". Although the depression-candidate dataset contained much noise, it contained more depressed users than randomly sampling.

The dataset can be downloaded [HERE](https://mailstsinghuaeducn-my.sharepoint.com/:u:/g/personal/sgy16_mails_tsinghua_edu_cn/EbcI8AuOdCVJp7Itjzx3U_4BkJf1iDJiGykLwkgNHDKHyg?e=lnuY91).

## Features

We intended to detect and analyze depressed users with offline and online behaviors. Regarding offline behaviors, there are clear definitions in depression criteria, which have been widely used in depression diagnosis. On the other hand, we harvested the social media and found some common online behaviors. With references in computer science and psychology, we finally defined and extracted six depression-oriented feature groups to comprehensively describe each user, that is, Social Network Feature, User Profile Feature, Visual Feature, Emotional Feature, Topic-level Feature and Domain-specific Feature.

Our feature table can be seen [HERE](https://www.dropbox.com/s/hernplxxgqrumhu/feature_table.xlsx?dl=0).

## Sentimental Emoji Labrary

Emoji are incompatible with many text processing algorithms. We thus removed the emoji in Tweets' texts with an emoji library collected from Twitter. We invited three annotators to vote for the sentiment of the emoji in our library. Based on the majority voting, we obtained a sentimental emoji library, with which we extracted the sentimental emoji counts.

The sentimental emoji library can be seen [HERE](https://www.dropbox.com/s/d5k4n4g3vj5yjyq/emoticon.xlsx?dl=0).

## Citation

If you use this dataset for your research, please cite our papers.

```
@inproceedings{shen2017depression,
  title={Depression Detection via Harvesting Social Media: A Multimodal Dictionary Learning Solution.},
  author={Shen, Guangyao and Jia, Jia and Nie, Liqiang and Feng, Fuli and Zhang, Cunjun and Hu, Tianrui and Chua, Tat-Seng and Zhu, Wenwu},
  booktitle={IJCAI},
  pages={3838--3844},
  year={2017}
}
```
