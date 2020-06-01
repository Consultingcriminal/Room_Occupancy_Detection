# Room_Occupancy_Detection
This dataset describes climatic features of a room and the objective is to predict whether or not the room is occupied.
There are 20,560 one-minute observations taken over the period of a few weeks,over which the model is to be trained and classified.This is a classification prediction problem on which 2 methods have been fit and compared-

1.Vector AutoRegression(Statistical Modelling)

2.Univariate Stacked LSTM(Deep Learning)


## Classification Model-

  Model-RandomForestClassifier(decision trees=100,Bootstrap=True)
  
  Model_Accuracy-0.9914(train:test=80:20)
  
  Model Fit After Balancing the data using SMOTE
  
## TimeSeries Forecasting
#### Vector AutoRegression(VAR)
   A VAR model was trained and tuned on the 80:20 split with a max. lag of 28 observations(aic=28).
   
   Observation-Though the computation is pretty inexpensive.The model does not genralise too well,resulting in poor classification accuracy and a less relaible model
   
#### Univarariate Stacked LSTM
  Individual Features were trained with a max. lag of 10 observations and stacked together for as final_forecast
  
  Model_Summary-4 LSTM Layers
  
                 1 Dense Layer
                           
                 optimizer=adam
  
  Observation-The model albeit computationally expensive,genralises pretty well and gives an almost 98% accuracy on classification wrt to test split.
  
  
  ## Model Comparision
  
  <img src="images/Model_Performance.png" title="Model_Comparision">
  
  ## Visual_Comparision
  
  VAR_Model
  
  <img src="images/VAR_Performance.png" title="VAR_Performance">
  
  The model seems to follow a long term sequence and does not generalise too well.
  
  LSTM Model
  
  <img src="images/LSTM_Performance.png" title="LSTM_Performance">
  
  The model seems to generalise very well giving us almost accurate results,upon which future can easily be forecasted and room avalablity can be understood well in advance.
  
  
  
