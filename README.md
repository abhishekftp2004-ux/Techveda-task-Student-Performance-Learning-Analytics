# Student Performance & Learning Analytics

## Project Overview
An end-to-end beginner-friendly data science project that studies student performance patterns using a reproducible synthetic dataset. It demonstrates data cleaning, exploratory data analysis, attendance and subject-related analysis preparation, correlation analysis, feature engineering, visualizations, and introductory prediction.

> **Important:** The included dataset is synthetic and intended for learning. It is not real student data. Subject-wise marks were not included in the brief, so subject-level analysis requires adding real, authorized subject columns or choosing a suitable public dataset.

## Objectives
- Inspect and clean inconsistent data.
- Handle missing values and duplicates.
- Explore attendance, study time, prior scores, assignment completion, and final scores.
- Visualize distributions and relationships.
- Engineer attendance/study bands and a pass/fail target.
- Build and evaluate a score-regression model and a pass/fail classifier.
- Produce reproducible reports and GitHub-ready documentation.

## Tech Stack
Python, Pandas, NumPy, Matplotlib, Seaborn (optional extension), scikit-learn, Jupyter Notebook, Excel, Git/GitHub.

## Dataset Columns
| Column | Description |
|---|---|
| student_id | Synthetic unique student identifier |
| study_hours_per_day | Approximate daily study time |
| attendance_percent | Attendance percentage |
| previous_score | Prior academic score |
| assignment_completion_percent | Assignment completion percentage |
| sleep_hours_per_day | Approximate daily sleep |
| internet_quality | Good / Average / Poor |
| parental_support | High / Medium / Low |
| final_score | Final score (target) |

## Workflow
1. **Data understanding:** inspect shape, types, missing values, duplicates and summary statistics.
2. **Data cleaning:** remove duplicate records, impute numeric values with medians and categorical values with modes, validate percentage ranges.
3. **EDA:** score distribution, attendance vs score, study time vs score, descriptive statistics and correlation matrix.
4. **Attendance analysis:** compare score summaries across attendance bands.
5. **Feature engineering:** attendance bands, study bands and pass/fail label (illustrative threshold 40).
6. **Modeling:** Linear Regression predicts final score; Logistic Regression predicts pass/fail.
7. **Evaluation:** MAE, RMSE and R² for regression; accuracy and class-wise precision/recall/F1 for classification.
8. **Communication:** document findings, limitations and ethical safeguards.

## Setup
```bash
python -m venv .venv
# Windows PowerShell:
.venv\Scripts\Activate.ps1
# Install dependencies:
pip install -r requirements.txt
jupyter notebook
```

Open `notebooks/student_performance_learning_analytics.ipynb` and run cells from top to bottom.

## Files
- `data/student_performance_raw.csv`: raw synthetic data with deliberately introduced missing values and duplicate rows.
- `data/student_performance_clean.csv`: cleaned data.
- `data/student_performance_features.csv`: cleaned data plus engineered bands and pass label.
- `notebooks/student_performance_learning_analytics.ipynb`: annotated end-to-end notebook.
- `reports/`: descriptive statistics, attendance summaries, correlation matrix, model metrics, plots and project summary.

## Key Interpretation Guidance
Do not assume that attendance or study hours cause better performance based on correlation alone. Model metrics are valid only for this generated dataset and split. Evaluate any real-world model on representative, authorized data and compare against a baseline.

## Ethics and Limitations
- Synthetic data cannot support claims about real students.
- Minimize personal data and remove direct identifiers from real datasets.
- Check model errors across relevant groups and avoid unfair use.
- Do not use the model as the sole basis for high-impact educational decisions.
- Subject-wise analysis requires subject-level columns; do not fabricate subject marks.
