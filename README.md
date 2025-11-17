#  Student Performance Analysis & GPA Prediction  
A complete Data Science project analyzing student academic & behavioral factors to predict GPA using Exploratory Data Analysis and Machine Learning.

---

##  Dataset  
**Columns:**  
- Numerical: `age`, `studytimeweekly`, `absences`, `gpa`  
- Categorical: `gender`, `ethnicity`, `parentaleducation`, `tutoring`, `parentalsupport`,  
  `extracurricular`, `sports`, `music`, `volunteering`, `gradeclass`  
- ID Column: `studentid` (dropped)

Dataset Source: Kaggle – Student Performance Dataset.

---

## Project Workflow  

### **1 Data Preprocessing**
- Cleaned column names  
- Handled missing values  
- Separated numerical & categorical features  
- Encoded all categorical variables  

### **2 EDA (Exploratory Data Analysis)**
- GPA distribution  
- Relationship of GPA with:
  - Study time  
  - Absences  
  - Parental education  
  - Tutoring  
  - Extracurricular activities  
- Correlation heatmap  
- Outlier detection  

### **3 Machine Learning Models**
Models trained:

| Model | R² Score | MAE | MSE | RMSE |
|-------|---------|---------|---------|--------|
| Linear Regression | 0.9532 | 0.1553 | 0.0387 | 0.1966 |
| Random Forest | 0.9286 | 0.1880 | 0.0591 | 0.2430 |
| Gradient Boosting | 0.9480 | 0.1619 | 0.0430 | 0.2074 |

**Best Model:** Linear Regression (R² = 0.9532)

---

## Final Model
The trained best model (`best_gpa_model.pkl`) is stored inside `/models`.

You can load it using:

```python
import joblib
model = joblib.load("models/model1.pkl")
