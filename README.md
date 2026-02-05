# 📊 Projeto Unsupervised Learning aplicado a Dados Epidemiológicos (COVID-19)

Este repositório contém um **notebook de aprendizado de máquina não supervisionado** do projeto de final de disciplina cujo objetivo é identificar **padrões latentes e perfis epidemiológicos** entre municípios brasileiros a partir de dados relacionados à COVID-19.

O projeto utiliza técnicas modernas de **redução de dimensionalidade** e **clusterização**, com foco em **interpretação**, **visualização** e **comparação entre métodos**.

---

## 🧠 Objetivo do Projeto

O principal objetivo é investigar se municípios brasileiros podem ser agrupados de acordo com **semelhanças no comportamento epidemiológico**, considerando múltiplas variáveis simultaneamente, **sem o uso de rótulos prévios**.

Especificamente, o projeto busca:

- Identificar **padrões naturais** nos dados;
- Reduzir a complexidade de dados de alta dimensionalidade;
- Comparar algoritmos de clusterização não supervisionados;
- Avaliar a qualidade e interpretabilidade dos agrupamentos obtidos.

---

## 📁 Estrutura do Projeto

├── main.ipynb # Notebook principal com toda a análise
├── README.md # Descrição do projeto


Todo o pipeline de análise está concentrado no notebook.

---

## 🗂️ Conjunto de Dados

Os dados utilizados são derivados de informações públicas sobre a COVID-19 no Brasil, agregadas por **município**.

Após o pré-processamento, o conjunto final contém **variáveis numéricas** que descrevem o comportamento da pandemia ao longo do tempo, tais como:

- Estatísticas de casos e óbitos (máximo, média, desvio padrão);
- Taxas derivadas (ex.: taxa de mortalidade);
- Métricas temporais e de crescimento;
- Codificação categórica (ex.: estados).

O resultado é um dataset **multivariado e de alta dimensionalidade**, adequado para análise exploratória e clusterização.

---

## ⚙️ Metodologia

O notebook segue as seguintes etapas:

### 1️⃣ Pré-processamento
- Limpeza dos dados;
- Seleção e engenharia de atributos;
- Padronização das variáveis numéricas.

### 2️⃣ Redução de Dimensionalidade

Foram avaliadas duas técnicas não lineares:

- **t-SNE**
  - Utilizado principalmente para **visualização exploratória**;
  - Preserva relações locais entre os dados.

- **UMAP**
  - Preserva estrutura local e global;
  - Apresenta maior estabilidade;
  - Utilizado como base para a clusterização.

### 3️⃣ Clusterização

Foram comparados dois algoritmos:

- **K-Means**
  - Aplicado sobre o espaço reduzido pelo UMAP;
  - Número de clusters definido com base em análise visual e métricas internas.

- **DBSCAN**
  - Baseado em densidade;
  - Não requer definição prévia do número de clusters;
  - Avaliado quanto à capacidade de identificar padrões e ruído.

---

## 📈 Principais Resultados

- A redução de dimensionalidade mostrou-se essencial para revelar **estruturas latentes** nos dados.
- O **UMAP** produziu um espaço latente mais adequado para clusterização do que o t-SNE.
- A combinação **UMAP + K-Means** apresentou:
  - Melhor separação entre clusters;
  - Maior estabilidade;
  - Agrupamentos mais interpretáveis.
- O **DBSCAN** apresentou limitações relacionadas à sensibilidade aos parâmetros e à variação de densidade dos dados.

---

## 🧪 Tecnologias e Bibliotecas Utilizadas

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Seaborn  
- UMAP-learn  

---
🚀 Possíveis Extensões
- Avaliação quantitativa com métricas internas (Silhouette, Davies–Bouldin);
- Análise semântica detalhada de cada cluster;
- Comparação com métodos hierárquicos;
- Aplicação da abordagem a outros contextos ou períodos.

