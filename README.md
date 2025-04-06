# ML2-Project
Brady Hobson and Sara Kent<br>
DS 4420 Spring 2025<br>

## Overview
This project aims to predict Locational Marginal Prices (LMPs) for a power plant located in Massachusetts. We implemented two models:

1. **AR(12) Model**: An AutoRegressive model with lag of 12 hours (AR(12)) written by hand in R.
  
2. **CNN with MLP**: A Convolutional Neural Network (CNN) combined with a Multi-Layer Perceptron (MLP) implemented in Python using Keras. This model used other data besides the LMP to learn patterns within the timeseries to make a prediction. 

## Data Sources
All data was collected from [GridStatus.io](https://www.gridstatus.io/live)
1. **[LMP for AR.BEARSWMP13.8BSW1P](https://www.gridstatus.io/datasets/isone_lmp_real_time_hourly_final)**: Hourly LMP for Bear Swamp, we collected data from Jan 1, 2024 - Mar 27, 2025. Stored in lmp_data.csv
2. **[ISONE Load Forecast](https://www.gridstatus.io/datasets/isone_load_forecast_hourly)**: Hourly load (demand) forecasts for ISO New England. Stored in load_forecast_data.csv
3. **[Day Ahead LMP for AR.BEARSWMP13.8BSW1P](https://www.gridstatus.io/datasets/isone_lmp_day_ahead_hourly)**: Day Ahead LMP for Bear Swamp. Stored in dayahead_data.csv

## Files
- **AR_model.rmd & AR_model.html**<br>AR model implemented by hand in R. Only the LMP data was used to make predictions.
- **cnn.ipynb**<br>CNN model implemented using keras in python. Load forecast, day ahead price, and month were features in the model. 
