HANDS-ON MACHINE LEARNING WITH SCIKIT-LEARN, KERAS & TENSORFLOW



MARCH 21

ml is good for any type of idea: forecasting next year's revenue, detect which transactions are likely to be fradulent, recommend products for each client based on what similar clients bought, segment customers and find the best marketing strategy for 	each group.

ml = is a science so computers can learn from data. a computer program is said to learn from experience E with respect to some task T and some performance measure P, if its performance on T, as measured by P, improves with experience E.

data mining = is when ml techniques are applied to dig into large amounts of data and it helps discover patterns that were not immediately apparent. For example, spam filter has been trained. We can inspect which words actually are best predictors of spam. Sometimes this will reveal unsuspected correlations or new trends, and this will lead to a better understanding of the problem.

at mit, almost every trash can has a camera with an ml application that identifies which trash can you should put it in. image classification using cnn.

for my projects on earnings calls and american dream, i will be using nlp (text classification using RNNs/CNNs/Transformers).

making app react to voice commands is speech recognition.

a typical supervised learning task is classification.

In Machine Learning, attrbitute is a data type while a feature has several meanings, but generally it is an attrbiute + its value like "mileage = 15,000"

Feature extraction = part of dimensionality reduction task in which the goal is to simplify the data without losing too much information by merging strongly correlated features into one. 

semisupervised learning is when data is just partially labeled becaused it is hard to label everything

There is batch and online learning. Batch is when you train the model on the whole dataset once, online is when the model is trained on mini-batches incrementally.

one important parameter of online learning systems is how fast they should adapt to changing data: this is called the learning rate. If you set a high learning rate, then your system will rapidly adapt to new data, but it will also tend to quickly forget the old data. Conversely, if you set a low learning rate, then the system will have more inertia. That is, it will learn more slowly, but it will also be less sensitive to noise is the new data or outliers (anomalies). 

client's will notice when we do online learning and we fed bad data to the system, performance will gradually drop.

parameters: weight and bias (model parameters) + hyperparameter (learning algorithm's parameter)

In 2009 famous Microsoft paper "The Unreasonable Effectiveness of Data" came out: "these results suggest that we may want to reconsider the trade-off between spending time and money on algorithm development versus spending it on corpus development".

Okay, I did not understand the difference between the instance-based learning & model-based learning (generalization approaches):
	1. generalize new cases by using a similarity measure to compare them to learned examples
	2. we build a model of these examples and then use that model to make predictions. example regression 
	countries gdp per capita vs life satisfaction



It is crucial to use a training set that is representative of the cases we want to generalize to.  


Most data scientists spend a significant amount of their time just cleaning up the training data.

Is it better to get rid of the missing values or fill them with the median?

Feature Engineering: feature selection and feature extraction.

overfitting = model performs well on the training data, but it does not generalize well.

contstraining a model to make it simpler and reduce the risk of overfitting is called regularization. overfitting happens when model is too complex relative to the amount and noisiness of the training data. 

Hyperparameter controls the regularization. 

diffence between model and learning algorithm?
algorithm = is the policy, set of rules, designed to solve a particular problem. Examples: linear regression, decision trees, nns
model = is the specific representation learned from data by applying an algorithm. 

underfitting = is when your model is too simple to learn the underlying structure of data. 

Machine Learning is about making machines get better at some task by learning from data, instead of having to explicitly code rules. Many many types of ML Systems: supervised or not, batch or online, instance-based or model-based. 



So, my overview: 
	1. Training
	2. Validation
	3. Testing

Training: 
	1. gather data
	2. training dataset (feature engineering bla-bla)
	3. feed the training dataset to the learning algorithm
	4. tunes parameters like weights, bias, hyperparameter if model-based
	   generalizes new instances by using similarity measure to compare with learned instances if instance-based
Training done.



If we are deciding between the models and let's say ultimately choose linear regression. How do we decide the value for the regularization hyperparameter?

It is called holdout validation. We hold out part of the training set to evaluate several candidate models and select the best one. Wait. Again: we train multiple models with different hyperparameters on the reduced training set, and we select the model that performs best on the validation set. 

The new held out set is called validation set. After the houdout validation process, we train the best model now on the full training set [p. 31]. This gives us the final model. We evaluate it on test set to get an estimate of the generalization error.


Cross-validation = just repeating validation using many small validation sets.


No Free Lunch Theorem: there is no model that is a apriori guaranteed to work better, so we make assumptions about the data. 


model parameters are learned automatically, while learning algorithms hyperparameter is specified by a human before training. 


