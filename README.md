# 📊 Student Performance Data Analysis

A comprehensive data science project analyzing student academic performance using **NumPy**, **Pandas**, **Seaborn**, and **Matplotlib**.

---

## 📁 Project Structure

    student-performance-analysis/
    ├── Data_Science_Project_on_Student_Data.ipynb
    ├── student_performance.csv
    └── README.md

---

## 📌 Dataset

| Column | Description |
|---|---|
| `StudentID` | Unique student identifier |
| `Gender` | Student gender |
| `Age` | Student age |
| `School` | School attended |
| `MathScore` | Math exam score |
| `ReadingScore` | Reading exam score |
| `WritingScore` | Writing exam score |
| `StudyTime` | Weekly study time |
| `Absences` | Number of absences |
| `Failures` | Number of past failures |
| `TestPreparation` | Test prep course status |
| `ParentEducation` | Parent's education level |
| `FamilySupport` | Family academic support |
| `ExtraCurricular` | Extracurricular participation |
| `Internet` | Internet access at home |
| `Health` | Health status (scale 1–5) |
| `FinalGrade` | Computed final grade |

---

## 🔬 Project Tasks & Analysis

### Part 1 — NumPy Operations
- Loaded scores and age as NumPy arrays
- Computed descriptive statistics (mean, median, std, min, max)
- Created weighted composite score: `0.4 * Math + 0.3 * Reading + 0.3 * Writing`
- Categorized students: **Fail / Pass / Merit / Distinction**
- Calculated Z-scores and applied square root transformation
- Stacked arrays into 2D matrix for row/column-wise stats

### Part 2 — Pandas EDA (Tasks 2.5 – 2.9)
- Inspected data with `.head()`, `.info()`, `.describe()`
- Filtering & Slicing: school, study time, test prep, parent education filters
- Missing Value Imputation: scores → school-wise mean; absences → median; health → mode
- Feature Engineering: `GradeCategory` and `HighAttendance` columns
- Statistical Analysis: skewness, kurtosis, group-by, correlation matrix

### Part 3 — Summary Report (Task 10)
- Score distributions are approximately symmetric
- Test Preparation Effect: Math +4.4% | Reading +15.4% | Writing +11.3%
- Study time has a monotonic positive relationship with final grade
- ReadingScore (0.85) and WritingScore (0.84) are strongest FinalGrade predictors

---

## 🛠️ Tech Stack

| Tool | Version |
|---|---|
| Python | 3.x |
| NumPy | ≥ 1.24 |
| Pandas | ≥ 2.0 |
| Matplotlib | ≥ 3.7 |
| Seaborn | ≥ 0.12 |
| Jupyter Notebook | ≥ 7.0 |

---

## 🚀 Getting Started

**1. Clone the repository**

    git clone https://github.com/AloneMask001/Student-Performance-Data-Analysis.git
    cd Student-Performance-Data-Analysis

**2. Install dependencies**

    pip install numpy pandas matplotlib seaborn jupyter

**3. Launch Jupyter Notebook**

    jupyter notebook Data_Science_Project_on_Student_Data.ipynb

---

## 📈 Key Findings

- 📚 Test preparation boosts scores — Reading (+15.4%) and Writing (+11.3%) most
- ⏱️ More study time correlates with higher final grades
- 🏫 School-wise imputation preserves group-level accuracy
- 📉 High absences (>15) negatively impact MathScore
- 🔗 ReadingScore has the highest correlation with FinalGrade (r = 0.85)

---

## 🙏 Acknowledgements

- Some visualizations developed with assistance from **Claude AI** and **Google Gemini**
- Dataset used for educational purposes

---

## 📄 License

This project is for academic and educational use only.
