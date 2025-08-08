# Projeto Telecom X - Parte 2: Previsão de Churn de Clientes

## Propósito do Projeto

Este projeto tem como objetivo principal **prever o churn (evasão) de clientes** de uma empresa de telecomunicações, utilizando um conjunto de variáveis relevantes extraídas dos dados de clientes. A análise busca identificar os fatores que mais influenciam a decisão dos clientes em cancelar o serviço, permitindo à empresa desenvolver estratégias para retenção.

---

## Estrutura do Projeto

- `TelecomX_Churn_Prediction.ipynb` - Notebook principal com todo o fluxo de análise, preparação dos dados, modelagem e avaliação.
- `dados_tratados.csv` - Arquivo CSV contendo os dados já tratados e preparados para modelagem.
- `/visualizacoes/` - Pasta contendo gráficos gerados durante a análise exploratória e visualizações dos resultados.

---

## Processo de Preparação dos Dados

### Classificação das Variáveis

- **Variáveis Categóricas**: Representam características qualitativas, como tipo de contrato, método de pagamento, presença de dependentes, etc.
- **Variáveis Numéricas**: Valores quantitativos, como tempo de contrato, valor mensal pago, número de serviços contratados, entre outros.

### Etapas de Tratamento

- **Codificação**: As variáveis categóricas foram transformadas em variáveis numéricas usando técnicas como `One-Hot Encoding` para que os modelos pudessem interpretá-las corretamente.
- **Normalização**: As variáveis numéricas foram normalizadas para uma escala comum, garantindo que os modelos não fossem influenciados por diferenças de magnitude entre variáveis.

### Separação dos Dados

- Os dados foram divididos em conjuntos de **treinamento** e **teste** para garantir uma avaliação justa da capacidade preditiva dos modelos. A divisão padrão utilizada foi 70% para treino e 30% para teste.

---

## Justificativas das Escolhas na Modelagem

- A codificação das variáveis categóricas via `One-Hot Encoding` foi escolhida por ser uma técnica robusta que evita que modelos interpretem categorias como valores ordinais.
- A normalização das variáveis numéricas é fundamental para modelos sensíveis à escala, como regressão logística e SVM.
- A divisão dos dados em treino e teste garante que o modelo seja avaliado em dados nunca vistos, evitando overfitting.
- Foram testados múltiplos modelos de classificação para encontrar o que melhor se adequa ao problema e à distribuição dos dados.

---

## Insights e Visualizações da Análise Exploratória (EDA)

Durante a análise exploratória, foram gerados gráficos que evidenciam:

- Distribuição dos clientes por tempo de contrato e valor pago mensalmente.
- Taxa de churn relacionada ao tipo de serviço contratado.
- Correlações entre variáveis numéricas e a variável target (churn).
- Gráficos de barras mostrando as categorias com maior índice de evasão.

Essas visualizações permitiram identificar quais fatores são mais críticos para o churn e direcionar a modelagem para eles.

---

## Como Executar o Notebook

### Requisitos

As seguintes bibliotecas Python são necessárias para rodar o notebook:

- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn


