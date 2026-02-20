# 👋 Olá! Eu sou o Wallace Goulart

### 📊 Analytics Engineer | Data Engineer | BigQuery · Power BI · Python

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
| **Streaming** | ![Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat&logo=apachekafka&logoColor=white) ![Flink](https://img.shields.io/badge/Apache%20Flink-E6526F?style=flat&logo=apacheflink&logoColor=white) |
| **Orquestração** | ![Airflow](https://img.shields.io/badge/Airflow-017CEE?style=flat&logo=apacheairflow&logoColor=white) |

</div>

---

## 🚀 Projetos em Destaque

### 🛒 [VitaShop — Customer Lifecycle Analytics](https://github.com/wallacegoulart/vitashop-customer-lifecycle)
> Pipeline completo em BigQuery para classificação de ciclo de vida de clientes com janela temporal deslizante de 24 meses.

- Procedural SQL com loop `WHILE` para backfill histórico mês a mês (2022–hoje)
- Classificação em 5 estados: **novo · recorrente · inativo · churn · recuperado**
- Multi-dimensional: cada cliente recebe labels independentes por marca, pagamento, produto e modalidade
- Window functions com `COUNT DISTINCT CASE WHEN` particionadas por múltiplas dimensões
- Atribuição de canal GA4 com deduplicação por `QUALIFY ROW_NUMBER()`
- Tabela final particionada, pronta para consumo em Power BI / Looker

```sql
-- Exemplo da lógica de classificação
CASE
  WHEN total_hist = 0 AND total_roll = 0 AND total_curr > 0 THEN 'new'
  WHEN total_hist > 0 AND total_roll = 0 AND total_curr = 0 THEN 'churned'
  WHEN total_hist > 0 AND total_roll = 0 AND total_curr > 0 THEN 'recovered'
  WHEN (total_roll + total_curr) >= 2                       THEN 'recurring'
  WHEN total_roll = 1     AND total_curr = 0                THEN 'inactive'
END AS lifecycle_state
```

---

## 💡 O que me motiva

Gosto de projetos onde a engenharia de dados e a análise se encontram — não só mover dados, mas **modelar de forma que o negócio consiga responder perguntas que antes eram impossíveis**. Tenho especial interesse em:

- Modelos de retenção e churn em e-commerce e saúde
- Atribuição de marketing multi-touch com dados GA4
- Arquiteturas de dados que escalam sem explodir o custo

---

## 📈 GitHub Stats

<div align="center">
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=wallacegoulart&show_icons=true&theme=dark&hide_border=true&count_private=true" />
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=wallacegoulart&layout=compact&theme=dark&hide_border=true" />
</div>

---

## 📬 Contatos

<div align="center">

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/wallacegoulart)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:seuemail@gmail.com)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white)](https://wa.me/55XXXXXXXXXXX)

</div>
