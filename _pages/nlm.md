---
title: "Text generation with neural language models"
permalink: /nlm/
---

* [Link to code for Alice's Adventures in Wonderland](https://github.com/clboetticher/DeepLearning/blob/master/MSDS458_A4_Neural%20Language%20Modeling%20for%20Text%20Generation_Alice%20in%20Wonderland.ipynb)
* [Link to code for The Metamorphosis](https://github.com/clboetticher/DeepLearning/blob/master/MSDS458_A4_Neural%20Language%20Modeling%20for%20Text%20Generation_Metamorphosis.ipynb)
* [Project report](https://github.com/clboetticher/DeepLearning/blob/master/pdfs/Boetticher_A4_NLM%20for%20text%20generation.pdf)

**Objective and approach**<br>
I selected text generation with neural language models for my final assignment for MSDS 458 Artificial Intelligence and Deep Learning - a brand new area for me though I was aware of how critical a foundation language models are to various NLP tasks. The ability to generate text that resembles the quality of human language has numerous applications, from machine translation to spelling correction, from text summarization to image captioning. This study seemed like a reasonable, feasible experiment in examining how neural language models work, how various design and pre-processing decisions impact performance and utility (I’ll get to that later - a very hairy subject!), and also how to tweak network architectures and hyper parameter settings for alternate outcomes.

**Data**<br>
I downloaded two texts from [Project Gutenberg](https://gutenberg.org) - a pretty amazing repository of over 60,000 publicly-available books, with focus on older works for which U.S. copyright has expired. Beyond a source of great literature free and open to everyone, the text versions of these works offer countless opportunities for experimentation with machine learning techniques using unstructured text. Because I knew I would be getting deep in the weeds with this data, I selected Lewis Carroll’s *Alice’s Adventures in Wonderland* (1865) and Franz Kafka’s *The Metamorphosis* (1915) – both of which I have read, enjoyed, and contain interesting and varied language. Where it made sense, I made some loose comparisons in terms of the language and styles that could come into play for the experiments in the study. I can’t say my selection process was incredibly scientific, but these two novels ended up being very entertaining as inputs; I enjoyed the exploratory analysis almost as much as the modeling itself.<br>

**Pre-processing and model design**<br>
To prepare data for training, I split tokens into sequences with length 50 + 1 (50 input words and 1 output word). These sequences serve as inputs/training patterns to the neural language models in the study, with each word’s probability predicted based on the given input sequence of text. Sequence length is a key design decision: they must be long enough to properly allow models to learn the context and make reasonable predictions. The sequence length also defines the seed text length used to generate text sequences for model evaluation. I chose 50 because it seemed reasonable but I think you could go down a serious rabbit hole (lame joke) experimenting with other lengths.<br>

For the majority of my experiments, I used varying flavors of LSTM RNNs, all with an embedding layer to learn the representations of the words and account for similarity/synonyms. Experiments contained either one or two hidden layers. a fully connected Dense layer, and an output layer using softmax for multi-class classification. In the last experiment of six, I used a bidirectional LSTM RNN, which takes as input not only the words preceding the input sequence but also the words following. The output, in theory, incorporates greater context for a given sequence’s meaning (from both directions). The same six experiments were run with both texts.<br>

**Results and conclusions**<br>
From each experiment I captured loss (most important, as a quantitative measure of performance) and accuracy (less important since 100 percent accuracy would simply mean rote memorization of the text - not generalizable at all). I also generated text from random seed text, sequences of 50 words, to see if the generated text followed the seed text logically. Finally I compared the generated text to the actual 50 words following the seed text. Sound subjective and loose? Now you see how I have spent my week. Despite that challenge, though, this was the only way I could even remotely gauge what was happening in the models and what kinds of features were being generalized. I went through a lot of examples, but here is one for reference/amusement:<br>

**Seed and generated text:**<br>
Seed text 2: begin again it was very provoking to find that the hedgehog had unrolled itself and was in the act of crawling away besides all this there was generally a ridge or a furrow in the way wherever she wanted to send the hedgehog to and as the doubledup soldiers were always<br>

Generated text 2: getting up and walking away without speaking but it was the jurors were writing on his cup of the ground as she added it isnt a little door and she did her to begin with it were beautifully else to make off the time my dear paws oh my fur<br>

**Actual text following seed:**<br>
getting up and walking off to other parts of the ground, Alice soon came
to the conclusion that it was a very difficult game indeed. The players all played at once without waiting for turns, quarrelling all the while, and fighting for the hedgehogs; and in a very short time<br>

And another:<br>

**Seed and generated text:**<br>
Seed text 2: she had to run back into the wood for fear of their hearing her and when she next peeped out the fishfootman was gone and the other was sitting on the ground near the door staring stupidly up into the sky alice went timidly up to the door and knocked theres<br>

Generated text 2: no use in knocking the queen was on for the executioner drink out of the distance and the next sidenote the royal soo oop of the evening beautiful soup of the e evening beautiful soup who chapter oop of the e e evening beautiful beautiful soup chapter soup of the<br>

**Actual text following seed:**<br>
no use in knocking," said the Footman, "and that for two reasons. First, because I'm on the same side of the door as you are; secondly, because they're making such a noise inside, no one could possibly hear you." And certainly there was a most extraordinary noise going on within<br>

That is some seriously beautiful soup.<br>

The generalizability of these particular models was tricky to evaluate and this study revealed to me that it may be impossible to remove subjectivity and individual judgment altogether from the effort. This is not to say the outputs, even in this limited range of experiments, did not hold value: for a language model to take a vocabulary of over 20,000 words (depending on point of training) and, from a sequence of 50 arbitrarily-selected words, generate a subsequent sequence of even remote logic and meaning seems quite astounding on the surface. The evaluation process also revealed some interesting patterns that led me to understand, more closely, what the outputs of neural language models might look like. From there, I could at least speculate on some of the development considerations for larger NLP tasks using those models as a foundation.
