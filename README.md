# 👔 HR Employee Attrition & Analytics — Exploratory Data Analysis

A complete data analysis project on IBM HR Employee data to identify attrition patterns, salary trends, work-life balance issues, and job satisfaction insights using Python.

---

## 📌 Project Overview

This project performs end-to-end Exploratory Data Analysis (EDA) on an HR dataset of **1,470 employees** across **35 features**. The goal is to help HR teams understand why employees leave, who is at high attrition risk, and what factors affect job satisfaction and performance.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core programming language |
| Pandas | Data manipulation and GroupBy analysis |
| NumPy | Feature engineering with `np.where` |
| Matplotlib | Data visualization |
| Jupyter Notebook | Interactive development environment |

---

## 📂 Project Structure

```
hr-employee-attrition-eda/
│
├── HR.ipynb              # Main analysis notebook
├── HR_Employee.csv       # Raw dataset (1470 employees, 35 features)
├── HR_Final_CSV.csv      # Processed dataset with engineered features
├── Subplot.png           # Combined visualization dashboard
└── README.md             # Project documentation
```

---

## 📊 Dataset Info

- **Source:** IBM HR Analytics Employee Attrition Dataset
- **Records:** 1,470 employees
- **Features:** 35 columns (Age, Department, MonthlyIncome, Attrition, OverTime, JobSatisfaction, WorkLifeBalance, and more)
- **Target:** `Attrition` — whether an employee left the company (Yes/No)

---

## 🔍 Analysis Workflow

### 1. 📦 Data Understanding
- Shape, column info, data types
- Statistical summary with `describe()`
- Missing value check

### 2. 🧹 Data Cleaning
- Removed duplicate rows
- Handled missing values
- Dropped irrelevant columns: `EmployeeCount`, `Over18`, `StandardHours`

### 3. ⚙️ Feature Engineering
Created 4 new meaningful columns:

| New Column | Logic |
|------------|-------|
| `income_category` | Low (<5K), Medium (5K–10K), High (>10K) |
| `experience_level` | Fresher (<5 yrs), Mid Level (5–9 yrs), Senior (>9 yrs) |
| `work_life_category` | Poor (<2), Average (2–4), Good (≥4) |
| `attrition_risk` | High / Medium / Low Risk based on OverTime + Satisfaction + WorkLife |

### 4. 🔎 Filtering Operations
- Employees working overtime
- Low job satisfaction employees
- High income employees (≥15K)
- Employees who left the company
- Low work-life balance employees

### 5. 📊 GroupBy Analysis
- Department-wise attrition count
- Gender-wise attrition
- Salary category vs attrition
- Overtime vs attrition
- Job role vs average satisfaction
- Work-life balance vs attrition

### 6. 🏆 Top / Bottom Analysis
- Top 10 highest salary employees
- Bottom 10 job satisfaction scores
- Most experienced employees
- Overtime impact on attrition and satisfaction

### 7. 📈 Visualizations

| Chart Type | What it Shows |
|------------|--------------|
| Bar Chart | Department vs Attrition, JobRole vs Satisfaction, Gender vs Attrition |
| Line Plot | Experience vs Monthly Income trend |
| Histogram | Monthly Income Distribution, Age Distribution |
| Scatter Plot | Age vs Income, WorkLifeBalance vs JobSatisfaction |
| Pie Chart | Attrition %, Department % |
| Subplots | Full 10-chart dashboard (saved as `Subplot.png`) |

### 8. 💡 Key Insights
- Employees with standard working hours have better satisfaction and lower attrition
- Low work-life balance is a strong predictor of attrition
- Sales and Research departments show higher attrition rates
- Low-income employees are more likely to leave
- Experience strongly correlates with higher monthly income
- Managers have the highest average salary across all job roles

### 9. 📋 Final Report
- Printed high-risk employee list
- Department attrition summary
- Salary and work-life balance insights

### 10. 💾 Export
- Processed data exported to `HR_Final_CSV.csv`

---

## ▶️ How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/priyanshupatel-tech/hr-employee-attrition-eda.git
   cd hr-employee-attrition-eda
   ```

2. Install required libraries:
   ```bash
   pip install pandas numpy matplotlib jupyter
   ```

3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook HR.ipynb
   ```

---

## 👤 Author

**[Priyanshu Patel]**
- GitHub: (https://github.com/priyanshupatel-tech)
- LinkedIn:(https://linkedin.com/in/priyanshupatel-tech)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
