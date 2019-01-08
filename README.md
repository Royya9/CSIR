# CSIR
Sample Project for CSIR

This project is done as a prerequisite for CSIR Intern qualification.

This project is mainly divied into two parts:

1. Sentiment Analysis
2. Vectoriztion of words

As required, I have scraped all the HIV related articles from Times of India Website using 'requests' and 'beautiful soup' libraries for content extraction. 

For the first part, as there is no labeled data for training a sentiment analysis model, I have used pre-trained Microsoft Azure's Cognitive Analytics API (free subscription) for rating each article. After obtaining sentiment scores on 0-1 scale for all articles, I've plotted the sentiment values verus number of articles on a density plot. Also analysed the articles with highest and lowest sentiment values.

For the second part, I have used nltk and gensim.word2vec libraries for word tokenizing and vectorization respectively. I have trained a word2vec model with the following params:

number of features = 500
minimum word count = 3
context size = 7
down sampling = 1e-3

I've trained the model for 10 epochs and the trained model vectors were reduced to 2 dimensions using t-Distributed Stochastic Neighbor Embedding (t-SNE).

The resultant 2 dimensional word vectors are plotted and analyzed. Similarities between words, word clusters are observed.
