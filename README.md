# Analyzing-the-Hottest-Topics-in-ML
[Neural Information Processing Systems](https://neurips.cc/About) (NIPS) is one of the top machine learning conferences in the world where groundbreaking work is published. In this Project, we will analyze a large collection of NIPS research papers from the past decade to discover the latest trends in machine learning. The techniques used here to handle large amounts of data can be applied to other text datasets as well.

![1200px-Logo_for_Conference_on_Neural_Information_Processing_Systems svg (4)](https://user-images.githubusercontent.com/65482013/83345754-4fc29300-a334-11ea-9c4a-b1bceb93413d.jpg)

## The Data

At each NIPS conference, a large number of research papers are published. Over 50,000 PDF files were automatically downloaded and processed to obtain a dataset on various machine learning techniques. These NIPS papers are stored in <code>datasets/papers.csv</code>. This CSV file contains information on the different NIPS papers that were published from 1987 until 2017 (30 years!). These papers discuss a wide variety of topics in machine learning, from neural networks to optimization methods and many more.

## Preparing the data for analysis

For the analysis of the papers, we are only interested in the text data associated with the paper as well as the year the paper was published in. We will analyze this text data using natural language processing. Since the file contains some metadata such as id's and filenames, it is necessary to remove all the columns that do not contain useful text information.

## Preprocessing the Data

In order to understand how the machine learning field has recently exploded in popularity, we will begin by visualizing the number of publications per year. We analyze the titles of the different papers to identify machine learning trends. First, we will perform some simple preprocessing on the titles in order to make them more amenable for analysis. We will use a regular expression to remove any punctuation in the title. We'll then print a word cloud to visualize the preprocessed text data.

## Prepare the text for LDA (Latent Dirichlet allocation) analysis

A 'topic' is a collection of words that tend to co-occur often. The hypothesis is that LDA might be able to clarify what the different topics in the research titles are, whcih can then be used as a starting point for further analysis.
LDA does not work directly on text data. First, it is necessary to convert the documents into a simple vector representation. This representation will then be used by LDA to determine the topics. Each entry of a 'document vector' will correspond with the number of times a word occurred in the document. In conclusion, we will convert a list of titles into a list of vectors, all with length equal to the vocabulary. We'll then plot the 10 most common words based on the outcome of this operation (the list of document vectors). As a check, these words should also occur in the word cloud.

## Analysing trends with LDA

**Finally, the research titles will be analyzed using LDA**. The only parameter we will tweak is the number of topics in the LDA algorithm. We play around with a different number of topics and the number of words. From there, we can distinguish what each topic is about ('neural networks', 'reinforcement learning', 'kernel methods', 'gaussian processes', etc.)

## Conclusion

Machine learning has become increasingly popular over the past years. The number of NIPS conference papers has risen exponentially, and people are continuously looking for ways on how they can incorporate machine learning into their products and services.

#### The most common topics in the 2018 NIPS conference were
1. Bayesian classification
2. Multi bandit theory
3. Neural Networks
4. Gaussian estimation
5. Stochastic/Multi-Sparse Learning
