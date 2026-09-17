## 1 - Explainability of Model Decisions with SageMaker Clarify

### 1.1 - SageMaker Clarify Overview

**Amazon SageMaker Clarify** is a capability within **Amazon SageMaker** that helps improve **responsible AI** by detecting **bias** and explaining **why a model makes specific predictions**.

Key purposes:
- Detect **bias in training data**
- Detect **bias in model predictions**
- Identify **underrepresented or overrepresented groups**
- Explain which **features influenced a prediction**
- Improve **model transparency and trustworthiness**

### 1.2 - Bias Detection

SageMaker Clarify can analyze both the **dataset** and the **model's predictions** for potential bias.

| **Bias Area**       | **What Clarify Detects**                                                           |
| ------------------- | ---------------------------------------------------------------------------------- |
| **Data bias**       | Groups that are underrepresented or overrepresented in the dataset                 |
| **Prediction bias** | Groups that may receive disproportionately favorable or unfavorable model outcomes |

Clarify can visualize the **distribution of predictions across different groups**, making it easier to identify disparities.

Example: A loan model may approve applicants from one group more frequently than another even when their financial characteristics are similar. Clarify can help reveal this difference.

### 1.3 - Model Explainability

SageMaker Clarify helps explain **why a model produced a particular prediction** by showing how individual features contributed to the result.

For a credit-risk model predicting that an application may default:
- **High debt-to-income ratio** → may push the prediction toward a higher default risk
- **Limited/weak credit history** → may contribute negatively
- **Steady employment** → may contribute positively

Clarify can present feature contributions using **visualizations** or **numerical values**, helping users understand which inputs had the greatest influence on a prediction.

**Model prediction → Feature contributions → Explanation of decision**

This supports **explainability**, **transparency**, **bias investigation**, and **trust in AI systems**.

### 1.4 - Exam Focus

- **Detect bias in datasets or model predictions → SageMaker Clarify**
- **Identify underrepresented/overrepresented groups → SageMaker Clarify**
- **Explain why a model made a prediction → SageMaker Clarify**
- **Determine which features influenced an individual prediction → SageMaker Clarify**
- **Responsible AI keywords: bias detection, explainability, transparency, feature contribution, fairness**
- Do not confuse **model explainability** with improving model accuracy; Clarify primarily helps you **understand and evaluate model behavior**

## 2 - Automating Data Labeling with Amazon SageMaker Ground Truth

### 2.1 - Amazon SageMaker Ground Truth Overview

**Amazon SageMaker Ground Truth** is a managed data labeling service used to create **high-quality labeled datasets** for machine learning

It combines **human labeling** with **machine-assisted** and **automatic labeling** to reduce the time and effort required to prepare training data.

Common labeling tasks include:
- **Image labeling** → Identify or classify objects in images
- **Text labeling** → Classify text, such as **sentiment analysis**
- Other annotation tasks required to create supervised ML training datasets

### 2.2 - Human Labeling Options

Ground Truth supports several sources of human workers:

| **Workforce**              | **Best Use**                                                |
| -------------------------- | ----------------------------------------------------------- |
| **Amazon Mechanical Turk** | Large-scale crowdsourced labeling                           |
| **Private workforce**      | Use your own employees or internal team for greater control |
| **Third-party vendors**    | Outsource labeling to external providers                    |

Human workers can manually assign labels, such as identifying an object in an image as a **fish** or marking a sentence as **positive sentiment**.

### 2.3 - Machine-Assisted and Automated Labeling

Ground Truth can use **machine learning assistance** to make labeling more efficient.

Initially:

**Machine suggests labels → Human reviews/corrects labels**

As enough labeled data becomes available, Ground Truth can use **automated data labeling**, allowing ML models to label suitable data with less human involvement

This creates a workflow such as:

**Human labeling → Machine-assisted labeling → Automated labeling**

The combination of humans and ML helps reduce **labeling cost, time, and manual effort** while maintaining label quality.

### 2.4 - SageMaker Ground Truth Plus

**SageMaker Ground Truth Plus** provides a more managed labeling experience for complex **data-labeling projects**

It can provide access to **expert workforces / subject matter expertise**, making it suitable when labeling requires specialized knowledge or more complex annotation.

