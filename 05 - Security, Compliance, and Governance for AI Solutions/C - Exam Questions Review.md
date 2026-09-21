## 1 - Practice Question

### 1.1 - Original Question

A financial technology organization is using a **Large Language Model (LLM)** to generate content. What critical OWASP LLM vulnerability should the SecOps team be most concerned about when defending against **malicious input and system manipulation**?

### 1.2 - Choices

A. Insecure output handling  
B. Training data poisoning  
C. Prompt injection  
D. Sensitive information disclosure

### 1.3 - Correct Answer

**C. Prompt injection**

### 1.4 - Why?

**Prompt injection** occurs when an attacker crafts malicious input designed to manipulate an LLM into performing unintended actions or ignoring its intended instructions.

The key exam clue is:
**Malicious input + manipulate LLM behavior → Prompt injection**

- **A. Insecure output handling** → Concerns unsafe handling of the **model's output**, not malicious input
- **B. Training data poisoning** → Manipulates the **training data** used to build or train the model
- **D. Sensitive information disclosure** → Involves exposing confidential or sensitive information, typically through model responses.

## 2 - Practice Question

### 2.1 - Original Question

An organization is building a generative AI solution using a **self-trained model**. It must comply with AI algorithm accountability requirements involving **transparency, fairness, and compliance**.

Which **two** laws or regulations should the organization consider?

### 2.2 - Choices

A. New York City's Automated Decision Systems Law  
B. Florida's AI Command Law  
C. Health Insurance Portability and Accountability Act (HIPAA)  
D. European Union Artificial Intelligence Act

### 2.3 - Correct Answer

**A. New York City's Automated Decision Systems Law**  
**D. European Union Artificial Intelligence Act**

### 2.4 - Why?

Both address governance and accountability concerns associated with **AI and automated decision-making**.

- **A** addresses automated decision systems and concerns such as **bias and accountability**
- **D** provides a regulatory framework for AI systems and includes requirements related to areas such as **risk management, transparency, and oversight**.
- **B is incorrect**: The referenced law is not a valid regulation
- **C is incorrect**: **HIPAA** primarily protects the privacy and security of **protected health information (PHI)** rather than serving as a general AI algorithm accountability law.

Key distinction:

**AI accountability / automated decisions → AI-specific regulation**
**Healthcare PHI → HIPAA**

## 3 - Practice Question

### 3.1 - Original Question

A startup has governance requirements for its AWS object storage infrastructure. It needs:

- Precise **data retention periods**
- Comprehensive **configuration tracking**

Which **two** AWS services best meet these requirements?

### 3.2 - Choices

A. Amazon Inspector  
B. AWS Config  
C. Amazon S3 Object Lock  
D. AWS IAM

### 3.3 - Correct Answer

**B. AWS Config**  
**C. Amazon S3 Object Lock**

### 3.4 - Why?

**AWS Config** records AWS resource configurations and tracks **configuration changes over time**, making it appropriate for governance, auditing, and compliance.

**Amazon S3 Object Lock** provides **data immutability** using a **Write Once, Read Many (WORM)** model and supports configurable retention periods.

S3 Object Lock provides:
- **Compliance mode** → Retention cannot be bypassed during the configured period
- **Governance mode** → Authorized users with appropriate permissions can bypass retention

Why the others are incorrect:

- **Amazon Inspector** → Vulnerability management and security scanning
- **AWS IAM** → Identity, permissions, and access control; not retention management or configuration history

Memory aid:

**Configuration tracking → AWS Config**
**Immutable S3 retention → S3 Object Lock**

## 4 - Practice Question

### 4.1 - Original Question

A startup is building its own generative AI models and wants to use the **Generative AI Security Scoping Matrix** to guide security and governance.

Which **three scopes** apply to organizations developing their own model-based AI solutions?

### 4.2 - Choices

A. Scope 1: Public Consumer App  
B. Scope 2: Enterprise App  
C. Scope 3: Pre-trained Model  
D. Scope 4: Fine-tuned Model  
E. Scope 5: Self-trained Model

### 4.3 - Correct Answer

**C. Scope 3: Pre-trained Model**  
**D. Scope 4: Fine-tuned Model**  
**E. Scope 5: Self-trained Model**

### 4.4 - Why?

The key clue is that the organization is concerned with developing **model-based AI solutions**, rather than simply consuming complete AI applications.

| **Scope**   | **Type**    | **Description**                                    |
| ----------- | ----------- | -------------------------------------------------- |
| **Scope 1** | Application | Public consumer AI application                     |
| **Scope 2** | Application | Enterprise AI application                          |
| **Scope 3** | Model       | Build an application using a **pre-trained model** |
| **Scope 4** | Model       | Customize or **fine-tune** an existing model       |
| **Scope 5** | Model       | Build and train a **model from scratch**           |

Scopes **3-5** therefore represent increasingly customized model-based approaches.

Memory aid:
**1-2 → Applications**
**3-5 → Models**

And:

**Scope ↑ → Organizational control ↑ → Security responsibility ↑**

## 5 - Practice Question

### 5.1 - Original Question

In AI systems, data logging involves systematically recording information related to AI workload processing.

Which **two** factors should be prioritized when configuring logging for AI workloads?

### 5.2 - Choices

A. Tracking outputs  
B. User preference configuration  
C. Data backup schedule  
D. Model performance metrics

### 5.3 - Correct Answer

**A. Tracking outputs**  
**D. Model performance metrics**

### 5.4 - Why?

Monitoring **AI inputs and outputs** can help identify abnormal or malicious behavior, including model misuse and prompt-based attacks.

Monitoring **model performance metrics** helps detect degradation, availability problems, and unusual system behavior.

- **B is incorrect**: User preferences may improve personalization but are not a primary security-monitoring requirement
- **C is incorrect**: Backup schedules are important for resilience, but the schedule itself is not a primary AI workload logging signal.

High-value monitoring areas include:
- **Model inputs and outputs**
- **Model performance metrics**
- Security events
- Infrastructure behavior
- Responsible AI concerns such as bias

## 6 - Exam Focus

Prioritize these scenario-to-answer mappings:

- **Malicious prompt manipulates LLM behavior → Prompt injection**
- **Malicious or compromised training dataset → Training data poisoning**
- **Sensitive data exposed by model → Sensitive information disclosure**
- **AI/automated decision accountability → AI-specific laws and regulations**
- **Track AWS resource configurations and changes → AWS Config**
- **Prevent S3 deletion/overwrite and enforce retention → S3 Object Lock**
- **Public consumer AI application → Scope 1**
- **Enterprise AI application → Scope 2**
- **Pre-trained foundation model → Scope 3**
- **Fine-tuned/customized model → Scope 4**
- **Self-trained model built from scratch → Scope 5**
- **Monitor AI behavior for misuse → Log inputs/outputs**
- **Monitor AI health and operational behavior → Model performance metrics**