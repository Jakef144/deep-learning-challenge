# deep-learning-challenge
Overview of the Analysis

The purpose of this analysis is to develop a deep learning model that can predict whether an applicant will be successful if funded by Alphabet Soup. Using a dataset of over 34,000 past funding recipients,
we preprocessed the data, built a neural network model, and evaluated its performance to optimize accuracy above 75% (69%).

Results

Data Preprocessing

Target Variable: IS_SUCCESSFUL (Binary classification: 1 for successful, 0 for unsuccessful)

Feature Variables:

APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT

Variables Removed:

EIN and NAME were dropped as they do not contribute to the predictive model.

Compiling, Training, and Evaluating the Model

Neural Network Architecture:

Input Layer: Number of input features based on preprocessed data.

First Hidden Layer: 80 neurons, ReLU activation function.

Second Hidden Layer: 30 neurons, ReLU activation function.

Output Layer: 1 neuron, Sigmoid activation function (for binary classification).

Training Configuration:

Loss function: binary_crossentropy

Optimizer: adam

Batch size: 64

Epochs: 50

Model Performance:

Initial accuracy: ~65.6%

Optimized accuracy: 69.5% (achieved by adjusting batch size to 64)

Optimization Attempts:

Added a third hidden layer (decreased performance).

Increased neuron count in hidden layers (decreased performance).

Adjusted batch size (improved performance).

Considered alternative activation functions and learning rate tuning.

Summary

Final Accuracy: 69.5% (Below 75% target but improved from baseline)

Potential Improvements:

Increase number of epochs for further training.

Experiment with alternative activation functions such as tanh.

Tune the learning rate using Adam optimizer.

Perform feature selection to reduce noisy or redundant inputs.

Alternative Model Recommendation:

A Random Forest Classifier or XGBoost model could be more interpretable and achieve higher accuracy.

Logistic Regression with feature engineering may also provide competitive results.

The deep learning approach provides a solid foundation for classification, but further hyperparameter tuning and alternative models should be explored to exceed the 75% accuracy threshold.