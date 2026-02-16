# Data Dictionary: Lung Disease Dataset

## Overview

This dataset contains patient information for lung disease diagnosis, including demographic data, clinical measurements, and diagnostic results. The target variable is `disease_type` with multiple classes including Healthy, Asthma, COPD, Lung Cancer, and Pneumonia.

## Feature Descriptions

### Demographic Features

| Feature Name | Description                        | Data Type   | Range/Values |
| ------------ | ---------------------------------- | ----------- | ------------ |
| patient_id   | Unique identifier for each patient | Integer     | 1-6836       |
| age          | Patient age in years               | Integer     | 18-90        |
| sex          | Patient gender                     | Categorical | Male, Female |
| bmi          | Body Mass Index                    | Float       | 16.0-45.6    |

### Lifestyle Factors

| Feature Name   | Description                                                 | Data Type   | Range/Values           |
| -------------- | ----------------------------------------------------------- | ----------- | ---------------------- |
| smoking_status | Smoking history category                                    | Categorical | Never, Former, Current |
| pack_years     | Smoking pack-years (cigarettes per day × years smoked / 20) | Float       | 0.0-79.4               |
| pm25_exposure  | Exposure to PM2.5 air pollution                             | Float       | 3.0-39.1               |

### Occupational Information

| Feature Name   | Description                    | Data Type   | Range/Values                                                                           |
| -------------- | ------------------------------ | ----------- | -------------------------------------------------------------------------------------- |
| occupation     | Patient's occupation type      | Categorical | Office, Manufacturing, Construction, Agriculture, Healthcare, Mining, Unemployed/Other |
| family_history | Family history of lung disease | Categorical | None, Asthma, COPD, Cancer                                                             |

### Symptoms (Binary Features: 0 = No, 1 = Yes)

| Feature Name | Description                   |
| ------------ | ----------------------------- |
| cough        | Presence of cough             |
| dyspnea      | Shortness of breath           |
| wheeze       | Wheezing sound when breathing |
| chest_pain   | Chest pain or discomfort      |
| fever        | Elevated body temperature     |
| hemoptysis   | Coughing up blood             |

### Physical Measurements

| Feature Name     | Description                        | Data Type | Range/Values |
| ---------------- | ---------------------------------- | --------- | ------------ |
| weight_loss_kg   | Weight loss in kilograms           | Float     | -5.0 to 13.3 |
| spo2             | Blood oxygen saturation percentage | Float     | 87.2-100.0   |
| respiratory_rate | Breaths per minute                 | Float     | 10.0-28.4    |

### Laboratory Tests

| Feature Name | Description                                           | Data Type | Range/Values |
| ------------ | ----------------------------------------------------- | --------- | ------------ |
| crp_mg_L     | C-reactive protein level (mg/L) - inflammation marker | Float     | 0.0-218.6    |
| wbc_10e9_L   | White blood cell count (10^9/L)                       | Float     | 2.0-20.7     |

### Pulmonary Function Tests

| Feature Name  | Description                                    | Data Type | Range/Values |
| ------------- | ---------------------------------------------- | --------- | ------------ |
| fev1_fvc      | FEV1/FVC ratio - key indicator of obstruction  | Float     | 0.20-0.95    |
| fev1_pct_pred | FEV1 percent predicted                         | Float     | 20.0-140.0   |
| fvc_pct_pred  | FVC percent predicted                          | Float     | 49.6-131.4   |
| dlco_pct_pred | DLCO percent predicted - gas exchange capacity | Float     | 20.0-133.6   |

### Imaging Findings

| Feature Name      | Description                   | Data Type   | Range/Values                                                                                                       |
| ----------------- | ----------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------ |
| cxr_finding       | Chest X-ray finding           | Categorical | Normal, Consolidation, Infiltrate, Mass/Nodule, Hyperinflation, Flattened Diaphragm, Pleural Effusion, Atelectasis |
| ct_nodule_size_mm | CT nodule size in millimeters | Float       | 0.0-42.8                                                                                                           |
| ct_emphysema_pct  | CT emphysema percentage       | Float       | 0.0-50.8                                                                                                           |

### Functional Test

| Feature Name | Description                        | Data Type | Range/Values |
| ------------ | ---------------------------------- | --------- | ------------ |
| sixmwd_m     | Six-minute walk distance in meters | Float     | -29 to 816   |

### Comorbidities (Binary: 0 = No, 1 = Yes)

| Feature Name              | Description                            |
| ------------------------- | -------------------------------------- |
| hypertension              | Presence of high blood pressure        |
| diabetes                  | Presence of diabetes mellitus          |
| hospital_visits_last_year | Number of hospital visits in past year |

### Target Variables

| Feature Name | Description            | Data Type   | Categories                                    |
| ------------ | ---------------------- | ----------- | --------------------------------------------- |
| disease_type | Primary diagnosis      | Categorical | Healthy, Asthma, COPD, Lung Cancer, Pneumonia |
| severity     | Disease severity level | Categorical | Mild/None, Moderate, Severe                   |

## Notes

- Some features contain missing values that require appropriate handling
- Binary features (cough, dyspnea, etc.) are encoded as 0 (No) or 1 (Yes)
- The dataset is imbalanced across disease types
- Negative values in `sixmwd_m` may indicate data entry errors
- `pack_years` of 0 indicates non-smoker or minimal smoking history
