---
title: Arvids analysisplan
author: Arvid
date: '2020-06-30'
slug: arvids-analysis
categories: []
tags: []
subtitle: ''
summary: ''
authors: []
lastmod: '2020-06-30T16:16:32+02:00'
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
projects: []
---
# Research plan for the Summer.
Lu Yi proposed three projects to work on, and i like the framing of that. I have based the structure of this plan from the [notes](https://www.evernote.com/shard/s219/client/snv?noteGuid=2f09e186-bcbe-42c9-a88f-23584ebfd119&noteKey=fdb8f26e89495bee&sn=https%3A%2F%2Fwww.evernote.com%2Fshard%2Fs219%2Fsh%2F2f09e186-bcbe-42c9-a88f-23584ebfd119%2Ffdb8f26e89495bee&title=Meet%2Bw%2BArvid%2Babout%2Bsummer%2Bprojects) 
on our meeting you sent me.

Some general ideas from Arvid:
I would like to apply a "multiverse" approach as discussed in [this article](http://www.stat.columbia.edu/~gelman/research/published/multiverse_published.pdf).
This approach has been used in other contemporary genetic research, such as in [Border et al](https://ajp.psychiatryonline.org/doi/full/10.1176/appi.ajp.2018.18070881). 

This is not very different from sensitivity analyses. This is how i summarized it to myself:

"At several stages in data-anaylsis in a paper there are often several arbitrary choices to make about data-processing and choices for statistical analysis. For each paper, therefore, a host of possible datasets exists, a multiverse of datasets, and a multiverse of ways of analyzing the datasets. The solution to this is to leverage the scalability of modern programming tools, and to do ALL THE ANALYSIS, on ALL OF THE DATASETS."

## What would this entail for this project?

1) There are multiple ways of computing the PRS. In the KI summer school, we computed several PRS by different p-val thresholds. I suggest we do the same thing again, but also use methods such as LASSO shrinkage. I'm using [this](https://www.biorxiv.org/content/10.1101/416545v1) paper as a guideline for the different methods of computing PRS, and we can compare which PRS has the best results.
2) The way we defined trauma in the linear interaction model in my thesis was kind of arbitrary. We used a 0-4 scale on each specific trauma measure. I suggest we run the same model but with all reasonble ways of defining trauma, such as a binary variable that is 1 if a subject has had severe trauma on any of the four measures, and a 0-16 scale which just sums up the score on each of the four trauma measures, which are reasonable ways to construct the variable from the top of my head.

3) if possible, and if computing power is not to expensive, we could run the vQTL with the three other ways of testing for equality of variance.

4) discuss the results from my thesis. 


## Project 1 - Dissecting the age of onset trait in the UKBB

### Step 1)  what are the genetic components influencing MDD age-of-onset?
Pretty straightforward. Find genetic variants related to age of onset, with the FastGWA?

Statistical analysis:
1) Conduct a GWAS on the age of onset trait in UKBB (Done by Lu Yi), using FastGWA, which
retains all individuals, even those who are related?
2) LD prune and check if these are close to protein coding genes?

3) And report the genetic correlations between other psychiatric traits?

### Step 2) To what extent does this AAO phenotype overlap w disease risks
If i understand this correctly, this question is about the relationship between age of onset and other diseases?
And statistical analysis on this question would be epidemiological models?

Statistical analysis:

1) Does age of onset predict other diseases?

2) Is age of onset predicted by other things, such as BMI, SES, etc?

### Step 3)
In this step we generate a PRS from the FASTGWA on age of onset, and see if it predicts disease severity in MDD, and 
it's relationship to other psychiatric illnesses.

Suggestion by Arvid: If possible, we could either 1) exclude all siblings in UKBB as done in this [preprint](https://www.biorxiv.org/content/10.1101/2020.03.04.976654v1) and then use siblings as out-of-sample test data
of PRS. Or even better, see if PRS predicts differences between DZ twins in STR. If the association is much weaker between sibling pairs this would indicate that
the PRS does not capture causal genetic variants. 

## Project 2 - vQTL on MDD severity, and maybe on neuroticism?

If i understood you correctly, we would run a vQTL, but use a MDD severity score as outcome variable instead. And use the same pipeline as for age of onset of depression.



## Project3 - MR of choice

As we discussed over lunch, i'm not convinced that a MR on sedentary behaviour will add much to the litterature, and i think there are several measurement and methodological problems.

One seed of an idea for a MR study is on iron load in the striatum, as my previous boss [Gregoria](https://ki-su-arc.se/about-us/faculty-and-staff/gregoria-kalpouzos/)is studying this. It might be an oppertunity to fill a gap in the litterature. 
I will continue exploring possibilties in this direction.


# Conclusion

I feel the most traction right now on project 1, which is the one im working the most on right now.
My plan for the coming week would ge to get access to the FastGWA results and use those to start generating PRS.



