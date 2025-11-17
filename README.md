# 📘 Análise Salarial com Python e Google Colab

## 📊 Sobre o Projeto
Este projeto apresenta uma análise exploratória e preditiva de um grande conjunto de dados salariais de profissionais de diferentes países, cargos, níveis educacionais, raças e gêneros.  

A análise foi desenvolvida em **Google Colab**, utilizando técnicas de **Ciência de Dados**, **Estatística**, **Visualização** e **Machine Learning**.

O objetivo é investigar padrões salariais, identificar fatores que influenciam a remuneração e avaliar modelos capazes de prever salários com base nas variáveis fornecidas.

---

## 📁 Conteúdo do Repositório
- `trabalho_final.ipynb` / `trabalho_final.py` — Notebook com todo o processo da análise.
- `Salary.csv` — Base de dados utilizada.
- `Relatorio final.pdf` — Relatório explicativo com análises e conclusões.
- Gráficos e visualizações gerados automaticamente ao executar o notebook.

---

## 🗂️ Sobre o Dataset

O dataset contém informações sobre:

| Variável | Descrição |
|---------|-----------|
| **Age** | Idade do profissional |
| **Gender** | Gênero |
| **Education Level** | Nível educacional (0 a 3) |
| **Job Title** | Cargo |
| **Years of Experience** | Anos de experiência |
| **Salary** | Salário anual em USD |
| **Country** | País |
| **Race** | Raça/etnia |
| **Senior** | Indica se o profissional é sênior |

O dataset não possui valores ausentes, permitindo análises estatísticas diretas.

---

## 🔍 Etapas da Análise

### ✔️ 1. Análise Exploratória (EDA)
A EDA inclui:
- Distribuições de idade, salário e experiência  
- Frequências de variáveis categóricas  
- Análise estrutural do dataset  
- Comparações de salário por:
  - Gênero  
  - Raça  
  - Cargo  
  - País  
  - Senioridade  

**Principais insights:**
- Salários apresentam distribuição assimétrica com outliers em cargos executivos.  
- Forte predominância masculina em posições sêniores.  
- Países como EUA, Reino Unido e Canadá têm maior diversidade.  

---

### ✔️ 2. Correlação e Inferência Estatística
- Matriz de correlação de Pearson mostra forte relação entre:
  - **Years of Experience → Salary**
  - **Education Level → Salary**
- Teste T indicou diferença salarial significativa entre gêneros.  
- ANOVA identificou impactos importantes de escolaridade e senioridade.

---

### ✔️ 3. Modelagem Preditiva

Modelos testados para prever salário:

| Modelo | MSE ↓ | R² ↑ | Observação |
|--------|--------|-------|------------|
| **Random Forest** | **86M** | **0.97** | Melhor desempenho |
| Decision Tree | 126M | 0.95 | Excelente, mas arriscado por overfitting |
| Gradient Boosting | 260M | 0.91 | Forte, porém inferior ao RF |
| Ridge / Lasso | ~485M | 0.83 | Regressão linear regularizada |
| Neural Network | 629M | 0.77 | Razoável |
| SVR | 2.7B | 0.00 | Ruim |

**Conclusão:**  
O modelo **Random Forest** apresentou o melhor desempenho para previsão salarial.

---

## 📈 Visualizações Produzidas

O notebook gera automaticamente:
- Histogramas de distribuição  
- Boxplots por gênero, raça e cargo  
- Gráficos de dispersão comparando idade × experiência × salário  
- Heatmap de correlação  
- Gráficos de pizza (raças, cargos)  
- Médias salariais por país, raça e cargo  
- Comparação das previsões dos modelos  

---

## 🧠 Tecnologias Utilizadas

| Área | Bibliotecas |
|-----|-------------|
| Manipulação de dados | `pandas`, `numpy` |
| Estatística | `scipy`, `pingouin` |
| Visualização | `matplotlib`, `seaborn`, `plotly` |
| Machine Learning | `scikit-learn`, `xgboost`, `catboost`, `tensorflow` |
| Ambiente | Google Colab |

---

## ▶️ Como Executar

### 1. Clonar o repositório
```bash
git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
```
### 2. Executar a instalação das dependencias
```bash
!pip install pandas numpy scipy scikit-learn matplotlib seaborn plotly tensorflow xgboost catboost pingouin
```