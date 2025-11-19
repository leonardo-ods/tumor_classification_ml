# 🎗️ Classificação de Tumores com Machine Learning: Detecção de Câncer de Mama

Este projeto consiste na implementação e avaliação comparativa de dois modelos de Machine Learning: **Random Forest** e **Support Vector Classifier (SVC)**, para a classificação de tumores (Malignos ou Benignos).

Utilizando um subconjunto do dataset **Breast Cancer Wisconsin**, o estudo foca na seleção estratégica de características, no impacto do pré-processamento dos dados e na análise detalhada das métricas de desempenho.

## 📊 Dataset e Features Selecionadas

A seleção de características foi guiada por uma Análise Exploratória de Dados (EDA). Utilizamos *pairplots* e *heatmaps* de correlação para identificar as variáveis com maior poder de discriminação entre as classes.

As **4 características principais** utilizadas foram:
1. `mean radius`
2. `mean texture`
3. `mean perimeter`
4. `mean area`

## ⚙️ Metodologia

O pipeline do projeto seguiu as seguintes etapas:

1.  **Seleção de Características:** Filtragem das variáveis mais correlacionadas com a variável alvo (`class`).
2.  **Divisão dos Dados:** Separação em conjuntos de Treino e Teste.
3.  **Normalização (StandardScaler):**
    *   Etapa crucial, especialmente para o SVC (que é baseado em distâncias).
    *   Garante que todas as features contribuam equitativamente, evitando viés por escala.
4.  **Treinamento:** Ajuste dos modelos `RandomForestClassifier` e `SVC` (Kernel Linear).
5.  **Avaliação:** Comparação baseada em Acurácia e Matriz de Confusão.

## 📈 Resultados

Ambos os modelos apresentaram desempenho robusto, mas houve uma vantagem para Random Forest.

| Modelo | Acurácia | Análise |
| :--- | :---: | :--- |
| **Random Forest** | **93.7%** | Apresentou o melhor equilíbrio, minimizando falsos positivos e negativos. |
| **SVC (Linear)** | 90.9% | Bom poder preditivo, mas ligeiramente inferior ao RF neste cenário específico. |

### 🧠 Insights

A análise das matrizes de confusão indicou que o **Random Forest** foi mais eficaz em capturar as nuances dos dados com as features selecionadas. A acurácia superior sugere que a estrutura de árvores de decisão lidou melhor com a separação das classes em comparação ao hiperplano linear do SVC neste contexto.

## 🚀 Abra o notebook completo no Colab:

[https://colab.research.google.com/drive/1G58d8Je1_QEaQ7tcmwYzhyR7BiF5EsHH?usp=sharing](https://colab.research.google.com/drive/1G58d8Je1_QEaQ7tcmwYzhyR7BiF5EsHH?usp=sharing)

## 🛠️ Tecnologias Utilizadas

**Linguagem:** Python

**Manipulação de Dados:** Pandas

**Visualização:** Matplotlib, Seaborn

**Machine Learning:** Scikit-learn

## 📝 Conclusão

O estudo concluiu que o Random Forest foi o modelo mais eficaz para este problema de classificação com as características selecionadas. O projeto ressalta a importância da seleção de features e da normalização (StandardScaler) para otimizar modelos baseados em distância e garantir comparações justas.
