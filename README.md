# Estudo de Machine Learning e Data Science - Pipeline de Classificação

Este repositório documenta a implementação prática de um pipeline completo de Machine Learning com Python, com foco exclusivo em algoritmos de **Classificação** (Aprendizagem Supervisionada). O objetivo é cobrir todo o ciclo de vida dos dados, desde a análise exploratória até a validação cruzada de múltiplos modelos preditivos.

## Bases de Dados

O projeto utiliza duas bases de dados clássicas para validar a robustez e a flexibilidade das técnicas aplicadas:
1. **Risco de Crédito (`credit_data.csv`):** Previsão de inadimplência (pagador vs. não pagador) com base em variáveis contínuas: idade, renda e valor da dívida.
2. **Censo Demográfico (`census.csv`):** Previsão de faixa salarial (<=50K ou >50K) com base em 14 variáveis mistas (categóricas e numéricas) sociodemográficas.

## Stack Tecnológico e Ferramentas

Abaixo estão as ferramentas definidas para a construção deste pipeline, suas características e a justificativa arquitetural de uso:

* **Python 3:** Linguagem base do projeto.
* **Pandas & NumPy:** Manipulação e limpeza de matrizes de dados.
  * *Vantagem:* Altíssimo desempenho computacional para dados estruturados em memória.
  * *Desvantagem:* Gargalos de RAM em conjuntos de dados de ordem de Terabytes (não aplicável a este escopo).
  * *Preferência:* São o padrão-ouro e a melhor escolha para engenharia de dados em escopos acadêmicos e analíticos.
* **Scikit-Learn:** Core de Machine Learning e transformações matemáticas.
  * *Vantagem:* API unificada, o que permite trocar de algoritmo (ex: de Árvore para SVM) com alterações mínimas no código.
  * *Desvantagem:* Não é a ferramenta ideal para arquiteturas profundas de Deep Learning.
  * *Preferência:* A melhor ferramenta do mercado para algoritmos clássicos e rotinas de pré-processamento.
* **Plotly:** Visualização de dados.
  * *Vantagem:* Renderiza gráficos altamente interativos em navegadores, facilitando a análise de *outliers*.
  * *Desvantagem:* Arquivos HTML finais mais pesados que imagens estáticas.
  * *Preferência:* Superior ao Seaborn/Matplotlib para a fase de Análise Exploratória (EDA) por permitir zoom e inspeção visual de pontos de dados específicos.

## Estrutura do Pipeline Desenvolvido

O fluxo de trabalho está organizado nas seguintes etapas lógicas:

### 1. Pré-processamento e Engenharia de Dados
* Tratamento de inconsistências (ex: correção de idades negativas) e imputação de valores nulos (uso da média via Pandas).
* **Binarização de Variáveis Categóricas:** Uso do `LabelEncoder` seguido pelo `OneHotEncoder` integrado via `ColumnTransformer` para impedir a criação de hierarquias matemáticas falsas pelo modelo.
* **Padronização de Escala:** Implementação do `StandardScaler` para garantir que algoritmos baseados em distância avaliem todas as variáveis na mesma proporção.
* Separação rigorosa de matrizes de Treinamento e Teste (`train_test_split`).

### 2. Modelagem Algorítmica (Roadmap de Implementação)
O código estrutura o treinamento e avaliação conceitual dos seguintes classificadores:
- [ ] Naïve Bayes (Modelo probabilístico *baseline*)
- [ ] Árvores de Decisão & Random Forest (Modelos baseados em entropia)
- [ ] k-Nearest Neighbors (k-NN) (Modelo baseado em cálculo de distância)
- [ ] Regressão Logística
- [ ] Support Vector Machines (SVM)
- [ ] Redes Neurais Artificiais (MLPClassifier)

### 3. Validação e Métricas
* Avaliação de Acurácia e Matriz de Confusão.
* Implementação de Validação Cruzada (k-fold com 10 *splits*) para garantir a generalização do modelo e evitar *overfitting*.

## Como executar este projeto

1. Clone este repositório.
2. Ative seu ambiente virtual Python (`.venv`).
3. Instale as dependências executando:
   `pip install pandas numpy scikit-learn plotly yellowbrick`
4. Execute os notebooks sequencialmente pelo JupyterLab.
