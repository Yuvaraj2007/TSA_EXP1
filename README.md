# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 22/04/2027

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
## TOOLS USED:
Dataset: DailyDelhiClimateTrain.csv
Google Colab
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
PREM R
212223240124

from matplotlib import pyplot as plt
import pandas as pd

# Load dataset
df = pd.read_csv("/content/DailyDelhiClimateTrain.csv")

# View data
print(df.head())

# Convert 'date' column to datetime
df['date'] = pd.to_datetime(df['date'])

# Check data types
print(df.dtypes)

# Set date as index
df.set_index('date', inplace=True)

# Select one column (like passengers → here meantemp)
df_resampled = df['meantemp'].resample('D').interpolate()

# Plot
df_resampled.plot(kind='line', label='Mean Temperature', color='black')

plt.title('Time Series Plot of Daily Mean Temperature')
plt.xlabel('Day')
plt.ylabel('Temperature')
plt.legend()
plt.grid(True)

plt.show()

```










# OUTPUT:

<img width="695" height="678" alt="image" src="https://github.com/user-attachments/assets/87f7d86b-5d59-4345-bff6-3ad1e9ed7ba7" />





# RESULT:
Thus we have created the python code for plotting the time series of given data.
