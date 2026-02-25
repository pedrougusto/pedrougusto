# 👋 Hi, I'm Pedro Augusto!

### 📊 Data Analytics | Data Science | ML & Advanced Analytics | Data-Driven Growth | AI, ETL, Statistics, Python, SQL, GCP, Power BI

I build end-to-end data pipelines and analytical models that turn raw data into business intelligence. My focus is on **scalable architectures in GCP**, **advanced analytical modeling**, and **dashboards that drive decisions**.

Currently working on customer lifecycle analysis, marketing attribution pipelines, and BigQuery automation.

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technologies |
|---|---|
| **Cloud & Warehouse** | ![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat&logo=googlecloud&logoColor=white) ![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?style=flat&logo=googlebigquery&logoColor=white) ![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat&logo=snowflake&logoColor=white) |
| **GCP Services** | ![Dataform](https://img.shields.io/badge/Dataform-4285F4?style=flat&logo=googlecloud&logoColor=white) ![Data%20Transfer](https://img.shields.io/badge/Data%20Transfer-4285F4?style=flat&logo=googlecloud&logoColor=white) |
| **Transformation & Processing** | ![SQL](https://img.shields.io/badge/SQL-003B57?style=flat&logo=sqlite&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) ![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat&logo=apachespark&logoColor=white) |
| **Data Science & ML** | ![Machine Learning](https://img.shields.io/badge/Machine%20Learning-FF6F00?style=flat&logo=tensorflow&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white) |
| **Generative AI** | ![GenAI](https://img.shields.io/badge/Generative%20AI-8E44AD?style=flat&logo=openai&logoColor=white) ![LLM](https://img.shields.io/badge/LLM-412991?style=flat&logo=openai&logoColor=white) |
| **Visualization** | ![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black) ![Looker](https://img.shields.io/badge/Looker-4285F4?style=flat&logo=looker&logoColor=white) |

</div>

---

## 🚀 Featured Projects

### 🛒 [VitaShop — Customer Lifecycle Analytics](https://github.com/pedrougusto/vitashop-customer-lifecycle)
> End-to-end BigQuery pipeline for multi-dimensional customer lifecycle classification using a 24-month rolling window.

- Procedural SQL with `WHILE` loop for month-by-month historical backfill
- 5-state classification: **new · recurring · inactive · churned · recovered**
- Independent labels per brand, payment method, product type and fulfillment modality
- Window functions with `COUNT DISTINCT CASE WHEN` across multiple partitions
- GA4 last-touch channel attribution with `QUALIFY ROW_NUMBER()` deduplication
- Partitioned output table ready for Power BI / Looker consumption

```sql
-- Lifecycle state classification logic
CASE
  WHEN total_hist = 0 AND total_roll = 0 AND total_curr > 0 THEN 'new'
  WHEN total_hist > 0 AND total_roll = 0 AND total_curr = 0 THEN 'churned'
  WHEN total_hist > 0 AND total_roll = 0 AND total_curr > 0 THEN 'recovered'
  WHEN (total_roll + total_curr) >= 2                       THEN 'recurring'
  WHEN total_roll = 1     AND total_curr = 0                THEN 'inactive'
END AS lifecycle_state
```

### 🐉 [Dragon Ball GenAI — LLM with Custom Knowledge Base](https://github.com/pedrougusto/bootcamp-genAI-LLM-dragonball)
> Bootcamp project: domain-specific LLM assistant grounded on Dragon Ball lore using Google NotebookLM.

- Custom knowledge base built from Dragon Ball story, characters and sagas
- Prompt engineering to reduce hallucination and keep responses canon-accurate
- Practical application of GenAI tools to domain-specific Q&A

---

## 💡 What drives me

I enjoy projects where data engineering and analytics meet — not just moving data, but **modeling it so the business can answer questions that were previously impossible**. I'm especially interested in:

- Retention and churn models for e-commerce and healthcare
- Multi-touch marketing attribution with GA4 data
- Applying **Generative AI and LLMs** to real-world data problems
- Data architectures that scale without exploding costs

---

## 📬 Get in touch

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pedro-augusto-camargo-de-oliveira)
[![Email](https://img.shields.io/badge/Hotmail-0078D4?style=for-the-badge&logo=microsoftoutlook&logoColor=white)](mailto:pedro_augusto95@hotmail.com)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/5515997584451)

</div>

---
---

# 👋 Olá! Eu sou o Pedro Augusto!

### 📊 Data Analytics | Data Science | ML & Advanced Analytics | Data-Driven Growth | IA, ETL, Estatística, Python, SQL, GCP, Power BI

Construo pipelines de dados e modelos analíticos que transformam dados brutos em inteligência de negócio. Meu foco está em **arquiteturas escaláveis no GCP**, **modelagem analítica avançada** e **dashboards que geram decisão**.

Atualmente trabalhando com análise de ciclo de vida de clientes, atribuição de marketing e automação de pipelines em BigQuery.

---

## 🛠️ Stack

<div align="center">

| Camada | Tecnologias |
|---|---|
| **Cloud & Warehouse** | ![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat&logo=googlecloud&logoColor=white) ![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?style=flat&logo=googlebigquery&logoColor=white) ![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat&logo=snowflake&logoColor=white) |
| **Serviços GCP** | ![Dataform](https://img.shields.io/badge/Dataform-4285F4?style=flat&logo=googlecloud&logoColor=white) ![Data%20Transfer](https://img.shields.io/badge/Data%20Transfer-4285F4?style=flat&logo=googlecloud&logoColor=white) |
| **Transformação & Processamento** | ![SQL](https://img.shields.io/badge/SQL-003B57?style=flat&logo=sqlite&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) ![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=flat&logo=apachespark&logoColor=white) |
| **Data Science & ML** | ![Machine Learning](https://img.shields.io/badge/Machine%20Learning-FF6F00?style=flat&logo=tensorflow&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white) ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white) |
| **IA Generativa** | ![GenAI](https://img.shields.io/badge/Generative%20AI-8E44AD?style=flat&logo=openai&logoColor=white) ![LLM](https://img.shields.io/badge/LLM-412991?style=flat&logo=openai&logoColor=white) |
| **Visualização** | ![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black) ![Looker](https://img.shields.io/badge/Looker-4285F4?style=flat&logo=looker&logoColor=white) |

</div>

---

## 🚀 Projetos em Destaque

### 🛒 [VitaShop — Customer Lifecycle Analytics](https://github.com/pedrougusto/vitashop-customer-lifecycle)
> Pipeline completo em BigQuery para classificação de ciclo de vida de clientes com janela temporal deslizante de 24 meses.

- Procedural SQL com loop `WHILE` para backfill histórico mês a mês
- Classificação em 5 estados: **novo · recorrente · inativo · churn · recuperado**
- Labels independentes por marca, pagamento, tipo de produto e modalidade de entrega
- Window functions com `COUNT DISTINCT CASE WHEN` particionadas por múltiplas dimensões
- Atribuição de canal GA4 com deduplicação por `QUALIFY ROW_NUMBER()`
- Tabela final particionada, pronta para consumo em Power BI / Looker

```sql
-- Lógica de classificação do ciclo de vida
CASE
  WHEN total_hist = 0 AND total_roll = 0 AND total_curr > 0 THEN 'novo'
  WHEN total_hist > 0 AND total_roll = 0 AND total_curr = 0 THEN 'churn'
  WHEN total_hist > 0 AND total_roll = 0 AND total_curr > 0 THEN 'recuperado'
  WHEN (total_roll + total_curr) >= 2                       THEN 'recorrente'
  WHEN total_roll = 1     AND total_curr = 0                THEN 'inativo'
END AS lifecycle_state
```

### 🐉 [Dragon Ball GenAI — LLM com Base de Conhecimento Customizada](https://github.com/pedrougusto/bootcamp-genAI-LLM-dragonball)
> Projeto de Bootcamp: assistente LLM especializado no universo Dragon Ball usando Google NotebookLM.

- Base de conhecimento customizada com história, personagens e sagas do Dragon Ball
- Engenharia de prompt para reduzir alucinações e manter respostas fiéis ao cânone
- Aplicação prática de ferramentas de GenAI para Q&A de domínio específico

---

## 💡 O que me motiva

Gosto de projetos onde a engenharia de dados e a análise se encontram — não só mover dados, mas **modelar de forma que o negócio consiga responder perguntas que antes eram impossíveis**. Tenho especial interesse em:

- Modelos de retenção e churn para e-commerce e saúde
- Atribuição de marketing multi-touch com dados do GA4
- Aplicação de **IA Generativa e LLMs** a problemas reais de dados
- Arquiteturas de dados que escalam sem explodir o custo

---

## 📬 Contatos

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pedro-augusto-camargo-de-oliveira)
[![Email](https://img.shields.io/badge/Hotmail-0078D4?style=for-the-badge&logo=microsoftoutlook&logoColor=white)](mailto:pedro_augusto95@hotmail.com)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/5515997584451)

</div>