| **Service**                     | **Key Association**                                           |
| ------------------------------- | ------------------------------------------------------------- |
| **SageMaker Ground Truth**      | Human + machine-assisted data labeling                        |
| **SageMaker Ground Truth Plus** | More managed, expert-supported labeling for complex workloads |

### 2.5 - Exam Focus

- **Create labeled datasets for ML training → SageMaker Ground Truth**
- **Combine human workers with ML-assisted labeling → SageMaker Ground Truth**
- **Crowdsourced labeling workforce → Amazon Mechanical Turk**
- **Use an organization's own employees for labeling → Private workforce**
- **Reduce manual labeling through ML suggestions/automation → Automated data labeling**
- **Complex labeling requiring expert support → SageMaker Ground Truth Plus**

**Memory aid:**
**Ground Truth = Label training data using humans + machine assistance**

## 3 - AI Governance

### 3.1 - AI Governance Overview

**AI governance** refers to the policies, processes, and tools used to ensure AI/ML systems are **transparent**, **accountable**, **reliable**, **and responsibly managed** throughout their lifecycle.

Key AWS governance-related tools in this topic:
- **SageMaker Model Cards** → document and govern model information
- **SageMaker Model Monitor** → monitor deployed models
- **Open-source models and open data licensing** → improve transparency and accountability

### 3.2 - Amazon SageMaker Model Cards

**SageMaker Model Cards** provide structured documentation about an ML model.

They can record:

| **Model Card Information** | **Purpose**                                                      |
| -------------------------- | ---------------------------------------------------------------- |
| **Intended use / purpose** | Describes what the model was designed to do                      |
| **Risk rating**            | Classifies model risk, such as **high, medium, low, or unknown** |
| **Limitations**            | Documents situations where the model may perform poorly          |
| **Ethical considerations** | Records concerns such as potential bias or harmful impacts       |
| **Performance metrics**    | Documents measurements such as **accuracy** and **precision**    |

Example: A facial-recognition model may document that it performs best under **well-lit conditions**, making this limitation visible to stakeholders.

**Key distinction:** Model Cards are primarily for **documentation and governance**, not real-time model monitoring.

### 3.3 - Amazon SageMaker Model Monitor

**SageMaker Model Monitor** monitors ML models **after deployment** to identify changes or problems in production.

One important issue is **data drift**, where incoming production data becomes significantly different from the data used when the model was trained.

**Training data → Deploy model → Production data changes → Model Monitor detects drift**

Model Monitor can help identify:
- **Data Drift** → production data differs from expected/training data
- **Bias changes** → model behavior begins producing unfair differences across groups
- **Model quality/performance degradation** → model performance declines over time

This allows organizations to investigate problems and take corrective action when deployed models no longer behave as expected.

### 3.4 - Model Cards vs Model Monitor

| **Service**                 | **Primary Purpose**                                                | **When Used**                    |
| --------------------------- | ------------------------------------------------------------------ | -------------------------------- |
| **SageMaker Model Cards**   | Document model purpose, risk, limitations, ethics, and performance | Model governance/documentation   |
| **SageMaker Model Monitor** | Monitor deployed models for drift, bias, and quality issues        | **Post-deployment / production** |

**Memory aid:**
**Model Cards = Document the model**
**Model Monitor = Watch the model**

### 3.5 - Open-Source Models and Transparency

**Open-source models** can support AI transparency by making information about how models are built available for review.

Depending on the project, this may include:
- Model architecture
- Training methods
- Model code or configuration
- Information about training datasets

Greater visibility can support **auditability, accountability, collaboration, and responsible AI development**.

**Hugging Face** is widely associated with sharing ML models, particularly models for **natural language processing and generative AI**.

**Kaggle** provides ML and data science resources such as **datasets, notebooks, and competitions**.

### 3.6 - Open Data Licensing

**Open data licensing** defines the rules under which publicly available datasets can be **accessed, reused, modified, or distributed**.

Clear licensing is important because public availability alone does not necessarily mean data can be used without restrictions.

Open data practices can support:
- **Transparency**
- **Reproducibility**
- **Innovation**
- **Accountability**

