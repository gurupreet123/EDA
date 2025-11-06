# Analyzing Food Security Data: A Multi-Algorithm Approach to Predicting Distribution Gaps

> A comprehensive machine learning project that analyzes India's Public Distribution System (PDS) to predict, explain, and segment system inefficiency.

This repository contains the complete code, data, and analysis for the project, which moves beyond simple forecasting to model a more meaningful metric: the **"Distribution Gap."**

## 📜 Table of Contents

  * [Project Overview](https://www.google.com/search?q=%23-project-overview-the-distribution-gap)
  * [Our 10-Algorithm Methodology](https://www.google.com/search?q=%23-our-10-algorithm-methodology)
  * [Key Findings & Results](https://www.google.com/search?q=%23-key-findings--results)
  * [Technologies Used](https://www.google.com/search?q=%23-technologies-used)
  * [How to Run This Project](https://www.google.com/search?q=%23-how-to-run-this-project)
  * [Project Structure](https://www.google.com/search?q=%23-project-structure)
  * [Conclusion & Future Work](https://www.google.com/search?q=%23-conclusion--future-work)
  * [License](https://www.google.com/search?q=%23-license)

-----

## 🚀 Project Overview: The "Distribution Gap"

The efficiency of India's Public Distribution System (PDS) is critical for national food security. While many analyses focus on forecasting *demand*, this project addresses a more significant challenge: **system inefficiency**.

To quantify this, we engineered a new metric, the **"Distribution Gap"**:


Distribution Gap = Food Grains Allocated - Total Food Grains Distributed.
A positive gap represents a failure to distribute allocated food, serving as a direct proxy for inefficiency, logistical failure, or waste. This project is a complete, end-to-end analysis to predict, explain, and segment this new metric.

-----

## 🔬 Our 10-Algorithm Methodology

Instead of relying on a single model, this project uses a "4-Squad" methodology, deploying 10 distinct algorithms to build a holistic, 360-degree view of the inefficiency problem.

### 🎯 Squad 1: Regression (Predicts "How Much?")

**Goal:** To predict the *exact value* of the `Distribution_Gap`.

* **Linear Regression:** The baseline model to establish a simple linear relationship.
* **Lasso Regression:** A smarter baseline that also performs automatic feature selection.
* **Decision Tree Regressor:** A non-linear, "if-then" rule-based model that is highly interpretable.
* **K-Neighbors Regressor:** A non-parametric model that predicts based on the "nearest" similar data points from the past.
* **Random Forest Regressor:** Our "champion" ensemble model, which averages hundreds of decision trees for high accuracy and stability.

### 💡 Squad 2: Feature Analysis (Explains "Why?")

**Goal:** To understand the root *drivers* of the `Distribution_Gap`.

* **Feature Importance (from Random Forest):** Opens the "black box" of our best model to rank which features (e.g., `Aadhaar_Auth_Pct`, `Manual_Distribution`) have the biggest impact.
* **Principal Component Analysis (PCA):** A dimensionality reduction technique to find the hidden "macro-patterns" or "super-features" in the data.

### 🗺️ Squad 3: Clustering (Finds "Who?")

**Goal:** To segment states into operational "personas" and find outliers.

* **K-Means Clustering:** An unsupervised algorithm to automatically group states into distinct "personas" (e.g., "High-Tech, Efficient" vs. "Manual-Heavy, Inefficient").
* **DBSCAN:** An anomaly detection algorithm that automatically finds the most unusual, "outlier" state-months that don't fit any group.

### 🚨 Squad 4: Classification (Predicts "If?")

**Goal:** To build an "early warning system" for policymakers.

* **Logistic Regression:** Trained on a binary target (`Had_Significant_Gap`), this model predicts the *probability* (0-100%) that an inefficiency event will occur.

-----

## ✨ Key Findings & Results

This multi-model approach yielded several key, actionable insights:

1.  **Inefficiency is Highly Predictable:** The `Distribution_Gap` is not random. Our **Random Forest Regressor** (Squad 1) was able to predict the *amount* of inefficiency with **0.93 R²** accuracy, proving the problem is non-linear and complex.

2.  **Inefficiency is Explainable:** The **Feature Importance** analysis (Squad 2) provided a clear "why." The **`Aadhaar_Auth_Transactions_Pct`** was the **\#1 driver of *efficiency*** (a low gap), while a reliance on `Manual_Distribution_MT` was the top predictor *of inefficiency*.

3.  **An "Early Warning System" is Viable:** Our **Logistic Regression** model (Squad 4) successfully predicted the *probability* of a gap occurring with **91.2% Accuracy** and a high Recall, making it a perfect tool for proactive alerts.

4.  **A "One-Size-Fits-All" Policy is Wrong:** **K-Means** (Squad 3) identified 4 distinct clusters of state operations, proving that targeted policies are needed for different "personas." **DBSCAN** successfully flagged 34 anomalous data points, providing a clear list for auditors to investigate.

-----

## 🛠️ Technologies Used

* **Python 3.9**
* **Pandas:** For all data loading, cleaning, and feature engineering.
* **Scikit-learn:** For all 10 machine learning models, preprocessing (StandardScaler), and metrics.
* **NumPy:** For numerical operations.
* **Matplotlib & Seaborn:** For all EDA and results visualizations.
* **Jupyter Notebook:** As the primary development environment.

-----

## ⚙️ How to Run This Project

### 1\. Clone the Repository

```bash
git clone https://github.com/[YourUsername]/[YourRepositoryName].git
cd [YourRepositoryName]
```

### 2\. Create a Virtual Environment (Recommended)

```bash
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

### 3\. Install Dependencies

This project's dependencies are listed in `requirements.txt`.

```bash
pip install -r requirements.txt
```

### 4\. Run the Project

All preprocessing, EDA, modeling, and analysis are contained in the Jupyter Notebook.

```bash
jupyter notebook "FoodSecurity_DSProject.ipynb"
```

-----

## 📂 Project Structure

```
.
├── data/
│   └──  Food_Security_Data.csv      # The raw dataset
├── notebooks/
│   └──  FoodSecurity_DSProject.ipynb  # Main notebook with all 10 algorithms
├── reports/
│   ├── MINI PROJECT REPORT FORMAT.pdf
│   └── Final Project Report.pdf         
└── README.md     
```

-----

## 🏁 Conclusion & Future Work

### Conclusion

This project successfully transformed raw PDS data into a comprehensive decision-support system. By engineering the `Distribution_Gap` metric, we provided a framework to not only forecast inefficiency but also to explain its causes, classify its probability, and segment states for targeted interventions.

### Future Work

1.  **Deployment:** Deploy the Logistic Regression "early warning system" (Squad 4) as a live web dashboard.
2.  **Deep Learning:** Implement an LSTM (Long Short-Term Memory) model to potentially improve the time-series forecasting of the `Distribution_Gap`.
3.  **Granular Analysis:** Re-apply this 10-algorithm methodology to district-level data for more localized and impactful insights.

-----

## ⚖️ License

This project is licensed under the MIT License. See the `LICENSE` file for details.
