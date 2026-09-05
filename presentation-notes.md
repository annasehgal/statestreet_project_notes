# Presentation Notes

---

# 1. Project Overview

## Problem

[Explain the problem in simple language.]

## Goal

Predict whether a Kickstarter campaign is likely to succeed or fail
and provide actionable recommendations.

## Why It Matters

[Add business/user value.]

---

# 2. My Individual Contribution

## One Sentence

[Write later]

## 30 Seconds

[Write later]

## 1 Minute

[Write later]

## Technical Deep Dive

[Write later]

---

# 3. Data Pipeline

## High-Level Architecture

Kickstarter dataset
→ Box
→ OAuth/API
→ Python
→ preprocessing
→ model
→ prediction
→ recommendations
→ application

---

# 4. Why Did I Use Box?

### Short Answer

[Write later]

### Technical Answer

[Write later]

### If Someone Says:

“But the Kickstarter dataset is public.”

Answer:

[Write later]

---

# 5. Why OAuth?

[Write later]

Possible explanation:

OAuth allows the application to access the Box resource through an
authorized application flow without embedding a user's Box password
in the application.

---

# 6. Why Not Just Download the CSV?

[Write later]

Possible reasoning:

Manual downloading works for a one-time analysis, but programmatic
access makes the data-access process reproducible and demonstrates how
the workflow could operate with controlled cloud-hosted data.

---

# 7. Why Logistic Regression?

[Write later]

---

# 8. Why Random Forest?

[Write later]

---

# 9. Why XGBoost?

[Write later]

---

# 10. Why These Evaluation Metrics?

## Accuracy

[Explanation]

## Precision

[Explanation]

## Recall

[Explanation]

## F1

[Explanation]

## ROC-AUC

[Explanation]

---

# 11. Target Leakage

## What Is It?

[Write explanation]

## Potential Leakage in Kickstarter Data

[Write specific columns/findings]

## What We Did

[Write decision]

---

# 12. Model Results

| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | | | | | |
| Random Forest | | | | | |
| XGBoost | | | | | |

---

# 13. Recommendation Engine

## Input

Campaign information

## Model

Classification model

## Output

- Probability of success
- Prediction
- Important factors
- Recommendations

---

# 14. Deployment

## Planned Architecture

Streamlit
→ user input
→ preprocessing
→ model.pkl
→ prediction
→ explanation
→ recommendations

---

# 15. Reproducibility

A reproducible result should include:

- Data snapshot/version
- Preprocessing code
- Model configuration
- Random seed
- Dependency versions
- Training/test methodology
- Saved model artifact

---

# 16. Challenges

### Challenge 1

[What happened]

### How I solved it

[Solution]

### Challenge 2

[What happened]

### How I solved it

[Solution]

---

# 17. Things I Learned

## Technical

- [ ]
- [ ]
- [ ]

## Machine Learning

- [ ]
- [ ]
- [ ]

## Engineering

- [ ]
- [ ]
- [ ]

## Team / Communication

- [ ]
- [ ]
- [ ]

---

# 18. Things I Would Improve

- [ ]
- [ ]
- [ ]

---

# 19. Final Takeaway

The most important thing I want the audience to remember:

[Write later]
