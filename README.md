<div align="center">

## Eric Grynspan &nbsp;·&nbsp; Data Engineer

**Healthcare AI &amp; Fintech &nbsp;|&nbsp; New York, NY**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Eric%20Grynspan-0A66C2?style=flat-square)](https://www.linkedin.com/in/ericgrynspan/)

</div>

---

Data Engineer building real-time RCM denial prevention and auditable AI governance pipelines for healthcare — Kafka streaming, LLM tool-use, FHIR R4, Snowflake. Fintech: quantitative financial research and alpha signal pipelines on AWS.

---

> Denied classifies denials retrospectively &nbsp;→&nbsp; Trust but Verify adds AI governance &nbsp;→&nbsp; Cleared prevents denials in real time

#### [Denied: Healthcare Claims Intelligence Pipeline](https://github.com/ericg1212/healthcare-claims-pipeline)

> Classifies 257K denied claims by root cause — systematic denials vs. documentation failures — where the remediation path differs fundamentally for each.

| | |
|:--|:--|
| **Stack** | Synthea FHIR R4 · Python · Snowflake (RAW → staging → mart) · dbt · Dagster |
| **Scale** | 495K total claims · 51.9% denial rate · $1.2M+ recoverable · 12 dbt models · 83 tests |
| **RWE** | T2D/CKD cohort · 104 patients · 54.8% metformin utilization |

#### [Trust but Verify: Clinical AI Governance Engine](https://github.com/ericg1212/ai-healthcare-pipeline)

> Dual-validation AI governance — LLM enrichment cross-validated by a deterministic rules engine. Every record routes to Gold (trusted) or Review (explainable reason). No black-box outputs.

| | |
|:--|:--|
| **Stack** | FHIR R4 · Python · Snowflake · dbt · Dagster · LLM API · Pydantic |
| **Design** | LLM-as-Judge blind audit · prompt caching · confidence threshold routing |
| **Data** | 226 patients · 25,958 clinical records · 6 enrichment categories · 6 rules engine domains |

#### [Cleared: Agentic RCM Prevention Pipeline](https://github.com/ericg1212/agentic-rcm-pipeline)

> Intercepts claims before submission instead of analyzing denials after the fact — a deterministic NCCI gate plus LLM tool-use prevent the two largest denial root causes at the source.

| | |
|:--|:--|
| **Stack** | Apache Kafka (KRaft) · LLM tool-use · Snowflake · dbt · Python |
| **Design** | NCCI gate (~85% cleared without LLM) · 3-condition auto-correct gate (confidence ≥ 0.92 + charge ≤ $500) · drift monitor (>20% → kill-switch) |
| **Proof** | 10% holdout control arm · provable intervention vs. control lift · $0.0119/claim live-validated · ~12,600× ROI · 272 tests · CI green |

#### [AI Builder Premium — Sharpe Ratio Analysis](https://github.com/ericg1212/sharpe-premium-pipeline)

> Proprietary AI builders generate a **+92.0% Sharpe ratio premium** over third-party integrators (Spearman ρ = +0.800, p ≈ 0.005) across 10 major tech stocks — visualized in an interactive Power BI dashboard.

| | |
|:--|:--|
| **Stack** | Airflow · S3 · Glue · Athena · Power BI · Terraform · GitHub Actions |
| **Storage** | Hive-partitioned S3 data lake · Parquet/Snappy · Glue catalog · serverless Athena |
| **Quality** | 184 pytest unit tests · moto AWS mocking · GitHub Actions CI/CD · Terraform IaC |

---

### Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=flat-square&logo=snowflake&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=flat-square)
![Apache Airflow](https://img.shields.io/badge/Apache%20Airflow-017CEE?style=flat-square&logo=apacheairflow&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache%20Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Dagster](https://img.shields.io/badge/Dagster-4F4FE6?style=flat-square)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square)
![GitHub Actions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white)
