---
title: "Project Archive"
permalink: /projects/
header:
  image: "/images/tim2.jpg"
---

I have had the good fortune of working on a wide variety of machine learning projects, both personally and over the course of my graduate program at Northwestern. This page contains project overviews by subject, with links to code and analyses.

My complete portfolio can be found on [GitHub](https://github.com/clboetticher/). 

### Data Cleaning

### Exploratory Data Analysis and Storytelling
**Wine review analysis**<br>
Exploratory analysis of the [Kaggle wine review data set](https://www.kaggle.com/zynicide/wine-reviews) (130,000 wine reviews scraped from Wine Enthusiast magazine during the week of November 22, 2017)<br>
* [Project code](https://github.com/clboetticher/ExploratoryML/blob/master/MSDS430_Final_Wine%20Reviews.ipynb) and [report](https://github.com/clboetticher/ExploratoryML/blob/master/pdfs/Winerevs_finalpaper.pdf)

### Regression

### Classification

### Unsupervised Learning/PCA

### Natural Language Processing
**Neural language modeling for text generation**<br>
The ability to generate text that resembles the quality of human language has numerous applications, from machine translation to spelling correction, from text summarization to image captioning. This study includes experiments in examining how deep neural language models work, how various design and pre-processing decisions impact performance and utility, and also how to tweak network architectures and hyper parameter settings for alternate outcomes.
* [Detailed post](https://clboetticher.github.io/nlm/)

### Computer Vision

### What's next
I have two remaining courses in my program - Natural Language Processing (a deep dive into theory) and Modeling for Supervised Learning (looking forward to reconnecting with R).

This summer, I will be working with a good friend and journalism professor from the University of Houston on Black Lives Matter protest coverage in social media and am also finishing up a long-running Outkast lyric analysis project. More on those soon...



### Text

Here's some basic text.

And here's some *italics*

Here's some **bold** text.

What about a [link](https://github.com/dataoptimal)?

Here's a bulleted list:
* First item
+ Second item
- Third item

Here's a numbered list:
1. First
2. Second
3. Third

Python code block:
```python
    import numpy as np

    def test_function(x, y):
      z = np.sum(x,y)
      return z
```

R code block:
```r
library(tidyverse)
df <- read_csv("some_file.csv")
head(df)
```

Here's some inline code `x+y`.

Here's an image:
<img src="{{ site.url }}{{ site.baseurl }}/images/perceptron/linsep.jpg" alt="linearly separable data">

Here's another image using Kramdown:
![alt]({{ site.url }}{{ site.baseurl }}/images/perceptron/linsep.jpg)

Here's some math:

$$z=x+y$$

You can also put it inline $$z=x+y$$
