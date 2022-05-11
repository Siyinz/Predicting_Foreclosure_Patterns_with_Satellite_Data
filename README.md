# Predicting_Foreclosure_Patterns_with_Satellite_Data

### Executive Summary 
- We asked ourselves, how can we get better foreclosure information to observe and understand patterns in the economic health of towns and cities, and so we set out to harness the power of remote sensing and see if we could inform a machine learning prediction model using satellite features. 
- We accessed and used CoreLogic data containing property deed, tax and foreclosure information. We used the features available from this source to fit a baseline model, scored with accuracy and mean squared error.
- To handle the large and messy datasets of CoreLogic, we dropped highly incomplete features, encoded categorical features and selected a county-level sample to make processing faster. 
- We accessed, processed and output light night intensity features for each property based on longitude and latitude coordinates using publicly available NOAA files. These monthly installments of brightness were affixed to each property as additional features for prediction. 
- Because only 6% of our dataset was a foreclosure, we conducted upsampling and downsampling to prevent bias in the model. Based on performance, we continued forward with the downsampled dataset to train and test our model. 
- After the addition of the satellite image features, we also ran our data through several other models like XGBoost and a Neural Network to improve performance.
- While we did see improvement in the model’s accuracy and MSE evaluation metrics with the downsampled data using the satellite features, these improved results were not supported when the model was limited to only CoreLogic features or only Satellite image features. Our highest performance for foreclosure prediction was from a combination of both sources together. This was achieved with our Neural Network model with two hidden layers and ReLU activation. 
