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

### 2.1 - Original Question

A company is developing a solution to classify medical images for detecting skin cancer. The solution must ensure **high accuracy in labeling** and minimize the risk of incorrect classifications, especially for **rare types of cancer**.

Which solution will meet these requirements?

### 2.2 - Choices

A. Image analysis by using **Amazon Rekognition**  
B. Text analysis by using **Amazon Comprehend Medical**  
C. Data augmentation by using an **Amazon Bedrock Knowledge Base**  
D. Human-in-the-loop validation by using **Amazon SageMaker Ground Truth Plus**

### 2.3 - Correct Answer

D. Human-in-the-loop validation by using **Amazon SageMaker Ground Truth Plus**

### 2.4 - Why?

**SageMaker Ground Truth Plus** is designed for complex data-labeling tasks and can use **expert human reviewers** to improve labeling quality. This is particularly useful for specialized scenarios such as **medical image labeling**, where rare conditions may require expert judgement.

- **A. Amazon Rekognition** → Performs image and video analysis, but it is not primarily a service for creating highly accurate, expert-reviewed training labels
- **B. Amazon Comprehend Medical** → Extracts information from **medical text**, not medical images
- **C. Amazon Bedrock Knowledge Bases** → Used for **retrieval-augmented generation (RAG)** and connecting foundation models to external data, not image labeling
- **D. SageMaker Ground Truth Plus** → Supports **human-in-the-loop**, **expert-assisted labeling** for complex datasets

### 2.5 - Exam Focus

- **Complex or specialized data labeling requiring expert reviewers → SageMaker Ground Truth Plus**
- **Create labeled ML training datasets → SageMaker Ground Truth**
- **Medical text analysis → Amazon Comprehend Medical**
- **Image/video analysis → Amazon Rekognition**
- **Connect foundation models to external knowledge for RAG → Amazon Bedrock Knowledge Bases**

**Exam keyword:**
**"High-quality labeling + expert human review + complex/rare cases" → SageMaker Ground Truth Plus**