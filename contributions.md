# My Contributions

This document tracks my individual contributions to the State Street 1C
Kickstarter Crowdfunding Recommendation Engine.

---

## 1. Data Engineering

### Box Integration

Status: In progress

- Created Box Platform App.
- Configured OAuth 2.0.
- Configured redirect URI.
- Added environment-based configuration.
- Added `.env.example`.
- Implemented Box authentication utility.
- Implemented Box data-access utility.
- Implemented file lookup by configured filename.
- Implemented programmatic CSV download.
- Implemented pandas loading.
- Added persistent token storage.
- Tested local authentication flow.
- Investigated Box administrator restriction.

### Why This Matters

This creates a reproducible programmatic path between the team's
cloud-hosted dataset and the Python analysis environment.

---

## 2. Data Preparation

Status: Not started / In progress

### My Work

- [ ] Investigated dataset structure
- [ ] Identified target variable
- [ ] Identified missing values
- [ ] Identified categorical features
- [ ] Identified numerical features
- [ ] Investigated duplicate records
- [ ] Investigated relevant campaign outcomes
- [ ] Investigated U.S. filtering
- [ ] Identified possible target leakage
- [ ] Built preprocessing pipeline

### Important Questions

- What information would actually be available at campaign launch?
- Are pledge/backers/funded percentage available before or after launch?
- Are comments and updates valid prediction features?
- Which columns should be excluded?

---

## 3. Exploratory Data Analysis

Status: Not started

### My Work

- [ ] Success/failure distribution
- [ ] Goal amount analysis
- [ ] Duration analysis
- [ ] Category analysis
- [ ] Subcategory analysis
- [ ] Location analysis
- [ ] Reward analysis
- [ ] Missing-value analysis
- [ ] Correlation analysis
- [ ] Visualization

### Findings

- [Add findings]

---

## 4. Machine Learning

Status: Not started / In progress

### Baseline

- Logistic Regression

### Advanced Models

- Random Forest
- XGBoost
- [Others]

### Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1
- ROC-AUC

### Results

| Model | Accuracy | Precision | Recall | F1 | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Logistic Regression | | | | | |
| Random Forest | | | | | |
| XGBoost | | | | | |

### Best Model

Model:

Reason:

---

## 5. Model Interpretability

Status: Not started

### My Work

- [ ] Feature importance
- [ ] Model coefficients
- [ ] SHAP / other interpretability method
- [ ] Identify factors associated with success
- [ ] Translate model findings into recommendations

---

## 6. Recommendation Engine

Status: Not started

### Goal

Convert model predictions and important features into actionable
recommendations for Kickstarter campaign creators.

### Example Structure

Campaign information
→ prediction
→ probability of success
→ important contributing factors
→ actionable recommendations

---

## 7. Model Persistence

Status: In progress

### Artifact

`model.pkl`

### Purpose

Save the trained model so it can later be loaded for inference without
retraining.

### Important Distinction

Training:

dataset → preprocessing → model training → saved model

Inference:

new campaign → same preprocessing → saved model → prediction

---

## 8. Deployment

Status: Planned

### Possible Application

Streamlit

### Planned Flow

User enters campaign information
→ preprocessing
→ model
→ prediction probability
→ explanation
→ recommendations

---

## 9. CI/CD

Status: Planned

### Possible GitHub Actions

- Install dependencies
- Run tests
- Check code
- Verify imports
- Verify data-processing functions

---

## 10. Team / Project Organization

- [Add team contributions]

---

# Final Contribution Summary

At the end of the project, summarize my contribution in 3 levels.

### 30-second version

[Write later]

### 1-minute version

[Write later]

### Technical version

[Write later]
