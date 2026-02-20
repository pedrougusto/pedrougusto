# 👋 Hi, I'm Pedro Augusto!

### 📊 Analytics Engineer | BigQuery · Power BI · Python · GCP

I build end-to-end data pipelines and analytical models that turn raw data into business intelligence. My focus is on **scalable architectures in GCP**, **advanced analytical modeling**, and **dashboards that drive decisions**.

Currently working on customer lifecycle analysis, marketing attribution pipelines, and BigQuery automation.

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technologies |
|---|---|
| **Cloud & Warehouse** | ![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat&logo=googlecloud&logoColor=white) ![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?style=flat&logo=googlebigquery&logoColor=white) |
| **Transformation** | ![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat&logo=dbt&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-003B57?style=flat&logo=sqlite&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) |
| **Visualization** | ![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black) ![Looker](https://img.shields.io/badge/Looker-4285F4?style=flat&logo=looker&logoColor=white) |
| **Streaming** | ![Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat&logo=apachekafka&logoColor=white) |
| **Orchestration** | ![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white) |

</div>

---

## 🚀 Featured Projects

### 🛒 [VitaShop — Customer Lifecycle Analytics](https://github.com/YOUR_USERNAME/vitashop-customer-lifecycle)
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

---

## 💡 What drives me

I enjoy projects where data engineering and analytics meet — not just moving data, but **modeling it so the business can answer questions that were previously impossible**.

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

### 📊 Analytics Engineer | BigQuery · Power BI · Python · GCP

Construo pipelines de dados e modelos analíticos que transformam dados brutos em inteligência de negócio. Meu foco está em **arquiteturas escaláveis no GCP**, **modelagem analítica avançada** e **dashboards que geram decisão**.

Atualmente trabalhando com análise de ciclo de vida de clientes, atribuição de marketing e automação de pipelines em BigQuery.

---

## 🛠️ Stack

<div align="center">

| Camada | Tecnologias |
|---|---|
| **Cloud & Warehouse** | ![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat&logo=googlecloud&logoColor=white) ![BigQuery](https://img.shields.io/badge/BigQuery-669DF6?style=flat&logo=googlebigquery&logoColor=white) |
| **Transformação** | ![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat&logo=dbt&logoColor=white) ![SQL](https://img.shields.io/badge/SQL-003B57?style=flat&logo=sqlite&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white) |
| **Visualização** | ![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black) ![Looker](https://img.shields.io/badge/Looker-4285F4?style=flat&logo=looker&logoColor=white) |
| **Streaming** | ![Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat&logo=apachekafka&logoColor=white) |
| **Orquestração** | ![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white) |

</div>

---

## 🚀 Projetos em Destaque

### 🛒 [VitaShop — Customer Lifecycle Analytics](https://github.com/YOUR_USERNAME/vitashop-customer-lifecycle)
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

---

## 💡 O que me motiva

Gosto de projetos onde a engenharia de dados e a análise se encontram — não só mover dados, mas **modelar de forma que o negócio consiga responder perguntas que antes eram impossíveis**.

---

## 📬 Contatos

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/pedro-augusto-camargo-de-oliveira)
[![Email](https://img.shields.io/badge/Hotmail-0078D4?style=for-the-badge&logo=microsoftoutlook&logoColor=white)](mailto:pedro_augusto95@hotmail.com)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/5515997584451)

</div>
