# Emotion and Sentiment Classification of Reddit Posts

For this mini-project, we experimented with different machine learning algorithms for text classification.
We used a modified version of the GoEmotion dataset and experiment with a variety of classifiers and features
to identify both the emotion and the sentiment of Reddit posts.

The focus of this mini-project lies more on the experimentations and analysis than on the implementation. 

## Analysis of the dataset 

As seen in the pie chart for each the emotions and sentiments classification, there is an unequal distribution of the classifications.
In the case of the emotions, roughly one third of the classifications are labeled as “neutral”. As for the rest of the emotions, each label roughly does not surpass 5%.
In the case of the sentiments, there is an improvement in the distribution of the classifications.
For example, “neutral” is 32.2% , “negative” is 22.4%, “ambiguous” 11.4%, and “positive” is 34.4% of the entire dataset.
Imbalanced classifications is a problem for predictive modeling since most of the machine learning algorithms used for classification are designed
around the assumption of an equal number of examples for each class. 

As seen in our dataset, there should be no surprise that the classification algorithms later on will have poor predictive outcomes, especially for the minority classes. 
This is a problem because typically, the minority class should be as important as the dominant class therefore the problem is more sensitive
to classification errors for the minority class than the majority class. 

## Analysis of the results of all the models for both classification tasks

In our case, for the alternate classification task we decided to use tf-idf instead of word frequencies.
By definition, tf-idf weight is composed of two terms: the first computes the normalized Term Frequency (TF),
the number of times a word appears in a document, divided by the total number of words in that document; the second term is the Inverse Document Frequency (IDF),
computed as the logarithm of the number of the documents in the corpus divided by the number of documents where the specific term appears. 

Overall, in most models there is an improvement of the precision, recall and f1 score when using tf-idf over word frequencies, but not my much.
In theory, word frequencies just create a set of vectors containing the count of word occurrences in the reddit posts, while the TF-IDF model contains information
on the more important classes and the less important ones as well. 

For example, in the case of Multinomial Naive Bayes with tf-idf, the precision for each sentiment has improved around 10 points,
whereas the recall score for some sentiments has improved, and worsened. F1 scores also seem to have mixed results. 

### Credits 
- Shawn Gorman 
- Rayan Abou 
- Dr. Leila Kosseim 



