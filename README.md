# BBC-Extractive-Text-Summarization
This project is about building the Automatic Extractive Text Summarization System. The dataset for this purpose has been taken from https://www.kaggle.com/pariza/bbc-news-summary

This dataset for extractive text summarization has four hundred and seventeen political news articles of BBC from 2004 to 2005 in the News Articles folder.
The dataset consists of 5 categories of news articles namely Business, Entertainment, Politics, Sports, Tech. We will build and test our model on Business news articles.

##Preprocessing the Data

After importing all the articles from the text files under Business folder, we preprocess the data by doing the following:

   1. Removing Extra New Lines

   2. Removing punctuations and Numbers and special characters.

   3. Removing the Stopwords.

##Exploring the Data

After Preprocessing, we'll do data exploration.

We will have a look at distribution of Article lengths.

![Link Text](https://github.com/SamSKore/BBC-Extractive-Text-Summarization/blob/master/Vizualizations/article_len_dist.PNG)

We see that major number of articles are of the length between 200-300 words.

##Top n-grams

We will further observe the words appearing in the articles by visualizing the Top Unigrams, Bigrams and Trigrams distributions.

![Link Text](https://github.com/SamSKore/BBC-Extractive-Text-Summarization/blob/master/Vizualizations/Top_Unigrams.PNG)

![Link Text](https://github.com/SamSKore/BBC-Extractive-Text-Summarization/blob/master/Vizualizations/Top_Bigrams.PNG)

![Link Text](https://github.com/SamSKore/BBC-Extractive-Text-Summarization/blob/master/Vizualizations/Top_Trigrams.PNG)

Upon observing the top ngrams present across the articles, it is clear that most of those are Business related articles, as it is obvious that we've selected the business articles folder.

We can also observe the Word CLoud and see the words appearing the most.

![Link Text](https://github.com/SamSKore/BBC-Extractive-Text-Summarization/blob/master/Vizualizations/Word_Cloud.PNG)

##Visualizing the GPEs

we will visualize the Geopolitical Entities present across the articles. Like top 10 GPEs mentioned across all the articles.

![Link Text](https://github.com/SamSKore/BBC-Extractive-Text-Summarization/blob/master/Vizualizations/Top_GPEs.PNG)

It is observed that the business news articles contain US the most. Apart from US, others such as UK, Chine, India, Japan are mentioned more frequently.

Most of the business news are related to these countires, while other african and american countries are covered less.

##And now the Summary Part

For summary, we calculate the word frequencies from the article and then calculate the sentence score by summing the frequencies of words present in it. If the length of a sentence is more than 30 words, we won't consider it to be in the summary.

At last we take the 7 highest scored sentences out of all to make the summary.


'''python
system_summary = generate_summary(df_articles['cleaned_up_text'][100], df_articles['stops_removed'][100])
'''

