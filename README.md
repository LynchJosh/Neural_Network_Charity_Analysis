# Neural_Network_Charity_Analysis



#	Overview 
preprocess data for a neural network model, and build a binary classifier to predict the success of applicants funded by Alphabet Soup. Then compile, train, and evaluate the model. Finally, optimize the model to try and achieve higher accuracy.

#	Results


Data Preprocessing
What variable(s) are considered the target(s) for your model?
The IS_SUCCESSFUL variable is the target for the model 

What variable(s) are considered to be the features for your model?
The features for the model were APPLICATION_TYPE, CLASSIFICATION,AFFILIATION , USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT 


What variable(s) are neither targets nor features, and should be removed from the input data?
EIN and NAME columns were removed as targets and features

Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
For the neural network, I used 2 hidden layers with one containing 8 and the other containing 5. These numbers were used in previous work and seemed to be a good starting point before optimizing them. Sigmoid was used as the Activision function for the output. ReLu was used on the hidden layers to find nonlinear relationships. 

Were you able to achieve the target model performance?
The target of 75% was not met as intended. The model was able to produce an accuracy of 73%

What steps did you take to try and increase model performance?
For the first attempt, I changed the replaced class to < 1000 and I changed the numbers for the hidden layers  ![Opt replace 1](https://user-images.githubusercontent.com/112728628/221437065-2597ee76-f456-4c7f-89d1-79a2b6cb8b39.PNG)
![opt 1](https://user-images.githubusercontent.com/112728628/221437070-8693f14c-711a-4277-847b-67276c5143d4.PNG)
![Opt 1 result](https://user-images.githubusercontent.com/112728628/221437075-914a9037-f03d-4b14-a361-54ab3e2553b8.PNG)

replace_class = list(classification_counts[classification_counts <1000].index)
Result: 73.4%

Second attempt a third hidden layer was added
Results: 72%
![Opt 2](https://user-images.githubusercontent.com/112728628/221437100-6429648e-b994-4536-94ca-656cdbbdbe68.PNG)
![Opt 2 result](https://user-images.githubusercontent.com/112728628/221437102-0cc69657-4f93-4729-b6d0-aaef990b2048.PNG)

Third attempt a fourth layer was added and the epoch was lowered to 50 
Result: 72%
![Opt 3](https://user-images.githubusercontent.com/112728628/221437111-63c88778-8d9b-4e1a-a6d3-f59a184d13ea.PNG)
![Opt 3 result](https://user-images.githubusercontent.com/112728628/221437117-d84b47af-30e7-4d98-adfe-0460ab8efbc0.PNG)

#	Summary

My second attempt had a .4% higher accuracy than the first model. Adding more hidden layers slightly increased the accuracy however the targeted goal was not met at 75%. I would recommend the use of a random forest model as it would yield better results for classification. 
