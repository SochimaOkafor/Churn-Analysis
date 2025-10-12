# Churn-Analysis
# Table of Content
- [Introduction](https://github.com/SochimaOkafor/Churn-Analysis/edit/main/README.md#introduction)
  
- [Dashboard](https://github.com/SochimaOkafor/Churn-Analysis/edit/main/README.md#dashboard)
  
- [Data Sources](https://github.com/SochimaOkafor/Churn-Analysis/edit/main/README.md#data-sources)

- [Data Preprocessing](https://github.com/SochimaOkafor/Churn-Analysis/edit/main/README.md#data-preprocessing)

- [Analysis Methods](https://github.com/SochimaOkafor/Churn-Analysis/edit/main/README.md#analysis-methods)

- [Results](https://github.com/SochimaOkafor/Churn-Analysis/edit/main/README.md#results)

- [Conclusions](https://github.com/SochimaOkafor/Churn-Analysis/edit/main/README.md#conclusions)

- [Tools and Technologies Used](https://github.com/SochimaOkafor/Churn-Analysis/edit/main/README.md#tools-and-technologies-used)

# Introduction 
Customer churn represents the percentage of customers who stop using a company’s product or service during a specific period. Understanding why customers churn is essential for improving retention strategies and increasing profitability.

This project aims to analyze customer churn patterns, identify key factors influencing churn, and provide actionable insights using SQL, Python, and Power BI.

The dataset contains customer demographics, account details, and service usage information. The analysis helps business stakeholders understand customer behavior and make data-driven decisions to reduce churn.
## Dashboard
![Churn Analysis ](https://github.com/user-attachments/assets/d2377f02-79a5-41c1-be09-e72f429ce794)

# Data Sources

- The dataset used for this analysis was sourced from a Telecom Customer Churn dataset (commonly available on Kaggle
).
- The dataset includes customer information such as:

  - Customer demographics (gender, senior citizen, tenure)

  - Account information (contract type, payment method)

  - Service usage details (internet service, tech support, streaming services)

  - Churn label indicating whether the customer left the service
 
# Data Preprocessing
The data preprocessing phase involved multiple steps to ensure data quality and readiness for analysis.

## **Steps Performed:**

1. **Data Cleaning:**
- Handled missing values and duplicates.
- Standardized column names for consistency.
- Converted categorical variables to appropriate formats.
2. **Feature Engineering:**
- Created new metrics such as average monthly spend and tenure groupings.
- Encoded categorical variables for modeling.
3.Exploratory SQL Queries:
- Used SQL to explore key churn indicators (e.g., churn rate by contract type, payment method, and internet service).

4. **Data Transformation (Python):**
- Applied transformations using pandas and numpy.
- Normalized numerical columns where required.

# Analysis Methods
This project used a combination of SQL, Python, and Power BI for a comprehensive churn analysis workflow.

**SQL**
- Used for data exploration, aggregation, and query-based insights.
- Sample queries:
```sql
SELECT Contract, COUNT(*) AS TotalCustomers, 
       SUM(CASE WHEN Churn = 'Yes' THEN 1 ELSE 0 END) AS ChurnedCustomers
FROM Customers
GROUP BY Contract;
```

**Python**
- Used for statistical analysis and machine learning modeling.
- Key libraries: pandas, numpy, matplotlib, seaborn, scikit-learn.
- Steps:
  - Performed exploratory data analysis (EDA) to uncover correlations.
  - Built a logistic regression model to predict churn probability.
  - Evaluated model performance using accuracy, precision, recall, and ROC-AUC metrics.

**Power BI**
- Used for interactive visualization and dashboard creation.
- Developed a Churn Dashboard to display:
  - Overall churn rate
  - Churn by customer segment
  - Churn by contract and service type
  - Key churn drivers and KPIs

# Results

**Key Insights:**
- Customers on month-to-month contracts had the highest churn rate.
- Customers with fiber optic internet were more likely to churn than those with DSL.
- Electronic check payment method was associated with higher churn.
- Longer tenure customers showed significantly lower churn rates.

# Conclusions
- **Retention Focus:** Businesses should prioritize customers with short tenures and flexible contracts.
- **Service Optimization:** Improving the quality of fiber optic services and addressing billing pain points can reduce churn.
- **Future Work:**
  - Apply advanced ML models (e.g., Random Forest, XGBoost) to improve prediction accuracy.
  - Conduct A/B testing on retention campaigns.
  - Integrate real-time churn prediction into a CRM system.

# Tools and Technologies Used

- **SQL:** Data querying and initial exploration
- **Python:** Data preprocessing, analysis, and modeling
- **Power BI:** Interactive visualizations and dashboards
- **Libraries:** pandas, numpy, matplotlib, seaborn, scikit-learn
