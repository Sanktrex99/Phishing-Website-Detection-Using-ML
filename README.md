# Phishing-Website-Detection-Using-ML
We propose an approach to set the parameters with boundary setting  for a functional neural network model for the phishing website identification model. Under  this methodology, the algorithm chooses a characteristic set appropriate for identifying  phishing sites. Then, the neural network trains the chosen feature set to build an ideal  classifier to characterize &amp; detect phishing websites.

## TDLHBA (Tuning Deep Learning using Bat/Hybrid Bat Algorithm)
Here we use the “TDLHBA (Tuning Deep Learning using Bat/Hybrid Bat Algorithm)” hyperparameter settings to determine the training loss and accuracy on the dataset.
To evaluate the effectiveness of our suggested model, two different approaches were assessed. 

### Approach 1 
Randomly Tuned Neural Network was utilized from the UCI phishing dataset  that has 11055 cases, with 55.7% genuine URLs and 44.3% phishing URLs. In the meantime, 70% of the total instances are utilized to train the neural network's classifier, with the leftover 30% being utilized for testing.

### Approach 2 
TDLHBA Hyperparameter Settings was utilized to check the increase in efficiency using tuned hyperparameters. This approach is based on the same dataset used  previously.

## Implementation

A neural network is a notable “supervised learning” strategy. They have solid indeterminate 
mapping abilities and can hypothetically fit unpredictable functions. The customary neural 
network model can be summed up into 3 layers:
● input layer 
● activation method
● output layer

For the most part, the neural network program contains two significant methods: 
● forward propagation method
● and backpropagation method

Whenever there is a signal input & forward propagation, the parameters of a similar layer of 
neurons are decided by the upper layer. Assuming that the computation value of the output 
layer is different from the genuine value, then backpropagation is done.
The ongoing gradient drop computation modifies the settings of every level of the neural unit 
until the inaccuracy is restricted in the backpropagation process.
The usage of a neural network can overcome the over-fitting issue for multi-feature 
characterization concerns in phishing site identification. The neural network system has high 
accuracy in detecting phishing assaults due to its dynamic learning and speculation abilities.
The whole detection process is isolated into two sections:
● the training part
● and the testing part

The feature extraction and feature selection algorithms build an effective feature set from the database during the training phase. The neural network is then used to learn the best features. We can acquire an effective neural network classifier for detecting phishing sites by varying the number of neural network layers and not showing the number of units and the learning rate during the training cycle.
During the testing phase, the extraction of features and selection algorithms eliminate the URLs' corresponding ideal feature set. Then, to achieve the phishing site detection results, these features are fed into the classifier.

Step 1. To produce an ideal feature collection for the training sample, phishing site feature 
extrication & optimization are performed. After playing out the cycle, the limit of FVV 
(Feature Validity Value) is set to 0.096 by taking out 8 features. We cut the dataset, passing 
on just 23 optimal features to participate in the optimization of the neural network model. 
The FVV is defined as 
𝐹𝑉𝑉 = 𝑁𝑢𝑚(𝑝𝑜𝑠𝑖𝑡𝑖𝑣𝑒)+𝑁𝑢𝑚(𝑛𝑒𝑔𝑎𝑡𝑖𝑣𝑒) / 𝑚

Step 2. Here we train a “neural network classifier” reasonable for identifying phishing sites. 
The ideal neural network model is acquired by changing configurations like the number of 
layers, the activation method, and the learning rate.
To acquire the ideal neural network model for identifying phishing sites, we contrasted the 
performances of 6 models with various layers of error.
It very well may be seen from Fig.8 that the classification accuracy is ideal when the 
classification accuracy is three layers. Besides, the classification accuracy arrives at a 
maximum of 97%. Along these lines, our neural network model is implemented as a three-
layered completely associated network with a blend of activation techniques of 'Sigmoid' and 'reLU'. By doing this, our model has a sum of 1406 (23×40+20×23+1×23+3×1=1406) weights 
and 3 biases.

Step 3. The extraction of features and selection interface are used to collect 23 useful attributes to distinguish phishing URLs. Then, at that point, for every URL, we can get a 23-layered effective feature vector [x1, x2, …, x23].

Input: “Fv: feature vector set; 𝜔: weights of NN model; b: bias of NN model; L: number of 
layers in the neural network.”

Output: “Y: phishing classification result.”
Algorithm: 

“NN model ← LoadWeightsBias(𝜔,b); 
𝑝𝑟𝑒𝑑𝑖𝑐𝑡𝑖𝑜𝑛[0] ← 𝐹𝑣; 
for i = 1, ..., L do 
𝑌[𝑖] ← 𝑟𝑒𝐿𝑈(𝑁𝑁 𝑚𝑜𝑑𝑒𝑙. 𝜔 × 𝑌[𝑖 − 1] + 𝑏[𝑖 − 1]); 
end for 
Y ← 𝑝𝑟𝑒𝑑𝑖𝑐𝑡𝑖𝑜𝑛[𝐿]; 
if Y < 0.5 then 
return -1 //It is a phishing URL; 
else 
return 1 //It is a legal URL.”

Step 4. We added the weight & activation variables to the neural network at this stage. Then, at that point, the vector sets of the extracted features were shipped off the prepared neural network classifier to get the phishing sites' identification values. The input parameters are typically handled by a reLU function for each layer. To get the operations to result for a layer, multiply the weighted matrix (𝜔) by the previous layer's result and add bias (b). The classifier's output (Y) is generated once the final layer is handled. If Y is less than 0.5, the program will yield -1 and record this URL as a fraudulent URL, as seen in the above 
computation. Regardless, the method computes 1 and stamps it as a valid URL.

## Summary
We have suggested a functional phishing website detection model in this paper, which is profoundly accurate. We used FVV (Feature Validity Value) to overview the impact of features appropriate to phishing website identification in this work. Our proposed model has a good ability for autonomous learning because it employs the neural network technique. This algorithm is capable of dealing with issues such as a large number of phishing sensitivity features and feature changes over time and also this can help to mitigate the neural network classifier's overfitting problem. Because the sensitivity of feature phishing websites is always 
changing, additional features will be required in the future to accomplish this model. As a next step, you can wrap the final model as a REST API endpoint and use it along with a webpage.
