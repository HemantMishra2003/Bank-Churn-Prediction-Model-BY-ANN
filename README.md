  ## Bank-Churn-Prediction-Model-BY-ANN
  
This project focuses on predicting customer churn. The goal is to identify which customers are likely to leave the service (churn) and which will continue using it.

my input features: credit card score , age , gender , balance , etc.
Target: Churn (1 = churn, 0 = retain)

  # ANN architechure
  
I used this architecture for  my nueral  network model .. i made nueral architecture 
a bit complex to better train as well also used dropout to not to learn  input ouput 
predict validation in a better way ...


model = Sequential()
model.add(Dense(32, activation="relu", input_dim=11))
model.add(Dropout(0.3))
model.add(Dense(16, activation="relu"))
model.add(Dropout(0.3))
model.add(Dense(8, activation="relu"))
model.add(Dense(1, activation="sigmoid"))

# what i got in my nueral network accuracy 

Accuracy  =            85.9% :
validation accuracy =  85.06 
loss                =   0.34 
Precision           =   0.7782
Recall              =   0.4482
F1 Score            =   0.5688

# conlusion 

The ANN model achieved an accuracy of 85.9% on the training data 
and 85.06% on the validation data with a loss of 0.34. 

- Precision = 0.7782 → When the model predicted churn, it was correct 77.8% of the time.
- Recall = 0.4482 → The model correctly identified 44.8% of the actual churn customers.
- F1 Score = 0.5688 → Overall balance between precision and recall.


  
# XG boost 
  
i also tried xg boost which are made of so many  decision tree base models 
its is boosting technique ....which is used to fix the error by next base model 
and this estimator keep rotating until least error..

#  what i got by this  model  :

Model     =   XGBoost
Accuracy  =   86.55%
Precision =   0.7967
Recall    =    0.4723
F1 Score  =    0.5930


