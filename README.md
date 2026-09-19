# Healthcare Analytics & Hospital Performance Dashboard

## 📌 Project Overview

This project analyzes a healthcare dataset containing **55,500 patient
records** across **15 variables** covering the period from **May 2019 to
May 2024**.

The objective is to transform raw healthcare data into actionable
insights around:

-   Patient demand
-   Medical-condition distribution
-   Billing performance
-   Length of stay
-   Admission patterns
-   Insurance-provider billing
-   Data-quality issues

The project follows an end-to-end analytics workflow:

**Raw Data → Data Cleaning → Feature Engineering → Exploratory Data
Analysis → Business Analysis → Dashboard → Insights & Recommendations**

------------------------------------------------------------------------

## 🎯 Business Objective

Hospital management needs visibility into patient demand, hospital stay
patterns, billing performance, and data-quality issues to support:

-   Operational planning
-   Financial oversight
-   Resource allocation
-   Data-quality management
-   Management decision-making

This project translates the dataset into business-oriented insights
rather than focusing only on technical exploration.

------------------------------------------------------------------------

## 📊 Dataset

### Dataset Scale

-   **Original records:** 55,500
-   **Original variables:** 15
-   **Time period:** May 2019 -- May 2024
-   **Duplicate records identified:** 534
-   **Records after duplicate removal:** 54,966

### Key Data Areas

The dataset contains information related to:

-   Patient demographics
-   Medical conditions
-   Admission dates
-   Admission types
-   Insurance providers
-   Billing amounts
-   Medication
-   Test results
-   Hospital stays

------------------------------------------------------------------------

## 🛠️ Technologies Used

-   **Python**
-   **Pandas**
-   **NumPy**
-   **Matplotlib**
-   **Seaborn**
-   **Jupyter Notebook**
-   **Google Looker Studio / Dashboarding**

------------------------------------------------------------------------

## 🔄 Project Workflow

### 1. Data Loading

The raw healthcare dataset was imported into Python using Pandas.

### 2. Exploratory Data Analysis

The dataset was examined for:

-   Dataset structure
-   Data types
-   Missing values
-   Duplicate records
-   Unique values
-   Distribution of numerical variables
-   Distribution of categorical variables
-   Relationships between important variables
-   Time-based patterns

### 3. Data Cleaning

The cleaning process included:

-   Duplicate detection and removal
-   Date standardization
-   Categorical-data standardization
-   Data-type conversion
-   Data-quality validation
-   Identification of anomalous billing records

A total of **534 exact duplicate records** were identified and removed.

### 4. Feature Engineering

The following derived features were created:

-   **Admission Year**
-   **Admission Month**
-   **Length of Stay**
-   **Age Group**
-   **Stay Category**

### 5. Analytical Segmentation

The cleaned dataset was analyzed across:

-   Medical condition
-   Age group
-   Admission type
-   Insurance provider
-   Gender
-   Time/month
-   Billing amount
-   Length of stay

### 6. Visualization & Dashboard

An interactive healthcare analytics dashboard was created to communicate
key KPIs and trends.

The dashboard includes:

-   Total Patients
-   Total Billing Amount
-   Average Billing
-   Average Length of Stay
-   Negative Billing Records
-   Patient volume by medical condition
-   Patient distribution by age group
-   Average billing by medical condition
-   Billing by insurance provider
-   Length of stay by admission type
-   Monthly patient admissions
-   Monthly billing trends

Interactive filters are available for:

-   Medical Condition
-   Admission Type
-   Insurance Provider
-   Gender

------------------------------------------------------------------------

## 📈 Key Findings

### 1. Patient Volume Is Broadly Distributed

Patient volume is relatively consistent across the six medical
conditions.

-   Highest volume: **Arthritis --- 9,218 records**
-   Lowest volume: **Asthma --- 9,095 records**
-   Difference: **123 records**

This represents approximately a **1.3% difference** between the highest
and lowest condition volumes.

------------------------------------------------------------------------

### 2. Average Billing Is Consistent Across Medical Conditions

Average billing values are relatively close across the medical
conditions.

-   Highest average billing: **Obesity --- \$25,804**
-   Lowest average billing: **Cancer --- \$25,152**
-   Difference: **\$652**

This indicates that average billing does not vary substantially by
medical condition within this dataset.

------------------------------------------------------------------------

### 3. Admission Type Does Not Meaningfully Differentiate Length of Stay

Average length of stay across:

-   Elective
-   Urgent
-   Emergency

admissions is tightly clustered between approximately **15.40 and 15.58
days**.

The difference between the longest and shortest average stay is only
**0.18 days**, approximately **4.3 hours**.

