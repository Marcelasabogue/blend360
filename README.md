# Blend360

# 🏥 Modernization of Healthcare Data Infrastructure  
### End-to-End Data Engineering Project on Azure + Databricks  
---

## 📌 Project Overview

This project simulates the migration of a legacy healthcare data infrastructure into a modern, scalable, and governed cloud-based architecture using **Azure Databricks**. It implements a **Bronze–Silver–Gold architecture pattern**, with emphasis on data quality, governance, automation, and analytics to support advanced data initiatives in healthcare.

### Key Objectives:
- Migrate data from legacy (on-premise) systems to a modern cloud platform
- Build scalable, modular data pipelines with PySpark and Delta Lake
- Apply robust QA testing and validation for sensitive healthcare data
- Implement security, governance, and access controls
- Create business-ready analytics and dashboards for decision-making
---

## 🧱 Architecture Diagram
```

\[Legacy Data Source]
↓ (CSV / SQL Server)
\[Azure Blob Storage - Raw]
↓
\[Databricks Bronze Layer] → (Delta Tables)
↓
\[Databricks Silver Layer] → (Cleaning, Joins, QA)
↓
\[Databricks Gold Layer] → (KPIs, Aggregations)
↓
\[Power BI / Dashboards]

```
---

## 🧰 Technologies Used

| Category               | Tools/Technologies                       |
|------------------------|------------------------------------------|
| Cloud Platform         | Azure Blob Storage, Azure DevOps         |
| Data Processing        | Azure Databricks, PySpark, Delta Lake    |
| Orchestration / CI-CD  | Azure Pipelines, Databricks Jobs         |
| Testing & QA           | PyTest, Great Expectations (optional)    |
| Visualization          | Power BI, Databricks Dashboards          |
| Governance & Security  | Unity Catalog, Data Masking, ACLs        |
| Data Discovery / Lineage | Unity Catalog, Data Dictionary          |

---

## 🗃️ Simulated Dataset

| File                  | Description                               |
|-----------------------|--------------------------------------------|
| `patients.csv`        | Anonymized patient demographic data        |
| `hospital_visits.csv` | Historical hospital visit records          |
| `medications.csv`     | Medication prescriptions                   |

📦 Data is simulated and uploaded to Azure Blob Storage at path `/raw-data/`
---

## 🧪 Data Quality & Testing

Includes automated and manual data quality validations:
- Business rule checks (e.g., non-negative ages, valid visit dates)
- Unit tests for transformation logic using `pytest`
- Schema validation, deduplication, null checks
- Optional integration with Great Expectations

---

## 🔐 Governance & Security

- Role-based access control using Unity Catalog
- Masking policies applied to sensitive columns (e.g., names, birthdates)
- Audit logs and access restrictions for regulated environments
---

## 🧑‍💻 Repository Structure
```

├── notebooks/
│   ├── bronze\_ingestion.py
│   ├── silver\_transformation.py
│   ├── gold\_kpis.py
│   ├── qa\_validation.py
├── tests/
│   └── test\_transformations.py
├── data/
│   ├── patients.csv
│   ├── hospital\_visits.csv
├── diagrams/
│   └── architecture\_diagram.png
├── azure-pipelines.yml
└── README.md

```
---
## ⚙️ CI/CD & Orchestration

CI/CD is handled via **Azure DevOps Pipelines**:
- Automatically runs unit tests and triggers pipelines on code push
- Uses `databricks-cli` to launch a chained **Databricks Job** with the following stages:
  - Bronze: raw ingestion with Autoloader
  - Silver: cleansing and transformation
  - Gold: KPI aggregation

---
## 📊 Analytics & Dashboards

Business-facing KPIs are computed in the **Gold Layer**, including:
- Total hospital visits per week per hospital
- Most common diagnoses
- KPIs by age group, region, and medical specialty

Dashboards are created with Power BI or native Databricks dashboards.
---

## 🧾 Data Lineage & Documentation

- Diagrams created with Draw.io or Lucidchart (`/diagrams`)
- Full technical documentation for each pipeline
- Data dictionary with schema descriptions, validations, and metadata
- Project reproducibility guide included in this repository

---

## 📈 Expected Outcomes

- Migrated data from legacy formats into secure, optimized Delta tables
- Validated and tested pipelines ready for production
- Governed, accessible, and traceable datasets for analytics and AI
- Business insights available via dashboards for stakeholder reporting

---

## 📬 Contact

**Author:** Marcela Sabogal Guerrero  
**Email:** marcelasabogue@ieee.org
**LinkedIn:** [linkedin.com/in/marcelasabogue](https://www.linkedin.com/in/marcelasabogue/)  
```

---
