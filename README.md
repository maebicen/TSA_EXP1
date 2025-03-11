# Ex.No: 01A PLOT A TIME SERIES DATA
# Date: 11/03/2025
# Name:Maebicen Kirubakaran C
# Reg no:24001839

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
import pandas as pd
df=pd.read_csv("Chocolate Sales.csv")
df.head()
df.tail()
import matplotlib.pyplot as plt
df['Date'] = pd.to_datetime(df['Date'])
df.set_index('Date', inplace=True)
import seaborn as sns
numeric_cols = ['Amount', 'Boxes Shipped']
categorical_cols = ['Sales Person', 'Country', 'Product']
for col in numeric_cols:
    plt.figure(figsize=(8, 4))
    sns.histplot(df[col], kde=True)
    plt.title(f'Distribution of {col}')
    plt.xlabel(col)
    plt.ylabel('Frequency')
    plt.tight_layout()
    plt.show()
for col in categorical_cols:
    plt.figure(figsize=(10, 4))
    sns.countplot(data=df, x=col, order=df[col].value_counts().index)
    plt.title(f'Count Plot of {col}')
    plt.xlabel(col)
    plt.ylabel('Count')
    plt.xticks(rotation=45)
    plt.tight_layout()
    plt.show()

```


# OUTPUT:

![image](https://github.com/user-attachments/assets/9b58e36b-eb8f-4677-8a1f-5a62f2316c90)
![image](https://github.com/user-attachments/assets/c8a141f4-5c5b-47cf-9052-2401a1547e67)
![image](https://github.com/user-attachments/assets/2c32d5f8-1f47-4567-b492-9b374555f60c)
![image](https://github.com/user-attachments/assets/17798dee-1fdc-4e2f-a339-450d2308872f)
![image](https://github.com/user-attachments/assets/e865a3a6-8d34-46d3-bff0-b63e167ad42b)




# RESULT:
Thus we have created the python code for plotting the time series of given data.




# RESULT:
Thus we have created the python code for plotting the time series of given data.
