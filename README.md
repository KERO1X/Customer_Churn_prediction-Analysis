
## 🧠 Introduction
This project focuses on predicting customer churn using machine learning. The goal is to identify which customers are likely to stop using a service so that companies can take proactive retention measures. The project involves multiple stages including data exploration, data cleaning, feature engineering, model training, and evaluation.

---

## 📊 Dataset Overview
The dataset used in this project comes from IBM Sample Data:
- **Source**: [Telco Customer Churn Dataset](https://www.ibm.com/communities/analytics/watson-analytics-blog/guide-to-sample-datasets/)
- **Records**: 7,043 customer records
- **Features include**:
  - Demographics (gender, senior citizen, partner, dependents)
  - Account information (tenure, contract type, billing method)
  - Service usage (internet service, phone service, streaming)
  - Charges (monthly charges, total charges)
  - Target variable: `Churn` (Yes/No)

| Feature          | Type        | Description                     | Cleaning Needed          |
|------------------|-------------|---------------------------------|--------------------------|
| customerID       | String      | Unique identifier               | Removed for modeling     |
| tenure           | Integer     | Months as customer              | None                     |
| Contract         | Categorical | Service contract type           | Ordinal encoding         |
| MonthlyCharges   | Float       | Recurring fees                  | None                     |
| TotalCharges     | Float       | Lifetime spending               | Fix missing values       |
| PaymentMethod    | Categorical | Payment type                    | One-hot encoding         |
| Churn (Target)   | Binary      | Did customer leave? (Yes/No)    | Label encoding           |

Dataset Size: 7,043 customers × 21 features


---

## 🧹 Data Cleaning Tasks
- Converted `TotalCharges` to numerical and handled missing values
- Removed unnecessary columns (e.g., `customerID`)
- Identified and handled outliers
- Encoded categorical variables using label encoding
- Scaled numerical features for model readiness

---

## ❓ Analytical Questions
- What features are highly correlated with churn?
- Do longer-tenure customers tend to churn less?
- Is monthly charge a strong indicator of churn?
- Do contract types and payment methods impact churn rate?

---

## 📦 Deliverables
- `notebooks/01_EDA.ipynb`: Exploratory Data Analysis
- `notebooks/02_preprocessing.ipynb`: Data Cleaning and Feature Engineering
- `data/WA_Fn-UseC_-Telco-Customer-Churn.csv`: Original Dataset
- `outputs/`: Folder for cleaned dataset and model outputs
- `README.md`: Project documentation
- `requirements.txt`: Project dependencies

---

## ⚙️ How to Run the Project

### Step 1: Clone the Repository
```bash
git clone https://github.com/YOUR_USERNAME/customer-churn-prediction.git
cd customer-churn-prediction
```

### Step 2: Create a Virtual Environment (Optional but Recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```


### Step 3: 📚 Install Required Libraries
Make sure you have pip installed. Then run:

```bash
pip install -r requirements.txt
```
📌Libraries used in this project:

- pandas – for data manipulation
- numpy – for numerical operations
- matplotlib & seaborn – for visualizations
- scikit-learn – for preprocessing, feature scaling, and model building
- plotly – for interactive visualizations (optional)

---

### Step 4: Run Jupyter Notebooks
```bash
jupyter notebook
```

Open `notebooks/01_EDA.ipynb` and `02_preprocessing.ipynb` to explore and process the data.

---

## ✅ Conclusion
This project demonstrates how to explore, clean, and analyze customer churn data to gain business insights. With the cleaned dataset, the next steps include building and evaluating machine learning models to accurately predict churn. These insights can then guide companies in making data-driven retention strategies.
