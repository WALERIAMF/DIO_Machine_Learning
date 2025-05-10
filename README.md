# Projeto 1
Foi criado Um notebook com dados de vendas de sorvete
com o código: 
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load the data
data = pd.read_excel('ice_cream_sales.xlsx')

# Display the first few rows of the data
print(data.head())

# Basic data analysis
print(data.describe())

# Visualize the data
plt.figure(figsize=(12, 6))
sns.lineplot(x='Date', y='Sales', data=data)
plt.title('Ice Cream Sales Over Time')
plt.xlabel('Date')
plt.ylabel('Sales')
plt.show()

plt.figure(figsize=(12, 6))
sns.scatterplot(x='Temperature', y='Sales', data=data)
plt.title('Ice Cream Sales vs Temperature')
plt.xlabel('Temperature')
plt.ylabel('Sales')
plt.show()