Therefore, admission type alone does not appear to be a strong
differentiator of length of stay in this dataset.

A limitation is that the dataset does not contain richer clinical
variables such as severity, procedures, and complications that could
help explain length-of-stay variation.

------------------------------------------------------------------------

### 4. Negative Billing Records Require Validation

The analysis identified **106 records with negative billing amounts**.

These records represent a data-quality issue and should not
automatically be treated as valid financial transactions.

The project therefore flags these records for validation rather than
silently removing them.

Before using billing figures for financial reporting or decision-making,
these records should be reviewed and corrected by the appropriate
data/finance teams.

------------------------------------------------------------------------

## 💡 Business Recommendations

### 1. Strengthen Billing Data Validation

Review the 106 negative billing records and introduce automated
validation rules before financial reporting.

### 2. Investigate the Real Drivers of Length of Stay

Since admission type alone shows little variation in length of stay,
future analysis should incorporate clinical factors such as:

-   Patient severity
-   Procedures
-   Complications
-   Other patient-level clinical variables

### 3. Monitor Patient Volume and Billing Together

Patient volume and billing can be monitored by:

-   Medical condition
-   Insurance provider
-   Admission type
-   Time period

This can support operational planning and capacity monitoring.

------------------------------------------------------------------------

## 📁 Project Structure

``` text
Healthcare-Analytics/
│
├── eda.ipynb
│   └── Data cleaning, EDA, feature engineering and analysis
│
├── healthcare_cleaned.csv
│   └── Cleaned dataset used for analysis/dashboarding
│
├── README.md
│   └── Project documentation
│
├── requirements.txt
│   └── Python dependencies
│
├── dashboard.pdf
│   └── Healthcare analytics dashboard/export
│
└── presentation.pptx
    └── Project findings and business recommendations
```

> File names may vary depending on the final repository structure.

------------------------------------------------------------------------

## 🚀 How to Run the Project

### 1. Clone the repository

``` bash
git clone <YOUR-GITHUB-REPOSITORY-URL>
cd <YOUR-REPOSITORY-FOLDER>
```

### 2. Install dependencies

``` bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook

``` bash
jupyter notebook
```

Open:

``` text
eda.ipynb
```

and execute the notebook cells sequentially.

------------------------------------------------------------------------

## 📌 Important Data-Quality Note

The analysis identified **106 negative billing records**.

These records were treated as a data-quality issue requiring validation
rather than being arbitrarily deleted. Consequently, billing-based
conclusions should be interpreted with this limitation in mind until
those records are validated.

------------------------------------------------------------------------

## 📊 Dashboard KPIs

The dashboard provides the following high-level indicators:

  KPI                            Value
  -------------------------- ---------
  Total Patients                54,966
  Total Billing Amount          \~1.4B
  Average Billing              \~25.5K
  Average Length of Stay          15.5
  Negative Billing Records         106

------------------------------------------------------------------------

## 🎓 Project Learning Outcomes

This project demonstrates practical experience with:

-   Data cleaning
-   Exploratory data analysis
-   Data-quality validation
-   Feature engineering
-   Categorical and numerical analysis
-   Time-based analysis
-   Business-oriented data interpretation
-   Dashboard development
-   Communicating analytical findings
-   Translating data findings into business recommendations

------------------------------------------------------------------------

## 🔮 Future Improvements

The current project focuses on Python-based analytics and dashboarding.
Potential extensions include:

-   Adding a **SQL/database layer**
-   Building SQL-based analytical queries
-   Connecting the dashboard directly to a database
-   Automating the data-cleaning pipeline
-   Adding automated data-quality checks
-   Implementing scheduled dashboard/data refresh
-   Incorporating richer clinical variables for deeper length-of-stay
    analysis

------------------------------------------------------------------------

## 👤 Author

**Lakshya Agarwal**

B.Tech --- Computer Science

GitHub: `https://github.com/lakshya-ag31`

LinkedIn: `https://www.linkedin.com/in/lakshya-agarwal-514b1a2a7/`

------------------------------------------------------------------------

## ⭐ Project Summary

This project demonstrates an end-to-end healthcare analytics workflow
that converts raw patient data into cleaned analytical data, business
insights, an interactive dashboard, and management-oriented
recommendations.

**Core pipeline:**

``` text
Raw Healthcare Data
        ↓
Data Quality Assessment
        ↓
Data Cleaning
        ↓
Feature Engineering
        ↓
Exploratory Data Analysis
        ↓
Business Analysis
        ↓
Dashboard
        ↓
Insights
        ↓
Recommendations
```
=======
# Healthcare-Analysis-
