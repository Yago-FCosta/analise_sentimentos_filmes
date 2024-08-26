# Análise Sentimentos Filmes

## Descrição do Projeto
Um sistema para filtrar e categorizar resenhas de filmes está sendo desenvolvido. O objetivo é treinar um modelo para detectar automaticamente resenhas negativas. 
Será utilizado um conjunto de dados de resenhas de filmes do IMDB com rotulagem de polaridade para criar um modelo para classificar resenhas como positivas e negativas. 

## Ferramentas e Bibliotecas Utilizadas
- Python: Linguagem principal utilizada para a análise.
- Pandas e Numpy: Biblioteca para manipulação e análise de dados.
- Sklearn, lightgbm: Biblioteca para construção de modelo de machine learning.
- Matplotlib.pyplot e Seaborn: Biblioteca para construção de gráficos
- re: Biblioteca para trabalhar com expreções regulares
- spacy: Biblioteca de software de código aberto para processamento avançado de linguagem natural

## Tabela
O conjunto de dados possui os seguntes campos:
- review: o texto da resenha
- pos: o objetivo, '0' para negativo e '1' para positivo
- ds_part: 'train'/'test' para a parte de treinamento/teste do conjunto de dados, respectivamente

## Metodologia
**Análise Exploratória de Dados**
- Importar as bibliotecas necessárias
- Carregar e visualizar os dados
- Dados ausentes
- Dados duplicados
  
**Análises**
- Número de filmes e resenhas ao longo dos anos.
- Verificar a distribuição do número de resenhas por filme com a contagem exata e o EDK (Estimativa de densidade kernel)
- Distribuição de resenhas negativas e positivas ao longo dos anos para duas partes do conjunto de dados

**Predição**
- Criação de uma função que irá treinar, testar e metrificar cada modelo de Machine Learning utilizado
- Normalização de textos
- Modelo Dummy
- Modelo 1 - NLTK, TF-IDF e Regressão Linear
- Modelo 2 - spaCy, TF-IDF e Regressão Linear
- Modelo 3 - SpaCy, TF-IDF e LGBMClassifier

**Aplicação dos modelos**
- Foram criadas novas resenhas de filmes que foram analisadas nos modelos treinados

## Resultados
Foram treiandos e testados 3 modelos diferentes para realizar a análise de sentimentos das reviews dos filmes. 
Foi recomendado primeiro modelo NLTK, TF-IDF e Regressão Linear, pois além do F1_score ser o maior de todos, as demais métricas tbm foram superiores aos demais modelos, como APS e ROC AUC.

## Aprendizados
- Análise de dados: interpretação e extração de insights valiosos a partir de grandes volumes de dados.
- Preparação do conjunto para aplicações em Machine Learning: separação do conjunto original em teste e treino, além da seleção das features e target do modelo.
- Funções: construção e aplicação de funções para simplificar o código.
- Regras de negócios: aplicação de regras de negócio para resolução de problemas.
- Trabalho com textos: uso de expressões regulares, vetorização, tokenização, Lematização
- Análise de sentimentos de textos: analisar qual o "sentimento" de uma determinado texto e como podemos realizar a predição do mesmo
- Aplicação de modelos de Machine Learning: aplicação, seleção de hiperparâmetros, teste e avalição do modelo.
- Documentação de projetos: elaboração de documentação clara e detalhada para garantir que o projeto seja compreensível e replicável.
- Utilização de bibliotecas e ferramentas: aplicação prática de diversas bibliotecas e ferramentas do ecossistema Python.
- Tomada de decisões baseadas em dados: uso de insights derivados da análise de dados para orientar decisões estratégicas.
