# ML Sea Level Predictions using LSTM RNN

This model was created to predict trends in sea level based on data collected in Charleston, South Carolina. The ultimate goal was to attempt to implement a model that could accurately predict the cyclical nature of the data, as well as other trends like the recent increase in sea level rise driven by climate change. 

Due to the presence of long-term dependencies in the time-series data (notably the consistently increasing average sea level), I chose to use an LSTM model for my predictions. This model is a type of recurrent neural network, and its nature was advantageous in this situation since: 
- It can capture long and short-term dependencies (in this case the increase and cyclical nature of the data)
- Overfitting can easily be regulated through hyperparameters like the dropout rate
- It can make accurate predictions for relatively large chunks of new time-series data

In order to accelerate modeling times, the CUDA platform is integrated to make use of the GPU for computation.  

**Sections**
- Imports and Configurations
- Data Preprocessing
    - Null Value Processing
    - Seasonal Decomposition / Analysis
    - Encoding Data
    - Splitting Data
    - Loading Data 
- Model Creation
    - LSTM Model Classes Configuration
    - Configuring Hyperparameters
- Model Training
- Results Analysis
    - Formulating Results
    - Calculating Error Metrics
    - Visualizing Predictions (on Test Data)
    - Future Sea Level Predictions
- Conclusions 
- Sources


  After analysing the model's predictions on test data, it had an RMSE value of 0.0681. The creation and training of the model was also timed with and without GPU integration, and GPU-based computation led to a decrease of 51.0% in training time on average. 
