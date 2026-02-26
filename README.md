# Understanding Customers with Clustering

## Overview

This project performs **customer segmentation** using **RFM (Recency, Frequency, Monetary) analysis** combined with **K-Means clustering** on transactional data from an online retail store. The goal is to identify distinct customer groups to enable targeted marketing strategies.

## Dataset

The dataset used is the **Online Retail II** dataset from UCI Machine Learning Repository, containing transactions from a UK-based online retail company between December 2009 and December 2011.

🔗 [Dataset](https://archive.ics.uci.edu/dataset/502/online+retail+ii)

## Methodology

1. **Data Exploration** - Understanding the structure and quality of data
2. **Data Cleaning** - Handling missing values, filtering valid transactions
3. **Feature Engineering** - Creating RFM features:
   - **Recency**: Days since last purchase
   - **Frequency**: Number of unique purchases
   - **Monetary Value**: Total spending amount
4. **Outlier Analysis** - Identifying and separating outlier customers
5. **K-Means Clustering** - Segmenting customers using elbow method and silhouette score

## Customer Segments

### Main Clusters (K-Means)

| Cluster | Name | Characteristics | Action |
|---------|------|-----------------|--------|
| 0 | **Retain** | Low recency, mid frequency & monetary | Increase AOV with bundled deals & cross-selling |
| 1 | **Revive** | High recency, very low frequency & monetary | Win-back campaigns with one-time discounts |
| 2 | **Nurture** | Very low recency, low frequency & monetary | Onboarding sequences & welcome offers |
| 3 | **Rewards** | Very low recency, very high frequency & monetary | VIP programs, early access, leverage for referrals |

### Outlier Clusters

| Cluster | Name | Characteristics | Action |
|---------|------|-----------------|--------|
| -1 | **Rescue** | High-value but erratic recency | Aggressive personalized VIP win-back offers |
| -2 | **Facilitate** | Low recency, high frequency, low-mid monetary | Subscription models, bulk discounts, loyalty programs |
| -3 | **Pamper** | Very low recency, extremely high frequency & monetary | Dedicated account managers, white-glove service, exclusive events |

## Installation

```bash
pip install -r requirements.txt
```

## Usage

1. Download the dataset and place `online_retail_II.xlsx` in the `data/` folder
2. Open and run `main.ipynb` in Jupyter Notebook