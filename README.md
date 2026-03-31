# Machine Learning Classification Lab

Laboratório prático de Machine Learning supervisionado com foco em classificação, pré-processamento de dados, comparação de modelos e análise de desempenho.

## Visão geral

Este repositório reúne experimentos práticos de classificação supervisionada em Python utilizando bases de dados reais. O objetivo é consolidar fundamentos de Machine Learning por meio da construção de fluxos completos que envolvem:

- análise exploratória
- tratamento de dados
- engenharia de atributos
- codificação de variáveis categóricas
- padronização
- treino de modelos
- avaliação comparativa

Mais do que um repositório de estudo, este projeto funciona como um laboratório técnico para desenvolver base sólida em modelagem preditiva.

## Objetivo do projeto

O foco principal é estudar como diferentes algoritmos de classificação se comportam diante de bases com características distintas, observando:

- qualidade dos dados
- impacto do pré-processamento
- diferença entre variáveis numéricas e categóricas
- comportamento de múltiplos classificadores
- importância da validação antes de escolher um modelo

## Bases de dados utilizadas

### 1. Risco de Crédito
Base voltada à previsão de inadimplência com variáveis como:

- idade
- renda
- valor da dívida

**Objetivo:** classificar se um cliente tende ou não a ser um bom pagador.

### 2. Censo Demográfico
Base com variáveis sociodemográficas numéricas e categóricas.

**Objetivo:** prever a faixa salarial do indivíduo a partir de características populacionais.

## O que é trabalhado no repositório

- limpeza de dados
- correção de inconsistências
- tratamento de valores ausentes
- transformação de atributos categóricos
- escalonamento de variáveis
- separação entre treino e teste
- treino de classificadores
- comparação de desempenho entre modelos

## Stack utilizada

- **Python**
- **Pandas**
- **NumPy**
- **Scikit-Learn**
- **Plotly**
- **Jupyter Notebook**

## Estrutura do repositório

```bash
estudo-machine-learning/
├── README.md
└── estudo/
    ├── Estudo ML e Data Science Python.ipynb
    ├── Machine Learning e Data Science (Classificação).ipynb
    ├── census.csv
    ├── census.pkl
    ├── credit_data.csv
    └── credit.pkl
