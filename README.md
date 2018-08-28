MINING DATA FROM NEWSFEEDS

The objective of my project was to categorize news articles. I downloaded a dataset that had the following fields from kaggle.

My dataset has the following features:

  1.Title: headline
  
  2.Media: Blog/News
  
  3.Content: Article
  
  4.Timestamp: Published date and time
  
  5.Source: source of article

The two main roadblocks I had to doing meaningful topic modeling/clustering were:

The articles were a mixture of news and blogs(opinions)
There was non-uniform representation of articles from the different sources.

For more accuracy, I decided to focus on only news articles of length 100 to 1000 words from 1402 sources.

I tried using custom tokenizer and stemmer functions along with NLTK’s built in tokenizer and stemmer. After that, I used tfidf vectorizing to vectorize the news articles contents.
I used SVD for dimensionality reduction from 2367 features to just 50 features. To cluster the articles, I used the silhouette score to decide on limiting the clustering to 40 clusters and implemented mini-batch KMeans algorithm.
I was able to assess the meaningfulness of the clusters by examining the “hot keywords” (top 10) from the each cluster.

I tried topic modeling with LDA, but it was not as insightful as the clustering output.

The categories, my model was successful in detecting:

Politics/Policy

International

Sports

Finance

