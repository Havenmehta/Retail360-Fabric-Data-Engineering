# Retail360 Architecture

## End-to-End Data Flow

```text
Source CSV Data
      │
      ▼
Retail360_Bronze
      │
      ▼
Silver_Transformation
      │
      ▼
Retail360_Silver
      │
      ▼
Gold_Transformation
      │
      ▼
Retail360_Gold
      │
      ▼
Direct Lake Semantic Model
      │
      ▼
Power BI Executive Dashboard
Pipeline Orchestration
Retail360_Master_Pipeline
          │
          ▼
Silver_Transformation
          │
       Success
          │
          ▼
Gold_Transformation
Medallion Architecture
Bronze

Raw/near-raw Delta tables.

Silver

Cleaned, validated and enriched datasets using PySpark.

Gold

Business-ready analytical datasets and KPIs.

Semantic Layer

Direct Lake semantic model with DAX measures.

Analytics

Power BI executive dashboard with interactive filtering and store drill-through.

Azure Blob Storage
  └── raw/
      ├── customers.csv
      ├── products.csv
      ├── stores.csv
      └── sales.csv
            ↓
    Fabric OneLake Shortcut
            ↓
    Retail360_Bronze
            ↓
    Silver Transformation
            ↓
    Retail360_Silver
            ↓
    Gold Transformation
            ↓
    Retail360_Gold
            ↓
    Direct Lake Semantic Model
            ↓
    Power BI Executive Dashboard
