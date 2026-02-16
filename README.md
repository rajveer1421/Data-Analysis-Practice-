# 🎓 Student Performance Factors – End-to-End Exploratory Data Analysis

## 📌 Project Objective
The goal of this project is to discover which academic, lifestyle, and environmental factors influence student exam performance.

The workflow follows a real analyst pipeline:

**Data Loading → Cleaning → Exploration → Visualization → Relationship Study → Correlation Validation → Recommendations**

---

## 📂 Dataset
Source:  
https://www.kaggle.com/datasets/lainguyn123/student-performance-factors/data

The dataset contains information about study habits, attendance, family background, institutional support, and final exam results.

---

## 🧰 Tools & Libraries Used
- Python  
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  

---

## 🔍 Data Preparation & Inspection

### Steps Performed
1. Loaded dataset using `pd.read_csv()`.
2. Used `.info()` to check data types.
3. Verified missing values → **no null values present**.
4. Removed duplicate rows.
5. Used `.describe()` to analyze:
   - mean  
   - standard deviation  
   - minimum & maximum  
   - quartiles / IQR  

### Result
Data was already very clean → more time could be invested in extracting insights.

---

## 🧾 Column Segregation

### Numerical Columns
```
['Hours_Studied', 'Attendance', 'Sleep_Hours', 'Previous_Scores',
 'Tutoring_Sessions', 'Physical_Activity', 'Exam_Score']
```

### Categorical Columns
```
['Parental_Involvement', 'Access_to_Resources',
 'Extracurricular_Activities', 'Motivation_Level', 'Internet_Access',
 'Family_Income', 'Teacher_Quality', 'School_Type', 'Peer_Influence',
 'Learning_Disabilities', 'Parental_Education_Level',
 'Distance_from_Home', 'Gender']
```

---

# 📊 Univariate Analysis

Goal: understand each variable independently.

---

## Numerical Features – Histogram Insights

Histograms were plotted using matplotlib subplots (3 per row).

### Observations
- **Hours_Studied** → most students studied **18–22 hours**.
- **Attendance** → large cluster around **~70%**.
- **Sleep_Hours** → majority sleep **7–8 hours**.
- **Previous_Scores** → common peak near **80**.
- **Tutoring_Sessions** → most attend **0–2 sessions**.
- **Physical_Activity** → typically **3–4 hours**.
- **Exam_Score** → many students score around **70**.

### Interpretation
Students generally lie in moderate ranges; extreme behaviors are rare.

---

## Numerical Features – Boxplot Analysis

Boxplots were drawn to:
- confirm median  
- understand spread  
- identify outliers  

### Findings
- Few extreme values.
- Data distribution is stable and reliable.

---

---

## Categorical Features – Distribution Summary

| Feature | Key Finding |
|---|---|
| Parental Involvement | Medium ~51%, High ~29%, Low ~20% |
| Access to Resources | Medium ~50%, High ~30%, Low ~20% |
| Extracurricular Activities | ~60% participate |
| Motivation Level | Mostly medium |
| Internet Access | ~92% have access |
| Family Income | Low & medium nearly equal |
| Teacher Quality | Majority medium |
| School Type | Mostly public |
| Peer Influence | Positive & neutral similar |
| Learning Disabilities | ~90% none |
| Parental Education | Mostly high school |
| Distance from Home | Majority near |
| Gender | ~58% male, ~42% female |

### Interpretation
Most students come from balanced or mid-level support environments.

---

---

# 🔗 Bivariate Analysis

Goal: understand which variables move with **Exam_Score**.

---

## Scatter Plot Findings

### Hours Studied vs Exam Score
Clear positive relationship → more study generally improves marks.

### Attendance vs Exam Score
Strongest visible trend → better attendance aligns with higher performance.

### Sleep Hours vs Exam Score
No strong linear pattern.

### Previous Scores vs Exam Score
Weak positive association.

### Tutoring Sessions vs Exam Score
Mild improvement but not dramatic.

### Physical Activity vs Exam Score
Minimal impact.

### Exam Score vs Exam Score
Perfect correlation with itself → analytically useless.

---

## Line Plot Observations

Line graphs reinforced:
- steady improvement with attendance  
- upward trend with study hours  

Other variables remain relatively flat.

---

---

# 🌡 Correlation & Heatmap – Statistical Validation

To verify visual findings, Pearson correlation was computed.

## Correlation with Exam Score

| Feature | Correlation |
|---|---|
| Attendance | **0.58** ⭐ |
| Hours_Studied | **0.45** |
| Previous_Scores | 0.18 |
| Tutoring_Sessions | 0.16 |
| Physical_Activity | 0.03 |
| Sleep_Hours | ~0 |

---

## Meaning

- Attendance is the **strongest performance driver**.
- Study hours are the second most important factor.
- Academic history provides some advantage.
- Lifestyle variables show weak direct effect.

---

---

# 🧠 Final Recommendations

If schools want maximum improvement impact, they should prioritize:

1. Increasing attendance rates  
2. Encouraging structured study time  
3. Supporting historically weaker students  

Focusing only on sleep or activity will not significantly change academic outcomes.

---

---

# 💼 Recruiter Value

This project proves ability to:

✔ work with clean real-world datasets  
✔ perform structured EDA  
✔ combine visuals with statistics  
✔ avoid misleading conclusions  
✔ translate numbers into decisions  

---

---

# 🚀 Future Work

Possible extensions:
- Predict exam scores using regression models  
- Build risk identification systems  
- Feature importance ranking  
- What-if performance simulations  

---

## 👤 Author
Project created as practical training for real industry-style analytical thinking and decision support.

## ⭐ Support the Work
If you found this analysis useful, insightful, or reusable in your own learning, consider supporting it on Kaggle:

👉 https://www.kaggle.com/code/rajveergup1455/complete-eda

Your feedback and upvotes help improve future projects and motivate deeper research.

