🍷 Classificando a Qualidade de Vinhos com Machine Learning
📌 Descrição do Projeto

Este projeto tem como objetivo desenvolver um modelo de classificação capaz de prever a qualidade de vinhos com base em suas características físico-químicas, utilizando o Wine Quality Dataset, disponível publicamente no Kaggle.

Tradicionalmente, a avaliação da qualidade de um vinho é realizada por especialistas por meio de análises sensoriais (aroma, sabor, acidez, equilíbrio), um processo que pode ser subjetivo e demorado. Com o uso de técnicas de ciência de dados e aprendizado de máquina, é possível apoiar enólogos e produtores na tomada de decisão, contribuindo para a padronização da qualidade do produto.

Para simplificar o problema, a variável de qualidade (nota de 0 a 10) foi transformada em uma classificação binária:

🟢 Alta Qualidade: nota ≥ 7
🔴 Baixa/Média Qualidade: nota < 7
🎯 Objetivo

Treinar e avaliar modelos de aprendizado de máquina capazes de prever a classificação de qualidade do vinho a partir de variáveis físico-químicas, além de identificar quais atributos mais influenciam essa qualidade.

📊 Sobre o Dataset

Fonte: Wine Quality Dataset - Kaggle

O conjunto de dados contém as seguintes variáveis:

Variável	Descrição
fixed acidity	Acidez fixa
volatile acidity	Acidez volátil
citric acid	Ácido cítrico
residual sugar	Açúcar residual
chlorides	Cloretos
free sulfur dioxide	Dióxido de enxofre livre
total sulfur dioxide	Dióxido de enxofre total
density	Densidade
pH	pH
sulphates	Sulfatos
alcohol	Teor alcoólico
quality	Qualidade do vinho (variável alvo)
🛠️ Pipeline do Projeto
Compreensão do Problema Interpretação do contexto, definição da variável alvo e transformação em classificação binária.
Análise Exploratória de Dados (EDA) Distribuição das variáveis, correlações, detecção de outliers/valores inconsistentes e análise do balanceamento das classes.
Pré-processamento de Dados Tratamento de dados faltantes, normalização/padronização de variáveis numéricas e criação de novas features.
Desenvolvimento de Modelos Treinamento de pelo menos dois modelos de classificação para comparação de desempenho.
Avaliação dos Modelos Avaliação com métricas adequadas (acurácia, precisão, recall, F1-score, AUC-ROC) e comparação entre os modelos testados.
Interpretação dos Resultados Identificação das variáveis mais relevantes para a qualidade do vinho e discussão de implicações para o processo produtivo.
📁 Estrutura do Repositório
wine-quality-classification/
│
├── data/              # Base de dados utilizada
├── notebooks/         # Notebook com a análise e modelagem
├── src/                # Scripts auxiliares (pré-processamento ou modelagem)
├── results/           # Gráficos e métricas dos modelos
├── requirements.txt   # Bibliotecas utilizadas
└── README.md          # Descrição do projeto
⚙️ Como Executar o Projeto
bash
# Clone o repositório
git clone https://github.com/seu-usuario/wine-quality-classification.git
cd wine-quality-classification

# Crie um ambiente virtual (opcional, mas recomendado)
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

# Instale as dependências
pip install -r requirements.txt

# Execute o notebook
jupyter notebook notebooks/
🤖 Modelos Utilizados
Modelo 1: (ex.: Logistic Regression)
Modelo 2: (ex.: Random Forest)

Atualize esta seção com os modelos efetivamente utilizados no projeto.

📈 Principais Resultados

(Resumo dos principais insights, métricas e variáveis mais relevantes obtidas durante a análise. Atualize após a conclusão da modelagem.)

📦 Entregáveis
✅ Repositório do GitHub com os códigos utilizados
✅ Apresentação executiva (storytelling da EDA) em PPT/PDF
✅ Vídeo executivo (até 5 minutos) com a apresentação dos resultados
