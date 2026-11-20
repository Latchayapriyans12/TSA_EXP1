# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 

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

```
from matplotlib import pyplot as plt
import pandas as pd

df = pd.read_csv("/content/Nile.csv")

df['time'] = pd.to_datetime(df['time'], format='%Y')
df.set_index('time', inplace=True)

df['Nile'].plot(
    kind='line',
    figsize=(12, 6),
    color='black',
    linewidth=1.8,
    label='River Flow'
)

plt.title('Time Series Plot of Nile River Flow',
          fontsize=14, fontweight='bold')
plt.xlabel('Year')
plt.ylabel('River Flow')
plt.legend()
plt.grid(True, linestyle='--', alpha=0.5)
plt.tight_layout()
plt.show()

```









# OUTPUT:

<img width="850" height="365" alt="image" src="https://github.com/user-attachments/assets/c00460e0-e87e-41bf-a944-cc39e8d71786" />





# RESULT:
Thus we have created the python code for plotting the time series of given data.
