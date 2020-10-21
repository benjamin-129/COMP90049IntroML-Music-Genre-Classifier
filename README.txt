================================================================================
This file describes the classifier implementations used in
COMP90049: Introduction to Machine Learning Project 2: 
Music Genre Prediction from Audio, Metadata, and Lyric Features
================================================================================

Functions:

def pre_process()
=> 	Used to pre process the data obtained from the training, validation and
	testing dataset and splits it into usable dataframes.

def meta_pre_process()
=>	Used to preprocess data to have training, validation and testing features
	and labels that pertain to metadata features

def audio_pre_process()
=>	Used to preprocess data to have training, validation and testing features
	and labels that pertain to audio features

def meta_audio_pre_process()
=>	Used to preprocess data to have training, validation and testing features
	and labels that pertain to audio and metadata features

def train_gnb(train_features, train_labels)
=> 	Used to train a gaussian naive bayes classifier using training features 
	and training labels.

def predict_gnb(gnb, valid_features)
=>	Used to return the predictions made by the gaussian NB classifier on
	the validation features

def train_tree(train_features, train_labels, depth)
=>	Used to train a decision tree classifier using training features and
	training labels. The function allows for the max_depth to be specified

def tree_predict(classifier, features)
=>	Used to return the predictions made by the decision tree classifier on
	the validation features

train_mlp(train_features, train_labels, random_state=1, max_iter=300)
=>	Used to train a multi-layer perceptron classifier using training features 
	and training labels.
	The function allows for the random state and iter to be specified

predict_mlp(mlp, valid_features)
=>	Used to return the predictions made by the multi-layer perceptron 
	classifier on the validation features

evaluate(true_list, predict_list)
=>	Used to output the confusion matrix, accuracy, precision, recall and F1
	metrics with the true labels and predicted labels

================================================================================

Classifiers that use Metadata Features

1. 	A baseline classifier is created using the zero-r/ most-frequent class

2. 	A decision tree classifier is trained using the training dataset. A max depth
	of 4 was used.
	The max depth was found by iterating over different depths and finding the
	depth that provides a high accuracy without it being too high
	A learning curve was created for the classifier

3.	A neural network MLP classifier is trained using the training dataset. 
	A learning curve was created for the classifier

4.	A gaussian naive bayes classifier is trained using the training dataset.
	A learning curve was created for the classifier
	
Classifiers that use Audio Features

1. 	A baseline classifier is created using the zero-r/ most-frequent class

2.	A neural network MLP classifier is trained using the training dataset. 
	A learning curve was created for the classifier

3.	A gaussian naive bayes classifier is trained using the training dataset.
	A learning curve was created for the classifier

4. 	A decision tree classifier is trained using the training dataset. A max depth
	of 8 was used.
	The max depth was found by iterating over different depths and finding the
	depth that provides a high accuracy without it being too high
	A learning curve was created for the classifier


Classifiers that use both Audio and Metadata Features

1. 	A baseline classifier is created using the zero-r/ most-frequent class

2.	A gaussian naive bayes classifier is trained using the training dataset.
	A learning curve was created for the classifier

3. 	A decision tree classifier is trained using the training dataset. A max depth
	of 2 was used.
	The max depth was found by iterating over different depths and finding the
	depth that provides a high accuracy without it being too high
	A learning curve was created for the classifier

4.	A neural network MLP classifier is trained using the training dataset. 
	A learning curve was created for the classifier

5.	A bagging implementation was used to see if bagging aided in the performance
	of the classifiers created above without feature selection

++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Thank you for taking the time to read this README :)

