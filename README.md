# 💳 Detector de Anomalias em Transações Financeiras

## 📌 Visão Geral

Este projeto tem como objetivo identificar transações financeiras suspeitas (fraudes) utilizando técnicas de ciência de dados e aprendizado de máquina. O modelo é treinado com um conjunto de dados real de transações de cartão de crédito, onde a grande maioria das operações é legítima e apenas uma pequena fração representa fraude — caracterizando um problema clássico de **dados desbalanceados**.

---

## 🎯 Objetivos

* Detectar transações fraudulentas com alta precisão
* Minimizar falsos positivos (transações legítimas classificadas como fraude)
* Trabalhar com dados altamente desbalanceados
* Aplicar pré-processamento e engenharia de atributos

---

## 🧠 Tecnologias Utilizadas

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib / Seaborn (para visualização, se aplicável)

---

## 📊 Dataset

O conjunto de dados utilizado está disponível publicamente e contém transações de cartões de crédito realizadas por usuários europeus.

🔗 Fonte: [https://storage.googleapis.com/download.tensorflow.org/data/creditcard.csv](https://storage.googleapis.com/download.tensorflow.org/data/creditcard.csv)

### Características do dataset:

* Total de transações: ~284.000
* Fraudes: ~0.17% dos dados
* Features anonimizadas (V1, V2, ..., V28)
* Colunas principais:

  * `Time`: tempo da transação
  * `Amount`: valor da transação
  * `Class`: variável alvo (0 = normal, 1 = fraude)

---

## ⚙️ Etapas do Projeto

### 1. 📥 Carregamento dos Dados

* Leitura do dataset diretamente via URL
* Visualização inicial com `head()`

### 2. 🔍 Análise Exploratória

* Verificação do balanceamento das classes
* Identificação da proporção de fraudes

### 3. 🧹 Pré-processamento

* Transformação logarítmica da variável `Amount` (`log1p`)
* Possível normalização dos dados

### 4. 🏗️ Modelagem

* Aplicação de algoritmos de machine learning
* Foco em modelos adequados para detecção de anomalias

### 5. 📈 Avaliação

* Métricas utilizadas:

  * Precisão
  * Recall
  * F1-score
  * Matriz de confusão

---

## ⚠️ Desafios do Projeto

* Dados extremamente desbalanceados
* Necessidade de métricas adequadas (accuracy não é suficiente)
* Identificação de padrões sutis de fraude

---

## 🚀 Possíveis Melhorias

* Aplicar técnicas de balanceamento (SMOTE, undersampling)
* Testar algoritmos como:

  * Isolation Forest
  * One-Class SVM
  * Redes neurais
* Deploy do modelo em API (Flask/FastAPI)
* Criação de dashboard interativo

---

## 📂 Estrutura do Projeto

```
📁 projeto
 ┣ 📄 Detector_de_Anomalias_em_Transações.ipynb
 ┗ 📄 README.md
```

---

## 🧪 Como Executar

1. Clone este repositório

```bash
git clone <url-do-repositorio>
```

2. Instale as dependências

```bash
pip install pandas numpy scikit-learn matplotlib
```

3. Execute o notebook

```bash
jupyter notebook
```

---

## 🤝 Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

---

## 📌 Considerações Finais

Este projeto é uma excelente aplicação prática de machine learning em um problema real do mercado financeiro, demonstrando como técnicas de análise de dados podem ajudar na prevenção de fraudes.
