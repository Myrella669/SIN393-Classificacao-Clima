# SIN393-Classificacao-Clima
# Classificação de Imagens Meteorológicas usando Deep Learning

## Descrição do Projeto
Este projeto foi desenvolvido para a disciplina SIN 393 - Introdução à Visão Computacional. O objetivo é classificar imagens de fenômenos meteorológicos (como chuva, neve, neblina, etc.) utilizando modelos de Deep Learning implementados no framework PyTorch. 

Para este experimento, realizamos uma análise comparativa entre as arquiteturas **ResNet18** e **EfficientNet-B0**, aplicando estratégias de Transfer Learning e Data Augmentation (Random Horizontal Flip, Random Rotation e Color Jitter) para melhorar a generalização dos modelos em cenários do mundo real.

## Instruções de Execução

### Dependências
O código foi desenvolvido no ambiente Google Colab. As principais bibliotecas utilizadas são:
- `torch` e `torchvision`
- `scikit-learn`
- `matplotlib` e `seaborn`
- `kaggle` (para download automático do dataset)

### Etapas para Execução
1. Abra o notebook `nome_do_seu_arquivo.ipynb` no Google Colab.
2. Configure o acelerador de hardware para **GPU** (Ambiente de execução > Alterar tipo de ambiente de execução > T4 GPU).
3. Adicione o seu token da API do Kaggle (`KAGGLE_API_TOKEN`) na célula de download para obter o dataset *Weather Image Recognition*.
4. Execute as células sequencialmente para baixar os dados, realizar o split (treino/validação/teste), e iniciar o treinamento dos modelos.
5. As métricas e matrizes de confusão serão geradas automaticamente na etapa final de avaliação.

## Apresentação em Vídeo
[Insira aqui o link do vídeo de apresentação no YouTube]