### 3.7 - Exam Focus

- **Document a model's intended use, risks, limitations, ethical considerations, and metrics → SageMaker Model Cards**
- **Monitor a deployed ML model in production → SageMaker Model Monitor**
- **Incoming production data differs from expected/training data → Data drift**
- **Detect changes in bias or model quality after deployment → SageMaker Model Monitor**
- **Model documentation/governance artifact → Model Cards**
- **Post-deployment monitoring → Model Monitor**
- **Open-source models / open datasets** → support **transparency and accountability**
- **Rules describing how public datasets may be reused** → **Open data licensing**

**Quick distinction:**
**Clarify** → Explain predictions and detect bias
**Model Cards** → Document model governance information
**Model Monitor** → Monitor deployed models over time

## 4 - Boosting ML Accuracy with Amazon A2I

### 4.1 - Amazon Augmented AI (A2I) Overview

**Amazon Augmented AI (Amazon A2I)** adds **human review** to machine learning predictions.

It combines:

**AI automation → Human review when needed → Final decision**

A2I is useful when predictions are **uncertain, sensitive, or require additional validation.**

### 4.2 - Human Review Triggers

Human review can be triggered in different ways:

| **Trigger**                    | **Example**                                            |
| ------------------------------ | ------------------------------------------------------ |
| **Confidence score threshold** | Send predictions below 50% confidence for human review |
| **Random sampling**            | Send 10% of predictions for review as a quality check  |

Example flow:

**Prediction confidence > threshold → Send result to application**
**Prediction confidence < threshold → Send to Amazon A2I for human review**

This enables organizations to automate high-confidence decisions while involving humans for uncertain cases

### 4.3 - Human Review Workforce

Amazon A2I can route review tasks to different workforces:
- **Private workforce** → your own employees or internal team
- **Third-party workforce** → external service providers
- **Amazon Mechanical Turk** → crowdsourced human workers

Reviewers receive a **task template** containing instructions and examples explaining how to evaluate the AI output.

### 4.4 - Amazon A2I vs SageMaker Ground Truth

| **Service**                | **Main Purpose**                                            |
| -------------------------- | ----------------------------------------------------------- |
| **Amazon A2I**             | Human review of **ML predictions/inferences**               |
| **SageMaker Ground Truth** | Human and automated **data labeling** for training datasets |

**Memory aid:**
**Ground Truth = Label training data**
**A2I = Review model predictions**

### 4.5 - Exam Focus

- **Add human review to AI/ML predictions → Amazon A2I**
- **Low-confidence prediction requires human validation → Amazon A2I**
- **Randomly sample model outputs for human review → Amazon A2I**
- **Human-in-the-loop ML workflow → Amazon A2I**
- **Review workforce** → private workers, third-party providers, or **Amazon Mechanical Turk**
- **Provide reviewers with instructions/examples → Task template**

**Key exam distinction:**
**Ground Truth** → labeling data **before/during model training**
**A2I** → human review of model **predictions/results**

## 5 - Using Guardrails in Amazon Bedrock for Fairness and Safety

### 5.1 - Amazon Bedrock Guardrails Overview

**Guardrails for Amazon Bedrock** provide configurable safety controls for **generative AI applications**.

They evaluate **user inputs and model outputs** to help prevent unsafe, inappropriate, or unwanted content from reaching end users.

Guardrails can help address:
- **Harmful or offensive content**
- **Biased or inappropriate responses**
- **Personally identifiable information (PII)**
- **Prompt attacks / attempts to override instructions**
- **Hallucinated or irrelevant responses**
- Organization-specific prohibited topics

### 5.2 - Content Filters and Denied Topics

Bedrock Guardrails can apply **content filters** to harmful categories and let you configure the desired filtering strength.

You can also define **denied topics** that the application should not discuss.

Example:

**Denied topic: Investment advice**
User asks for investment advice → **Guardrail blocks the response** → configured refusal message is returned

This allows organizations to enforce application-specific policies beyond the model's default behavior.

### 5.3 - Prompt Attack Protection

Guardrails can help detect and block **prompt attacks**, where users attempt to manipulate a model or override its intended instructions.

**Malicious/manipulative input → Guardrail evaluation → Input blocked when policy is violated**

