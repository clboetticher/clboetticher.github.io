---
title: "Portfolio"
permalink: /projects/
---

I have had the good fortune of working on a wide variety of machine learning projects, both personally and over the course of my graduate program at Northwestern. This page contains project overviews by subject, with links to code and analyses of results.

My complete portfolio can be found on [GitHub](https://github.com/clboetticher/). 

## *Data Cleaning*

## *Exploratory Data Analysis*

**Northwestern MS in Data Science student survey analysis**<br>
An annual program survey aims to assess current students’ perception of the field’s needs with respect to programming and software skills; it also provides a snapshot of course completion progress for student respondents and interest in future program offerings. In conjunction with the input of an external advisory board of 30 industry leaders who commented on their data science capability needs in a 2-5 year period, these results form part of the ongoing effort to evaluate how well the program is meeting both student and market demands, training new data scientists sufficiently for the field. This report includes data preparation (including scaling), exploration, and analysis of the survey data, providing a basis for recommendations for future direction for the MSDS program with respect to overall curriculum and related software and systems.
* [Project code](https://github.com/clboetticher/AppliedML/blob/master/MSDS422_A1_Exploring%20and%20Visualizing%20Data.ipynb) and [report](https://github.com/clboetticher/AppliedML/blob/master/pdfs/A1_report.pdf)

**Wine review analysis**<br>
This exploratory analysis of the [Kaggle wine review data set](https://www.kaggle.com/zynicide/wine-reviews) (130,000 wine reviews scraped from Wine Enthusiast magazine in 2017) was an early (in my graduate program) experiment with potentially-interesting correlations across features. Given the unique, highly subject-specific language, sentiment analysis and scores' correlation to price and Wine Enthusiast points assigned also made for an interesting investigation into the specificities of review language and the complexities of the domain's language in reflecting how much any given reviewer enjoyed a wine and perceived its value. I'm hoping to return to this one later to develop text-related predictive models, possibly identifying variety or location based on the description field.<br>
* [Project code](https://github.com/clboetticher/ExploratoryML/blob/master/MSDS430_Final_Wine%20Reviews.ipynb) and [report](https://github.com/clboetticher/ExploratoryML/blob/master/pdfs/Winerevs_finalpaper.pdf)

## *Regression*

**Evaluating regression models with the Boston Housing dataset**<br>
Evaluation of multiple regression models (Linear, Ridge, Lasso, Elastic Net, Random Forest, and Extra Trees) with a cross-validation design, using root mean-squared error (RMSE) as an index of prediction error. The Boston Housing Study, a market response study of 506 census tracts in the Boston metropolitan area. Explanatory variables include per capita crime rate by town annd average number of rooms per dwelling, with the response variable as median price of homes. Data is scaled in multiple ways to examine impact on prediction error.
* [Project code](https://github.com/clboetticher/AppliedML/blob/master/MSDS422_A2_Evaluating%20Regression%20Models.ipynb) and [report](https://github.com/clboetticher/AppliedML/blob/master/pdfs/A2_report.pdf)
* Second project focusing on Random Forest and Gradient Boosting methods in more depth: [project code](https://github.com/clboetticher/AppliedML/blob/master/MSDS422_A4_Random%20Forests%20and%20Gradient%20Boosting.ipynb) and [report](https://github.com/clboetticher/AppliedML/blob/master/pdfs/A4_report.pdf)

## *Classification*

**Logistic regression and naive Bayes classification with Portuguese bank marketing data**<br>
This project employs the [Bank Marketing Dataset](https://archive.ics.uci.edu/ml/datasets/bank+marketing) as a basis for developing and evaluating two classification approaches for predicting the binary response variable of whether a client has subscribed to a term deposit. The area under the receiver operating characteristic (ROC) curve serves as an index of classification performance. The resulting analysis informs recommendations on most effective marketing campaigns for targeting the most promising customers for new term deposit offerings.
  * [Project code](https://github.com/clboetticher/AppliedML/blob/master/MSDS422_A3_Evaluating%20Classification%20Models.ipynb) and [report](https://github.com/clboetticher/AppliedML/blob/master/pdfs/A3_report.pdf)

**Neural network benchmark study on MNIST dataset**<br>
This benchmark study aims to compare and evaluate two neural network types (simple multilayer perceptrons and convolutional neural networks) with various architectures (shallow and deep) and optimizers (SGD and Adam) to determine their potential utility in multi-class classification problems on the MNIST dataset of hand-drawn digits and for future analogous Optical Character Recognition (OCR) efforts.
* [Project code](https://github.com/clboetticher/AppliedML/blob/master/MSDS422_A6_Neural_Networks.ipynb) and [report](https://github.com/clboetticher/AppliedML/blob/master/pdfs/A6_report.pdf)
* An extension of this study examines varying network topologies (in terms of depth and width) in more detail, aiming for digit classification accuracy and an opportunity to gain an in-depth understanding of how the neurons in the simple single-hidden layer network have learned to represent features within the input data. [Project code](https://github.com/clboetticher/DeepLearning/blob/master/MSDS458_A1_Digit%20classification%20with%20simple%20neural%20networks.ipynb) and [report](https://github.com/clboetticher/DeepLearning/blob/master/pdfs/A1_report.pdf)

**Random Forest classifiers with PCA**<br>
Building on the classifiers developed in the first multi-class classification work, PCA is executed to reduce dimensionality and identify principal components representing 95 percent of the variability in the explanatory variables (substantially fewer than the original 784 explanatory variables). These components are used to train another Random Forest classifier for comparison. 
* [Project code](https://github.com/clboetticher/AppliedML/blob/master/MSDS422_A5_Principal%20Components%20Analysis.ipynb) and [report](https://github.com/clboetticher/AppliedML/blob/master/pdfs/A5_report.pdf)

## *Natural Language Processing*

**Neural networks for IMDB movie review classification**<br>
This benchmark study evaluates fully-connected dense neural networks (as a baseline), RNNs (specifically to demonstrate sequence learning’s performance), and one-dimensional convolutional neural networks (CNNs) with the binary classification task of assigning a positive or negative polarity score to IMDB movie reviews using text as features. Varying neural network architectures are explored using either recurrent or convolutional layers, trained with either learned embeddings or pre-trained gloVe embeddings (100-dimensional and 300-dimensional vectors). 
* [Project code](https://github.com/clboetticher/AppliedML/blob/master/MSDS422_A8_Language%20Modeling%20with%20RNNs.ipynb) and [report](https://github.com/clboetticher/AppliedML/blob/master/pdfs/A8_report.pdf)

**Reuters newswire classification with RNNs annd 1-D CNNs**<br>
This study is a comparative exploration of dense, recurrent, and convolutional neural networks for news classification with the Reuters newswire dataset, containing 11,228 newswires from Reuters labeled over 46 topics. This well-known text dataset is useful for experimenting with models to achieve reliable discriminatory power between topics. The study has a two-fold goal: develop a neural network model for highly-accurate and generalizable classification and gain an in- depth understanding of how various factors affect fitting and ultimate test set performance with networks of differing topologies and hyperparameter settings. This will shed light on how hidden nodes learn to extract features from inputs; with additional layers, the objective is to better understand how each successive layer extracts progressively abstract and generalized features. Specifically, the study will accomplish this through exploration of various neural network structures and topologies, including DNNs, RNNs, and one- dimensional CNNs. Overfitting and the challenge of vanishing gradients, in addition to the so-called curse of dimensionality, are a constant presence with training these models and attempting to design for generalizability. Various mitigating steps, for example using LSTM RNNs and regularization techniques, will be evaluated for impact on performance and future utility on unseen data.
* [Project code](https://github.com/clboetticher/DeepLearning/blob/master/MSDS458_A3_Deep%20Neural%20Networks%20for%20NLP.ipynb) and [report](https://github.com/clboetticher/DeepLearning/blob/master/pdfs/A3_report.pdf)

**Neural language modeling for text generation**<br>
The ability to generate text that resembles the quality of human language has numerous applications, from machine translation to spelling correction, from text summarization to image captioning. This study includes experiments in examining how deep neural language models work, how various design and pre-processing decisions impact performance and utility, and also how to tweak network architectures and hyper parameter settings for alternate outcomes.
* [Detailed post](https://clboetticher.github.io/nlm/)

## *Computer Vision*

**Binary image classifiers - cats versus dogs**<br>
This benchmark study examines the performance, processing time, and generalizability of neural network models, specifically CNNs, in binary image classification using the [cats and dogs image dataset](https://www.kaggle.com/c/dogs-vs-cats-redux-kernels-edition/overview) from Kaggle. OpenCV and the Keras Image Data Generator are employed to prepare the image data and attempt a reduction of overfitting.
* [Project code](https://github.com/clboetticher/AppliedML/blob/master/MSDS422_A7_Image%20Processing%20with%20CNNs.ipynb) and [report](https://github.com/clboetticher/AppliedML/blob/master/pdfs/A7_report.pdf)

**Fashion image classification with deep neural networks**<br>
Where simple neural networks have been found to perform relatively well with certain tasks, such as digit classification, images from photos have proven much more challenging given the astounding variety in how objects, even of the same class, can look vastly different depending on size, shape, detail, and positioning (to name only a few). The Fashion MNIST database, with labeled articles of clothing across ten categories, offers a more complex dataset for benchmarking complex dense and convolutional neural networks and how they compare in classification accuracy and process time. This study explores varying architectures with dense and convolutional layers with varying depths and widths with the objective of configuring effective models. Specific hyperparameter settings are adjusted to evaluate potential effects on classification performance and process time as well and dropout regularization is added in some cases to determine potential impact on reducing model complexity and mitigating overfitting. Greater understanding of the intricacies of these architectures and the numerous ways they can be adjusted lead to more performant models more likely to work well in real-life image classification scenarios, with applications in retail and far beyond.
* Project code [with no dropout regularization](https://github.com/clboetticher/DeepLearning/blob/master/MSDS458_A2_CNNs_for_Computer_Vision_no_dropout.ipynb) and [with dropout regularization](https://github.com/clboetticher/DeepLearning/blob/master/MSDS458_A2_CNNs_for_Computer_Vision_dropout_experiments.ipynb)
* [Report](https://github.com/clboetticher/DeepLearning/blob/master/pdfs/A2_report.pdf)

## What's next
I have two remaining courses in my program - Natural Language Processing (a deep dive into theory) and Modeling for Supervised Learning (looking forward to reconnecting with R).

This summer, I will be working with a good friend and journalism professor from the University of Houston on Black Lives Matter protest coverage in social media and am also finishing up a long-running Outkast lyric analysis project. More on those soon...

