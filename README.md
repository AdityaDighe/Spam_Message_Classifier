# Overview
This project involves a message spam detection model developed with the concepts of natural language processing, ensemble learning techniques like stacking and voting classifiers, vectorization and other machine learning concepts. This is represented or is tested by creating a pickle based file containing the vectorized (term-frequency inverse-document-frequency) output based on the tokens created while training the ML model in a StreamLit user interface.

# Data Visualization 
The dataset used in this project is UCI-ML Dataset repository, which is popular research university repository made publicly available for machine learning community. Its consists of approximately 50,000 lines of labelled data, consisting of message and its identification of wether spam or ham(not spam). 

The below image shows the data imbalance among spam and ham messages.
![image](https://github.com/AdityaDighe/Spam_Message_Classifier/assets/98305705/179b7c34-c0cf-4f0a-9322-cf3fbcf475b3)

Thus to represent which all neccessary features are present in the dataset or to extract some hidden features data preprocessing is neeeded.
NLTK library was used and tokens are created in the form of alphabets, words and sentences. Stop words and punctuations are removed, are stemming is done by porter stemmer (i.e. making words like running to run etc.). 

The below image shows the correlation between different sets of token
![image](https://github.com/AdityaDighe/Spam_Message_Classifier/assets/98305705/a8446199-f8f3-4932-a0d0-9ef10c8e8330)
It can be observed that the num_word shows most correlation between all, and hence we choose to go ahead with it.

This is the heat map between them
![image](https://github.com/AdityaDighe/Spam_Message_Classifier/assets/98305705/e8d8bd68-719c-4f61-8659-09e583f67708)

In the below images we can see the WordClould for both spam and ham messages

Word Cloud for spam messages is as follows:
![image](https://github.com/AdityaDighe/Spam_Message_Classifier/assets/98305705/58372825-0b5f-4126-9a2c-ddbea59ffdf7)
