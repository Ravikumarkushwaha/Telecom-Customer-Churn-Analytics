# Telecom Customer Churn Analytics

**Business Intelligence Dashboard using Big Data Analytics**

An end-to-end customer churn analytics project combining Python, machine learning, and Microsoft Power BI to analyze customer behavior, identify churn patterns, and predict customers who may be likely to leave a telecom company.

## Project Overview

Customer churn is a major challenge for subscription-based businesses. This project analyzes telecom customer data through descriptive, diagnostic, and predictive analytics to help identify high-churn segments and support targeted customer retention strategies.

The project includes three interactive Power BI report pages:

1. **Executive Overview — What is happening?**  
   Summarizes the customer base, churn rate, contract patterns, internet services, and payment methods.

2. **Customer & Service Analysis — What factors are associated with churn?**  
   Examines customer demographics, tenure, technical support, and monthly charges to identify patterns associated with churn.

3. **ML Prediction & Risk Analysis — Who is likely to churn?**  
   Uses K-Nearest Neighbors (KNN) predictions to examine churn probability, customer risk categories, and predicted churn across service types.

## Objectives

- Analyze historical telecom customer data.
- Identify customer segments associated with higher churn.
- Explore relationships between churn, contract type, tenure, service usage, and monthly charges.
- Train and compare machine-learning classification models.
- Evaluate models using standard classification metrics.
- Visualize business insights and predicted customer risk in Power BI.
- Recommend data-driven customer retention strategies.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Data preparation and machine learning |
| Pandas and NumPy | Data manipulation |
| Scikit-learn | Model training and evaluation |
| Jupyter Notebook | Experimentation and analysis |
| Microsoft Power BI | Interactive dashboards and visualization |
| Power Query | Data cleaning and transformation |
| DAX | Measures and calculated columns |
| Git and GitHub | Version control and project sharing |

## Dataset

The project uses the publicly available **Telco Customer Churn** dataset.

**Source:** [Kaggle — Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn/data)

The dataset contains customer demographic information, account details, subscribed services, billing information, and churn status.

The project report describes 7,043 original customer records and a separate 1,407-row dataset used for machine-learning prediction analysis. Refer to the included data files and notebook for the exact preprocessing and evaluation workflow.

### Data tables

| Table | Purpose |
|---|---|
| `Customer_Details` | Demographics, contracts, tenure, and billing information |
| `Customer_Services` | Phone, internet, and additional services |
| `Churn_Analysis` | Actual customer churn outcome |
| `Telecom_ML` | Machine-learning predictions, churn probabilities, and risk categories |

**Churn encoding:** `0` represents retained/no churn, while `1` represents churned.

**Note:** The ML table contains 1,407 customers and is used for the predictive dashboard. It is a separate analysis set, not the entire customer population.

## Machine Learning

Five classification algorithms were compared:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Random Forest
- Support Vector Machine (SVM)

KNN was selected for the predictive dashboard based on the model comparison.
### Reported KNN performance

| Metric | Score |
|---|---:|
| Accuracy | 76.19% |
| Precision | 54.96% |
| Recall | 57.75% |
| F1-score | 56.32% |
| ROC-AUC | 78.59% |

The model implementation and evaluation details.

## Key Findings

The Power BI dashboards highlight the following findings:

- The overall reported customer churn rate is **26.54%**.
- Month-to-month contracts show a much higher churn rate than long-term contracts.
- Fiber Optic customers have a higher observed churn proportion than other internet-service groups.
- Customers with shorter tenure show substantially higher churn rates.
- The `$60–$90` monthly charge band has the highest reported churn rate among the displayed charge bands.
- The predictive dashboard identifies **393 predicted churn customers**, including **185 high-risk customers**, within its 1,407-customer analysis set.

These findings describe patterns in the analyzed data and do not establish that any single customer characteristic causes churn.

## Power BI Dashboards

The report contains three pages:

### Dashboard 1 — Executive Overview
Provides overall customer KPIs and churn breakdowns by contract, internet service, and payment method.

### Dashboard 2 — Customer & Service Analysis
Explores churn patterns by gender, tenure, technical support, and monthly charge band.

### Dashboard 3 — ML Prediction & Risk Analysis
Displays customer risk distribution, churn probability bands, predicted churn by contract and risk, and predicted churn by internet service alongside average churn probability.

Dashboard screenshots can be placed in the `images/` folder.

## Repository Structure

```text
Telecom-Customer-Churn-Analytics/
├── data/
│   ├── Customer_Details.csv
│   ├── Customer_Services.csv
│   ├── Churn_Analysis.csv
│   ├── Telecom_ML.csv
│   
├── notebooks/
│   └── Telecom_project.ipynb
├── powerbi/
│   └── Telecom_Customer_Churn.pbix
├── reports/
│   ├── Project_Report.pdf
│   └── Project_Presentation.pptx
├── images/
│   ├── dashboard_1.png
│   ├── dashboard_2.png
│   └── dashboard_3.png
|--- Video
├── README.md
└── .gitignore
```

## How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/Telecom-Customer-Churn-Analytics.git
cd Telecom-Customer-Churn-Analytics
```

Replace `YOUR-USERNAME` with your GitHub username.

### 2. Install Python dependencies

Create and activate a virtual environment if desired, then install the libraries used by the notebook:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
```

If the notebook imports additional libraries, install those as well.

### 3. Run the notebook

```bash
jupyter notebook
```

Open the notebook inside `notebooks/` and run its cells in order. Update dataset paths if necessary.

### 4. Open the Power BI report

Open the `.pbix` file in Microsoft Power BI Desktop. If the report uses local CSV files, update the source paths to the location of the `data/` folder and refresh the data.

## Recommendations

Based on the dashboard findings, the project recommends:

- Prioritize customers classified as high risk for retention outreach.
- Explore suitable incentives for month-to-month customers to consider longer contracts.
- Improve onboarding and engagement during the early customer lifecycle.
- Review support and service experiences for customer groups with higher churn.
- Use churn probabilities and risk categories to help prioritize retention resources.


## Authors

**Ravi Kumar Kushwaha**  
**Mukund Kuthe**

Symbiosis Institute of Technology, Nagpur  
B.Tech — Computer Science and Engineering  
Course: Big Data Analytics  
Academic Year: 2026–27

