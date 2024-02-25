# Ex.No: 01 PLOT A TIME SERIES DATA
###  Date: 25-02-2024

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
## Population:

```python
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("POPTHM.csv",parse_dates=["DATE"],index_col="DATE")
df.head()
df_filtered = df["2000":"2023"]
annual_mean = df_filtered.resample('Y').mean()
mean = annual_mean.plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Population (in Thousands)")
plt.title("Average Annual Population (2000-2023)")
plt.show()
```
# Market Price:
```python
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("trainset.csv",parse_dates=["Date"],index_col="Date")
df.head()
df.Close.resample('M').mean()
mean=df.Close.resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Price")
plt.show()
mean=df.Close.resample('Y').mean().plot(kind='line')
plt.xlabel("Year")
plt.ylabel("Price")
plt.show()
```
# Temperature:
```python
import matplotlib.pyplot as plt
import pandas as pd
df=pd.read_csv("DailyDelhiClimateTrain.csv",parse_dates=["date"],index_col="date")
df.head()
mean=df["meantemp"].resample('M').mean().plot(kind='line')
plt.xlabel("Month")
plt.ylabel("Temperature")
plt.show()
```


# OUTPUT:
## Population:
![image](https://github.com/vikashsenthil21/TSA_EXP1/assets/119433834/3abd2eab-03df-4746-b71d-44483a5691f7)
## Market Price:
![image](https://github.com/vikashsenthil21/TSA_EXP1/assets/119433834/f27f1b4e-cbfd-4179-bb9c-39e69e97bf4e)



# Temperature:

![image](https://github.com/vikashsenthil21/TSA_EXP1/assets/119433834/07446df4-1225-419d-b081-d66612bd9a6c)






# RESULT:
Thus we have created the Python code for plotting the time series of given data.











