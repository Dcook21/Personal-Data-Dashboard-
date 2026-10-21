# AI Usage in Student Life — Research Dashboard

**Author:** Dallas Cook  
**Date:** July 17, 2025  
**Dataset:** [AI Assistant Usage in Student Life (Synthetic)](https://www.kaggle.com/datasets/ayeshasal89/ai-assistant-usage-in-student-life-synthetic/data) — Kaggle

---

## Research Question

> Does a higher level of AI assistance lead to increased student satisfaction and a greater likelihood of completing assignments in writing tasks?

## Hypothesis

Students who receive a higher level of AI assistance during writing tasks will report higher satisfaction ratings and will be more likely to complete their assignments compared to students who receive a lower level of AI assistance.

---

## Abstract

This study explores whether higher levels of AI assistance influence student satisfaction and assignment completion during writing tasks. Using a synthetic dataset simulating AI assistant usage among students, univariate and bivariate analyses were conducted, followed by an ANOVA and Chi-square test to assess relationships between assistance level, satisfaction rating, and task completion.

Results showed that students receiving higher levels of AI assistance reported significantly greater satisfaction (p = 0.0009) and were more likely to complete their assignments (p = 0.0009). These findings highlight the potential of robust AI support systems to enhance learning experiences and academic performance.

---

## Dataset

| Field | Detail |
|---|---|
| Source | Kaggle — Ayesha Sal89 |
| Type | Synthetic (no real student data) |
| Size | 1,000 sessions |
| Time Period | August 2024 – June 2025 |

**Key Variables:**

| Variable | Description |
|---|---|
| `AI_AssistanceLevel` | Level of AI support (1–5 scale) — Independent Variable |
| `SatisfactionRating` | Student satisfaction score (1.0–5.0) — Dependent Variable |
| `FinalOutcome` | Whether the assignment was completed — Dependent Variable |
| `TaskType` | Type of task (filtered to "Writing" for core analysis) |
| `SessionLengthMin` | Duration of the AI session in minutes |
| `TotalPrompts` | Number of prompts submitted during session |

> See [`data/README.md`](data/README.md) for download instructions.

---

## Analysis Overview

### Exploratory Data Analysis (EDA)
- Shape, data types, missing value assessment
- Summary statistics across all numerical columns
- Univariate distributions (histograms + boxplots) with IQR-based outlier detection

### Bivariate Analysis
- Scatter plots: Session Length vs. Satisfaction, Total Prompts vs. Satisfaction
- Correlation heatmap across numerical features
- Boxplots: Satisfaction by AI Assistance Level and Task Type

### Statistical Tests (Writing Tasks Only)

| Test | Result | Interpretation |
|---|---|---|
| One-Way ANOVA | F = 7.134, p = 0.0009 | Significant difference in satisfaction across AI assistance levels |
| Chi-Square | χ² = 18.623, df = 4, p = 0.0009 | Significant association between AI assistance level and assignment completion |

Both results support the hypothesis.

---

## Key Findings

1. **Satisfaction increases with AI assistance** — Students with higher AI assistance levels reported significantly greater satisfaction ratings during writing tasks.
2. **Completion rates improve** — Higher AI assistance was associated with a greater proportion of completed assignments.
3. **Weak session-level correlations** — Session length and total prompts showed weak correlation with satisfaction individually, suggesting that the quality of AI support (captured by `AI_AssistanceLevel`) matters more than raw usage quantity.

---

## Visualizations

Generated in the notebook:
- Distribution of Satisfaction Ratings (Writing Tasks)
- Session Length vs. Satisfaction Rating (scatter)
- Average Satisfaction by AI Assistance Level (bar plot)
- Assignment Completion Rate by AI Assistance Level (bar plot)
- Satisfaction by AI Assistance Level (boxplot)
- Assignment Outcome by AI Assistance Level (stacked bar chart)
- Correlation Matrix heatmap

---

## Project Structure

```
Personal-Data-Dashboard-/
├── README.md
├── .gitignore
├── notebooks/
│   └── EDA_Research_Notebook_Dallas_Cook.ipynb
└── data/
    └── README.md
```

---

## How to Run

1. **Download the dataset** — follow instructions in [`data/README.md`](data/README.md)
2. **Open the notebook** in Google Colab or Jupyter
3. **Update the file path** in the data loading cell to point to your downloaded CSV
4. **Run all cells** top to bottom

### Dependencies

```
pandas
numpy
matplotlib
seaborn
scipy
```

Install with:
```bash
pip install pandas numpy matplotlib seaborn scipy
```

---

## Background Research

| # | Reference | Summary |
|---|---|---|
| 1 | Kizilcec & Lee (2024). *Exploring the effectiveness of AI course assistants on student outcomes.* OpenPraxis. | Students using AI assistants showed higher performance, motivation, and self-efficacy. |
| 2 | Zheldibayeva & Kalantzis (2025). *Case study of CGScholar AI feedback in ELA classrooms.* arXiv. | Tailored AI feedback helped students produce higher-quality writing revisions. |
| 3 | Liu et al. (2025). *AI Literacy and Self-Regulated Learning as Predictors of Writing and Digital Well-Being.* PMC. | AI literacy and learning strategies were strong predictors of writing success. |

---

## Limitations

- Dataset is **synthetic** — patterns may not generalize to real students
- No demographic variables (age, gender, prior GPA)
- Cross-sectional data only — no longitudinal tracking
- Observational design — causal conclusions cannot be drawn

## Future Directions

- Test findings with real-world student data across different disciplines
- Explore the role of AI literacy and student motivation
- Use longitudinal or experimental designs
- Apply regression or ML classifiers to predict outcomes from usage patterns

---

*Note: This dataset is fully synthetic. No real student data was collected or used.*
