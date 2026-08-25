# Classificação da Qualidade de Vinhos com Machine Learning

**Tech Challenge — Fase 2 — Pós-Graduação em Data Analytics — FIAP/POSTECH**

## 📋 Descrição do projeto

Este projeto desenvolve um pipeline de análise e modelagem para prever se um vinho é de **alta qualidade** (nota ≥ 7) ou **baixa/média qualidade** (nota < 7) a partir de suas características físico-químicas, utilizando o [Wine Quality Dataset](https://www.kaggle.com/datasets) (variante tinto, `WineQT.csv`).

O objetivo é apoiar enólogos e produtores na tomada de decisão durante o processo produtivo, substituindo parte da avaliação sensorial subjetiva por um modelo preditivo baseado em dados.

## ❓ Perguntas de negócio

1. É possível prever a qualidade de um vinho a partir de suas características físico-químicas, sem depender exclusivamente da avaliação sensorial de especialistas?
2. Quais variáveis físico-químicas mais influenciam a qualidade final do vinho, e o que isso implica para o processo de produção?

## 🗂️ Estrutura do repositório

```
wine-quality-classification/
│
├── data/                # Base de dados utilizada (WineQT.csv)
├── notebooks/           # Notebook com a análise e modelagem (wine_notebook.ipynb)
├── src/                 # Scripts auxiliares (pré-processamento ou modelagem)
├── results/             # Gráficos e métricas dos modelos
├── requirements.txt     # Bibliotecas utilizadas
└── README.md            # Este arquivo
```

## 🔍 Metodologia

O pipeline segue 6 etapas:

1. **Compreensão do problema** — transformação da variável `quality` (0-10) em classificação binária `high_quality`.
2. **Análise Exploratória de Dados (EDA)** — distribuição das variáveis, correlações, outliers e balanceamento de classes.
3. **Pré-processamento** — padronização de variáveis numéricas e feature engineering (razão SO₂ livre/total).
4. **Desenvolvimento de modelos** — Regressão Logística e Random Forest, com `class_weight="balanced"` para lidar com o desbalanceamento de classes (~14% de vinhos "alta qualidade").
5. **Avaliação** — acurácia, precisão, recall, F1-score, AUC-ROC, matriz de confusão e curva ROC.
6. **Interpretação** — importância de variáveis e implicações para o processo produtivo.

## 📊 Principais resultados

| Métrica | Regressão Logística | Random Forest |
|---|---|---|
| Acurácia | 0,79 | 0,93 |
| Precisão | 0,36 | 1,00 |
| Recall | 0,66 | 0,50 |
| F1-score | 0,47 | 0,67 |
| AUC-ROC | 0,86 | 0,92 |

**Variáveis mais relevantes:** `alcohol` (teor alcoólico), `sulphates`, `citric acid` e `volatile acidity` (acidez volátil), nessa ordem de importância no Random Forest.

Detalhes completos da análise estão disponíveis no notebook: [`notebooks/wine_notebook.ipynb`](notebooks/wine_notebook.ipynb).

## ⚙️ Como reproduzir

```bash
# Clonar o repositório
git clone <url-do-repositorio>
cd wine-quality-classification

# Criar ambiente virtual (opcional, recomendado)
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Instalar dependências
pip install -r requirements.txt

# Rodar o notebook
jupyter notebook notebooks/wine_notebook.ipynb
```

## 🛠️ Ferramentas utilizadas

- **Python** (pandas, numpy, scikit-learn, matplotlib, seaborn)
- **Jupyter Notebook**
- **GitHub** (versionamento e entrega)

## 📦 Entregáveis

- [x] Repositório GitHub com os códigos utilizados
- [ ] Apresentação executiva (storytelling da EDA) — `results/apresentacao_executiva.pdf`
- [ ] Vídeo executivo (até 5 minutos)

## 👥 Autores

- Nome do integrante — RM XXXXXX
- Nome do integrante — RM XXXXXX

## 📚 Fonte dos dados

Wine Quality Dataset — Kaggle (variante tinto, 1.143 amostras, 11 variáveis físico-químicas).
