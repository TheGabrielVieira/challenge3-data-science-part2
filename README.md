# 🔍 Previsão de Evasão de Clientes com Modelos Preditivos

Este projeto tem como objetivo analisar e prever a **evasão de clientes** (churn) com base em dados reais de uma empresa de telecomunicações. Através de técnicas de ciência de dados e aprendizado de máquina, buscamos identificar os fatores mais relevantes para a evasão e propor **estratégias de retenção**.

---

## 🚀 Tecnologias Utilizadas

- **Linguagem**: Python 3.x
- **Bibliotecas principais**:
  - `pandas`, `numpy` – Manipulação e análise de dados
  - `matplotlib`, `seaborn`, `plotly` – Visualização gráfica
  - `scikit-learn` – Modelagem preditiva e avaliação
  - `imbalanced-learn` – Balanceamento de dados com SMOTE
  - `joblib` – Serialização de modelos
- **Ambiente**: Jupyter Notebook / Google Colab

---

## ⚙️ Como Executar na Sua Máquina

### 1. Clone o repositório:

```bash
git clone https://github.com/TheGabrielVieira/challenge3-data-science-part-3.git
cd challenge3-data-science-part-3
```

### 2. Instale as dependências:

Crie um ambiente virtual (opcional):

```bash
python -m venv venv
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
```

Instale os pacotes:

```bash
pip install -r requirements.txt
```

### 3. Execute o notebook:

Abra o Jupyter Notebook ou Google Colab e siga as células para reproduzir a análise.

---

## 📁 Etapas do Projeto

### 🔍 1. Análise Exploratória de Dados (EDA)
- Carregamento da base de dados `telecomx_data_gold.csv`
- Limpeza e tratamento de dados ausentes
- Visualizações: histogramas, boxplots, scatterplots
- Cálculo de correlação entre variáveis

### ⚖️ 2. Balanceamento de Dados
- Aplicação da técnica **SMOTE** para equilibrar as classes alvo (clientes que evadiram vs. não evadiram)

### 🧠 3. Seleção de Variáveis
- Seleção baseada em correlação e no método `SelectKBest`
- Avaliação de multicolinearidade com VIF

### 🤖 4. Modelagem Preditiva
- Separação dos dados em treino e teste (80/20)
- Modelos aplicados:
  - **K-Nearest Neighbors (KNN)** – com dados normalizados
  - **Random Forest Classifier** – sem necessidade de normalização
- Avaliação dos modelos com:
  - Acurácia
  - Precisão, Recall, F1-score
  - Matriz de Confusão
  - AUC ROC

### ⭐ 5. Análise da Importância das Variáveis
- Avaliação dos atributos mais relevantes via Random Forest e SelectKBest
- Comparativo visual das importâncias

### 📊 6. Relatório Final — Análise da Evasão de Clientes

---

## 📝 Relatório Final — Análise da Evasão de Clientes

### 🎯 Objetivo
Analisar os principais fatores que influenciam a evasão de clientes e propor estratégias de retenção com base nos dados e na modelagem preditiva.

### 🧪 Modelos Utilizados

- **KNN**: Requer normalização. Aplicado com `StandardScaler`.
- **Random Forest**: Robusto e interpretável, não exige normalização.

### 📈 Comparativo de Desempenho

| Métrica       | KNN     | Random Forest |
|---------------|---------|----------------|
| Acurácia      | 0.80    | 0.85           |
| F1-score (1)  | 0.82    | 0.85           |
| Recall (1)    | 0.92    | 0.87           |
| AUC           | 0.80    | 0.85           |

✅ **Conclusão**: O modelo Random Forest apresentou desempenho superior, sendo o mais indicado para uso em produção.

---

### 🔍 Principais Fatores de Evasão

Identificados com base nos modelos e análise de importância:

- **Tempo de Contrato (Tenure)**
- **Total Gasto**
- **Tipo de Contrato**
- **Serviços adicionais**
- **Suporte Técnico / Atendimento**

---

### 💡 Estratégias de Retenção Recomendadas

1. **Campanhas de fidelização antecipadas**
2. **Descontos para clientes com alto gasto**
3. **Incentivo a contratos longos**
4. **Oferecer serviços adicionais gratuitos no início**
5. **Sistema de alertas baseado no modelo**

---

## 👨‍💻 Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

---

## 🛡️ Licença

Este projeto está licenciado sob a **MIT License**.

---

## 📬 Contato

- Desenvolvido por Gabriel Vieira  
- GitHub: [https://github.com/TheGabrielVieira](https://github.com/TheGabrielVieira)