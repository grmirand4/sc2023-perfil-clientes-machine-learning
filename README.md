# [Analisando e determinando perfis de clientes com base em dados sintéticos de uma campanha de marketing](https://github.com/grmirand4/sc2023-perfil-clientes-machine-learning)

**Projeto - Machine Learning II**

Instrutor: [Victor Brito](https://www.linkedin.com/in/victorcbrito/)

**Equipe: [Gabriel Miranda](https://www.linkedin.com/in/grmiranda/), [Marcus Thadeu](https://www.linkedin.com/in/marcus-thadeu/), [Ruann Campos](https://www.linkedin.com/in/ruann-campos/) e [Thiago Caveglion](https://www.linkedin.com/in/thiago-caveglion/)**

## 🎯 Objetivos
* Analisar, de forma exploratória, os dados correspondentes a clientes provindos de uma campanha de marketing.
* Agrupar os clientes em diferentes perfis utilizando aprendizagem de máquina não-supervisionada (K-means).
* Predizer, com base nos perfis criados, as categorias nas quais possíveis novos clientes seriam classificados utilizando aprendizagem de máquina supervisionada (SVM e XGBoost).

## 📊 Sobre o data set
O data set `marketing_campaign.csv` utilizado em nossa análise apresenta informações sintéticas retiradas [dessa base de dados do Kaggle](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis). É um data set simulado contendo diversas informações de clientes que realizaram compras em uma campanha de marketing de uma empresa do ramo alimentício. As colunas do arquivo incluem:
* `ID`: identificador exclusivo do cliente
* `Year_Birth`: Ano de nascimento do cliente
* `Education`: nível de escolaridade do cliente
* `Marital_Status`: estado civil do cliente
* `Income`: renda familiar anual do cliente
* `Kidhome`: Número de crianças na residência do cliente
* `Teenhome`: Número de adolescentes na residência do cliente
* `Dt_Customer`: Data de cadastro do cliente na empresa
* `Recency`: número de dias desde a última compra do cliente
* `Recover`: 1 se o cliente reclamou nos últimos 2 anos, 0 caso contrário

* `MntWines`: Valor gasto em vinho nos últimos 2 anos
* `MntFruits`: Valor gasto com frutas nos últimos 2 anos
* `MntMeatProducts`: Valor gasto com carne nos últimos 2 anos
* `MntFishProducts`: Valor gasto com pescado nos últimos 2 anos
* `MntSweetProducts`: Valor gasto em doces nos últimos 2 anos
* `MntGoldProds`: Valor gasto em ouro nos últimos 2 anos

* `NumDealsPurchases`: Número de compras realizadas com desconto
* `AcceptedCmp1`: 1 se o cliente aceitou a oferta na 1ª campanha, 0 caso contrário
* `AcceptedCmp2`: 1 se o cliente aceitou a oferta na 2ª campanha, 0 caso contrário
* `AcceptedCmp3`: 1 se o cliente aceitou a oferta na 3ª campanha, 0 caso contrário
* `AcceptedCmp4`: 1 se o cliente aceitou a oferta na 4ª campanha, 0 caso contrário
* `AcceptedCmp5`: 1 se o cliente aceitou a oferta na 5ª campanha, 0 caso contrário
* `Response`: 1 se o cliente aceitou a oferta na última campanha, 0 caso contrário

* `NumWebPurchases`: Quantidade de compras realizadas pelo site da empresa
* `NumCatalogPurchases`: Número de compras feitas usando um catálogo
* `NumStorePurchases`: Número de compras feitas diretamente nas lojas
* `NumWebVisitsMonth`: Número de visitas ao site da empresa no último mês

## 💡 Principais conclusões
* Utilizando o K-means, fomos capazes de clusterizar nossos clientes em quatro perfis distintos.
  * Cluster 0 - "Estabilidade Moderada": Maior população, adultos com estabilidade econômica moderada, preferem compras em lojas físicas, menos influenciados por campanhas, mas visitam sites.
  * Cluster 1 - "Prosperidade, Pouco Interesse em Descontos": Grupo mais próspero, adultos mais velhos, menos sensíveis a descontos, preferem produtos de ouro, impactados por campanhas (1 e 5), menos propensos a visitar sites.
  * Cluster 2 - "Diversidade de Compra": Segunda maior população, comportamento de compra diversificado, influência moderada por campanhas, gastos significativos em vinhos, compras em lojas físicas e online, visitam sites e usam descontos.
  * Cluster 3 - "População Idosa Online": População idosa, equilíbrio graduados/pós-graduados, terceira maior renda, menos impactada por campanhas, gastos em vinhos, compra online, visita sites e usa descontos.
* Tanto o modelo de SVM quanto o de XGBoost utilizados apresentaram um ótimo desempenho no que diz respeito à predição de perfis de clientes.

**Limitações:**
* O fato de se tratar de um dataset fictício, que apresentou um ótimo desempenho para uma clusterização de 4 classes, nos indica que essa pode ter sido a intenção inicial de seus autores. Dessa forma, os dados foram provavelmente direcionados de forma proposital para se encaixarem nesses perfis, enviezando nossos modelos de predição, o que implicou na obtenção de ótimas métricas de avaliação. Reconhecemos que esse cenário ideal está longe da realidade.

## 💻 Principais linguagens
- Python
  - Pandas
  - Numpy
  - Seaborn
  - Plotly
  - Matplotlib
  - Sklearn

## 👨‍💻 Execução
Para executar os notebooks localmente, certifique-se de:

* Fazer o download do arquivo `marketing_campaign.csv` [neste link do Kaggle](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis) ou pegar diretamente deste repositório.
* O arquivo `dataset_cluster.csv` diz respeito ao data set tratado utilizado diretamente nos notebooks `02-analise-perfis.ipynb`, `03-svm.ipynb` e `04-xgboost.ipynb`.
  * Ele foi obtido após a classificação e tratamento adotados no notebook `01-eda_kmeans.ipynb`.
* Alterar o caminho nas linhas de código que lêem os data sets em seus respectivos notebooks.

###### Tags: `python` `data-science` `random-forest` `credit-card` `knn` `decision-tree` `fraud-detection` `gradient-boosting`
