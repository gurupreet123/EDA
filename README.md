# 🧪 Exploratory Data Analysis (EDA) – Agricultural Landholding Dataset

This repository contains a complete Exploratory Data Analysis (EDA) of an Indian agricultural landholding dataset. The objective is to explore structure, detect missing values, find outliers, and uncover relationships using visualizations and summary statistics.

---

## 📁 Dataset Overview

- **Rows**: ~28,000+
- **Columns**: A mix of categorical and numerical features:
  - `State`, `District`, `Year`, `Social Group Type`, `Category Of Holdings`
  - Statistical values like `Wholly Owned Holdings`, `Leased Holdings`, `Area (Ha.)`, etc.

---

## 🧾 Step-by-Step EDA Process

### ✅ Step 1: Import Required Libraries  
Loaded libraries like `pandas`, `numpy`, `matplotlib`, and `seaborn` for data handling and visualization.

### ✅ Step 2: Load the Dataset  
Used `pandas.read_csv()` to load the CSV file and previewed the first few records.

### ✅ Step 3: Dataset Overview  
Printed the shape, info, and descriptive statistics of the dataset to understand its structure and types of features.

### ✅ Step 4: Check Missing Values  
Counted and visualized missing values using a heatmap to highlight incomplete data columns.

### ✅ Step 5: Data Types and Column Categories  
Separated the dataset into **categorical** and **numerical** columns for specialized handling and visualization.

### ✅ Step 6: Univariate Analysis (Categorical Columns)  
Used count plots to visualize frequency distribution for each categorical variable.

### ✅ Step 7: Univariate Analysis (Numerical Columns)  
Plotted histograms of numerical columns to understand value distributions and detect skewness.

### ✅ Step 8: Boxplots to Detect Outliers  
Created boxplots for each numerical feature to visually identify the presence of outliers.

### ✅ Step 9: Correlation Matrix (Numerical Features)  
Generated a heatmap showing correlation among numerical features to uncover relationships.

### ✅ Step 10: Pairplot (Optional Sample)  
Plotted pairwise scatter plots for a 500-row sample to explore feature interactions and patterns.

---

## 📊 Sample Visualizations

> ⚠️ Note: Replace the placeholders below with your actual file paths after uploading images.

### 🔸 Missing Values Heatmap
Visualizes missing/null values across the dataset.  
![Missing Values](plots/missing_values_heatmap.png)

### 🔸 Category of Holdings Distribution
Shows frequency of each holding category in the dataset.  
![Category Count Plot](plots/category_count_plot.png)

### 🔸 Distribution of Area (Ha.)
Displays the area distribution through a histogram.  
![Area Histogram](plots/area_histogram.png)

### 🔸 Boxplot of Area (Ha.)
Highlights outliers and value spread for land area.  
![Area Boxplot](plots/area_boxplot.png)

### 🔸 Correlation Heatmap
Shows correlation between numerical columns like landholding types.  
![Correlation Heatmap](plots/correlation_heatmap.png)

### 🔸 Pairplot of Sampled Data
Explores pairwise relationships between top numerical features.  
![Pairplot](plots/pairplot.png)

---

## 🛠 How to Generate the Plots

All plots are generated in `Untitled.ipynb`.  
To save each plot:

```python
plt.savefig("plots/plot_name.png")
