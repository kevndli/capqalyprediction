# README for Prostate Cancer Quality of Life and Complications Risk Prediction Model

## Background

Machine learning (ML) algorithms have the potential to revolutionize the prediction of post-treatment complications and quality of life degradation in prostate cancer patients. Traditional statistical methods may struggle with complex variable interactions or nonlinearity; ML algorithms do not. They can autonomously discern complex patterns and nonlinear relationships within the data. The dynamic and adaptable nature of ML facilitates continuous learning and model refinement, which is vital for maintaining the relevance and accuracy of clinical predictive models. ML's ability to personalize medicine by generating customized risk predictions is invaluable, utilizing patient demographics, comorbidities, and specific prostate cancer variables to provide individualized patient care.

## Objective

- To build a prostate cancer quality of life and complications risk prediction model using CaPSURE registry data.
- To develop a patient-facing platform, such as a nomogram or web application, based on the risk models.

## Cohort

- **Inclusion**: Patients with localized prostate cancer.
- **Exclusion**: Patients with metastatic prostate cancer.

## Covariates

- Age
- Race/ethnicity
- Body mass index (BMI)
- Comorbid conditions (Diabetes, cardiac conditions, cognitive function, urological conditions)
- Family history
- Primary treatment (Active surveillance/watchful waiting, Radiation therapy, Radical prostatectomy, Others)
- Clinical T stage (UICC TNM classification)
- Primary and Secondary Gleason grades
- Biopsy Gleason grade group
- NCCN clinical risk group
- Total number of biopsy cores examined
- Core positivity rate
- Preoperative PSA level
- Surgical features (Open vs. laparoscopic/robotic)

## Continuous Outcomes (PROMs)

- Quality of life (QoL)
  - SF-36 General Health Score
  - UCLA Prostate Cancer Index (Urinary function, Bowel function, Sexual function)

## Time-to-event Outcomes

- Severe complication requiring treatment (surgery, procedure, admission, or ER visit)
  - GI toxicity
  - Cystitis
  - Incontinence requiring a procedure
  - Ureteral injury
  - Urinary stricture

Censoring occurs at the last visit, treatment, evaluation, patient-reported questionnaire, hospital audit, or death certificate date.

## Models

- Cox proportional hazard regression
- Random survival forest
- DeepSurv

Workflow: Data cleaning → Feature selection → Hyper-parameter tuning → Model training → Model evaluation

## Model Evaluation

- Harrell’s concordance index (discrimination)
- Integrated Brier score (calibration)
- AUROC
- SHAP values
- LIME values

## Model Deployment

- Breslow Estimator for baseline survival function and probability of outcome at each time point.
- Deployment platforms for models may include R Shiny or Streamlit for the patient-facing web application.

## Initial Proposal

**Background**: Leveraging the CaPSURE registry data, this study aims to enhance patient access to research data and understanding of QoL post-prostate cancer treatment.

**Objective**: To develop a patient-facing risk prediction model using ML and traditional biostatistical methods for predicting QoL outcomes and complications post-treatment.

**Methodology**:

1. Data Source: The CaPSURE database will be utilized.
2. Models grouped by Outcome Type:
   - Time-to-event: Cox Proportional Hazards, Random Survival Forests, Deep Survival Networks.
   - Binary Outcomes: Logistic Regression, Random Forest, XGBoost.
   - Continuous Outcomes (PROMs): Linear Regression, XGBoost.
3. Model Evaluation: Utilize Model Evaluation Metrics including ROC curves, AUC, SHAP values.

**Significance**: The project focuses on developing an accessible risk prediction model, fostering informed decision-making for patients.

**Example**: Modeled after existing resources like the MSKCC nomograms, but with the integration of ML methods.

## Meetings and Progress

### Jeong Meeting #1

- Discussion points and notes from the first meeting with Dr. Jeong.

### Carroll Meeting 1/29/24

1. Introduction and goals for the research year under Dr. Breyer at UCSF.
2. Updates from the meeting with Dr. Steve Jeong on the two-stage approach and communication protocols.
3. Current proposal overview, including background on Cox regression/ML, objectives, and deployment strategies.
4. Discussion on defining binary outcomes from PROMs and collaboration with UCLA Chris Saigal.
5. Next steps towards group presentation and data acquisition.

## Next Steps

- Determine the presentation length and finalize steps for data acquisition.
- Collaborate with experts for analysis plan and QALY calculator development.
