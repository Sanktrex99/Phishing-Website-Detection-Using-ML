# Phishing-Website-Detection-Using-ML
We propose an approach to set the parameters with boundary setting  for a functional neural network model for the phishing website identification model. Under  this methodology, the algorithm chooses a characteristic set appropriate for identifying  phishing sites. Then, the neural network trains the chosen feature set to build an ideal  classifier to characterize &amp; detect phishing websites.

#TDLHBA (Tuning Deep Learning using Bat/Hybrid Bat Algorithm)
Here we use the “TDLHBA (Tuning Deep Learning using Bat/Hybrid Bat Algorithm)” hyperparameter settings to determine the training loss and accuracy on the dataset.
To evaluate the effectiveness of our suggested model, two different approaches were assessed. 

Approach 1 (Randomly Tuned Neural Network) was utilized from the UCI phishing dataset  that has 11055 cases, with 55.7% genuine URLs and 44.3% phishing URLs. In the meantime, 70% of the total instances are utilized to train the neural network's classifier, with the leftover 30% being utilized for testing.

Approach 2 (TDLHBA Hyperparameter Settings) is utilized to check the increase in efficiency using tuned hyperparameters. This approach is based on the same dataset used  previously.

#Summary
We have suggested a functional phishing website detection model in this paper, which is profoundly accurate. We used FVV (Feature Validity Value) to overview the impact of features appropriate to phishing website identification in this work. Our proposed model has a good ability for autonomous learning because it employs the neural network technique. This algorithm is capable of dealing with issues such as a large number of phishing sensitivity features and feature changes over time and also this can help to mitigate the neural network classifier's overfitting problem. Because the sensitivity of feature phishing websites is always 
changing, additional features will be required in the future to accomplish this model. As a next step, you can wrap the final model as a REST API endpoint and use it along with a webpage.
