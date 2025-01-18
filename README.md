# Evaluation-Scheme-Experiment

## **1. Common Evaluation: Textual Similarity Assessment (Total: 30 points)**

### **1-1. Contextual Similarity (15 points)**

#### **Semantic Alignment with Gold Standard (10 points)**
Evaluates how semantically aligned the report is with the diagnostic and observational content of the Gold Standard.

- **Perfect Alignment (10 points):**
  - Semantic alignment exceeds 90%.
  - **Example:**
    - Gold Standard: "Pneumonia detected in the right lower lobe."
    - Report: "Pneumonia observed in the right lower lobe."
    - *(Accurately reflects the key diagnostics and observations.)*

- **Partial Alignment (7 points):**
  - Semantic alignment ranges from 70% to 89%.
  - **Example:**
    - Gold Standard: "Pneumonia and mild pleural effusion."
    - Report: "Pneumonia observed."
    - *(Omission of pleural effusion details.)*

- **Some Omissions (4 points):**
  - Semantic alignment ranges from 40% to 69%.
  - **Example:**
    - Gold Standard: "Pneumonia detected in the right lower lobe."
    - Report: "Pneumonia detected."
    - *(Missing details about the location.)*

- **Significant Omissions (1 point):**
  - Semantic alignment is below 40%.
  - **Example:**
    - Gold Standard: "Pneumonia detected in the right lower lobe."
    - Report: "Cardiomegaly suspected."
    - *(Both diagnostic condition and location are missing.)*

#### **Focus on Diagnosis (5 points)**
Evaluates whether the report is primarily diagnosis and observation-centric.

- **Fully Diagnosis-Centric (5 points):**
  - Over 70% of the report focuses on diagnostics and observations.
  - **Example:**
    - Report: "Pneumonia observed in the right lower lobe, aligning with clinical symptoms and imaging findings."

- **Partially Diagnosis-Centric (3 points):**
  - 50% to 69% of the report focuses on diagnostics.
  - **Example:**
    - Report: "Pneumonia observed. Patient reports fatigue."
    - *(Non-diagnostic content detracts from the focus.)*

- **Lacking Diagnosis Focus (1 point):**
  - Less than 50% of the report focuses on diagnostics.
  - **Example:**
    - Report: "Patient reports stress and fatigue. No significant findings in family history."
    - *(Minimal diagnostic content.)*

---

### **1-2. Consistency with Diagnostic Basis (15 points)**

#### **Adherence to Diagnostic Basis (10 points)**
Evaluates how accurately the report reflects the diagnostic basis outlined in the Gold Standard.

- **Fully Adherent (10 points):**
  - Over 90% of the diagnostics align with the Gold Standard.
  - **Example:**
    - Gold Standard: "Pneumonia confined to the right lower lobe."
    - Report: "Pneumonia identified in the right lower lobe."

- **Partially Adherent (7 points):**
  - 70% to 89% of diagnostics align with the Gold Standard.
  - **Example:**
    - Gold Standard: "Pneumonia and bronchitis."
    - Report: "Pneumonia observed."
    - *(Bronchitis diagnosis is omitted.)*

- **Some Adherence (4 points):**
  - 40% to 69% of diagnostics align with the Gold Standard.
  - **Example:**
    - Gold Standard: "Pneumonia confined to the right lower lobe with mild pleural effusion."
    - Report: "Pneumonia suspected."
    - *(Details about location and pleural effusion are missing.)*

- **Minimal Adherence (1 point):**
  - Less than 40% of diagnostics align with the Gold Standard.
  - **Example:**
    - Gold Standard: "Pneumonia confined to the right lower lobe."
    - Report: "Cardiomegaly suspected."
    - *(The report is largely unrelated to the Gold Standard.)*

#### **Absence of Unnecessary or Incorrect Information (5 points)**
Evaluates whether the report avoids unnecessary or erroneous details.

- **No Unnecessary Content (5 points):**
  - The report contains no unnecessary or inaccurate information.
  - **Example:**
    - Report: "Pneumonia observed, and antibiotic treatment is recommended."

- **Minor Unnecessary Content (3 points):**
  - The report includes minor non-diagnostic details that do not significantly affect accuracy.
  - **Example:**
    - Report: "Pneumonia observed. Patient reports recent lack of exercise."
    - *(Details about exercise are irrelevant.)*