This helps keep generative AI applications operating within their intended boundaries.

### 5.4 - Word Filters and Sensitive Information

Guardrails support **word and phrase filters**, including filtering of inappropriate language such as **profanity**.

They can also detect **sensitive information**, including **PII** such as email addresses.

Sensitive information can be configured to be:
- **Blocked** → prevent the information from appearing
- **Masked** → replace or obscure the sensitive value

Example:
**Email address in output → Guardrail detects PII → Email is masked before being shown to the user**

### 5.5 - Reducing Hallucinations with Grounding Checks

Bedrock Guardrails can perform checks designed to determine whether responses are **relevant and grounded in appropriate information**

These checks can help reduce **hallucinations**, where a generative AI model produces information that sounds plausible but is unsupported or factually incorrect.

**Prompt + reference/context → Model response → Guardrail grounding/relevance checks**

### 5.6 - Guardrails Input and Output Evaluation

A key concept is that Guardrails can be applied to both sides of a generative AI interaction:

| **Area**             | **Example**                                                   |
| -------------------- | ------------------------------------------------------------- |
| **Input filtering**  | Block prompt attacks or requests involving denied topics      |
| **Output filtering** | Block harmful responses, mask PII, or check generated content |

This provides a safety layer between the **user** and the **foundation model**.

### 5.7 - Exam Focus

- **Apply safety controls to generative AI applications → Guardrails for Amazon Bedrock**
- **Block specific subjects → Denied topics**
- **Filter harmful or inappropriate content → Content filters**
- **Stop attempts to override model instructions → Prompt attack protection**
- **Block or hide email addresses and other PII → Sensitive information filters**
- **Obscure sensitive information instead of removing the whole response → Masking**
- **Filter specific words, phrases, or profanity → Word filters**
- **Help reduce unsupported or irrelevant generated responses → Grounding/relevance checks**
- **Guardrails can evaluate both prompts and model responses → Input + output protection**

**Memory aid:**
**Bedrock Guardrails = Block harmful content + Deny topics + Protect against prompt attacks + Filter PII + Reduce hallucinations**

## 6 - Exam Tips

### 6.1 - Responsible AI Tools Recap

| **AWS Tool**                  | **Exam Association**                                                                    |
| ----------------------------- | --------------------------------------------------------------------------------------- |
| **SageMaker Clarify**         | Detect **bias** and explain **model predictions**                                       |
| **SageMaker Ground Truth**    | Create **labeled training datasets** using human and automated labeling                 |
| **SageMaker Model Cards**     | Document model **purpose, performance, limitations, risks, and ethical considerations** |
| **SageMaker Model Monitor**   | Monitor deployed models for **data drift, bias, and performance degradation**           |
| **Amazon Augmented AI (A2I)** | Add **human review** to ML predictions                                                  |
| **Amazon Bedrock Guardrails** | Apply **safety controls** to generative AI inputs and outputs                           |

### 6.2 - Quick Service Distinctions

**Clarify** → Understand **bias and explainability**
**Ground Truth** → **Label training data**
**Model Cards** → **Document** the model
**Model Monitor** → **Monitor** the deployed model
**A2I** → Humans **review predictions**
**Bedrock Guardrails** → **Filter and protect generative AI interactions**

For **A2I**, human review can be triggered by:
- **Low confidence scores**
- **Random sampling**

For **Bedrock Guardrails**, think:

**Prompt attacks + Denied topics + Harmful content + Profanity + PII**

### 6.3 - Exam Focus

1. **Detect bias or explain why a model predicted something → SageMaker Clarify**
2. **Label data for ML training → SageMaker Ground Truth**
3. **Document model purpose, limitations, risks and metrics → SageMaker Model Cards**
4. **Detect data drift or model degradation after deployment → SageMaker Model Monitor**
5. **Human-in-the-loop review of uncertain AI predictions → Amazon A2I**
6. **Protect generative AI from unsafe prompts/content and PII exposure → Amazon Bedrock Guardrails**

**Fast memory aid:**
**Clarify = Explain
Ground Truth = Label
Cards = Document
Monitor = Watch
A2I = Human Review
Guardrails = Protect**
