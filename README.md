# Classificação de Imagens com Redes Convolucionais Pré-treinadas

## Equipe
* Gabriel Fernando Floriano - 2564149
* Robson Luis de Carvalho - 2539039

## Descrição do(s) Descritor(es) Implementado(s)
Neste projeto, utilizamos a arquitetura de Rede Neural Convolucional **ResNet50** como principal descritor de características. A ResNet50 é uma rede neural profunda pré-treinada no vasto dataset ImageNet, o que lhe confere a capacidade de extrair **características hierárquicas e complexas** das imagens. Ela atua como um poderoso extrator de características genéricas (bordas, texturas, formas, etc.), que são então adaptadas para a tarefa de classificação específica do nosso dataset através de camadas adicionais e um ajuste fino (fine-tuning).

## Repositório do Projeto
https://colab.research.google.com/drive/1GN7ioEdsnzQbzo9y7FgBTf5GeXi2KKXL#scrollTo=F8IQ16yXmgMx

## Classificador e Acurácia
O classificador utilizado é uma **Rede Neural Densa (MLP)** construída sobre as características extraídas pela ResNet50. Após o extrator de características ResNet50 (com camadas congeladas), foram adicionadas camadas densas com ativação ReLU, uma camada de Dropout para regularização e uma camada de saída com ativação Softmax para classificação multirrótulo.

**Acurácia Obtida:** 88%
**Loss Obtido:** 0.3016 (No campo de treinamento)

## Instruções de Uso
Para executar este projeto, siga os passos abaixo no Google Colab:

1.  **Faça o upload do arquivo `.ipynb`** (ou abra-o diretamente do GitHub/Drive se for o caso) no seu ambiente Google Colab.
2.  **Execute as células sequencialmente.**
    * As primeiras células farão o download e a descompactação do dataset.
    * O código verificará e removerá quaisquer imagens corrompidas.
    * Os datasets serão carregados e visualizados.
    * O modelo ResNet50 será carregado, as camadas adicionais serão definidas e o modelo será compilado e treinado.
    * Ao final, a matriz de confusão e outras métricas de avaliação serão exibidas.
3.  **Certifique-se de que o ambiente tem GPU ativada** para um treinamento mais rápido (Tempo de Execução -> Alterar tipo de ambiente de execução -> Acelerador de hardware -> GPU).
