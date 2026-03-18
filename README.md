# ☕ Starbucks Customer Segmentation

> Uncovering hidden customer patterns to drive smarter, personalized marketing decisions.

---

## 📌 Project Overview

This project segments Starbucks customers based on their **demographic profiles** and **offer interaction behavior** to identify distinct customer groups and determine the most effective promotional delivery strategies.

By understanding *who* the customers are and *how* they respond to different offers, businesses can move from generic promotions to hyper-targeted campaigns — reducing wasted spend and increasing customer retention.

---

## 🎯 Business Problem

Starbucks sends various promotional offers (BOGO, discounts, informational) to customers through different channels. But not every customer responds to every offer. The key questions are:

- Which customers are most likely to respond to which offers?
- Are there identifiable segments based on demographics and behavior?
- What delivery strategy works best for each segment?

---

## 📂 Dataset

- **Source:** [Kaggle – Starbucks Capstone Dataset](https://www.kaggle.com/datasets/ihormuliar/starbucks-customer-data)
- **Size:** 300,000+ transaction entries across 3 files
- **Files:**
  - `portfolio.json` — Offer details (type, difficulty, reward, channels)
  - `profile.json` — Customer demographics (age, gender, income, membership date)
  - `transcript.json` — Event log (offer received, viewed, completed, transactions)

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Data Manipulation | Pandas, NumPy |
| Machine Learning | Scikit-learn (K-Means, PCA) |
| Visualization | Matplotlib, Seaborn, t-SNE |
| Environment | Jupyter Notebook |

---

## 🔬 Methodology

```
Raw Data (3 datasets)
      ↓
Data Cleaning & Merging
      ↓
Exploratory Data Analysis (EDA)
      ↓
Feature Engineering
      ↓
Dimensionality Reduction (PCA)
      ↓
K-Means Clustering
      ↓
Cluster Validation (Silhouette Score + SSE / Elbow Method)
      ↓
Cluster Visualization (t-SNE)
      ↓
Insights & Recommendations
```

### Key Steps

1. **Data Consolidation** — Merged 3 datasets (300,000+ rows) with careful handling of null values, type mismatches, and event-based log structure
2. **EDA** — Analyzed distributions of age, income, gender, and offer completion rates across channels
3. **Feature Engineering** — Created behavioral features such as offer completion rate, response time, and channel preference per customer
4. **PCA** — Reduced high-dimensional feature space to retain maximum variance with fewer components
5. **K-Means Clustering** — Segmented ~17,000 customers into distinct groups
6. **Validation** — Used Silhouette Score and SSE (Elbow Method) to determine optimal number of clusters
7. **t-SNE Visualization** — Plotted clusters in 2D to visually confirm separation and cohesion

---

## 📊 Key Findings

- Identified **distinct customer segments** with clearly different demographic and behavioral profiles
- Found that **offer type and delivery channel** significantly impact completion rates across segments
- High-income, older customers showed stronger response to discount offers via email
- Younger customers with lower income were more responsive to BOGO offers via mobile/social channels
- Recommended **personalized delivery strategies** per segment to maximize offer ROI

---

## 📁 Repository Structure

```
starbucks-customer-segmentation/
│
├── data/
│   ├── portfolio.json
│   ├── profile.json
│   └── transcript.json
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_feature_engineering.ipynb
│   ├── 04_clustering.ipynb
│   └── 05_insights.ipynb
│
├── images/
│   ├── elbow_curve.png
│   ├── tsne_clusters.png
│   └── segment_profiles.png
│
├── requirements.txt
└── README.md
```

---

## ▶️ How to Run

1. **Clone the repository**
```bash
git clone https://github.com/Lokesh-Kumar/<repo-name>.git
cd starbucks-customer-segmentation
```

2. **Install dependencies**
```bash
pip install -r requirements.txt
```

3. **Download the dataset** from [Kaggle](https://www.kaggle.com/datasets/ihormuliar/starbucks-customer-data) and place the JSON files inside the `data/` folder

4. **Run the notebooks** in order (01 → 05) inside the `notebooks/` folder

---

## 📦 Requirements

```
pandas
numpy
scikit-learn
matplotlib
seaborn
jupyter
```

> Save these in a `requirements.txt` file in your repo root.

---

## 👤 Author

**Lokesh Kumar**
B.S. Physics | IIT Kanpur
[GitHub](https://github.com/Lokesh-Kumar) • [LinkedIn](https://linkedin.com/in/Lokesh-Kumar)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
