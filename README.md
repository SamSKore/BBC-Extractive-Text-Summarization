# BBC-Extractive-Text-Summarization
This project is about building the Automatic Extractive Text Summarization System. The dataset for this purpose has been taken from https://www.kaggle.com/pariza/bbc-news-summary

This dataset for extractive text summarization has four hundred and seventeen political news articles of BBC from 2004 to 2005 in the News Articles folder.
The dataset consists of 5 categories of news articles namely Business, Entertainment, Politics, Sports, Tech. We will build and test our model on Business news articles.


After importing all the articles from the text files under Business folder, we preprocess the data by doing the following:

   1. Removing Extra New Lines

   2. Removing punctuations and Numbers and special characters.

   3. Removing the Stopwords.

After Preprocessing, we'll do data exploration.

We will have a look at distribution of Article lengths.



![Link Text](https://github.com/SamSKore/BBC-Extractive-Text-Summarization/blob/master/Vizualizations/article_len_dist.PNG)

We see that major number of articles are of the length between 200-300 words.

