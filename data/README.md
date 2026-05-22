# Dataset

This project uses the **AI Assistant Usage in Student Life (Synthetic)** dataset from Kaggle.

## Download Instructions

1. Go to the Kaggle dataset page:  
   https://www.kaggle.com/datasets/ayeshasal89/ai-assistant-usage-in-student-life-synthetic/data

2. Click **Download** (you will need a free Kaggle account)

3. Extract the ZIP and place the CSV file in this `data/` folder

4. Rename the file to `ai_assistant_usage_student_life.csv` (or update the file path in the notebook)

## Dataset Details

| Field | Detail |
|---|---|
| Rows | 10,000 sessions |
| Columns | 11 |
| Time Period | August 2024 – June 2025 |
| Type | Synthetic — no real student data |

## Variables

| Column | Type | Description |
|---|---|---|
| `SessionID` | string | Unique session identifier |
| `StudentLevel` | string | Academic level (e.g., Undergraduate) |
| `Discipline` | string | Field of study |
| `SessionDate` | date | Date of session |
| `SessionLengthMin` | float | Session duration in minutes |
| `TotalPrompts` | int | Number of prompts sent during session |
| `TaskType` | string | Type of task (Writing, Coding, Studying, etc.) |
| `AI_AssistanceLevel` | int | Level of AI support received (1–5) |
| `FinalOutcome` | string | Whether the assignment was completed |
| `UsedAgain` | bool | Whether the student used AI again |
| `SatisfactionRating` | float | Self-reported satisfaction score (1.0–5.0) |

## Data Quality

- No missing values
- Fully synthetic — designed to mimic real-world behavior
- No personal or identifiable student information
