## Part 1. Sequence Tagging: NER
Part 1 was run without the use of a GPU

# Question 1.1
The output provides us with the words that are most similar to “student”, “Apple” and “apple” followed by their cosine similarity.

# Question 1.2a
The first output here prints the last few rows of each dataset. This is for us to ensure that every sentence in each dataset ends with a new line such that we are able to count the number of sentences using the number of new lines. Through looking at the last few rows of each dataset, we realised that the development dataset used was missing a new line at the very end, hence we included that into the dataset.
The next output shows the size of the training, development and test files. We also included the complete set of all word labels.

# Question 1.2b
The output here provides the example sentence chosen along with all the named entities in this sentence.

# Question 1.3a
Under this section, we included the way we deal with new words. The output here shows the detailed setting of the neural network used.

# Question 1.3b
The output here contains the shape of the parameters that are updated during the forward computation of the Bidirectional LSTM used.

# Question 1.3c/d
Here, we ran the model using the f1 score to stop the model from training. We printed the f1 scores and classification report for each epoch trained. Then we ran the model on the test dataset and printed the f1 score on the test set.

## Part 2. Sentence-Level Categorization: Question Classification
Part 2 REQUIRES the use of a GPU. We recommend running it in Google Colab using the T4 GPU. This is because we try to find optimal hyperparameter values through bruteforce. 

# Question 2a
The output of this part should show the 2 classes that occur at the lowest frequency. These classes are then merged and a new label is assigned to this merged class.

# Question 2b
The output of this part should show us experimenting with two different aggregation methods: max and average. It is here that the hyperparameter optimisation is carried out and the output would reflect the training and evaluating of 24 models to choose the one that yields the highest accuracy. 

# Question 2c
This output should be in the form of the model summary that is generated through tensorflow model summary. There is also another neural network visualisation that is created using the 'plot_model' function.

# Question 2d
The number of epochs is decided after the optimal model is selected based on accuracy values. After inspection, it is 10. 

# Question 2e
This output is similar to that of part b. Accuracy is collected using the 'AccuracyCallBack' class. Accuracies of all the models is then plotted (for training, evaluation and testing).
