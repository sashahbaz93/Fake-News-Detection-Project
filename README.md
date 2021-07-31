# Fake-News-Detection-Project

<b>Overview </b>

The authenticity of Information has become a longstanding issue affecting businesses and society, both for printed and digital media. On social networks, the reach and effects of information spread occur at such a fast pace and so amplified that distorted, inaccurate, or false information acquires a tremendous potential to cause real-world impacts, within minutes, for millions of users. Recently, several public concerns about this problem and some approaches to mitigate the problem were expressed. 

The Aims of this projects is to use the Natural Language Processing and Machine learning to detect the Fake news based on the text content of the Article.And after building the suitable Machine learning model to detect the fake/true news then to deploye it into a web interface using python_Flask.

<b>Data- Description: </b>

There are 6 columns in the dataset provided to you. The description of each of the column is given below:

“id”:  Unique id of each news article

“headline”:  It is the title of the news.

“news”:  It contains the full text of the news article

“Unnamed:0”:  It is a serial number

“written_by”:  It represents the author of the news article

“label”:  It tells whether the news is fake (1) or not fake (0).

<b>Data preprocessing</b>

1). Remove all unwanted columns.

2). Remove All Missing Values Records.

3). Removing all the extra information like brackets, any kind of puctuations - commas, apostrophes, quotes, question marks from Text.

4). Remove all the numeric text, urls from Text.

<b>ML model Traning and Building </b>

Here we have build all the classifiers for predicting the fake news detection. The extracted features are fed into different classifiers. We have used Logistic Regression, Stochastic gradient descent,Random forest, GBC, xgboost, DecisionTree, Multinomial Naive Baye and Bernoulli Naive Baye classifiers . Each of the extracted features were used in all of the classifiers. Once fitting the model, we compared the accuracy score and checked the confusion matrix.

The highest accuracy score we are getting is 97.68 but don't worry the model was trained with 61,000+ record 
it will perform well Our finally selected and best performing classifier was Random Forest which was then 
saved on disk with name model.pkl. Once you clone this repository, this model will be copied to your machine 
and will be used for prediction. It takes a news article as input from user then shown to user whether it is true 
or Fake. model.pkl is used to deploy the model using Flask.

<b>ML model Deployment</b>

For Deploying we need to create a sample web interface which will get the text from the user and then send it 
to the flask server. In the flask server we will use the saved model model.pkl to predict the news is real or fake 
and then return the result to the user through web interface.

<b> Summary </b>

As we can see that our best performing models had a 97.68 accuracy score. This is due to the text are still 
containing stopwords and wordnet and for classification we used all the default parameters and we didn't try 
the Deep Learning based classification. Although 97.68 % accuracy with 61,000+ training dataset is not bad We 
will extend this project to implement these techniques in future to increase the accuracy and performance of 
our models.

