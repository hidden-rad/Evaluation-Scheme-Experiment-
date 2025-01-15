# Evaluation-Scheme-Experiment-

## 1. Common Evaluation: Textual Similarity Assessment (30 points)
### 1-1. Contextual Similarity (15 points)
#### * Semantic Consistency with Gold Standard (10 points)

Evaluates how semantically consistent the report is with the Gold Standard.
#####   * Perfect Consistency (8–10 points):
The report is at least 90% semantically consistent with the Gold Standard.
Example:
Gold Standard: "Pneumonia observed in the right lower lobe."
Report: "Pneumonia detected in the right lower lobe."
(The report accurately reflects key diagnoses and observations.)

#####   * Partial Consistency (5–7 points):
The report is 70–89% semantically consistent with the Gold Standard.
Example:
Gold Standard: "Pneumonia and mild pleural effusion."
Report: "Pneumonia detected."
(Pleural effusion is omitted in the report.)

#####   * Some Missing Information (3–4 points):
The report is 50–69% semantically consistent with the Gold Standard.
Example:
Gold Standard: "Pneumonia observed in the right lower lobe."
Report: "Pneumonia detected."
(Location information is missing.)

#### * Diagnosis-Focused Writing (5 points)

Evaluates whether 70% or more of the report content is centered around diagnoses and observations.
#####   * Fully Diagnosis-Focused (4–5 points):
Example:
Report: "Pneumonia detected in the right lower lobe, consistent with imaging findings and symptoms."
(Focused entirely on diagnosis-related information.)

#####   * Partially Diagnosis-Focused (3 points):
Example:
Report: "Pneumonia detected. The patient also reported fatigue."
(Contains unrelated information about fatigue.)

### 1-2. Diagnosis-Based Writing (15 points)
#### * Evaluation of Diagnosis-Based Writing (10 points)

Determines whether all diagnoses are accurately reflected from the Gold Standard.
#####   * Clearly Based on Diagnosis (8–10 points):
Example:
Gold Standard: "Pneumonia localized in the right lower lobe."
Report: "Pneumonia detected in the right lower lobe."
(The report accurately reflects the diagnosis.)

#####   * Partial Accuracy (5–7 points):
Example:
Gold Standard: "Pneumonia and bronchitis detected."
Report: "Pneumonia detected."
(Bronchitis is omitted in the report.)

#### * Absence of Unnecessary or Inaccurate Information (5 points)

Evaluates whether the report avoids unnecessary or inaccurate content.
#####   * No Unnecessary Content (4–5 points):
Example:
Report: "Pneumonia detected and consistent with imaging findings and symptoms."
(Focused without irrelevant content.)

#####   * Contains Some Unnecessary Content (3 points):
Example:
Report: "Pneumonia detected. The patient recently exercised."
(Includes irrelevant information about exercise.)

## 2. Task 1: MIMIC Report Assessment (70 points)
### 2-1. Consistency with MIMIC Items (40 points)
#### * Observation Accuracy (20 points)

Evaluates whether the observations in the Gold Standard are accurately reflected in the report.
Example:
Gold Standard: "Pneumonia and pleural effusion."
Report: "Pneumonia detected."
(Pleural effusion is missing from the report.)

#### * Appropriateness of Interpretation (20 points)

Evaluates whether the observations from the Gold Standard are interpreted in a clinically appropriate manner.
Example:
Gold Standard: "Pneumonia appears infectious."
Report: "Pneumonia suspected to be infectious."
(The report accurately reflects the diagnosis.)

### 2-2. Restoration of Hidden Causality (30 points)
#### * Clarity of Restoration (15 points)

Assesses how well the Gold Standard’s causal relationships are restored in the report.
Example:
Gold Standard: "Functional impairment associated with pneumonia."
Report: "Pneumonia identified as a primary cause of functional impairment."
(The relationship between pneumonia and functional impairment is clearly restored.)

#### * Consistency in Gold Standard-Based Interpretation (15 points)

Evaluates whether the report maintains consistency with the Gold Standard’s diagnostic and interpretive content.
Example:
Gold Standard: "Small nodules observed near the lung borders."
Report: "Small nodules near the lung borders identified as benign findings."
(The report maintains the Gold Standard’s observation while adding appropriate interpretation.)

## 3. Task 2: QA5 Causality Evaluation (70 points)
### 3-1. QA5 Causality Appropriateness (50 points)
#### * Causality Connection (30 points)

Assesses whether the report correctly reflects the causality outlined in QA5.
Example:
QA5: "Pneumonia is the cause of shortness of breath."
Report: "Pneumonia identified as the primary cause of shortness of breath."
(Causal connection between pneumonia and symptoms is accurately reflected.)

#### * Clinical Appropriateness of Reasoning (20 points)

Evaluates whether QA5’s abnormal scenarios or causal relationships are properly reflected in the report.
Example:
QA5: "Asymmetric nodule distribution near lung borders."
Report: "The asymmetric distribution of nodules suggests tumor rather than infection."
(Abnormal findings are correctly reflected.)

### 3-2. QA4 Diagnosis Mapping Accuracy (20 points)
#### * Reflection of Diagnostic Results (10 points)

Evaluates whether all diagnostic results from QA4 are accurately reflected in the report.
Example:
QA4: "Pneumonia diagnosis."
Report: "Pneumonia confirmed based on imaging and symptoms."
(QA4’s diagnosis is correctly reflected in the report.)

#### * Completeness and Relevance of Diagnoses (10 points)

Evaluates whether QA4’s diagnostic results are fully included and appropriately expressed in the report.
Example:
QA4: "Pneumonia, mild pleural effusion."
Report: "Mild pleural effusion observed, but pneumonia likelihood low."
(All diagnostic results are included, but clinical appropriateness may be lacking.)
