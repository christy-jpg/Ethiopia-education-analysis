#  Predicting Ethiopian Student Academic Performance Using Machine Learning

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-black)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

---

## 📌 Project Overview

Education shapes the future of individuals and nations, yet student performance is often discussed emotionally rather than scientifically.

As someone who personally experienced the pressure of the Ethiopian Grade 12 national entrance examination, I wanted to investigate a deeper question:

> **What truly drives student success?**  
> Is it family background? School resources? Student behaviour? Or something else entirely?

To answer this, I analyzed a large Ethiopian student dataset using **Machine Learning, Statistical Testing, and Predictive Modeling**.

This project combines data science with a real educational challenge affecting thousands of students.

---

## 🎯 Objectives

This project was designed to answer five major questions:

- Can student academic performance be predicted accurately?
- Which factors most strongly influence performance?
- Do school resources matter more than family background?
- Does student behaviour improve prediction accuracy?
- Are there statistically significant differences across gender, region, school type, and internet access?

---

## 📂 Dataset

**Source:** Kaggle – Ethiopian Students Dataset

The dataset employed here is a simulated version of a real Ethiopian education dataset, specifically crafted to reflect the characteristics and challenges of actual student records. Real government data of this nature is confidential and inaccessible, making this simulated dataset an invaluable resource for this study.The raw dataset is a vary rich data covering demographics, parental background, school characteristics, attendance, homework, and national examination results.

Due to GitHub file size limitations, the dataset is hosted externally.

Processed dataset used in this project is loaded directly within the notebook.

Original source: [https://www.kaggle.com/datasets/yeneinehseiba/ethiopian-students-data]

### Raw Dataset Size:

- **100,000 student records**
- **634 original variables**

### Included Information:

- Demographics
- Region
- Parent education
- School type
- School location
- Internet & electricity access
- Attendance
- Homework completion
- Class participation
- Test scores
- National exam scores

### Final Cleaned Dataset:

After preprocessing and feature selection:

- **15 contextual predictors**
- **4 behavioural engineered features**
- **3 academic target variables**

---

## 🧹 Data Cleaning & Preprocessing

The raw dataset required substantial cleaning before modelling.

### Steps Performed:

✅ Removed leakage-prone grade score variables  
✅ Converted Date of Birth → Age  
✅ Encoded categorical variables  
✅ Handled missing values  
✅ Created behavioural aggregate variables  
✅ Selected interpretable predictors only

---

## 🎯 Target Variables

The models predicted:

- **Total_Test_Score**
- **Overall_Average**
- **Total_National_Exam_Score**

---

# 🤖 Machine Learning Models

---

## 🔹 Model 1: Contextual Factors Only

Used:

- Family background
- School resources
- Parent education
- Region
- Gender
- Infrastructure
- Age

### Results

| Target | R² Score |
|-------|----------|
| Total Test Score | 0.572 |
| Overall Average | 0.574 |
| National Exam Score | 0.096|

### Interpretation

Contextual factors explain internal school performance moderately well, but are weak predictors of national exam outcomes.

---

## 🔹 Model 2: Context + Behavioural Factors

Added engineered features:

- Attendance Mean
- Homework Mean
- Participation Mean
- Engagement Index

### Results

| Target | R² Score |
|-------|----------|
| Total Test Score | 0.79 |
| Overall Average | 0.79 |
| National Exam Score | 0.40 |

### Interpretation

Student behaviour dramatically improved prediction performance.

This suggests:

> Environment matters but engagement turns opportunity into results.

---

# 📈 Most Important Predictors

Across both models, strongest variables included:

1. School Resources Score  
2. Engagement Index  
3. School Academic Score  
4. Homework Completion  
5. Participation  
6. Parental Involvement

---

# 📊 Statistical Hypothesis Testing

---

## ANOVA Tests

Tested whether performance differs across:

- Region
- School Type
- Health Condition

### Key Findings:

✅ Region significantly affects performance  
✅ School Type strongly affects performance  
✅ Health issues affect internal scores  
❌ Health issue did not significantly affect national exam scores

---

## Independent T-Tests

### Gender Performance

- Male Mean = 314.69  
- Female Mean = 314.58  
- p = 0.660

✅ No significant difference

### Internet Access

- With Internet = 315.51  
- Without Internet = 314.33  
- p < 0.001

✅ Significant advantage

---

# 🏫 Educational Insights

## Highest Performing School Type

| School Type | Avg National Score |
|------------|-------------------|
| Private | 326.59 |

## Lowest Performing School Type

| School Type | Avg National Score |
|------------|-------------------|
| Community | 310.86 |

---

## Highest Performing Region

| Region | Avg National Score |
|-------|-------------------|
| Addis Ababa | 317.45 |

## Lowest Performing Region

| Region | Avg National Score |
|-------|-------------------|
| Benishangul-Gumuz | 313.72 |
---

# 📖 Final Discussion

This project revealed that student achievement is not determined by one single factor.

Academic success appears to operate through **two layers**:

## Layer 1: Structural Opportunity

- School resources  
- Family support  
- Infrastructure  
- Region  
- Parent education

These create the conditions for learning.

## Layer 2: Student Engagement

- Attendance  
- Homework  
- Participation

These determine whether opportunity becomes performance.

That explains why Model 2 significantly outperformed Model 1.

A student may attend a strong school, but without engagement, performance suffers.

Likewise, a motivated student can outperform expectations even under weaker conditions.

---

# 🧠 Real-World Implications

This study suggests that improving education requires more than building schools.

If we want better student outcomes, we should not only ask students to work harder.

We should also ask:

- Are schools equipped?  
- Are classrooms manageable?  
- Are parents supported?  
- Are students engaged?  
- Are regions equally resourced?  
- Is technology accessible?

Because student success is not only built by effort.

It is built by systems.

And when systems improve, students rise with them.

---

## Closing Statement

This project used machine learning to predict scores.

But its deeper purpose was something more meaningful:

**To show that behind every score is a story and behind every story is a system that can be improved.**


## Policymakers should focus on:

### Infrastructure

- Resources
- Teacher support
- Internet access

### Behavioural Support

- Attendance programs
- Homework systems
- Student engagement strategies

### Equity

- Support underperforming school types
- Reduce regional gaps

---

# 💻 Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Scikit-Learn
- Google Colab

---

# 🚀 Future Improvements

- Use real government education data
- Add deep learning models
- Predict dropout risk
- Time-series student tracking
- Explainable AI dashboards

