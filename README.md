---

## 📌 Dataset

The dataset `student_performance.csv` contains academic and demographic information for students. Key columns include:

| Column | Description |
|---|---|
| `StudentID` | Unique student identifier |
| `Gender` | Student gender |
| `Age` | Student age |
| `School` | School attended (e.g., School_A) |
| `MathScore` | Math exam score |
| `ReadingScore` | Reading exam score |
| `WritingScore` | Writing exam score |
| `StudyTime` | Weekly study time |
| `Absences` | Number of absences |
| `Failures` | Number of past failures |
| `TestPreparation` | Test prep course completion status |
| `ParentEducation` | Parent's education level |
| `FamilySupport` | Family academic support |
| `ExtraCurricular` | Extracurricular activity participation |
| `Internet` | Internet access at home |
| `Health` | Health status (scale 1–5) |
| `FinalGrade` | Computed final grade |

---

## 🔬 Project Tasks & Analysis

### Part 1 — NumPy Operations
- Loaded `MathScore`, `ReadingScore`, `WritingScore`, and `Age` as NumPy arrays
- Inspected shapes and dtypes
- Computed NaN counts and descriptive statistics (mean, median, std, min, max)
- Created a **weighted composite score**: `0.4 * Math + 0.3 * Reading + 0.3 * Writing`
- Categorized students into: **Fail / Pass / Merit / Distinction**
- Calculated **Z-scores** for Math
- Applied **square root transformation** to reduce variance
- Stacked arrays into a 2D matrix; computed row-wise and column-wise stats

### Part 2 — Pandas EDA (Tasks 2.5 – 2.9)
- Loaded data into a DataFrame; inspected with `.head()`, `.info()`, `.describe()`
- Analyzed missing value counts and percentages
- **Filtering & Slicing** (Task 2.6): School A / StudyTime / TestPreparation / ParentEducation filters; assigned `NaN` to MathScore where Absences > 15
- **Missing Value Imputation** (Task 2.7): Scores → school-wise mean; Absences → median; Health → mode; FinalGrade → recalculated
- **Feature Engineering** (Task 2.8): Dropped `StudentID`; created `GradeCategory` and `HighAttendance` flag
- **Statistical Analysis** (Task 2.9): Skewness & kurtosis; group-by analysis; full correlation matrix

### Part 3 — Summary Report (Task 10)
- **Score Distribution**: all distributions are approximately symmetric
- **Test Preparation Effect**: Math +4.4% | Reading +15.4% | Writing +11.3%
- **Study Time & Performance**: monotonic positive relationship confirmed
- **Correlation Insights**: ReadingScore (0.85) and WritingScore (0.84) are the strongest FinalGrade predictors

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

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/student-performance-analysis.git
cd student-performance-analysis
```

### 2. Install Dependencies
```bash
pip install numpy pandas matplotlib seaborn jupyter
```

### 3. Launch Jupyter Notebook
```bash
jupyter notebook Data_Science_Project_on_Student_Data.ipynb
```

> ⚠️ Make sure `student_performance.csv` is in the **same directory** as the notebook before running.

---

## 📈 Key Findings

- 📚 **Test preparation** significantly boosts scores — especially Reading (+15.4%) and Writing (+11.3%)
- ⏱️ **More study time** correlates with higher final grades (monotonic relationship)
- 🏫 **School-wise imputation** preserves group-level accuracy for missing scores
- 📉 **High absences** (>15) negatively impact MathScore
- 🔗 **ReadingScore** has the highest correlation with FinalGrade (r = 0.85)

---

## 🙏 Acknowledgements

- Some visualizations and correlation logic were developed with assistance from **Claude AI** and **Google Gemini**
- Dataset used for educational purposes

---

## 📄 License

This project is for academic and educational use only.
