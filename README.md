# SIN393-Classificacao-Clima

# Classificação de Imagens Meteorológicas usando Deep Learning

## Descrição do Projeto

Este projeto foi desenvolvido para a disciplina SIN 393 – Introdução à Visão Computacional. O objetivo é classificar imagens de fenômenos meteorológicos, como chuva, neve e neblina, utilizando modelos de Deep Learning implementados com PyTorch.

Foi realizada uma comparação entre os modelos **ResNet18** e **EfficientNet-B0**, utilizando Transfer Learning e técnicas de Data Augmentation para o treinamento e a avaliação dos modelos.

## Instruções de Execução

### Dependências

O notebook foi desenvolvido para execução no Google Colab. As principais bibliotecas utilizadas são:

- `torch` e `torchvision`
- `scikit-learn`
- `matplotlib`
- `seaborn`
- `kaggle`

### Etapas para Execução

1. Abra o notebook `Classificacao-Clima_codigo.ipynb` no Google Colab.
2. Configure o ambiente de execução para utilizar GPU, se disponível.
3. Configure a autenticação da API do Kaggle para permitir o download do conjunto de dados.
4. Execute as células do notebook em sequência para baixar os dados, separar os conjuntos de treino, validação e teste e treinar os modelos.
5. Ao final da execução, serão apresentadas as métricas de avaliação, as matrizes de confusão e exemplos de classificações corretas e incorretas.

## Apresentação em Vídeo

[Insira aqui o link do vídeo de apresentação no YouTube.]
