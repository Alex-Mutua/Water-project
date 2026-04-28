#  Optimizing Revenue Management for Sustainable Water Distribution  
### QUATECH Senegal – Customer Data Analysis

##  Overview
This project analyzes the decline in **Water Development Fund (FDE)** revenues at QUATECH Senegal despite increasing water production.

A **data-driven approach** is used to uncover key drivers of revenue decline and support strategic decision-making.

---

##  Problem Statement
Why are FDE revenues decreasing despite increased water production and high payment compliance?

---

##  Objectives
- Segment subscribers based on **consumption and payment behavior**
- Analyze **billing and payment trends**
- Identify key factors driving **FDE revenue decline**
- Build predictive models for **revenue estimation**

---

## 📊 Dataset
- **Size:** 1.14M records, 23 features  
- **Period:** 2014 – 2019  
- **Region:** Saint-Louis (Region 4)  
- Includes:
  - Consumption (cubage)
  - Billing & payments
  - Customer category (Private/Admin)
  - Financial metrics (FDE, VAT, FNE)

---

##  Data Preprocessing
- Renamed variables for clarity  
- Converted date and monetary fields  
- Handled missing values (`PAY_DATE` retained for delay analysis)  
- Removed extreme anomalies (outliers in FDE)  
- Encoded categorical variables  
- Feature engineering:
  - `PAYMENT_DELAY`
  - Time-based features  

---

##  Key Insights
- FDE revenue **peaked in 2017**, declined sharply after  
- **94.5% pay on time**, but revenue still drops  
- **Administrative customers consume ~87.5%** of water  
- Revenue concentrated in few regions:
  - Bakel (**52.6%**)
  - Foundiougne (**13.5%**)
  - Birkelane (**12.1%**)  
- Average payment delay ≈ **30 days**

---

##  Methodology
### 1. Exploratory Data Analysis (EDA)
- Trend analysis (FDE over time)
- Payment behavior analysis
- Regional contribution analysis

### 2. Dimensionality Reduction
- **PCA** to identify key behavioral patterns:
  - Axis 1 → Consumption & billing
  - Axis 2 → Payment behavior

### 3. Modeling
- Regression Models:
  - **Ridge** (best performance)
  - Lasso
- Neural Network:
  - MLP Regressor

### 4. Feature Selection
- RFE used to select most relevant predictors:
  - Consumption variables
  - VAT, FNE, sanitation

---

## 📈 Model Performance
| Model | RMSE | Notes |
|------|------|------|
| Ridge | 13 | Best overall |
| Lasso | 430 | Less stable |
| Neural Network | 1350 | Improved after feature selection |

---

##  Key Findings
- Revenue decline is **not driven by payment rates**
- Likely drivers:
  - High consumption concentration (Admin users)
  - Regional dependency
  - External or structural factors

---

##  Recommendations
### Revenue Optimization
- Target **high-consumption administrative users**
- Implement **payment monitoring & incentives**

### Segmentation & Strategy
- Focus on key regions (Bakel, Foundiougne, Birkelane)
- Use predictive models for **risk detection**

### Operations
- Improve **billing efficiency**
- Reduce payment delays via automation

### Awareness
- Educate users on the role of FDE

### Growth
- Diversify revenue sources (e.g., additional services)

---

## 🛠️ Tech Stack
- Python (Pandas, NumPy)
- Visualization: Matplotlib, Seaborn, Plotly
- Machine Learning: Scikit-learn
- Deep Learning: TensorFlow / Keras
- Statistics: Statsmodels, SciPy

---

##  Conclusion
This project provides a **robust analytical framework** to:
- Understand FDE revenue decline
- Identify high-impact customer segments
- Support **data-driven policy and operational decisions**

---

## 👤 Author
**Mutua Vundi**  
Data Scientist

---
