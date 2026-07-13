# AI-Powered Speech Analysis for Early Prediction of Parkinson's Disease

### Quantitative Hypokinetic Dysarthria as a Biomarker for Early Parkinson's Detection: A Machine Learning Approach

![Workflow](assets/workflow.png)

---

## Published Research

**Journal:** Digital Health (SAGE Journals)

**Publication Date:** March 2026

**DOI:** 10.1177/20552076261432053

**Read the publication:** https://journals.sagepub.com/doi/10.1177/20552076261432053

---

## Project Highlights

- Machine Learning for Early Parkinson's Detection
- Speech Biomarker Analysis
- Non-invasive Diagnostic Framework
- Ensemble Learning Models
- Healthcare AI
- Python-based Research

---

## Overview

Parkinson's disease is a progressive neurodegenerative disorder where early diagnosis remains difficult due to subtle and heterogeneous symptoms. Speech impairments, particularly hypokinetic dysarthria, often appear in the early stages of the disease and can serve as objective, non-invasive biomarkers.
This research investigates whether speech-derived acoustic features can be used with machine learning techniques to predict Parkinson's disease severity and support earlier clinical intervention.

#### Dataset

The data used in this project is publicly available on Kaggle (https://www.kaggle.com/datasets/porinitahoque/parkinsons-telemonitoring). 
The dataset was created by Athanasios Tsanas and Max Little of the University of Oxford, in collaboration with 10 medical centers in the US and Intel Corporation who developed the telemonitoring device to record the speech signals.

---
## Repository Purpose

This repository showcases the published research, methodology, machine learning workflow, and key findings of the study.
The source code used during the research is not publicly available.

---
## Research Motivation

Traditional Parkinson's diagnosis often depends on motor symptoms that become apparent only after significant neurological degeneration.
Speech analysis offers a scalable, low-cost, and non-invasive alternative capable of identifying subtle vocal changes associated with Parkinson's disease at much earlier stages.
This research investigates the use of quantitative speech biomarkers for identifying Parkinson's disease at an early stage. The proposed machine learning approach demonstrates the potential of non-invasive speech analysis as a decision-support tool for clinical screening and future healthcare applications.

---

## Objectives

- Analyze dysphonia-based speech biomarkers
- Reduce feature redundancy using PCA
- Compare multiple machine learning algorithms
- Evaluate predictive performance using clinical assessment scores (UPDRS)

---

## Technical Stack

- Python
- Machine Learning
- Scikit-learn
- NumPy
- Pandas
- Principal Component Analysis (PCA)
- Ensemble Learning
- Speech Signal Processing

---

## Machine Learning Pipeline

<img width="985" height="366" alt="ML pipeline PD" src="https://github.com/user-attachments/assets/a2f2e374-7353-46fe-9709-02bbb83fe750" />

---

## Key Findings

The study evaluated multiple regression-based machine learning models for predicting Parkinson's disease severity from speech-derived acoustic features.

Key findings include:

- Random Forest achieved the highest predictive performance.
- Gradient Boosting delivered comparable accuracy.
- Ensemble models significantly outperformed traditional linear approaches.
- Speech biomarkers demonstrated strong potential as objective indicators of Parkinson's disease severity.

---

## Repository Structure

```text
assets/
    Workflow diagram

figures/
    Machine Learning pipeline

docs/
    Detailed methodology

references/
    Publication details

README.md
```

---

## Research Impact

This work demonstrates the potential of speech-derived acoustic biomarkers combined with machine learning to support earlier, scalable, and non-invasive assessment of Parkinson's disease.
The findings contribute to ongoing research in digital health, speech analytics, and AI-assisted clinical decision support.


## Code Availability

The implementation code associated with this publication is not publicly available.
This repository is intended to document the research methodology and published findings.
