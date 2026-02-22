# Comprehensive Clustering Analysis of Airline Passenger Data

A Python-based clustering analysis project comparing **K-Means**, **DBSCAN**, and **Hierarchical Clustering** algorithms on airline passenger satisfaction data.

This project evaluates algorithm performance using **silhouette scores** and **confusion matrix validation** against actual satisfaction labels.

---

## Overview

The objective of this project is to apply and compare three clustering algorithms to identify meaningful passenger segments based on:

- Flight statistics  
- Service ratings  
- Operational factors  

The analysis provides insights into which algorithm best captures passenger behavior patterns and aligns with actual satisfaction outcomes.

---

## Dataset

- **Dataset:** [Kaggle] (https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction)
- **Size:** 103,904 rows × 25 columns  
- **Target Column:** `satisfaction`

### Target Classes
- `satisfied` → Satisfied passengers  
- `neutral or dissatisfied` → Unsatisfied passengers  

### Features
- Demographics  
- Flight details  
- Service ratings  
- Operational metrics  

---

## Features Analyzed

### Flight Statistics
- Flight Distance  
- Departure Delay in Minutes  

### Passenger Experience
- Inflight wifi service  
- Inflight entertainment  
- Online boarding  
- Ease of Online booking  

### Service Comfort
- Food and drink  
- Departure/Arrival time convenient  
- Seat comfort  

These features capture passenger behavior, service quality perceptions, and operational factors influencing overall satisfaction.

---

# Clustering Algorithms Compared

## 1. K-Means Clustering
- **Approach:** Partition-based (spherical clusters)
- **Optimal k:** 3 (determined using Elbow Method)

**Strengths**
- Simple and computationally efficient  
- Works well for well-separated clusters  

**Weaknesses**
- Assumes spherical clusters  
- Sensitive to outliers  

---

## 2. DBSCAN (Density-Based Spatial Clustering)
- **Approach:** Density-based clustering
- **Parameters:** `eps=0.5`, `min_samples=5`

**Strengths**
- Handles noise effectively  
- Identifies clusters of arbitrary shapes  

**Weaknesses**
- Sensitive to parameter tuning  
- Struggles with varying density datasets  

---

## 3. Hierarchical Clustering
- **Approach:** Agglomerative (bottom-up)
- **Linkage:** Ward’s Method  

**Strengths**
- No predefined cluster count required  
- Captures hierarchical relationships  

**Weaknesses**
- Computationally expensive  
- Rigid structure  

---

# Performance Metrics

| Algorithm     | Silhouette Score | Accuracy | Precision | Recall | F1 Score |
|--------------|------------------|----------|-----------|--------|----------|
| K-Means     | 0.1934           | 72.89%   | 65.13%    | 57.98% | 61.32%   |
| DBSCAN      | 0.2644           | 54.74%   | 100.00%   | 0.75%  | 1.49%    |
| Hierarchical| 0.1170           | 63.83%   | 66.86%    | 34.91% | 45.87%   |

---

# Key Findings

## K-Means — Best Overall Performance
- Highest accuracy (72.89%)
- Balanced precision-recall (65.13% / 57.98%)
- Best F1 Score (61.32%)
- Identified 3 well-defined passenger segments

---

## DBSCAN — Precision Specialist
- Perfect precision (100%)
- Extremely low recall (0.75%)
- Identified 572 clusters (over-segmentation)
- High noise labeling

---

## Hierarchical — Moderate Performance
- Decent precision (66.86%)
- Low recall (34.91%)
- Limited flexibility for complex patterns  

---

# Algorithm Comparison Summary

| Aspect | K-Means | DBSCAN | Hierarchical |
|--------|---------|--------|--------------|
| Cluster Shape | Spherical | Arbitrary | Tree-based |
| Noise Handling | Poor | Excellent | Poor |
| Predefined k | Required | Not required | Not required |
| Optimal Use Case | Customer Segmentation | Anomaly Detection | Hierarchical Data |
| Overall Performance | 3/3 | 1/3 | 2/3 |

---

# Tech Stack

- Python 3 (Google Colab)
- pandas, numpy — Data manipulation  
- scikit-learn — Clustering algorithms, preprocessing, metrics  
- matplotlib, seaborn — Visualization  
- scipy — Hierarchical clustering  

---

# Implementation Highlights

## Data Preprocessing
- Feature selection and grouping  
- StandardScaler normalization  
- Missing value handling  

## Algorithm Implementation
- Elbow method for optimal k  
- Dendrogram analysis  
- Parameter tuning for DBSCAN  

## Evaluation Methods
- Silhouette scores  
- Confusion matrices  
- Accuracy, Precision, Recall, F1 Score  

---

# Conclusions

K-Means clustering is the optimal choice for this airline passenger dataset, demonstrating:

- Highest overall accuracy (72.89%)  
- Balanced precision-recall trade-off  
- Meaningful passenger segmentation  
- Best alignment with satisfaction patterns  

While DBSCAN excels at noise detection and Hierarchical Clustering captures structural relationships, K-Means provides the most actionable insights for passenger segmentation and service improvement strategies.

---

# Future Improvements

- Hyperparameter optimization using GridSearch  
- Dimensionality reduction (PCA)  
- Feature importance analysis  
- Deployment as an interactive dashboard  

---

## Author
Henry Hezekiah Nafora
Data Science / Machine Learning Project  
