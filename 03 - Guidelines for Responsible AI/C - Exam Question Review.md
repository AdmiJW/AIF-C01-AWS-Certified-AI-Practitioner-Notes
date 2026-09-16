## 1 - Responsible AI Systems

### 1.1 - Original Question

A bank's machine learning model predicts auto loan approvals. The model rejects rural applicants more often than urban applicants, despite similar credit histories and incomes.

Which type of bias is affecting the model output?

### 1.2 - Choices

A. Measurement bias  
B. Confirmation bias  
C. Observer bias  
D. Sampling bias

### 1.3 - Correct Answer

**D. Sampling bias**

### 1.4 - Why?

**Sampling bias** occurs when the training data is **not representative of the population** the model will encounter.

In this scenario, rural applicants are rejected more frequently even though their credit histories and incomes are similar to those of urban applicants. This suggests that the model may have been trained on data that **overrepresented urban applicants and underrepresented rural applicants**.

Why the other options are incorrect:
- **A. Measurement bias** → Occurs when data is systematically measured incorrectly, such as a faulty credit scoring system producing inaccurate scores. No measurement problem is described.
- **B. Confirmation bias** → Occurs when evidence supporting an existing belief is favored while contradictory evidence is ignored. No such behavior is mentioned.
- **C. Observer bias** → Occurs when a person's subjective opinions influence data collection, interpretation, or labeling. The question does not mention human observers influencing the data
- **D. Sampling bias** → Correct because one population group appears to be inadequately represented in the training data.

### 1.5 - Exam Focus

**Training data does not represent the full target population → Sampling bias**

Quick distinctions:
- **Measurement bias** → Data measured incorrectly
- **Sampling bias** → Population not represented properly
- **Confirmation bias** → Favoring evidence that supports existing beliefs
- **Observer bias** → Human judgement influences recorded or labeled data

**Exam clue:** When one demographic, geographic, or population group performs worse despite otherwise similar characteristics, consider whether the **training sample was unrepresentative**



## 2 - Building Responsible AI with AWS Tools