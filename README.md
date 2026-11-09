# 📊 Churn Analysis and Customer Intelligence

A Python-based Data Analytics project focused on understanding customer churn, analyzing customer behavior, measuring retention, and identifying potential revenue loss through data cleaning, feature engineering, SQL integration, and interactive visualizations.

## 📌 Project Overview

Customer churn is one of the major challenges faced by subscription-based businesses. Losing customers directly impacts revenue and long-term business growth.

This project analyzes customer, subscription, and customer support data to understand why customers leave, identify churn patterns, evaluate customer retention, and measure revenue at risk.

The project uses Python, Pandas, NumPy, SQL, Matplotlib, and Seaborn to transform raw customer data into meaningful business insights.

## 🎯 Project Objectives

- Analyze overall customer churn and retention rates.
- Identify churn patterns across different subscription plans.
- Understand customer behavior based on subscription and demographic information.
- Calculate Average Revenue Per User (ARPU).
- Measure average customer subscription tenure.
- Identify revenue at risk due to customer churn.
- Analyze the relationship between customer support escalations and churn.
- Categorize customers into different churn-risk levels.
- Visualize trends and patterns to support data-driven decisions.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Data analysis and processing |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical operations and feature engineering |
| SQLite | Database connectivity and SQL operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Jupyter Notebook | Development and analysis environment |

## 📂 Dataset Structure

The project works with a SQLite database named `customer_churn.db`, containing three primary tables:

**1. Customer Table**
- Customer ID
- Customer name
- Gender
- Date of birth
- State
- Country
- Other customer attributes

**2. Subscription Table**
- Customer ID
- Plan type
- Contract type
- Monthly charges
- Subscription start date
- Renewal date
- Cancellation date
- Churn score

**3. Support Table**
- Customer ID
- Complaint date
- Escalation information
- Customer support details

*Note: The database file is required to execute the complete analysis and is not included in the uploaded notebook.*

## ⚙️ Project Workflow

### 1. Data Extraction and Database Connectivity
- Connected Python with SQLite using `sqlite3`.
- Retrieved database tables using SQL queries.
- Loaded individual database tables into Pandas DataFrames.
- Explored table structures and column information.

### 2. Data Cleaning and Preprocessing

Performed the following operations:

- Renamed columns for better readability.
- Removed unnecessary columns such as `interests`, `pincode`, and irrelevant support fields.
- Converted date columns into appropriate datetime formats.
- Standardized gender values (Men → Male, Women → Female).
- Identified missing country values and handled them using state-to-country mapping.
- Checked data types and dataset structure.

### 3. Feature Engineering

Created meaningful features to support customer churn analysis.

**Churn Flag**

Created a binary feature based on cancellation date:
- `1` – Customer has churned.
- `0` – Customer is retained.

**Complaint Count**

Calculated the number of support complaints associated with each customer.

**Customer Tenure**

Calculated the number of days a customer has used the service.

**Churn Risk Categorization**

Classified customers using their churn scores:

| Churn Score | Risk Category |
|---|---|
| Below 50 | Low |
| 50–69 | Medium |
| 70 and above | High |

### 4. Data Integration

- Merged customer, subscription, and support datasets using `customerid`.
- Used LEFT JOIN operations to preserve subscription records.
- Handled duplicate customer support records by retaining the latest complaint record.
- Exported the processed dataset into `exported_churn_data.csv`.

### 5. Exploratory Data Analysis (EDA)

Calculated important business metrics:

| Metric | Description |
|---|---|
| Churn Rate | Percentage of customers who discontinued the service |
| Retention Rate | Percentage of customers retained |
| Churn by Plan | Churn comparison across subscription plans |
| ARPU | Average Revenue Per User |
| Average Tenure | Average duration of customer subscriptions |
| Revenue at Risk | Monthly revenue associated with churned customers |
| Escalation Rate | Percentage of support records with escalations |
| Average Complaints | Average complaint count per customer |
| Escalation vs Churn | Correlation between escalations and customer churn |

### 6. Data Visualization

Created visualizations using Matplotlib and Seaborn to understand customer behavior and identify patterns.

- Monthly Churn Trend – Tracks customer cancellations over time.
- Churn Rate by Plan Type – Compares churn across subscription plans.
- Churn by State – Examines geographical churn patterns.
- Correlation Heatmap – Identifies relationships between numerical and encoded categorical features.
- Pairplot – Visualizes pairwise relationships between selected variables.
- Categorical Comparison Plot – Compares monthly charges across plan types, gender, and churn-risk categories.

### 7. Pivot Table Analysis

Used Pandas pivot tables to summarize:
- Churn rate by subscription plan.
- Total monthly charges.
- Unique customer counts.
- Aggregated customer churn metrics.

## 📈 Key Business Insights

The analysis is designed to help businesses:

- Identify subscription plans with higher customer churn.
- Understand customer retention performance.
- Detect customers belonging to high churn-risk categories.
- Evaluate the potential revenue impact of customer cancellations.
- Understand whether customer support escalations are associated with churn.
- Identify geographical and monthly churn patterns.

## 🚀 How to Run the Project

**Step 1: Clone the repository**

```bash
git clone https://github.com/your-username/churn-analysis.git
```

**Step 2: Navigate to the project directory**

```bash
cd churn-analysis
```

**Step 3: Install the required libraries**

```bash
pip install numpy pandas matplotlib seaborn jupyter
```

**Step 4: Add the database**

Place the required `customer_churn.db` SQLite database file in the project root directory.

**Step 5: Launch Jupyter Notebook**

```bash
jupyter notebook
```

**Step 6: Run the notebook**

Open `churn_analysis.ipynb` and execute the cells sequentially.

## 📁 Project Structure

```text
Churn-Analysis/
│
├── churn_analysis.ipynb
├── customer_churn.db
├── exported_churn_data.csv
├── README.md
│
└── requirements.txt
```

*The database and exported CSV are generated or supplied separately; they are not included in the uploaded notebook.*

## 🔮 Future Enhancements

- Develop a machine learning model to predict customer churn.
- Identify the most influential factors contributing to customer churn.
- Build an interactive customer churn dashboard using Power BI or Streamlit.
- Implement customer segmentation to understand different customer groups.
- Develop a customer retention recommendation system.
- Automate churn monitoring through periodic data updates.

## 👩‍💻 Skills Demonstrated

- Data Cleaning and Preprocessing
- Exploratory Data Analysis (EDA)
- SQL and SQLite Database Connectivity
- Data Manipulation using Pandas
- Feature Engineering using NumPy
- Statistical Analysis and Correlation
- Data Visualization
- Business KPI Analysis
- Data Interpretation and Problem Solving

---

**Project Title:** Churn Analysis and Customer Intelligence  
**Domain:** Data Analytics | Customer Intelligence | Business Analytics  
**Tools:** Python, SQL, Pandas, NumPy, Matplotlib, Seaborn, SQLite

