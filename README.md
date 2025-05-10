# Projeto 1
Foi provisionado um cluster standard

Foi criado Um notebook com dados de vendas de sorvete:
Foi criado um excel com os dados para serem treinados através do copilot e testados, foram 100 linhas
com o código: 

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

data = pd.read_excel('ice_cream_sales.xlsx')
print(data.head())
print(data.describe())
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

#Foi criado 2 Automateed ML para treinar o modelo
