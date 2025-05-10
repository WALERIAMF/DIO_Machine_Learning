# Projeto 1
Foi provisionado um cluster standard

Foi criado Um notebook com dados de vendas de sorvete:
Foi criado um excel com os dados para serem treinados através do copilot e testados, foram 100 linhas
com o código: 
---------------------------------------------
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

--------------------------------------------
# Pipeline de Teste - Azure Machine Learning Studio (Designer)

Foi criada uma pipeline de teste com os seguintes componentes, na ordem:

## Componentes do Azure Machine Learning Studio (Designer)

### 1. Parameter
Permite definir valores ajustáveis (parâmetros) que podem ser utilizados em outros componentes do pipeline, como hiperparâmetros de modelos.  
**Exemplo**: taxa de aprendizado, número de iterações.

---

### 2. Select Columns in Dataset
Usado para selecionar colunas específicas do conjunto de dados, seja para manter ou excluir.  
Ajuda a focar nas variáveis relevantes para o modelo e remover informações irrelevantes ou sensíveis.

---

### 3. Linear Regression
Componente que representa o modelo de regressão linear.  
Utilizado para prever valores contínuos com base em variáveis independentes.  
Este componente define o tipo do modelo, mas não o treina sozinho.

---

### 4. Split Data
Divide o conjunto de dados em duas partes, normalmente:
- Treinamento (ex: 20%)
- Teste (ex: 20%)

Essa divisão permite avaliar o desempenho do modelo com dados que ele ainda não viu.

---

### 5. Train Model
Treina o modelo selecionado (como Regressão Linear) usando os dados de treinamento.  
É necessário informar qual coluna será prevista (rótulo ou `target`).

---

### 6. Score Model
Aplica o modelo treinado aos dados de teste para gerar previsões.  
Permite avaliar se o modelo está generalizando bem.

---

## Modelos com Automated ML

Além da pipeline manual, foram criados **2 experimentos com Automated ML** para treinar modelos automaticamente com base no mesmo conjunto de dados.

O AutoML avalia diversos algoritmos e hiperparâmetros, escolhendo os melhores com base em métricas como MAE, RMSE, R², entre outros.

---



