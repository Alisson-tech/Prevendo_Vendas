# Prevendo_Vendas
Quarta aula da semana python do canal "HashtagProgramação" sobre ciência de dados.

## Situação:

A empresa fornece uma base de dados referentes ao seu gasto em propagandas e o valor das suas vendas,
o objetivo é análisar essa base de dados e desenvolver um algoritmo para previsão de vendas de acordo com o gasto em propagandas.

## Análise

### Biblitoecas utilizadas:

Pandas - manipular os dados

Seaborn - Biblioteca gráfica

Matplotlib - Biblioteca gráfica

sklearn - Algoritmos de IA

### Base de dados:

meios de divulgação do produto (Milhares):
- TV
- Rádio
- Jornal

Vendas decorrentes(Milhões):
- Vendas

![Dados](https://github.com/Alisson-tech/Prevendo_Vendas/blob/master/img/dados.PNG)

### Tratamento dos dados:

A base de dados já está tratada, não existe valores nulos nem colunas irrelevantes.

![ColunasInfo](https://github.com/Alisson-tech/Prevendo_Vendas/blob/master/img/ColunasInfo.PNG)


### Correlação

Primeiro análisamos a correlação dos meios de propaganda com as vendas.

- -1 (correlação negativa quanto maior um menor o outro)
- 0 (Pouca correlação entre as informações)
- 1 (Correlação positiva quanto maior um maior o outro)

O Meio de propaganda "TV" é o que existe maior correlação com o aumento das vendas, o "Jornal" é o que menos indica correlação.
Isso mostra que possivelmente as propagandas realizadas na TV é a que causa maior influência nas vendas dos produtos.

![Correlação](https://github.com/Alisson-tech/Prevendo_Vendas/blob/master/img/Correlacao.PNG)

## Inteligência artificial

### Algoritmos 

- LinearRegression
- RandomForestRegressor

### Overfitting

Muitos Imaginam que quanto mais dados utilizados para treinar a IA, melhor será seu resultado. Porém isso pode causar um overfitting, ou 
seja a sua IA está tão familiarizada com aqueles dados que se mostra ineficaz para realizar previsões.

Para corrigir esse problema, Iremos separar dados para Treinar a nossa IA, e dados para testar sua eficácia.

### Testar algoritmos 

#### Score 

Iremos análisar qual algoritmo é mais eficaz para prever as vendas. Para isso utilizaremos dois métodos do Sklearn, 
R2_score para verificar o score de acertos dos algoritmos, e o mean_squared_error para verificar o score de erros do algoritmo.

O algoritmo random forest se mostrou mais eficaz, pois tem um score de acertos maior e o de erro menor.

![Score](https://github.com/Alisson-tech/Prevendo_Vendas/blob/master/img/score.PNG)

#### Tabelas

Podemos exibir na tela uma tabela para comparar as previsões do RandomForest e do LinearRegression com as Vendas reais separadas para teste.

![TabelaComparacao](https://github.com/Alisson-tech/Prevendo_Vendas/blob/master/img/TabelaComparacao.PNG)

#### Gráfico

Podemos gerar um gráfico para comparar os valores das previsões e as vendas reais.

![GraficoComparacao](https://github.com/Alisson-tech/Prevendo_Vendas/blob/master/img/GraficoComparacao.PNG)


### Prever Vendas

Após testar a eficácia dos algoritmos, conseguimos utiliza-los para prever as vendas.

Nesse exemplo utilizaremos o RandomForest já que ele se mostrou mais eficiente.

A tabela mostra a quantidade prevista de investimento em propagandas na TV, Jornal, Rádio e mostra as vendas prevista pelo algoritmo.

![Previsão](https://github.com/Alisson-tech/Prevendo_Vendas/blob/master/img/previsao.PNG)


