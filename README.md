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
import matplotlib.pyplot as plt
import pandas as pd

df = pd.read_csv("climate.csv", sep="\t")

df.head()

df["date(X)"] = pd.to_datetime(
    df["date(X)"], format="%d-%m-%Y"
)

df.set_index("date(X)", inplace=True)

df["meantemp(Y)"].plot(
    kind="line",
    label="Mean Temperature",
    color="black"
)

plt.title("Time Series Plot of Delhi Mean Temperature")
plt.xlabel("Date")
plt.ylabel("Mean Temperature")
plt.legend()
plt.grid(True)
plt.show()

```







# OUTPUT:


<img width="720" height="577" alt="image" src="https://github.com/user-attachments/assets/51a64762-aaa3-4837-ac1c-394377fccc58" />




# RESULT:
Thus we have created the python code for plotting the time series of given data.