- **Significant Unnecessary Content (1 point):**
  - The report includes substantial non-diagnostic content or erroneous information.
  - **Example:**
    - Report: "Pneumonia suspected, but the patient’s occupational stress is likely the primary cause."
    - *(Unnecessary or unsupported content lowers credibility.)*

## **2. Task 1: MIMIC Report Evaluation (Total: 70 points)**

### **2-1. Consistency with MIMIC Items (40 points)**

#### **Accuracy of Observations (20 points)**
Evaluates how accurately the report reflects observations stated in the Gold Standard.

- **All Observations Accurately Reflected (20 points):**
  - Over 90% of observations are accurately reflected.
  - **Example:**
    - Gold Standard: "Pneumonia and mild pleural effusion observed."
    - Report: "Pneumonia observed, and mild pleural effusion confirmed."
    - *(All observations are accurately reflected.)*

- **Some Observations Reflected with Missing Details (15 points):**
  - 60% to 89% of observations are reflected, but some details are missing.
  - **Example:**
    - Gold Standard: "Pneumonia and mild pleural effusion observed."
    - Report: "Pneumonia observed."
    - *(Details about pleural effusion are missing.)*

- **Partial Observations Reflected (10 points):**
  - 30% to 59% of observations are reflected, with key information missing.
  - **Example:**
    - Gold Standard: "Pneumonia and mild pleural effusion observed."
    - Report: "Mild pleural effusion observed."
    - *(Pneumonia diagnosis is missing.)*

- **Observations Poorly Reflected (5 points):**
  - Less than 30% of observations are reflected or are distorted.
  - **Example:**
    - Gold Standard: "Pneumonia and mild pleural effusion observed."
    - Report: "Severe pleural effusion observed."
    - *(Severity of pleural effusion is exaggerated.)*

#### **Interpretation Appropriateness (20 points)**
Evaluates whether the observations in the report are interpreted in a clinically appropriate manner.

- **All Observations Appropriately Interpreted (20 points):**
  - All observations are clinically relevant and appropriately interpreted.
  - **Example:**
    - Gold Standard: "Pneumonia appears infectious."
    - Report: "Pneumonia is likely infectious in nature."
    - *(Observations are accurately interpreted with clinical appropriateness.)*

- **Key Observations Appropriately Interpreted with Missing Details (15 points):**
  - Key observations are appropriately interpreted, but some details are lacking.
  - **Example:**
    - Gold Standard: "Pneumonia appears infectious, with a high likelihood of viral etiology."
    - Report: "Pneumonia appears infectious."
    - *("Viral etiology" is omitted.)*

- **Some Observations Misinterpreted (10 points):**
  - Some observations are clinically inaccurate or misinterpreted.
  - **Example:**
    - Gold Standard: "Pneumonia appears infectious."
    - Report: "Pneumonia appears non-infectious."
    - *(The interpretation contradicts the Gold Standard.)*

- **Most Observations Misinterpreted (5 points):**
  - Observations are largely misinterpreted or clinically irrelevant.
  - **Example:**
    - Gold Standard: "Pneumonia appears infectious."
    - Report: "Pneumonia is determined to be non-infectious."
    - *(Most of the observations are misinterpreted or clinically inaccurate.)*

---

### **2-2. Evaluation of Hidden Causality Restoration (30 points)**

#### **Clarity of Restoration (15 points)**
Evaluates how clearly the report restores and reflects causality stated in the Gold Standard.

- **All Causalities Clearly Restored (15 points):**
  - All causalities in the Gold Standard are clearly restored and appropriately reflected.
  - **Example:**
    - Gold Standard: "Functional impairment linked to pneumonia."
    - Report: "Pneumonia identified as the primary cause of functional impairment."
    - *(Causal relationship between impairment and pneumonia is clearly described.)*

- **Key Causalities Restored with Missing Details (10 points):**
  - Key causalities are restored, but additional details are omitted or incomplete.
  - **Example:**
    - Gold Standard: "Pneumonia likely causes coughing and fever."
    - Report: "Pneumonia identified as a cause of coughing."
    - *(Details regarding fever are missing.)*

