# Fraudulent-News-Detection
<br>
The aim of this project is to provide aid in detecting fraudulent news that has been on the rise on social media and news platforms online.<br>
<br>
Specifically, the project consists of the following parts:  

* **Preliminaries**: 
  + Exploratory analysis: examination of data and exclusion of non-useful records  
  + Pre-processing: removal of stop words (e.g., "the", "a", "an", and "in")
  + Text visualization: bar plots/ word clouds of frequent words for each feature column
  + Sentiment analysis: creation of sentiment features (i.e., <i>positive, negative, neutral</i>) using polarity scores  
* **Modeling**:<br>
We first built the Logistic Regressions using different sets of features: 
  + Title Sentiments
  + Text Sentiments
  + Title Sentiments & Text Sentiments 
  + Title (transformed into embedding vectors using Word2Vec embedding model with skip-gram method)
  + Text (transformed into embedding vectors using Word2Vec embedding model with skip-gram method)
  + Title & Text (concatenated Title and Text vector representations)<br><br>
Since the combined feature of Title and Text demonstrated competency, we used this feature for training non-linear models. In particular, the following models:
    + Decision Tree
    + Neural Network (MLP) <br>
<br>
Lastly, we tried something different; while the models mentioned so far based on the skip-gram word embedding method, now we wanted to observe if the performance differs by using another word embedding technique: Continuous Bag of Words (CBOW). 
  

* **Model Comparison**: As the dataset was fairly balanced (i.e., 22,850 fake records and 21,416 real records), we defined the measurement of goodness to be accuracy. Among the models trained with skip-gram and the model trained with CBOW, the highest performing models on the validation dataset were the logistic regression and MLP with the combined feature of Title & Text constructed using skip-gram. Further, we introduced a new dataset from Kaggle containing fake & real news records to test the models' performance, where the logistic classifier led to the highest accuracy.  


<br>
Below are the folders and files created for this project:<br> 
<br>

* **Data**: This folder contains data we used in the project  
  + Fake.csv: ISOT data containing records of fraudulent news 
  + True.csv: ISOT data containing records of real news 
  + kaggle_dataset.csv: data containing both fraudulent and real news records, used for testing the model performance<br><br>
* **Fake_News_code.ipynb**: This is the script that performs everything from the preliminaries to model comparison<br><br>
* **Fake_News_code.html**: html file of the code for a quick view

<br>
For the complete methodologies, results, and discussion, please see <b>Model Analysis to Provide Aid in Detecting Fake News.pdf</b>. 
