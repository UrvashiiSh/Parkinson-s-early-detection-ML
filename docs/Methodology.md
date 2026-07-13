## Methodology

This document provides an overview of the methodology used in the research paper **"Quantitative Hypokinetic Dysarthria as a Biomarker for Early Parkinson's Detection: A Machine Learning Approach."** The objective was to investigate whether speech-derived acoustic features could serve as reliable biomarkers for assessing Parkinson's disease severity using machine learning.

---

### Research Objective

The primary objective of this study was to evaluate whether subtle speech abnormalities associated with hypokinetic dysarthria could be quantified and used to predict Parkinson's disease severity.

The study focused on building regression-based machine learning models capable of estimating clinical assessment scores (UPDRS) from speech-derived acoustic biomarkers.


### Dataset

The study utilized a publicly available longitudinal Parkinson's disease speech dataset.

##### Dataset Summary

| Feature | Description |
|---------|-------------|
| Participants | 42 individuals diagnosed with idiopathic Parkinson's Disease |
| Total Speech Samples | 5,875 sustained phonation recordings |
| Recording Type | Sustained vowel (/a/) phonation |
| Number of Acoustic Features | 16 dysphonia-related features |
| Target Variables | Motor UPDRS and Total UPDRS |

Each participant contributed multiple recordings collected over several months, allowing longitudinal analysis of disease progression.


### Feature Extraction

The speech recordings were represented using sixteen quantitative acoustic features that quantify variations in pitch, loudness, voice quality, and signal regularity.
These features capture subtle vocal impairments associated with **hypokinetic dysarthria**, one of the earliest speech manifestations of Parkinson's disease.

The extracted features can be grouped into four categories:

| Feature | Description |
|---------|-------------|
| Frequency Perturbation (Jitter) | Jitter-based measures quantify cycle-to-cycle variations in the fundamental frequency of speech, reflecting instability in vocal fold vibration.|
| Amplitude Perturbation (Shimmer) | Shimmer measures evaluate variations in speech amplitude across vocal cycles, indicating instability in vocal intensity. |
| Noise-Based Features | Noise-related acoustic measures assess the degree of turbulent or breathy phonation caused by incomplete or inconsistent vocal fold closure. |
| Nonlinear Dynamic Features | Advanced nonlinear measures characterize complex vocal dynamics that are difficult to capture using conventional acoustic analysis. |


###### Frequency Perturbation (Jitter)
- Jitter (%)
- Jitter (Absolute)
- Relative Average Perturbation (RAP)
- Pitch Perturbation Quotient (PPQ5)
- Difference of Differences of Periods (DDP)

###### Amplitude Perturbation (Shimmer)
- Local Shimmer
- Shimmer (dB)
- APQ3
- APQ5
- APQ11
- Difference of Differences of Amplitudes (DDA)

###### Noise-Based Features
- Noise-to-Harmonics Ratio (NHR)
- Harmonics-to-Noise Ratio (HNR)

###### Nonlinear Dynamic Features
- Recurrence Period Density Entropy (RPDE)
- Detrended Fluctuation Analysis (DFA)
- Pitch Period Entropy (PPE)


Together, these acoustic biomarkers provide an objective representation of vocal motor function.
The abnormalities captured by these features arise from impaired neuromuscular control of the laryngeal muscles caused by dopaminergic neuron loss in the substantia nigra.
This disruption affects basal ganglia signalling, leading to reduced precision in vocal fold vibration and producing the characteristic speech impairments observed in Parkinson's disease.

These biomarkers capture subtle irregularities in speech that are difficult to detect through subjective clinical assessment.

### Exploratory Data Analysis

Before model development, an extensive exploratory analysis was performed to better understand the characteristics of the dataset.

The analysis included:

- Descriptive statistics
- Distribution analysis
- Feature correlation analysis
- Skewness and kurtosis evaluation
- Identification of multicollinearity
- Visualization of demographic and clinical variables

This step provided insights into feature relationships and guided subsequent preprocessing decisions.

### Data Preprocessing

Several preprocessing techniques were applied before model training.

These included:

- Patient-level train-test splitting to prevent data leakage
- Handling multicollinearity
- Dimensionality reduction using Principal Component Analysis (PCA)

PCA retained over 98% of the original variance while reducing redundancy among highly correlated acoustic features.

### Machine Learning Models

A diverse set of regression algorithms was evaluated to determine the most effective approach for predicting Parkinson's disease severity.

The models included:

- Linear Models
- Kernel-Based Models
- Ensemble Models
- Probabilistic Models

Hyperparameter optimization was performed using cross-validation techniques to improve model performance and reduce overfitting.


### Model Evaluation

The predictive performance of each model was evaluated using standard regression metrics.

| Metric | Purpose |
|---------|----------|
| R² Score | Measures the proportion of variance explained by the model |
| RMSE | Measures prediction error magnitude |
| MAE | Measures average absolute prediction error |
| MSE | Penalizes larger prediction errors |

These metrics enabled a comprehensive comparison across different machine learning approaches.


### Results

Among all evaluated algorithms, ensemble learning methods consistently produced the strongest predictive performance.

###### Best Performing Models

| Model | Performance Summary |
|---------|--------------------|
| Random Forest | Highest predictive accuracy (R² ≈ 0.91) |
| Gradient Boosting | Comparable performance (R² ≈ 0.90) |
| Gaussian Process Regression | Moderate predictive capability |
| Linear Regression Models | Limited ability to model nonlinear speech characteristics |

The results indicate that nonlinear ensemble models are better suited for capturing the complex relationships between acoustic biomarkers and Parkinson's disease severity.


### Research Contributions

This study demonstrates that:

- Speech-derived acoustic biomarkers provide meaningful information about Parkinson's disease severity.
- Machine learning can effectively model subtle vocal abnormalities associated with hypokinetic dysarthria.
- Ensemble learning methods significantly outperform traditional linear regression approaches.
- Non-invasive speech analysis has strong potential for scalable and cost-effective clinical decision support.


### Limitations

Although promising, several limitations should be considered.

- Relatively small patient cohort
- Demographic imbalance within the dataset
- External validation on independent datasets was not performed
- Clinical deployment requires further prospective evaluation

### Future Work

Potential directions for future research include:

- Validation using larger and more diverse patient populations
- Deep learning approaches for speech analysis
- Integration of multimodal biomarkers
- Real-time mobile health applications
- Remote monitoring systems for continuous disease assessment


### Workflow Overview

The overall research workflow followed the process below.

```
Speech Recordings
        │
        ▼
Feature Extraction
        │
        ▼
Exploratory Data Analysis
        │
        ▼
Principal Component Analysis (PCA)
        │
        ▼
Machine Learning Model Training
        │
        ▼
Model Evaluation
        │
        ▼
Prediction of Parkinson's Disease Severity
```

---

### Additional Resources

- See the project `README` for an overview of the research.
- Publication details and citation information are available in `publication.md`.
