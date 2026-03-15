# RetailPulse Data Ingestion and Exploration

## Project Overview

This repository contains the code and documentation for the data ingestion and exploration phase of the **RetailPulse Analytics** project. RetailPulse is a hypothetical retail analytics company focused on helping small and medium-sized retailers improve inventory planning, sales forecasting, and customer insights using transaction data.

For this phase of the project, the team used the **Online Retail II** dataset and implemented a workflow in **AWS S3** and **Amazon SageMaker Studio** to ingest, access, and explore the data in the cloud.

## Business Problem

Retail businesses often struggle with:
- overstocking low-demand items
- running out of high-demand products
- poor visibility into customer purchasing trends
- limited understanding of seasonal sales patterns

The goal of this project is to explore transaction-level data and identify useful patterns that can later support:
- inventory optimization
- customer segmentation
- sales forecasting
- product demand analysis

## Dataset

The dataset used in this project is the **Online Retail II** dataset, which contains historical transaction records for an online retail business.

### Example fields in the dataset
- `InvoiceNo`
- `StockCode`
- `Description`
- `Quantity`
- `InvoiceDate`
- `UnitPrice`
- `CustomerID`
- `Country`

## Cloud Storage and Access Workflow

The data ingestion workflow used in this project is:

1. Manually upload the raw dataset to an **Amazon S3** bucket
2. Store the raw file in the `raw-data/` folder
3. Open **Amazon SageMaker Studio**
4. Use a notebook to download the dataset from S3 to the local SageMaker environment
5. Load the data into pandas for exploration
6. Optionally save cleaned output files back to the `processed-data/` folder in S3

### S3 Folder Structure

```text
your-bucket-name/
├── raw-data/
│   └── online_retail.csv
└── processed-data/
    └── cleaned_retail_data.csv
