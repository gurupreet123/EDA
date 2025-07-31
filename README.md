# Exploratory Data Analysis of Agricultural Holdings in India

## 📝 Project Overview

This project provides a comprehensive Exploratory Data Analysis (EDA) of an agricultural holdings dataset from India. The analysis involves data cleaning, processing, and visualization to uncover key insights, patterns, and relationships within the data. The entire process is documented in the `Untitled.ipynb` Jupyter Notebook.

---

## 📊 Dataset

The dataset used is `gurupreetdhande20_17538577291145594.csv`. It contains detailed information about agricultural land holdings, categorized by state, district, social group, land area size, and the type of ownership (e.g., wholly owned, leased, etc.).

---

## 🛠️ Methodology

The analysis follows a structured approach to ensure the data is clean and the insights are reliable.

1.  **Data Loading and Initial Inspection**: The dataset was loaded into a pandas DataFrame. Initial checks were performed using `.head()`, `.info()`, and `.describe()` to understand its structure, data types, and basic statistics.

2.  **Data Cleaning**:
    * **Column Name Standardization**: The original long and complex column names were cleaned by removing special characters, converting them to lowercase, and making them more readable.
    * **Data Integrity Check**: The dataset was checked for missing values and duplicate rows. **No missing values or duplicates were found**, indicating a high-quality dataset.

3.  **Univariate Analysis**: Individual variables were analyzed to understand their distributions.
    * **Numerical Columns**: Histograms were generated for all numerical features to visualize their distribution and skewness.
    * **Categorical Columns**: Count plots were created for categorical features like `State`, `Social_Group`, and `Category_Of_Holdings` to see the frequency of each category.

4.  **Bivariate and Multivariate Analysis**: Relationships between two or more variables were explored.
    * **Correlation Heatmap**: A heatmap of the correlation matrix was created to identify linear relationships between numerical variables.
    * **Scatter Plot**: A scatter plot was used to visualize the direct relationship between the number of holdings and their corresponding area.
    * **Box Plot**: A box plot was generated to compare the distribution of holding areas across different holding categories.

---

## 📈 Key Visualizations & Insights

Below are some of the key findings from the analysis:

### State-wise Distribution of Holdings
The analysis of categorical data revealed that the dataset is not uniformly distributed across all states. A few states contribute the majority of the data points, with **Uttar Pradesh** having the highest number of entries.

### Correlation Between Land Metrics
The heatmap reveals strong positive correlations between the number of holdings of a certain type and their corresponding area. This is an expected relationship and confirms the consistency of the data. For instance, `whollyownedholdingsnum` is highly correlated with `whollyownedareaha`.

### Area Distribution by Holding Category
The box plot clearly demonstrates that the median area of holdings increases as the category moves from **'Marginal'** to **'Large'**. This visualization effectively shows the vast difference in land size between small and large agricultural holdings.

---

## ⚙️ Dependencies

This project uses the following Python libraries:
* pandas
* numpy
* matplotlib
* seaborn

To install the necessary libraries, you can run:
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

---

## 🚀 How to Run

1.  **Clone the repository**:
    ```bash
    git clone <your-repository-url>
    ```
2.  **Navigate to the project directory**:
    ```bash
    cd <project-folder-name>
    ```
3.  **Install the dependencies** as mentioned above.
4.  **Launch Jupyter Notebook**:
    ```bash
    jupyter notebook
    ```
5.  Open the `Untitled.ipynb` file and run the cells sequentially to reproduce the analysis.

---

## ⚙️ Conclusion 

This Exploratory Data Analysis successfully transformed the raw agricultural holdings data into a clean, well-understood dataset. The process confirmed the high quality of the data, as it contained no missing values or duplicate entries, which provides a strong foundation for any subsequent analysis.

Key insights revealed a significant geographic concentration of data, with a majority of entries originating from Uttar Pradesh. The analysis of distributions highlighted that most land holdings are classified as "Marginal" and are small in area, a trend supported by the right-skewed nature of the data. Furthermore, the strong positive correlations between the number of holdings and their total area confirmed the dataset's internal consistency.

In conclusion, this EDA provides a solid baseline understanding of the agricultural holdings landscape as represented in this dataset. The findings are crucial for anyone looking to perform more advanced modeling, such as predicting land area based on ownership type and location, or for policymakers interested in land distribution patterns. The project serves as a clear example of a complete data analysis workflow, from initial cleaning and debugging to insightful visualization.
