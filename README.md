# Overview
This project involves a message spam detection model developed with the concepts of natural language processing, ensemble learning techniques like stacking and voting classifiers, vectorization and other machine learning concepts. This is represented or is tested by creating a pickle based file containing the vectorized (term-frequency inverse-document-frequency) output based on the tokens created while training the ML model in a StreamLit user interface.

# Data Visualization, Preprocessing and Explanation
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

Word Cloud for ham messages is as follows:
![image](https://github.com/AdityaDighe/Spam_Message_Classifier/assets/98305705/ff92a8b7-b08e-49f2-a49e-efa19ee7bcb5)

The bigger the representaion over wordcloud the more its occurance shall affect the classification.
This distribution shows the words that if included into a sentence based on the dataset which are ml model will be trained will show bias by flaging it as spam or ham messages.

Now to show that the training and testing accuracy of the conventional machine learning algorithms, it is represented in the table below
![image](https://github.com/AdityaDighe/Spam_Message_Classifier/assets/98305705/8d58f330-4c16-4808-8aee-42edef51ffd4)

As you can see some of the training algorithms show much better accuracy and precision results as compared to others. But if change the dataset or the above dataset is flooded with another 50,000 lines of data, are we gonna be sure that the one algorithm we picked is going to perform the best among the all. Not quite so.
So to overcome this ensemble learning techniques like voting classifiers and stacking are used.

Voting classifiers - The selected sub-classifiers will have equal share of vote to flag a text as spam or ham.
Stacking classifiers - The selected sub-classifiers will have share of vote to flag a text as spam or ham based on their accuracy and precision.

Precision and accuracy for voting classifiers - 
![image](https://github.com/AdityaDighe/Spam_Message_Classifier/assets/98305705/d845f72e-f965-4b9e-b8ce-d722bb09b1c3)

Precision and accuracy for stacking classifiers - 
![image](https://github.com/AdityaDighe/Spam_Message_Classifier/assets/98305705/26611752-c0e7-49c5-a76c-8be85e38ea11)

# User Interface
A simple user interface is developed to test the model we have build using StreamLit. The training algorithm which is a mixture of ensemble and conventional learning techniques its output is converted into a single output vector using vectorization particularly tfidf. Later this pickled in a pickle file to use it at testing at frontend.

On the frontend interface simple text transformation is done and the result is displayed at the bottom after processing the text box.

![image](https://github.com/AdityaDighe/Spam_Message_Classifier/assets/98305705/42b7d83a-ce5b-4151-8255-48113c5cecaa)

![image](https://github.com/AdityaDighe/Spam_Message_Classifier/assets/98305705/bebabe86-4f6b-41fc-9344-3be061f512ea)


