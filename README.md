# Electricity-Consumption-Forecast
The model provides a forecast of electricity consumption with an accuracy of 98%.

# Background:
With the growing population and technology, the demand for electricity has increased rapidly over the period of time. However, the electricity is still generated using the old method of burning fossil fuel. Since fossil fuels are non-renewable source of energy. Hence, it is vey important to use it wisely and ensure it does not get wasted. This brings us to that the fact that it is also important to not waste the electricity and ensure every unit created finds it use.

This model is created on the whole idea of reducing the wastage of electricity during the production process. It provides the production team a detailed idea about the consumption of electricity with respect to the hour of the data. The dataset proves to provide this estimation with an r2_score of 98%.

# Objective:
To create a machine learning model that helps forecast the future electricity consumption.

# Assumption:
•	People do not switch to new methods of electricity production like solar, wind etc.<br>
•	Fossil fuel-based electricity generation is the only way people are consuming electricity.<br>
•	There is no new player in competition.<br>
•	There is no reform introduced by the government with respect to the factors affecting electricity.<br>
 
# Short comings:
•	The dataset is collected from only one of the electricity consumption boards.<br>
•	The dataset only provides area of a particular district and hence cannot be used for reference in another district.<br>
# Method:
1.	Data and libraries import:<br>
The dataset was downloaded in the csv file and imported in the jupyter notebook for further analysis. Alongside this the required libraries were also imported to help make the Machine Learning model.

2.	Checking null values:<br>
The dataset was checked for potential null values and it was found that all of the columns expect the timestamp contained null values. Interpolation method was used on columns like temperature and humidity. Forward fill and backward fill method was used on columns namely hour, dayofweek, month, year, dayofyear. 
3.	Tackling Outliers: <br>
The data did contain outliers but we cannot remove them as on days with high temperature and low humidity people tend to use a lot of electricity while using air conditioner. Similarly, on freezing cold days the demand of electricity increases due to high usage of heater or geysers. Hence, we will not be removing outliers as they will play an important role in model creation.

4.	 Feature Creation:<br>
Rolling Average column was created for the demand column. It contained 24-hour demand lags and 168 hours demand lag. This was done to understand the change in demand every 24 hour i.e. 1 day and every 168 hours i.e. 7 days or 1 week time interval. Rolling average play an important role in time series analysis. <br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Graphs were created to understand its change in demand over time., year, month, temperature.<br>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Correlation heatmap was created to understand the correction between all the variables and the columns that are not important are 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; removed from the dataset.

5.	Model Creation and Forecasting:<br>
XGBoostRegressor was used to create the machine learning model. This model forecasted the future consumption with 98% r2_score. This could also be seen in the actual vs predicted plotted line chart.

# Final Verdict:
The model is able to predict the electricity requirement when provided with the temperature, humidity, date and time with an accuracy of 98%.  The metrics like temperature, humidity, date and time are easy to get and work with and hence getting an idea of the electricity consumption is an easy task.   
The authorities can have an idea about the estimated amount of electricity that they need to generate in a particular hour of the day. This helps them maintain keep the required amount owing to the demand. Thus, reducing electricity wastage. 

