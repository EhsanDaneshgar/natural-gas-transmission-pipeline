
# EU Natural Gas Flow ETL Pipeline (ADF Simulation)

## 🔍 Overview

This project builds an end-to-end data pipeline using Azure Data Factory (ADF)-style transformations. It processes monthly gas flow data from the International Energy Agency (IEA) and prepares it for analytics.

## 📦 Dataset

- **Source**: IEA Gas Transmission Flows (EU)
- **File**: `Export_GTF_IEA_202505.xlsx`
- **Format**: Monthly gas volumes at borderpoints (2008–2025)
- **Unit**: Million Cubic Meters (mcm)

## 🛠️ Pipeline Structure

```
project-root/
├── data/
│   └── raw/
│       └── Export_GTF_IEA_202505.xlsx
├── transformed/
│   └── entry_monthly_flow.csv
├── adf_pipeline/
│   ├── pipeline_definition.json
│   ├── transformations.json
│   └── trigger_config.json
├── sql/
│   └── create_table.sql
├── docs/
│   └── gas_flow_pipeline.md
└── README.md
```

## 🔄 ETL Steps

1. **Extract**: Upload Excel to Blob Storage
2. **Transform (ADF)**:
    - Unpivot monthly columns to long format
    - Convert flow values to BCF
    - Replace or drop null values
3. **Load**: Output to Azure SQL or clean CSV

## 📈 Tools Used

- Azure Data Factory
- Azure Blob Storage
- Azure SQL Database
- Python (for local testing)
- Excel (preview and validation)

## 🚀 Automation

- Simulated trigger: daily or file-drop based
- JSON configuration for pipeline deployment

## 📑 Author Notes

This project is based on a post-college ADF portfolio assignment. Dataset and logic are publicly shareable.
