This was a group project work of the Machine Learning course as part of the Machine Learning Developer training in April 2025.

The task was to find the best possible model for diabetes prediction using the unbalanced diabetes dataset from kaggle (https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset/data). Each participant was assigned an algorithm (NaiveBayes, SVM, Decision Tree/Random Forest, Logistic Regression). The best model for each algorithm was determined by cross-validation and gridsearch and later combined by voting.

My Naive Bayes algorithm allows little room for variation in terms of parameters for model optimization, which is why the focus here was more on data preparation, which varied depending on the Naive Bayes algorithm. The Gaussian model is completely unsuitable due to the data. Due to the large amount of binary data, BernoulliNB or CategoricalNB are primarily suitable, which becomes clear in the evaluation.

The final voting was slightly improved by a voting pipeline due to the different data preparation of the four models. This takes into account the different scalers or no scaling as well as different encoding. The NB model was omitted from the final voting pipeline as it worsened the score.
