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
#Foi criado uma pipeline de teste com os seguintes complementos nessa ordem:
<h1>Componentes do Azure Machine Learning Studio (Designer)</h1>

    <div class="component">
        <h2>1. Parameter</h2>
        <p>Permite definir valores ajustáveis (parâmetros) que podem ser utilizados em outros componentes do pipeline, como hiperparâmetros de modelos. Exemplo: taxa de aprendizado.</p>
    </div>

    <div class="component">
        <h2>2. Select Columns in Dataset</h2>
        <p>Usado para selecionar colunas específicas do conjunto de dados, seja para manter ou excluir. Ajuda a focar nas variáveis relevantes para o modelo.</p>
    </div>

    <div class="component">
        <h2>3. Linear Regression</h2>
        <p>Modelo estatístico usado para prever valores numéricos com base em variáveis independentes. Este componente define o tipo do modelo a ser treinado.</p>
    </div>

    <div class="component">
        <h2>4. Split Data</h2>
        <p>Divide o conjunto de dados em duas partes, normalmente em dados de treino e teste. Ajuda a validar o desempenho do modelo de forma imparcial.</p>
    </div>

    <div class="component">
        <h2>5. Train Model</h2>
        <p>Treina o modelo escolhido (como regressão linear) usando os dados de treino. Requer a especificação da coluna alvo (rótulo) para aprendizado supervisionado.</p>
    </div>

    <div class="component">
        <h2>6. Score Model</h2>
        <p>Usado para aplicar o modelo treinado a dados de teste e gerar previsões. Permite avaliar como o modelo se comporta em dados não vistos.</p>
    </div>




#Foi criado 2 Automateed ML para treinar o modelo