- **Causalities Inaccurately Restored or Not Restored (5 points):**
  - Causalities are inaccurately restored or not restored.
  - **Example:**
    - Gold Standard: "Functional impairment linked to pneumonia."
    - Report: "Relationship between functional impairment and pneumonia is unclear."
    - *(Fails to accurately reflect the causal relationship.)*

#### **Consistency of Interpretation Based on Gold Standard (15 points)**
Evaluates how consistently the diagnostic content and interpretation from the Gold Standard are reflected in the report.

- **All Interpretations Consistently Reflected (15 points):**
  - Gold Standard diagnostic content and interpretations are perfectly consistent, maintaining meaning and context.
  - **Example:**
    - Gold Standard: "Small nodules observed near the borders of both lungs."
    - Report: "Small nodules near both lung borders are interpreted as benign."
    - *(Observation and interpretation align with the Gold Standard.)*

- **Key Interpretations Consistently Reflected with Some Contradictions (10 points):**
  - Key diagnostic content is reflected, but some interpretations are contradictory or lack logical consistency.
  - **Example:**
    - Gold Standard: "Pneumonia confined to the right lower lobe."
    - Report: "Pneumonia observed in the right lower lobe; however, mild pleural effusion is unrelated to pneumonia."
    - *(Key content is reflected, but there are inconsistencies in interpretation.)*

- **Interpretations Contradict Gold Standard and Are Inconsistent Within the Report (5 points):**
  - Diagnostic content contradicts the Gold Standard and lacks consistency within the report.
  - **Example:**
    - Gold Standard: "Pneumonia confined to the right lower lobe."
    - Report: "Pneumonia observed in the right lower lobe, but later concluded to not be pneumonia."
    - *(Contradictions in interpretation and lack of consistency within the report.)*
   
## **3. Task 2: QA5 Causality Evaluation (Total: 70 points)**

### **3-1. QA4 Diagnosis Mapping Accuracy (20 points)**

#### **Reflection of Diagnostic Results (10 points)**
Evaluates whether the diagnostic results provided by QA4 are accurately and comprehensively reflected in the report.

- **All Diagnostic Results Accurately Reflected (10 points):**
  - All diagnostic results from QA4 are accurately and fully included in the report.
  - **Example:**
    - QA4: "Pneumonia and mild pleural effusion."
    - Report: "Pneumonia and mild pleural effusion confirmed through imaging and symptoms."
    - *(All diagnostic results are fully and accurately reflected.)*

- **Key Diagnostic Results Reflected, Missing Details (7 points):**
  - Key diagnostic results from QA4 are reflected, but some details are missing.
  - **Example:**
    - QA4: "Pneumonia and mild pleural effusion."
    - Report: "Pneumonia observed, pleural effusion suspected."
    - *(Details about pleural effusion are incomplete.)*

- **Partial Diagnostic Results Reflected (5 points):**
  - Only part of QA4’s diagnostic results are reflected, with key information missing.
  - **Example:**
    - QA4: "Pneumonia and mild pleural effusion."
    - Report: "Mild pleural effusion observed."
    - *(Pneumonia diagnosis is missing.)*

- **Diagnostic Results Not Reflected (1 point):**
  - QA4’s diagnostic results are not reflected or completely misrepresented in the report.
  - **Example:**
    - QA4: "Pneumonia and mild pleural effusion."
    - Report: "Lung condition appears normal."
    - *(QA4’s diagnostic results are entirely omitted.)*

#### **Completeness and Appropriateness of Diagnostic Results (10 points)**
Evaluates whether all diagnostic results from QA4 are accurately included and clinically appropriately expressed in the report.

- **All Diagnostic Results Accurately Reflected and Appropriate (10 points):**
  - All diagnostic results are fully included, and the content is expressed with clinical relevance.
  - **Example:**
    - QA4: "Pneumonia, mild pleural effusion."
    - Report: "Pneumonia and mild pleural effusion confirmed through imaging and symptoms; treatment recommended."
    - *(All diagnostic results are included and clinically appropriate.)*

- **Diagnostic Results Included but Lacking Clinical Relevance (7 points):**
  - All diagnostic results are included but expressed with insufficient clinical relevance or logical clarity.
  - **Example:**
    - QA4: "Pneumonia, mild pleural effusion."
    - Report: "Pneumonia and mild pleural effusion confirmed, but the need for treatment is unclear."
    - *(Diagnostic results are included but lack clinical relevance.)*

