# E-Commerce Customer Segmentation for Growth Strategy

**Behavioural Customer Segmentation using Unsupervised Machine Learning**

---

## 📌 Project Overview
This project applies unsupervised learning to a large-scale global e-commerce dataset to identify **actionable customer segments**. By transforming raw transaction logs into behavioural metrics, the analysis enables data-driven decisions around **retention, reactivation, and marketing cost efficiency**.

- **Customers:** 68,000+  
- **Transactions:** ~950,000  
- **Geography:** 47 countries  
- **Segments Identified:** 5 behavioural tiers  

---

## 🎯 Business Objective
The company treats its international customer base as largely homogeneous, leading to:
- Inefficient marketing spend  
- Under-leveraged high-value customers  
- Limited prioritisation of churn risk  

**Goal:**  
Uncover latent behavioural segments to maximise **Customer Lifetime Value (CLV)** and improve **marketing ROI**.

---

## 🧠 Technical Approach

### 1. Data Engineering
- Cleaned and validated ~1M transaction records  
- Parsed accounting-style currency values  
- Standardised temporal fields and enforced business logic  

### 2. Feature Engineering
Customer-level aggregation using:
- **Recency:** Days since last purchase  
- **Frequency:** Unique order count  
- **Monetary (CLV):** Total revenue  
- **Avg Unit Cost:** Price sensitivity proxy  
- **Customer Age:** Demographic context  

### 3. Preprocessing
- Skewed behavioural features transformed using **Yeo-Johnson**
- All features standardised for Euclidean distance stability
- Modular preprocessing via `ColumnTransformer`

### 4. Clustering & Optimisation
- **K-Means clustering**
- Optimal `k=5` selected using:
  - Elbow Method (WCSS)
  - Silhouette Analysis
  - Hierarchical Dendrograms

### 5. Validation & Interpretability
- PCA and t-SNE projections
- Median-based cluster profiling
- Segment re-indexing for intuitive value tiers

---

## 📊 Key Results (Median Metrics)

| Tier | Segment Name        | CLV        | Frequency | Recency (Days) | Avg Unit Cost | Age        | Population |
|-----:|---------------------|-----------:|----------:|---------------:|--------------:|-----------:|-----------:|
| 5    | Champions           | $3,759     | 20        | 33             | $79.65        | 33 yrs     | 24%        |
| 4    | Loyal Regulars      | $1,630     | 10        | 112            | $71.42        | 58 yrs     | 23%        |
| 3    | At-Risk Mid-Tier    | $1,347     | 9         | 279            | $70.88        | 23 yrs     | 24%        |
| 2    | High-Ticket Lapsed  | $819       | 3         | 722            | $117.15       | 48 yrs     | 13%        |
| 1    | Budget Churned      | $243       | 3         | 716            | $42.50        | 53 yrs     | 15%        |

---

## 💡 Business Recommendations (High Level)

- **Tiers 4–5:** Prioritise retention and churn monitoring (revenue core)
- **Tiers 2–3:** Targeted reactivation and value-uplift experiments
- **Tier 1:** Cost-controlled or passive engagement only

---

## 🔁 Reproducibility
- Fixed random seeds
- Modular preprocessing and clustering pipelines
- Designed for reruns on new or refreshed data

---

## 🚧 Limitations & Next Steps
- No temporal backtesting of segment stability
- No direct ROI or uplift estimation
- Future work:
  - Segment transition modeling
  - A/B testing framework
  - Production scoring for new customers

---

## 🛠️ Tech Stack
- **Python:** pandas, numpy, scikit-learn, scipy  
- **Visualisation:** matplotlib, seaborn  

---

## 👤 Author
Ehsan Abdi  
Focus: **Customer analytics, growth strategy, unsupervised learning**
