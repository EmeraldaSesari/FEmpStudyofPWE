# An Empirical Study on the Fairness of Pre-trained Word Embeddings
From medical diagnostics to loans, software has a significant impact on the decisions that create our society. Unfortunately, there are several examples of unfairness in software. Software fairness is a property that refers to a software ability to operate in a fair and unbiased manner. Furthermore, given that learning biased data might lead to software bias, it is essential to ensure that the learning method itself is fair.
This study attempts to explore the fairness of pre-trained word embedding models using multiple bias metrics. We conduct a com- prehensive literature review by collecting 37 unique publications that focus on quantifying bias on pre-trained word embeddings. Then, we extract the pertinent information such as the most com- monly used pre-trained word embedding models and bias metrics. We then use these outcomes as building blocks for our empirical study to assess the most fair pre-trained word embeddings. We experiment with three of the most frequently used models: GloVe, word2vec, and fastText, along with four of the most widely used bias metrics: WEAT, Sembias, Direct Bias, and ECT. We also examine the relationship between fairness and parameters involved in the training process, such as vector length and subword information. Our experiments indicate that amongst the three pre-trained word embedding models, fastText carries the least bias for three of the four bias metrics we investigated, and, overall, for 8 out of 12 cases. This study also reveals that word embeddings with smaller vector length are more biased than those with bigger vector length.

# Fair Pre-trained Word Embeddings
We can infer from this data that fastText pre- trained word embeddings perform the best with respect to three of the four most used bias metrics. According to SemBias and ECT scores, FastText Common Crawl is the least biased. Using the same corpus but with addition of subword information, the embed- dings has the least biased according to WEAT Test 6. Furthermore, FastText Wiki News is least biased on WEAT Test 5. In addition, the embeddings has the least bias on WEAT Test 3, Test 4, and Test 10 while including subword information.

# The Effect of Parameters on the Fairness
## Vector Length
Most observations from the WEAT, Sembias, Direct Bias, and ECT scores indicate evidence for improved fairness in pre-trained word embeddings when the number of dimensions is increased. This result implies that lower dimensionality word em- beddings are not expressive enough to capture all word associations and analogies, and that when the bias metric is applied to them, they become more biased than embeddings with larger dimensions.
## Subword Informations
Five of the eight observations found that using subword information results in less biased word embeddings, while three of the eight observations found the opposite. The corpus used to produce the word embeddings may have hampered our findings. These results therefore need to be interpreted with caution. It might be related to the main purpose of subword model in fastText developed by [Bojanowski et al. 2017], which is to learn more reliable representation for rare words that does not necessarily correspond to fairer representation. Due to inconsistency of the results, it is unclear whether the usage of subword improves or degrades the fairness of an embedding.
