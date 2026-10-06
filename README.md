# CS_Final_Project

Complex Systems project testing whether a substation's physical network position can help predict future electrical interruptions.

<br>

#### Problem Statement  
The model is asked to predict which substations are going to experience a simulated interruption in the next 24 hours, given their position in the network and that one initial substation has already failed. This analysis strives to deduce whether this position will improve the quality of the predictions.

#### Data Set  
The data utilized are not real metrics but rather a synthetic teaching dataset representing a 12 by 12 grid graph of 144 substations. Base variables include load ratios (from 0.42 to 0.94) and equipment age (from 2 to 40). The 39 future interruptions are generated through a constructed probability and the initial interruption is always substation SO66.

#### Method(s)  
For this analysis Logistic Regression models are used along with stratified test split. For the preprocessing we also utilize standard scaling.

#### Results  
The added network structure causes a substantial improvement in the models predictions, as depicted through the rise of the F1 score, the Accuracy and ROC AUC. Via the confusion matrix we can further inspect those improvements, where it is demonstrated that the model remarkably reduced its missed actual interruptions from 8 to 3.

#### Interpretation  
These metrics and results undeniably indicate that network structure (degree and clustering) can greatly enhance a model's abilities. Despite these improvements, the model still sustains inaccuracies that could result in community blackouts or unnecessary resource consumption if utilized without professional validation.

#### Reflection  
This analysis proved to be widely successful in deducing the importance of network data. However, it also highlighted how important it is to always verify automated models with human judgement. It is necessary to remember that the model's results are pure math translated into words and will never suffice as proof of their own, no matter how impressive accuracies are.

<br>

*(Special thanks to the instructors and the LEAP program for guiding this project)*
