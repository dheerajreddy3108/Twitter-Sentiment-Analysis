# Twitter-Sentiment-Analysis


## NLP project to find analyze the sentiment of the tweet usng Deep Learning techniques

## Sentiment Analysis 

Sentiment Analysis is defined as a profound text analysis tool that automatically interpert the emotion and classifies the text information provided. It is widely used in Socail Media. Few examples are rating for a new launched product, track how the changes product affects the feel of customer, review of a newly released movie and many more daily use cases to quote. 

## Dependicies 

Followig Libraires are used in the process of Programming Sentiment Analysis


Python
matplotlib
NumPy
NLTK 
TensorFlow
seaborn
gensim
re


## Data 

The dataset is made of 2 files, each for training and testing data. A total of 1,600,000 tweets in training csv file categorized into 2 classes. Positve tweets are labelled as class 4 and negative into class 0. The maximum length of tweet is 57 and tweet length is close to 14. A detialed distrbution image is given below.

![image](https://user-images.githubusercontent.com/55786239/184653596-2b91ae5c-384f-4b1d-bc9c-9e92742b6916.png)


## Data Preperation

Following Data Preprocessing steps are followed to clean the data and remove any artifacts in the data. 

1. Remove Hyperlinks : Most of the hyperlinks carry no information about the emotion in the tweet. By removing the hyperlinks unnecessary complexity in data can be eliminated.

2. Removing Special Charecters and punctuations: Few special charecters like &, ( add no value to the text. So, they can be avoided.

3. Expanding Contractions : The words can't and cannot literally mean the same thing to the humans. But the program cannot find the similarity between the two and learn them as two independent words which is undesirable. So contracted words are expanded.

4. Removing Stopwords : Stopwords like a, the, an etc are more frequernt in english and contribute minimum to the overall context of the context. So, by removing them, we can reduce the length of tweet on a large scale.

5. Word2Vec: Word2Vec is used for word representations in Vector Space. It is a shallow Neural Network that can be trained with the corpus from the training data. These models use context. After completion of learning process the model can group similar words together. They eventaully end up having similar embeddings. A example is shown in the figure below.

![Capture](https://user-images.githubusercontent.com/55786239/184655511-8927ff15-febe-4901-9eb5-0f1e2db1cd96.PNG)

6.Tokenization : It is referred as a process to split the larger text into smaller lines or individual words. It is basically splitting the sentence into individual words

## Training

Model is built using a embedding layer from keras and a LSTM layer. Model is trained for 8 epochs with a batch size of 1024. Adam optimizer with learning rate of 1e-4 is used. Two callbacks EarlyStopping and ModelCheckpoint are used to monitor the model.
