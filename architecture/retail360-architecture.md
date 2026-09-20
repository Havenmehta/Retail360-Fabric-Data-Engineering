# Retail360 Architecture

```mermaid
flowchart LR

A[Source CSV Data] --> B[Bronze Lakehouse]
B --> C[Silver Transformation<br/>PySpark]
C --> D[Silver Lakehouse]
D --> E[Gold Transformation<br/>PySpark]
E --> F[Gold Lakehouse]
F --> G[Direct Lake<br/>Semantic Model]
G --> H[Power BI<br/>Executive Dashboard]

P[Retail360 Master Pipeline] --> C
P --> E
Medallion Architecture
Bronze: Raw/near-raw Delta data
Silver: Cleaned, validated and enriched data
Gold: Business-ready analytical datasets
Semantic Model: Direct Lake analytical layer
Power BI: Executive reporting and business insights
Orchestration

Silver_Transformation → Gold_Transformation

The workflow is orchestrated using the Retail360_Master_Pipeline Fabric Data Pipeline.
