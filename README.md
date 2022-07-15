# MushroomClassifier
Harrison Carter
Flatiron School NYC Data Science

## Business Understanding
Determining the edibility of mushrooms is of crucial importance in the field. Our field guide uses a data science approach to determine the edibility of any given mushroom within the 173 species provided in the supplementary dataset. This classifier has potential uses as a classifier of unknown species, and can be used by a lay person to determine the edibility of the mushroom in question.

## Data Understanding
The data used for training and testing is a synthetic dataset generated expressly for the purpose of machine learning classification. The data was generated from the secondary dataset of 173 real mushroom species, meaning all entries in the testing set are properly labeled and correspond to a known species. The generative data for each of these species contains 353 hypothetical with minor variations on the numerical portion of the data. For this reason, we expect the classification scores to be very high, provided we find the best model. This will impose some limitations down the line that we will discuss later.

![Dataframe Sample](

## Modelling
For the rest of the project, we rely heavily on sklearn's Pipeline to create and assess our models. We first combine the transformers under the ColumnTransformer. We then establish our baseline model pipeline using the logistic regression classifier and fit it to the training data, and determine the accuracy of the model on training and test data sets. Below is the baseline confusion matrix, ROC curve, and classification report.



The model is surprisingly good for a baseline, but we need to ensure we increase recall. This is because false negatives in this case represent mushrooms that are classified as edible but are in fact poisonous. We will need a model with a better score, and then we also need to increase the threshold to reduce our false negatives. We then try a decision tree model by replacing the logistic regression model in the pipeline. The model trains at 1.0 and tests at 0.9986, which is fantastic, but take a look at the confusion matrix below.





## Evaluation


## Deployment

