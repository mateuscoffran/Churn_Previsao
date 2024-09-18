# Probabilidade de Churn de uma empresa de Telecomunicação

****

## 🔍 Sobre o Projeto

O objetivo deste projeto é analisar quais os fatores que mais influenciam no Índice de Churn de uma empresa de Telecomunicação e elaborar Modelos de Machine Learning que ajudem a empresa a identificar os clientes com a maior probabilidade de cancelarem o serviço, a fim de que ela possa atuar com antecedência sobre esses clientes, propondo condições especiais para que eles se mantenham em sua base.

O projeto foi desenvolvido em Jupyter Notebook. Todo o trabalho foi elaborado a partir de duas base de dados csv com diversas informações de clientes da empresa.

## 🗃️ Etapas do Projeto

Para o desenvolvimento do projeto foram importadas e utilizadas várias bibliotecas, como pandas, numpy, scikit-learn, matplotlib, seaborn e optuna.

Foi elaborada a fase de Preparação de Dados, em que foram analisados os Missing Values e valores duplicados e variáveis foram transformadas.

Em seguida, foi realizada a Análise Exploratória de Dados (EDA). Foi realizada a análise univariada das variáveis numéricas e categóricas. Posteriormente, foi realizada a análise multivariada, sendo calculado o Índice de Correlação entre variáveis quantitativas e o nível de associação entre as variáveis e a variável binária (Churn ou Não Churn),  utilizando o IV (Information Value). Com base nesses cálculos, realizei uma série de análises do comportamento das variáveis e dos relacionamentos entre elas.

Com a EDA finalizada, desenvolvi 9 modelos para avaliar qual teria o melhor poder de classificação dos clientes que deram churn.
Os 9 modelos desenvolvidos foram: Regressão Logística, Árvore de Decisão, Bagging de Regressão Logística, Random Forest, AdaBoost, Gradient Boosting, XG Boost, LightGBM e CatBoost.

Foram calculadas métricas de desempenho dos modelos. A principal medida utilizada para avaliação dos modelos foi o Recall, uma vez que a perda de clientes pela não identificação de potenciais canceladores tende a ser mais impactante para o negócio do que o custo de oportunidade de oferecer condições especiais para clientes que provavelmente continuariam com o serviço (o qual é medido pela medida Precision).

Uma vez analisados todos os modelos, realizei a Tunagem dos Hiperparâmetros de todos os modelos, considerando como referência para a otimização, a métrica Recall.

Após a Tunagem, o modelo que apresentou a melhor performance foi a Árvore de Decisão (Decision Tree) apresentando um Recall de 78% na base de teste e entregando uma boa capacidade de generalização.
