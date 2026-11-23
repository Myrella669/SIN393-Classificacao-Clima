**SIN393-Classificação-Clima**

Classificação de fenômenos meteorológicos em imagens usando Deep Learning

**Descrição do projeto**

Este projeto foi desenvolvido para a disciplina SIN 393 – Introdução à Visão Computacional. O objetivo é classificar imagens de fenômenos meteorológicos, como chuva, neve e neblina, utilizando modelos de Deep Learning implementados com PyTorch.

Foi realizada uma comparação entre os modelos ResNet18 e EfficientNet-B0, utilizando Transfer Learning e técnicas de Data Augmentation para o treinamento e a avaliação dos modelos.

**Conjunto de dados**

O conjunto de dados é o [Weather Image Recognition](https://www.kaggle.com/datasets/jehanbhathena/weather-dataset), do Kaggle, com 6.862 imagens. As classes são orvalho, neblina ou fumaça, geada, gelo liso, granizo, relâmpago, chuva, arco-íris, escarcha, tempestade de areia e neve.

**Configuração do experimento**

O conjunto de dados não é fornecido dividido. Por isso, 70% das imagens foram destinadas ao treino, e o restante foi dividido igualmente entre validação e teste (4.803, 1.029 e 1.030 imagens). A divisão utiliza o `train_test_split` do scikit-learn, estratificada por classe e com `random_state = 42`. O conjunto de teste é empregado apenas na avaliação final.

As imagens são redimensionadas para 224 × 224 e normalizadas com a média e o desvio padrão da ImageNet. No treino, são aplicados espelhamento horizontal, rotação de até 15 graus e pequenas variações de brilho e contraste. Espelhamento vertical e rotações grandes não foram usados, pois a posição do céu e do solo é informativa para fenômenos como arco-íris e relâmpago.

O treinamento utiliza entropia cruzada, otimizador Adam com taxa de aprendizado de 0,001, lotes de 32 imagens e 5 épocas. A cada época, o modelo é avaliado na validação, e os pesos da melhor época são os usados no teste. A avaliação inclui matriz de confusão, acurácia, precisão, recall e F1-score, com média macro e média ponderada.

**Instruções de execução**

**Requisitos**

- Conta no Google, para usar o Google Colab.
- Conta no Kaggle, para baixar o conjunto de dados pela API.
- GPU (opcional, mas recomendada). O Colab oferece uma GPU T4 gratuita.

**Dependências**

O notebook foi desenvolvido para execução no Google Colab. As principais bibliotecas utilizadas são:

- `torch` e `torchvision`
- `scikit-learn`
- `matplotlib`
- `seaborn`
- `kaggle`

**Etapas para execução**

1. Abrir o notebook `Classificacao-Clima_codigo.ipynb` no Google Colab.
2. Configurar o ambiente de execução para usar GPU, se disponível.
3. Configurar a autenticação da API do Kaggle para permitir o download do conjunto de dados. O token deve ser gerado em Settings > API, no Kaggle, e não deve ser publicado no GitHub.
4. Executar as células do notebook em sequência para baixar os dados, separar os conjuntos de treino, validação e teste e treinar os modelos.
5. Ao final da execução, serão apresentadas as métricas de avaliação, as matrizes de confusão e os exemplos de classificações corretas e incorretas.

**Vídeo de apresentação**
https://youtu.be/qhVoQJQO7vk
