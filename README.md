### NAME : YUVARAJ M
### REG NO : 212224040377
###  DATE : 2/05/2027
# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
## TOOLS USED:
Dataset: stockmarket
Google Colab
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
from matplotlib import pyplot as plt
import pandas as pd

df = pd.read_excel("/content/dataset.xlsx")

df['Date'] = pd.to_datetime(df['Date'])

df = df.groupby('Date')['Open'].mean()

df_resample = df.resample('D').interpolate()

df_resample.plot(kind='line', label='Open Price')

plt.title('Time Series Analysis of Dataset')
plt.xlabel('Date')
plt.ylabel('Open Price')

plt.legend()
plt.grid(True)

plt.show()

```


# OUTPUT:

<img width="767" height="590" alt="image" src="https://github.com/user-attachments/assets/d2f35c4a-3df4-4852-ace9-edb0ccf2505f" />




# RESULT:
Thus we have created the python code for plotting the time series of given data.
