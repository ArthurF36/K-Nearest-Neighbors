# K-Nearest Neighbors (KNN) - Aprendizado Supervisionado

Este projeto implementa e explora o algoritmo **K-Nearest Neighbors (KNN)** para resolver um problema de classificação binária, utilizando o conjunto de dados *Breast Cancer Wisconsin (Diagnostic)*.

## 📖 Sobre o KNN

O **K-Nearest Neighbors** é um dos algoritmos mais simples de aprendizado de máquina supervisionado. Ele funciona com base no princípio de que instâncias semelhantes estão próximas umas das outras no espaço de características.

### Principais Características:
* **Aprendizado Preguiçoso (Lazy Learning)**: O algoritmo não possui uma fase de treino especializada; ele utiliza todos os dados disponíveis para classificar novas instâncias no momento da predição.
* **Não Paramétrico**: Não assume hipóteses sobre a distribuição dos dados, o que é ideal para dados reais que não seguem pressupostos teóricos como a distribuição uniforme.
* **Requisitos**: Necessita apenas do valor de **K** (número de vizinhos) e de uma **função de distância** (ex: Euclidiana ou Manhattan).

### ✅ Vantagens:
* Implementação extremamente simples.
* Previsões em tempo real rápidas por não exigir treino prévio.
* Facilidade em adicionar novos dados continuamente.

### ❌ Desvantagens:
* Desempenho reduzido com dados de alta dimensionalidade.
* Alto custo computacional em grandes datasets (precisa calcular a distância para todos os pontos).
* Dificuldade em lidar com variáveis categóricas.

## 📊 O Conjunto de Dados

O projeto utiliza o dataset **Breast Cancer Wisconsin (Diagnostic)**, proveniente do repositório UCI Machine Learning.

* **Objetivo**: Auxiliar no diagnóstico médico precoce, prevendo se um tumor é maligno ou benigno.
* **Instâncias**: 569 amostras de biópsias.
* **Atributos**: 30 características numéricas (ex: textura, área, simetria) extraídas de imagens digitalizadas.
* **Classes (Target)**:
    * `M` ou `1`: Maligno
    * `B` ou `2`: Benigno

## 🛠️ Tecnologias e Implementação

O notebook foi desenvolvido em Python e utiliza as seguintes bibliotecas:
* `pandas`: Manipulação e carga do dataset via URL.
* `numpy`: Operações matemáticas e geração de números aleatórios para divisão de dados.
* `math` e `operator`: Suporte à lógica do algoritmo e cálculos de distância.

### Fluxo de Trabalho:
1. **Pré-processamento**: Mapeamento das classes para valores numéricos e remoção de colunas irrelevantes (como IDs).
2. **Divisão dos Dados**: Os dados são divididos aleatoriamente em **70% para treino** (395 observações) e **30% para teste** (174 observações).
3. **Execução do KNN**: Aplicação da lógica de vizinhança para classificar as amostras de teste com base no conjunto de treino.

## 🚀 Como usar

1.  Clone este repositório.
2.  Instale as dependências:
    ```bash
    pip install pandas numpy
    ```
3.  Execute o notebook `KNN_Aprendizado_Supervisionado.ipynb` em um ambiente Jupyter ou no Google Colab.

---
*Este projeto foi baseado no material original de [akshayrb22/playing-with-data](https://github.com/akshayrb22/playing-with-data/blob/master/supervised_learning/KNN/KNN.ipynb).*