- **Some Diagnostic Results Incomplete or Inappropriate (5 points):**
  - Only part of the diagnostic results are included, or the content is clinically inappropriate.
  - **Example:**
    - QA4: "Pneumonia, mild pleural effusion."
    - Report: "Pneumonia observed, but mild pleural effusion ignored."
    - *(Diagnostic results are incomplete and inappropriate.)*

- **Diagnostic Results Not Reflected or Completely Inappropriate (1 point):**
  - Diagnostic results from QA4 are not reflected or expressed in a clinically irrelevant manner.
  - **Example:**
    - QA4: "Pneumonia, mild pleural effusion."
    - Report: "No pneumonia observed; condition appears normal."
    - *(Diagnostic results are omitted or entirely inappropriate.)*

---

### **3-2. Causality Appropriateness Evaluation (50 points)**

#### **Causality Connection Appropriateness (30 points)**
Evaluates whether the report appropriately connects the causality relationships outlined in the Gold Standard.

- **All Causalities Accurately and Appropriately Connected (30 points):**
  - All causality relationships in the Gold Standard are logically and accurately connected in the report.
  - **Example:**
    - Gold Standard: "Pneumonia is the cause of shortness of breath."
    - Report: "Pneumonia identified as the primary cause of shortness of breath."
    - *(Causality between the condition and symptom is appropriately connected.)*

- **Key Causalities Connected, Missing Details (20 points):**
  - Key causality relationships are connected, but some details are missing or incomplete.
  - **Example:**
    - Gold Standard: "Pneumonia causes shortness of breath and fever."
    - Report: "Pneumonia identified as a cause of shortness of breath."
    - *(Details about fever are omitted.)*

- **Some Causalities Connected, Missing Key Information (10 points):**
  - Only part of the causality relationships are connected, with significant omissions or inaccuracies.
  - **Example:**
    - Gold Standard: "Pneumonia causes shortness of breath and fever."
    - Report: "Cause of shortness of breath unclear, but pneumonia suspected."
    - *(Relationship between the condition and symptom is incomplete.)*

- **Causalities Incorrectly Connected or Not Reflected (1 point):**
  - Causality relationships are incorrectly connected or not reflected at all.
  - **Example:**
    - Gold Standard: "Pneumonia is the cause of shortness of breath."
    - Report: "Shortness of breath is unrelated to pneumonia."
    - *(Causality is misinterpreted or omitted.)*

#### **Clinical Appropriateness of Inferences (20 points)**
Evaluates whether the abnormal situations and causality relationships described in the Gold Standard are appropriately reflected in the report.

- **All Abnormal Situations and Causalities Appropriately Reflected (20 points):**
  - All causality relationships are appropriately reflected with logical and clinical accuracy.
  - **Example:**
    - Gold Standard: "Asymmetric nodule distribution near both lung borders."
    - Report: "Asymmetric nodule distribution suggests a higher likelihood of tumors than infections."
    - *(Abnormal findings are clinically and appropriately reflected.)*

- **Key Abnormal Situations Reflected, Missing Details (15 points):**
  - Key abnormal situations are reflected, but additional interpretations or details are incomplete.
  - **Example:**
    - Gold Standard: "Asymmetric nodule distribution near both lung borders."
    - Report: "Asymmetric nodule distribution observed near lung borders."
    - *(Abnormal findings are mentioned but lack clinical interpretation.)*

- **Some Abnormal Situations Reflected, Inappropriate Interpretation (10 points):**
  - Only part of the abnormal situations are reflected, or the clinical interpretation is inappropriate.
  - **Example:**
    - Gold Standard: "Asymmetric nodule distribution near both lung borders."
    - Report: "Possible asymmetric nodule distribution."
    - *(Abnormal findings are incomplete or inaccurately interpreted.)*

- **Abnormal Situations Not Reflected or Completely Inappropriate (5 points):**
  - Abnormal situations and causality relationships are not reflected or clinically irrelevant.
  - **Example:**
    - Gold Standard: "Asymmetric nodule distribution near both lung borders."
    - Report: "Lung condition appears normal."
    - *(Abnormal findings are entirely omitted.)*
