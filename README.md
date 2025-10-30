# 🧠 Strategic Segmentation: Customer Profiling with Credit Card Data

This project analyzes customer behavior using credit card usage data to identify distinct client segments. The goal is to uncover behavioral patterns and define actionable profiles that support marketing, retention, and credit strategies.

---

## 🎯 Objective

To test the hypothesis:

> Customer segments can be identified using behavioral and financial features, and strategic profiling can guide personalized business actions.

---

## 🛠️ Technologies Used

- **Python**: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn  
- **Jupyter Notebook**: Interactive environment for analysis  
- **CSV Dataset**: `/datasets/CC_GENERAL.csv` (Credit card client data)

---

## 🔍 Key Steps

### 1. Exploratory Data Analysis (EDA)

- Assessed missing values and imputed with median using `fillna()`.
- Reviewed distributions and outliers with `describe()` and `boxplot()`.
- Selected key features: `BALANCE`, `PURCHASES`, `CREDIT_LIMIT`, `PAYMENTS`, `TENURE`.

### 2. Feature Scaling and Clustering

- Normalized numerical features using `StandardScaler()`.
- Applied the Elbow Method to determine optimal number of clusters:
  - Iterated `k` from 2 to 10 and plotted SSE.
  - Identified the “elbow” point for best `k`.
- Trained `KMeans` clustering model with optimal `k`.
- Assigned cluster labels to each client.

### 3. Strategic Profiling

- Calculated average values per cluster using `groupby().mean()`.
- Mapped clusters to strategic profiles:
  - Cluster 0 → “Clientes Premium”
  - Cluster 1 → “Sensibles al Crédito”
  - Cluster 2 → “Clientes de Alto Potencial”
  - Cluster 3 → “Clientes Nuevos”
- Compared profiles using bar plots and boxplots:
  - Key differences in `CREDIT_LIMIT`, `BALANCE`, and `PURCHASES`.

### 4. Profile Comparison

- Created a focused comparison between:
  - **Clientes Premium**: Alto gasto, buen historial, alta antigüedad.
  - **Sensibles al Crédito**: Bajo límite, pagos mínimos, riesgo financiero.
- Visualized with grouped bar charts for strategic insight.

---

## ✅ Results

- Identified 4 distinct customer segments with actionable traits.
- Key insights:
  - Premium clients show high engagement and financial stability.
  - Credit-sensitive clients require cautious management and tailored offers.
- Strategic recommendations:
  - Upselling and loyalty programs for Premium clients.
  - Risk control and education for Credit-sensitive clients.

---

## 📚 Sources Consulted

- Scikit-learn Documentation – Clustering and scaling techniques  
- Pandas & NumPy Docs – Data manipulation and statistical summaries  
- Seaborn Gallery – Visualizing distributions and comparisons  
- Marketing Segmentation Techniques (HubSpot) – Cluster-based targeting  
- GitHub – Segmentación de Clientes con Python (CC_GENERAL.csv)  
- Towards Data Science – Data cleaning and clustering guides  
- Jupyter Notebook Tips (Real Python) – Workflow optimization  
- GitHub Markdown Guide – Project documentation formatting
