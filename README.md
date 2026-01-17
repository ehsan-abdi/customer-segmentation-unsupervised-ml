# Customer Segmentation Using Unsupervised Learning on Large-Scale E-Commerce Data

## Executive Summary
This project applies unsupervised machine learning to segment customers based on purchasing behaviour using a large real-world e-commerce dataset. After feature engineering and clustering analysis, five interpretable customer segments were identified, differing primarily in customer value, engagement, and demographic characteristics. While the customer space is continuous and clusters overlap, the resulting segments provide a practical foundation for targeted marketing and retention strategies.

---

## Problem Statement
Retail and e-commerce businesses rely on effective customer segmentation to personalise marketing, improve retention, and allocate resources efficiently. The objective of this project is to identify and interpret customer segments from transactional and demographic data using unsupervised learning, with the aim of supporting targeted marketing and customer retention strategies.

---

## Dataset
- Approximately 950,000 transaction records  
- Around 68,000 unique customers  
- 47 countries, spanning multiple years  
- Real-world data containing missing values, duplicates, and skewed distributions  

Raw transactional data was aggregated to the customer level to enable behaviour-based segmentation.

---

## Feature Engineering
Transaction-level data was transformed into customer-level metrics capturing engagement and value:
- **Frequency**: number of orders per customer  
- **Recency**: days since last purchase  
- **Customer Lifetime Value (CLV)**: total revenue per customer  
- **Average Unit Cost**: mean purchase price  
- **Customer Age**: age at a defined reference date  

Skewed features were transformed and standardised to improve comparability and better satisfy model assumptions.

---

## Methodology
- Exploratory Data Analysis (EDA) to assess distributions and outliers  
- Feature transformation and scaling  
- **K-Means clustering** as the primary segmentation method  
- Cluster selection using:
  - Elbow method  
  - Silhouette analysis  
  - Hierarchical clustering (Ward’s linkage)  
- Dimensionality reduction using **PCA** and **t-SNE** for qualitative assessment  

---

## Results
Five customer segments were identified, primarily differentiated by:
- Customer value (CLV)  
- Engagement (frequency and recency)  
- Demographic characteristics  

The resulting clusters reveal a high-value active segment, a low-value inactive segment, and several mid-tier groups with distinct behavioural profiles.

---

## Interpretation and Limitations
Cluster visualisations indicate substantial overlap between segments, suggesting a dense and continuous customer space rather than sharply separated groups. As a result, cluster membership should be interpreted as probabilistic rather than as strict boundaries.

Further validation with business stakeholders would be required to refine segment definitions and confirm their practical usefulness.

---

## Potential Business Applications
- Targeted marketing and promotional strategies  
- Customer retention and reactivation campaigns  
- Resource prioritisation across customer segments  
- Input features for downstream predictive models  

---

## Technologies Used
- Python  
- Pandas, NumPy  
- scikit-learn  
- Matplotlib, Seaborn  

---

## Next Steps
- Evaluate alternative clustering approaches (e.g. Gaussian Mixture Models, HDBSCAN)  
- Assess cluster stability across multiple random initialisations  
- Incorporate additional behavioural or contextual features  
- Validate segmentation effectiveness using campaign outcomes or A/B testing  

---

## Repository Structure
.
├── customer_segmentation.ipynb
├── README.md
└── data/
