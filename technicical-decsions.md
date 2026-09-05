# Technical Decisions

---

## Decision 1 — Use Box for Programmatic Data Access

### Date

September 2026

### Decision

Build a Python-based Box integration using OAuth 2.0.

### Context

The project dataset is stored in the team's shared Box folder.

### Alternatives

1. Manually download the CSV.
2. Mount cloud storage.
3. Use Box API programmatically.

### Chosen Approach

Box API + OAuth 2.0.

### Reason

- Reproducible data access
- Programmatic workflow
- Authentication experience
- Enterprise cloud-storage experience
- Separates data access from analysis code

### Tradeoff

This is more engineering work than manually downloading a public CSV.

### Important Perspective

The dataset is public, so Box integration is not strictly necessary
for the machine learning task.

The integration is primarily an engineering/reproducibility exercise
and mirrors a controlled enterprise data-access workflow.

---

## Decision 2 — Store Credentials in `.env`

### Decision

Keep Box credentials in environment variables rather than hardcoding
them in Python.

### Reason

Avoid placing credentials directly in source code.

### Repository Rule

`.env` must remain ignored by Git.

`.env.example` documents required variables without containing secrets.

---

## Decision 3 — Use Logistic Regression as Baseline

### Decision

Use Logistic Regression as the initial classification baseline.

### Reason

The project is predicting binary campaign success/failure.

A simple baseline provides a reference point for evaluating more complex
models.

### Advanced Models

Random Forest and XGBoost can then be compared against the baseline.

---

## Decision 4 — Do Not Copy the Previous BTT Project's Persistence Model

### Context

The previous BTT project used a Persistence Model as a baseline.

### Reason We Are Different

Their project was time-series energy forecasting.

A persistence model makes sense when predicting future energy demand
from recent energy demand.

The Kickstarter project is a binary classification problem.

### Decision

Use Logistic Regression as the baseline rather than implementing a
persistence model.

---

## Decision 5 — Model Persistence

### Decision

Use `model.pkl` for the trained model artifact.

### Purpose

Allow the model to be loaded for inference without retraining.

### Important Consideration

The model artifact alone is not sufficient for complete reproducibility.

Reproducibility also requires:

- preprocessing code
- dependency versions
- model configuration
- random seed
- training/test methodology
- data version/snapshot
