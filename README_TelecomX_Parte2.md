#  Telecom X - Predição de Evasão de Clientes (Parte 2)

## Objetivo
Desenvolver modelos preditivos capazes de prever quais clientes têm maior chance de cancelar seus serviços na Telecom X, utilizando técnicas de Machine Learning.

---

##  Etapas Realizadas

### 1. Pré-processamento dos Dados
- Remoção de colunas irrelevantes (ex: identificadores únicos).
- Transformação de variáveis categóricas em numéricas (One-Hot Encoding).
- Avaliação de balanceamento da variável alvo (churn).
- Aplicação de **SMOTE** para balanceamento em caso de desequilíbrio.

### 2. Análise de Correlação
- Geração de matriz de correlação para identificar variáveis mais relacionadas ao churn.
- Gráficos exploratórios:
  - Tempo de contrato × Evasão
  - Total gasto × Evasão

### 3. Divisão dos Dados
- Separação em treino (70%) e teste (30%).

### 4. Modelagem
Foram treinados dois tipos de modelos:
1. **Regressão Logística** (com normalização) – bom para interpretar coeficientes.
2. **Random Forest** (sem normalização) – bom para capturar não-linearidades.

### 5. Avaliação
Métricas utilizadas:
- Acurácia
- Precisão
- Recall
- F1-Score
- Matriz de Confusão

---

## Resultados Comparativos

- A **Random Forest** apresentou melhor desempenho geral, com maior recall e f1-score.
- A **Regressão Logística** mostrou bom equilíbrio e interpretabilidade.
- O dataset apresentava certo desequilíbrio de classes, corrigido com oversampling.

---

## Principais Fatores de Evasão

- **Tempo de contrato**: clientes com contratos mensais apresentaram maior evasão.
- **Total gasto**: valores mais baixos estavam associados à maior evasão.
- **Serviços adicionais**: ausência de serviços extras estava correlacionada a maior churn.
- **Tipo de pa**
