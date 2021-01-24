---
permalink: /
title: "Topic-based sentiment analysis of Amazon reviews (NLP course, Polytechnic university of Tehran)"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
Introduction
======

As it’s conspicuous from the title of the project we have 2 main phases. At first, we find sentiment of reviews and then we extract topics. A long the way we graph topic-based sentiment analysis of reviews and evaluate both main phases.
We will use Textblob library and Deep learning approach for finding sentiment and we will get 80% accuracy for textblob and 50% accuracy for deep learning approach .

There is no need to mention countless use cases of sentiment analysis, since we can use it for any work for finding more insightful details. 
and for Topic extraction, we can think of it as a space-reduction function that maps document whit many words to just a few number of topics. 
. You can download [the Jupyter notebook file with this link](https://colab.research.google.com/drive/1UBXn_B3cGYniRxN4B-GfAp3r_BQ9Z1kg#scrollTo=JVgHEc-PHPP5) and fill free to contact us for more detail: [Matthew anderson](ardestani.zm@gmail.com), [Roozbehbazargani](roozbehbazargani@gmail.com).

How to setup 
------
0.1) Setups and input, output format and data frame clarification

How to run:
I.	At first you should have been installed all required libraries and Jupyter notebook.
II.	Create a folder & paste Ass2_spamDetectionInPersainLang.ipynb' and ' stopwords.txt ' and  'emails.folder' .
III.	At the address bar write “cmd” then click “Enter”.
IV.	At the Cmd console type “jupyter notebook” and then “Enter”.
V.	Open Jupyter sourceCode and run each cell in order
VI.	Notice some cells take a few second to run completely 


Preprocessing data 
------
1.1) cleaning data: 
We go through following steps:
1.	removing user names
2.	removing numbers
3.	removing URLs
4.	removing punctuations
5.	removing stopwords
6.	removing words with length less than 3
7.	transform to the lower case
8.	stemming


Phase One (Finding Sentiments with textblob library and deep learning methods)  
------
![textblob](https://miro.medium.com/max/2334/1*roddopPJFRjl6t1MyEzB_Q.png)
In a nut shell, TextBlob library has unsupervised methods for finding polarity and subjectivity (and etc) of a text. A lot of linguists, namely Tom De Smedt, have come together and have figured out all different aspect of words manually. Based on this great job that has done recently, we are able to estimate polarity (means sentiment score that is between -1 and +1) even better than KNN or Bayes which have expensive calculation. In our case, we have reached 0.799 percent accuracy for estimating polarity (sentiment) of reviews. We will explain this in “Evaluation of TextBlob” part.(More info about textblob for interested reader, perhaps you!, : link1 , link2)
2.1.1) Estimating Sentiments

We help of polarity function we can easily find sentiment score and map it to {Pos , Neg , Neu}.
2.1.2) Extrapolating ratings
For finding ratings we need to extrapolate them with respect to current behavior of users. For this purpose, beside defining a linear map from sentiment score to {1,2,3,4,5}, we define a non-linear function that is trained by ratings distribution of the reviews in data set. 


Phase Two (Extracting Topics using LDA method)
------
As an input we receive M document. Then we pass them into the black box that is LDA (hopefully it will not remain black box after this explanations) then we do some works (that will be explained in 3.0). As an output we have 3 things: 
1) soft/fuzzy clustering of words , 
2) words distribution for each Topic ,
3) Topics-distribution for each document



Evaluations and visualizations 
------
**Markdown generator**

add results 

**Markdown generator**

(add results later)
(add results  | figure no1 | LDA result )
![Editing a markdown file for a talk](/images/editing-talk.png)

Aknowledgement
------
I am grateful to all of those with whom I have had the pleasure to work during this and other related projects, especially Dr. Mohammad Akbari (akbari.ma@aut.ac.ir) and Mr. Arman Malekzade(malekzadeh@ieee.org).
