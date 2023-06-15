---
layout: post
title:  "Hypothesis testing for leakage assessment in side channel analysis"
date:   2023-06-14 11:21:09 +0100
categories: leakage assessment
authored: Ileana Buhan
---

This post has a slightly different format compared to previous posts, as the material was prepared for an three hour in-person tutorial at the amazing [summer school on on real-world crypto and privacy](https://summerschool-croatia.cs.ru.nl/2023/index.html)  in Vodice, Croatia. 

The tutorial aims to give participants a solid technical understanding of the mechanics of hypothesis testing in the context of side-channel analysis. In the first part, we focus on the fundamental concepts of hypothesis testing: we practise choosing the null-hypothesis $H_0$ (1), mention the data collection step (2) and  take a deep dive on testing  which requires building the *null-distribution*  estimating *p-values* (3).

![NHST]({{site.url}}/assets/img//Hypothesis_testing/NHST.png){:class="img-responsive"} 

 To follow along, download [the workbook](Croatia_23/tutorial_workbook.pdf) and  [the slides](Croatia_23/NHST-part1.pdf) and work on the exercises in the suggested order. I use three running examples to illustrate these concepts. The first, [Lake_water.ipynb](https://colab.research.google.com/drive/1geYPLVc9_ywZPMd8PQSd8R6eZ2OWX0gp?hl=en) is a one-sample t-test where we want to estimate the salt concentration in a body of water. The second, [PhD_vs_Faculty.ipynb](https://colab.research.google.com/drive/1r3RiT3YXhv9fg-gx4CJksoEJDVtQBu62?usp=sharing)  is a two-sample t-test where we test if height has an influence on the chances of becoming a faculty member. Finally, the third example [Magic_coins](https://colab.research.google.com/drive/1r3RiT3YXhv9fg-gx4CJksoEJDVtQBu62?usp=sharing) is helful for understanding p-values. 

![files]({{site.url}}/assets/img//Hypothesis_testing/files.png){:class="img-responsive"} 

 In the workbook you will find three exercises, pick and choose the one you find useful: 

- The learning objective of exercise 1 is threefold: (1)  we prove that there is natural variation when estimating a test statistic; (2) we determine the influence of the sample size samples on  test statistic and (3) we demonstrate that the distribution of the mean test statistic is different compared to the distribution of the sample data; 
- The learning objective of exercise 2 is to practice constructing null-distributions. In question 1 we explore what is a t-score and construct the null distribution for a one-sample t-test. In  question 2 we construct a null-distribution for a two-sample t-test and in question 3 we construct a null-distribution for data that follows a binomial distribution. 
- The learning objective of exercise 3 is  to get an intimate understanding of how p-values are computed and what they represent and as a sanity check compare the p-values we estimated with the ones calculated by the python library. 

In Part 2, we apply we apply hypothesis testing, in particular a two-sample t-test on a set of real traces for traces collected for two algorithms. Use the same [workbook](Croatia_23/tutorial_workbook.pdf) and these [slides](Croatia_23/NHST-part2.pdf) for guidance.  

**Further reading**:

- The Reassure project produced a very interesting tutorial on [Understanding Leakage Detection]( *https://reassure.eu/leakage-detection-tutorial/*)  worth checking out.
- Carolyn Whitnall, Elisabeth Oswald: *A Critical Analysis of ISO 17825 ('Testing Methods for the Mitigation of Non-invasive Attack Classes Against Cryptographic Modules').* ASIACRYPT (3) 2019: 256-284;
- François-Xavier Standaert: *How (Not) to Use Welch's T-Test in Side-Channel Security Evaluations.* CARDIS 2018: 65-79
- Tobias Schneider, Amir Moradi: *Leakage Assessment Methodology - A Clear Roadmap for Side-Channel Evaluations.* CHES 2015 495-513;

