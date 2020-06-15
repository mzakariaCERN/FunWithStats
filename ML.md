Overfitting is a common problem in ML, where a model performs well in training data but doesn't generalize well to unseen data (testing data).

If a model suffers from overfitting, it can be described as having high variance, which can be caused by having too many parameters, leading to a model that is too complex (tries to fit the noise)

If a model suffers from underfitting, it can be described as having high bias, which means that the model is not complex enough to capture the patterns in the training data. 

One way to find the right bias-variance trade off is using regularization. Which fights collinearity (features with high correlation) and thus over-fitting. See rashka P77
