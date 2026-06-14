# Customer360 Analytics Platform

A unified analytics solution built using **Microsoft Fabric**, combining customer transaction data, sentiment analysis, and churn prediction. This project aims to deliver actionable insights through intelligent dashboards and machine learning using PySpark MLlib and Power BI.

---

## Project Overview

This platform simulates a 360-degree customer analytics solution for retail/e-commerce businesses. It includes:

- Data ingestion and cleansing using Fabric Lakehouse
- Sentiment analysis using Text Analytics for customer reviews
- Churn prediction using PySpark (MLlib)
- Visual reporting via Power BI dashboard (auto-created)

---

## Project Structure

Customer360-Analytics-Platform/
│
├── data/ # Sample customer datasets (CSV)
├── notebooks/ # ML notebooks (sentiment analysis + churn model)
├── dashboard/ # Power BI screenshot / .pbix report
├── README.md # Project documentation (this file)


---

## Key Components

### 1. Sentiment Analysis (Step 5)
- Performed using Azure AI Text Analytics on customer review text.
- Each review is tagged with a sentiment (positive, neutral, negative).
- Sentiment score indexed numerically using a UDF in PySpark.

### 2. Churn Prediction (Step 6)
- Labels customers as **churned** (1) or **retained** (0) using randomized sampling.
- Features include:
  - Purchase amount
  - Sentiment index
- Trained using PySpark MLlib with a Logistic Regression classifier.
- Accuracy evaluated on test data.

### 3. Power BI Dashboard (Step 7)
Auto-generated using Microsoft Fabric from the semantic model. Key visuals include:
- Total Customers
- Churn Rate %
- Churn Prediction Breakdown by Location/Product
- Purchase vs Sentiment Comparison

---

## Dashboard Preview

Find the `.pbix` or dashboard screenshots inside `dashboard/`.

---

## Learnings

Used Microsoft Fabric for end-to-end data handling.

Leveraged PySpark for scalable ML training.

Integrated structured + unstructured data for richer customer insights.

Automated reporting with Power BI to accelerate decision-making.

## Tech Stack

Microsoft Fabric (Lakehouse, Notebooks, Power BI)

PySpark (MLlib)

Azure Text Analytics

Power BI (auto-report generation)
