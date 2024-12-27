# mlproject
# Análise de Sentimento em Reviews de Filmes do IMDb

Este projeto é uma aplicação de aprendizado de máquina que prediz se uma review de filme é positiva ou negativa. O modelo foi treinado usando o dataset de reviews de filmes do IMDb, disponível no TensorFlow.

## Visão Geral
O objetivo deste projeto é classificar reviews de filmes como positivas ou negativas com base no texto fornecido. Esta tarefa binária de análise de sentimento é um desafio comum em processamento de linguagem natural (PLN) e tem aplicações na compreensão de feedbacks e reviews em larga escala.

## Dataset
O dataset utilizado neste projeto é o conjunto de reviews de filmes do IMDb, disponível diretamente no módulo TensorFlow Datasets. Ele consiste em 25.000 reviews rotuladas para treinamento e 25.000 reviews rotuladas para teste, divididas igualmente entre sentimentos positivos e negativos.

### Preprocessamento
- Tokenização dos dados textuais.
- Aplicado padding para garantir consistência no comprimento das entradas.
- Utilização de um tamanho de vocabulário predefinido para limitar a dimensionalidade da entrada.

## Arquitetura do Modelo
O modelo foi construído utilizando uma arquitetura sequencial com as seguintes camadas:
- **Camada de Embedding**: Converte palavras de entrada em representações vetoriais densas. Foi utilizada uma camada de embedding com dimensão de 128.
- **Camada SimpleRNN**: Uma camada de rede neural recorrente simples com 128 unidades e ativação ReLU, responsável por capturar dependências sequenciais no texto.
- **Camada Dense**: Uma camada totalmente conectada com ativação sigmoid para realizar a classificação binária do sentimento (positivo ou negativo).

### Hiperparâmetros
- Tamanho do vocabulário: 10.000
- Dimensão do embedding: 128
- Unidades RNN: 128
- Tamanho do batch: 64
- Número de épocas: 20

### Deploy
O deploy foi feito por meio de um app Streamlit