# Module 21 – Alphabet Soup Investment Classification Report

## Overview of the Analysis

Machine Learning models are wonderful tools to use in predicting outcomes. For our purposes today, we are using a neural network model to see if we can predict the success of investments by using the features in our database. If we can determine the successful parameters, we can choose where to invest our money wisely. 
  
## Results

•	Data Preprocessing:
o	Model Target = “Is Successful” data column is being used as the targe in the modeling, as this shows the success of the investment opportunity.
o	Model Variables = The following features were used in the model:
	    - APPLICATION_TYPE - Alphabet Soup application type
	    - AFFILIATION — Affiliated sector of industry
	    - CLASSIFICATION — Government organization classification
	    - USE_CASE — Use case for funding
	    - ORGANIZATION — Organization type
	    - STATUS—Active - status
	    - INCOME_AMT — Income classification
	    - SPECIAL_CONSIDERATIONS — Special considerations for application
	    - ASK_AMT — Funding amount requested  
o	Model Variables Removed = “EIN”, “NAME” columns were removed, because these features would have no direct impact on the outcomes.


•	Compiling, Training, and Evaluating the Model:
o	Model Definition = The initial model was defined with the following parameters:
	    - Input – Length of Training Data 
	    - Layer1 – Nodes=5, Activation=relu 
	    - Layer2 – Nodes=5, Activation=relu
	    - Output – Activation=sigmoid
        - Epochs = 100
o	Accuracy = Unfortunately, the model’s accuracy came in at 72.5%. Our hopes were to reach 75% accuracy. 
o	Optimization = We attempted to increase accuracy by tweaking the definitions.  
	    - Op1 (tanh, layer1 = 5nodes, layer2 = 5nodes) – Keeping the layers and nodes the same, we were looking to see if changing the activation to tanh would help to optimize the model. This resulted in a slight improvement to 72.8% accuracy, so we decided to keep the activation as tanh.
	    - Op2 (tanh, layer1 = 8nodes, layer2 = 8nodes) – Keeping the layers and activation the same, we were looking to see if increasing the nodes from 5 to 8 per hidden layer would help to optimize the model. This actually took us back down to 72.5% accuracy.  
	    - Op3 (tanh, layer1 = 5nodes, layer2 = 5nodes, layer3 = 5nodes) – Seeing as the increased nodes did not add to the accuracy, we took it back down to 5 nodes, but we wanted to see if adding an additional layer would help to optimize the model. This kept us right in the same ballpark of 72.5% accuracy.

## Summary

Unfortunately, we were not able to quite meet our goal at having a 75% accurate prediction from our Neural Network. My attempts at optimization didn’t increase the accuracy of the model, as I would have expected. That said, I would be interested at looking at other supervised machine learning models like linear regressions to see if we can get a better look at the relationships between the features. Given that the deep learning model should be the most accurate, I am not sure which models will increase accuracy aside from perhaps a random forest model could be worth exploring as it is typically known for accuracy as well.   
