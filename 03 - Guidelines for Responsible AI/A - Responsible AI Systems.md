## 1 - Features of Responsible AI

### 1.1 - Responsible AI Overview

**Responsible AI** ensures AI systems are not only effective, but also **ethical, transparent, trustworthy, fair, reliable, and aligned with human values**

Key dimensions include:
- **Fairness and bias mitigation**
- **Explaiability**
- **Transparency**
- **Robustness**
- **Veracity**
- **Controllability**
- **Environmental sustainability**

### 1.2 - Fairness and Bias Mitigation

**Fairness** means AI systems should not unfairly affect different groups or subpopulations.

For example, a self-driving vehicle should detect and respond appropriately to pedestrians regardless of **race, gender, age, or background**.

Reducing bias starts with **inclusive and representative training data**. Training datasets should include:
- People from diverse backgrounds and demographics groups
- Different road users, such as pedestrians, cyclists, and vehicle types
- Different behaviors and driving styles
- A wide variety of scenarios and tasks, such as parking, merging, and lane changing
- **Balanced representation** so groups or conditions are not overrepresented or underrepresented

Data should also come from **high-quality sources** and be **consistently labeled**.

**Ethical labeling** requires annotators to remain **neutral** and **objective**, helping prevent human biases from being introduced into training data.

### 1.3 - Explainability

**Explainability** means being able to understand the reasoning behind an AI model's prediction or decision.

This is particularly important for complex models such as **neural networks**, which may otherwise behave like **black boxes**.

For example, instead of simply returning:

> Loan denied

an explainable model could identify factors such as:
- Credit score below an established threshold
- Income below the requirement for the loan

Explainability helps:
- Build **trust**
- Identify errors
- Detect potential bias
- Evaluate whether AI decisions are reasonable

### 1.4 - Transparency

**Transparency** means being open about **how an AI system is designed, trained, and operated**

Transparency can include information about:

| **Component**                  | **What is disclosed**                        |
| ------------------------------ | -------------------------------------------- |
| **Algorithms**                 | Techniques/models used to process data       |
| **Training data**              | Data used to train the model and its sources |
| **Training process**           | How the system was trained                   |
| **Decision criteria/features** | Factors used when producing decisions        |

For example, a transparent credit scoring system might disclose that it uses **credit score and income**, where those values originated, and which algorithm processes them.

#### Explainability vs. Transparency

| **Concept**        | **Focus**                                                                                        |
| ------------------ | ------------------------------------------------------------------------------------------------ |
| **Explainability** | Understanding **why a specific prediction or decision occurred**                                 |
| **Transparency**   | Understanding **how the overall AI system works**, including its data, algorithms, and processes |

### 1.5 - Robustness and Veracity

**Robustness** is the ability of an AI system to continue operating effectively under **challenging, unexpected, or changing conditions**

Example: A self-driving vehicle correctly detecting a pedestrian even during **bad-weather**

**Veracity** relates to the **accuracy and truthfulness of the information** used by the AI system. Decisions should be based on reliable and, where necessary, **up-to-date or real-time data**

| **Dimension**  | **Key idea**                                               |
| -------------- | ---------------------------------------------------------- |
| **Robustness** | Performs reliably despite difficult or changing conditions |
| **Veracity**   | Uses accurate and trustworthy information                  |

### 1.6 - Controllability

**Controllability** ensures AI systems remain aligned with **human values and intentions** and that humans can maintain appropriate control over their behavior.

For example:
- A self-driving vehicle may be designed to prioritize **safety over speed**.
- Humans should have the ability to **intervene or override** an automated system when necessary.

**Key idea:** AI should support human objectives rather than removing meaningful human control.

### 1.7 - Environmental Sustainability

Responsible AI also considers the **environmental impact** of developing and operating AI systems.

Choosing energy-efficient infrastructure can reduce the energy consumption and carbon footprint associated with AI workloads.

AWS provides specialized AI/ML hardware:

| **AWS hardware**   | **Primary purpose**                                     |
| ------------------ | ------------------------------------------------------- |
| **AWS Trainium**   | Optimized for **ML model training**                     |
| **AWS Inferentia** | Optimized for **ML inference / production predictions** |

These accelerators are designed to provide high performance and efficiency for AI workloads, including large models.

**Memory aid:**
**Trainium → Training**
**Inferentia → Inference**

### 1.8 - Exam Focus

1. **Prevent unfair treatment across groups → Fairness and bias mitigation**
2. **Diverse, balanced, representative training data** → Reduces **bias**
3. **Understand why a particular prediction occurred → Explainability**
4. **Know the model's data, algorithms, training process, and decision criteria → Transparency**
5. **Operate reliably under unexpected or difficult conditions → Robustness**
6. **Use accurate and trustworthy information → Veracity**
7. **Keep humans in control / allow intervention → Controllability**
8. **Reduce the environmental impact of AI workloads → Environmental sustainability**
9. **Optimized hardware for model training → AWS Trainium**
10. **Optimized hardware for inference → AWS Inferentia**

## 2 - Bias and Variance

### 2.1 - Model Fit

**Model Fit** describes how well a machine learning model learns from its **training data** and performs on **new, unseen data**.

A good model should **generalize** well rather than simply memorizing the training data.

Two key sources of model error are:
- **Bias** → model is too simple and consistently misses important patterns
- **Variance** → model is too sensitive to the training data and does not generalize well.

### 2.2 - Bias

**Bias** is the systematic difference between a model's predictions and the actual values

**High bias** usually means the model has not captured enough of the underlying patterns in the data.

Example: Predicting house prices using only **square footage** while ignoring important factors such as location or number of bedrooms.

Ways to reduce high bias include:
- Add **relevant features**
- Use a model capable of capturing more complex patterns

### 2.3 - Variance

**Variance** measures how much a model's predictions change when it is trained on different datasets.

**High variance** means the model is overly sensitive to its training data, including noise or irrelevant patterns.

The model may perform extremely well on training data but poorly on **new, unseen data**.

Ways to reduce high variance include:
- Remove **irrelevant or unnecessary features**
- Increase the amount of **training data**
- Use **data augmentation** when collecting additional real-world data is difficult.

**Data augmentation** creates additional training examples by modifying existing data, such as:
- Rotating or transforming images
- Making controlled modifications to text

### 2.4 - Underfitting vs. Overfitting

| **Concept**      | **Cause**                                                     | **Training Performance** | **Unseen Data Performance** |
| ---------------- | ------------------------------------------------------------- | ------------------------ | --------------------------- |
| **Underfitting** | **High bias;** model is too simple                            | Poor                     | Poor                        |
| **Overfitting**  | **High variance;** model learns noise and details too closely | Very good                | Poor                        |
| **Balanced fit** | Appropriate bias-variance balance                             | Good                     | Good                        |

#### Underfitting

**Underfitting** occurs when a model does not learn enough from the training data

It fails to capture important underlying patterns and therefore performs poorly on **both training and test data**.

Example: A diabetes model considers only age, gender, and BMI while ignoring other relevant predictive information

#### Overfitting

**Overfitting** occurs when a model learns the training data too closely, including **noise and irrelevant patterns**.

It performs well on the training set but poorly on unseen data because it does not **generalize** effectively.

Example: A loan-default model uses many irrelevant features that happen to fit historical loans but do not reliably predict future cases.

**Memory aid:**
**High-bias → Underfitting**
**High variance → Overfitting**

### 2.5 - Bias-Variance Tradeoff

A robust model aims to achieve an appropriate balance between **bias and variance**

- Too much bias → model is too simple
- Too much variance → model is too specialized to training data
- Balanced model → learns meaningful patterns and **generalizes well** to unseen data

The goal is not simply to achieve the best possible training performance; it is to achieve reliable performance on **new data**.

### 2.6 - Subgroup Analysis and Fairness

**Subgroup analysis** evaluates model performance separately across different groups to identify potential **bias or fairness issues**

Subgroups may be defined using attributes such as:
- Race
- Gender
- Age
- Socioeconomic status

A model can have acceptable overall accuracy while performing poorly for a particular subgroup

Subgroup analysis therefore helps determine whether a model performs **accurately and fairly across different populations**.

### 2.7 - Exam Focus

1. **High bias → Underfitting**
2. **High variance → Overfitting**
3. Poor performance on **training and test data** → Likely **underfitting**
4. Excellent training performance but poor unseen-data performance → Likely **overfitting**
5. Reduce high bias → Add **relevant features** or use a more capable model
6. Reduce high variance → Remove unnecessary features, obtain **more training data**, or use **data augmentation**
7. Ability to perform well on unseen data → **Generalization**
8. Evaluate model performance across demographic or protected groups → **Subgroup analysis**
9. Goal of model fitting → Balance **bias** and **variance** so the model generalizes well.

## 3 - Types of Bias

### 3.1 - Measurement Bias

**Measurement bias** occurs when the data being collected is systematically inaccurate because of a problem with the **measurement process or instrument**.

Example: A poorly calibrated blood pressure device consistently records readings lower than the true values. A model trained on this faulty data may learn incorrect relationships and produce inaccurate predictions.

**Key idea:**
**Faulty measurement → Faulty data → Biased model**

### 3.2 - Sampling Bias

**Sampling bias** occurs when the training data is **not representative of the overall population** the model will be used on.

Example: A model studying the relationship between a supplement and heart health is trained only on people with healthy lifestyles. Its predictions may not generalize to people with less healthy lifestyles.

Sampling bias can cause poor **generalization** because important groups or conditions are underrepresented or excluded.

### 3.3 - Confirmation Bias

**Confirmation bias** occurs when people focus on data that supports an existing belief while ignoring evidence that contradicts it.

Example: A hiring team assumes that only candidates with a particular degree will succeed and selects data that supports this assumption while disregarding successful candidates without that degree.

**Key idea**: Existing belief influences which evidence is considered.

### 3.4 - Observer Bias

**Observer bias** occurs when a person collecting, interpreting, or labeling data allows their **subjective opinions** or **preferences** to affect the recorded data.

Example: If a loan officer unconsciously gives lower ratings to equally qualified applicants from certain demographic groups, those biased judgements may become part of the historical training data. The model can then learn and reproduce that bias.

Observer bias is especially relevant during **data collection and labeling**.

### 3.5 - Bias Comparison

| **Bias Type**         | **Main Cause**                                     | **Exam Clue**                         |
| --------------------- | -------------------------------------------------- | ------------------------------------- |
| **Measurement bias**  | Inaccurate measurement method or instrument        | Faulty sensor, device, or measurement |
| **Sampling bias**     | Dataset does not represent the target population   | Missing or underrepresented groups    |
| **Confirmation bias** | Evidence is selected to support an existing belief | Ignoring contradictory information    |
| **Observer bias**     | Human judgement influences collection or labeling  | Subjective annotator or evaluator     |

### 3.6 - Exam Focus

1. **Faulty or miscalibrated measurement device → Measurement bias**
2. **Training sample does not represent the full population → Sampling bias**
3. **Only considering evidence that supports an existing assumption → Confirmation bias**
4. **Human opinions influence data collection or labeling → Observer bias**
5. Historical human bias recorded in training data can be **learned and reproduced by the model**
6. For exam questions, identify **where the bias originates**: measurement, sample selection, existing beliefs, or human observation

## 4 - Transparency and Explainability in Models

### 4.1 - Transparency, Interpretability, and Explainability

**Transparency** refers to how clearly the internal workings, structure, data, and decision process of a model can be understood.

Greater transparency generally leads to greater **interpretability**.

**Interpretability** is the degree to which a human can understand how a model produces its outputs.

**Explainability** focuses on understanding **why a specific prediction or decision was made**, even when the underlying model is complex.

| **Concept**          | **Main Focus**                                  |
| -------------------- | ----------------------------------------------- |
| **Transparency**     | Visibility into how the model works             |
| **Interpretability** | How easily humans can understand the model      |
| **Explainability**   | Why a particular prediction or decision occured |

### 4.2 - Transparent Models

Some models are naturally easier to understand than others.

**Decision trees** are highly transparent and interpretable because their structure resembles a **flowchart**. A prediction can be traced through a sequence of decisions based on input features.

This makes it relatively easy to identify:
- Which features were used.
- Which decisions were made
- How those decisions led to the final prediction

**Decision tree → High transparency → High interpretability**

### 4.3 - Black-Box Models

**Neural networks** are typically much harder to interpret because they contain many interconnected layers and parameters

Their complexity makes it difficult to directly understand how individual inputs produce a particular prediction. For this reason, they are often described as **black-box models**.

However, a black-box model can still be made **partially explainable** using techniques that identify which features or input region influenced a prediction.

Example: For an image classification mode, an explanation might identify which parts of the image contributed most strongly to the prediction.

### 4.4 - Transparency vs. Model Performance

There can be a trade-off between **transparency and model performance**.

Simple models are often easier to interpret, while more complex models may capture more intricate patterns in data.

| **Model Characteristic** | **Typical Effect**                                            |
| ------------------------ | ------------------------------------------------------------- |
| Simpler model            | Higher transparency and interpretability                      |
| More complex model       | Lower transparency, potentially greater predictive capability |

This is not an absolute rule, but it is an important exam concept.

**Memory aid:**
**Simple → Easier to understand**
**Complex → Harder to interpret**

### 4.5 - Transparency and Safety

Greater transparency can improve AI safety by helping teams identify:
- **Bias**
- **Unintended consequences**
- **Harmful behavior**
- Errors in the decision process

However, excessive transparency can also create security risks.

If too many internal details are disclosed, malicious actors may discover **system vulnerabilities** and exploit them.

Therefore, responsible AI requires balancing:

**Transparency ↔ Performance ↔ Security/Safety**

### 4.6 - Exam Focus

1. **Understand how the model works → Transparency**
2. **Understand how easily humans can follow the model's logic → Interpretability**
3. **Understand why a specific prediction was made → Explanability**
4. **Decision tree** → Typically **high transparency and interpretability**
5. **Neural network** → Often a **black-box model** with lower interpretability
6. Complex models can still use explanation techniques to identify **important features or influential input areas**
7. Greater transparency can help reveal **bias, harmful behavior, and unintended consequences**
8. Too much transparency can expose **security vulnerabilities**
9. Common trade-off → More complex models may offer stronger performance while being harder to interpret

## 5 - Risks of GenAI Models

### 5.1 - Hallucination

A **hallucination** occurs when a generative AI model produces information that sounds plausible but is **incorrect, fabricated, or unsupported by facts**.

Examples include:
- Inventing a quotation
- Making up a source or reference
- Providing false factual information with confidence

Generative AI models do not inherently verify whether information is true. They generate outputs by predicting likely patterns based on their training data.

**Key mitigation**: Verify important AI-generated information against trusted sources.

**Memory aid:**
**Believable but false → Hallucination**

### 5.2 - Prompt Leaking

**Prompt leaking** occurs when a model reveals information about its **internal instructions, system prompts, hidden context, or prior interaction history** that should not be exposed.

Examples may include disclosure of:
- Internal system instructions
- Hidden prompts
- Conversation context that should remain private
- Internal rules governing model behavior

Prompt leaking is a security and privacy concern because it can expose information about how the system operates.

### 5.3 - Model Exposure

**Model exposure** refers to the unintended disclosure of **sensitive, confidential, or private information** through a model's output

This information could originate from:
- Previous user inputs
- Confidential organizational data
- Sensitive information present in training or connected data sources

Example: A model unintentionally reveals a company's confidential business strategy.

#### Prompt Leaking vs. Model Exposure

| **Risk**           | **What is exposed?**                                             |
| ------------------ | ---------------------------------------------------------------- |
| **Prompt leaking** | Internal prompts, instructions, context, or conversation history |
| **Model exposure** | Sensitive, private, or confidential information                  |

### 5.4 - Intellectual Property Infringement

Generative AI models may be trained on data that includes **copyrighted or proprietary material**.

A model may generate content that closely resembles or reproduces protected material, creating a risk of **intellectual property (IP) infringement**.

Possible concerns include:
- Reproducing copyrighted text or creative works
- Generating content that is substantially similar to protected material
- Legal risks for organizations or users that publish or distribute generated content

**Key idea:** AI-generated content is not automatically free from copyright or IP concerns.

### 5.5 - Major GenAI Risk Comparison

| **Risk**            | **Exam Clue**                                                 |
| ------------------- | ------------------------------------------------------------- |
| **Hallucination**   | Plausible but false or fabricated information                 |
| **Prompt leaking**  | Internal instructions or hidden context are revealed          |
| **Model exposure**  | Confidential or private information is disclosed              |
| **IP infringement** | Generated output resembles or reproduces copyrighted material |

### 5.6 - Exam Focus

1. **AI generates convincing but incorrect information → Hallucination**
2. **Internal system instructions or hidden prompts are disclosed → Prompt leaking**
3. **Sensitive or confidential information is unintentionally revealed → Model exposure**
4. **Generated content reproduces or closely resembles copyrighted material → Intellectual property infringement**
5. GenAI output should be **validated against trusted sources** when factual accuracy matters
6. Remember the distinction: **prompt leaking exposes instructions/context; model exposure exposes sensitive data**

## 6 - Human-centered Design for Explainable AI

### 6.1 - Human-Centered Design Overview

**Human-centered design (HCD)** is a methodology that places **human needs, abilities, and experiences** at the center of the AI design process.

The goal is to build AI systems that are not only effective, but also:
- Easy to understand
- Fair and transparent
- Accessible and usable
- Supportive of human decision-making

**Key idea:** AI should **augment human abilities**, not simply replace human judgement.

### 6.2 - Design for Amplified Decision-Making

AI should help humans make **better and faster decisions**, especially in high-pressure situations.

Key characteristics include:
- **Clarity** → Information and explanations should avoid unnecessary complexity.
- **Simplicity** → Interfaces and explanations should avoid unnecessary complexity
- **Usability** → Systems should be intuitive and practical for users
- **Reflexivity** → Systems should evaluate past outcomes and use them to improve future behavior.

Example: A self-driving vehicle should make rapid decisions while presenting controls and information in a way that is clear and intuitive to the human user.

### 6.3 - Design for Unbiased Decision-Making

AI systems should support **fair and transparent decision processes** and help reduce human and algorithmic bias.

This includes:
- Making relevant decision factors visible
- Applying consistent criteria across users
- Training human decision-makers to recognize and address bias.

Example: An AI hiring system should clearly show how factors such as **experience and qualifications** influenced a recommendation.

A loan approval system should apply the same relevant criteria regardless of characteristics such as **gender or ethnicity**.

### 6.4 - Design for Human and AI Learning

Human-centered AI should create environments where **both humans and AI systems can learn effectively**

Three important strategies are:

| **Strategy**                 | **Purpose**                                          |
| ---------------------------- | ---------------------------------------------------- |
| **Cognitive apprenticeship** | AI learns from human guidance and feedback           |
| **Personalization**          | Learning experiences are adapted to individual needs |
| **User-centered design**     | Tools are intuitive and accessible to diverse users  |

#### Cognitive apprenticeship and RLHF

**Cognitive apprenticeship** emphasizes learning through human guidance and feedback.

In AI, this is commonly associated with **Reinforcement Learning from Human Feedback (RLHF)**, where human feedback is used to improve model behavior.

**Human feedback → Model learns preferred behavior → Improved responses**

#### Personalization

**Personalization** adapts the learning experience to the individual user's:
- Needs
- Preferences
- Abilities
- Learning style

#### User-Centered Design

**User-centered design** ensures systems and learning tools are usable and accessible to a broad range of people.

This includes consideration for users with:
- **Disabilities**
- **Language barriers**
- Different technical abilities or needs

### 6.5 - Human-Centered Design Principles

| **Principle**                 | **Main Goal**                                     |
| ----------------------------- | ------------------------------------------------- |
| **Amplified decision-making** | Help humans make better decisions                 |
| **Unbiased decision-making**  | Promote fair and transparent decisions            |
| **Human and AI learning**     | Enable humans and AI to improve through learning  |
| **Personalization**           | Adapt experiences to individual needs             |
| **Accessibility**             | Ensure systems can be used by diverse populations |

### 6.6 - Exam Focus

1. **Put user needs at the center of AI development → Human-centered design**
2. **AI assists rather than replaces human judgement → Amplified decision-making**
3. **Clarity, simplicity, usability, reflexivity** → Principles supporting better human decision
4. **Transparent and consistent decision criteria → Unbiased decision-making**
5. **AI learns from human feedback → RLHF / cognitive apprenticeship**
6. **Adapt experience to an individual learner → Personalization**
7. **Support users with disabilities or language barriers → User-centered and accessible design**
8. Human-centered AI should promote **fairness, transparency, usability, and improved human experience**

## 7 - Exam Tips

### 7.1 - Responsible AI Recap

**Responsible AI** ensures AI/ML systems are **ethical, transparent, trustworthy, fair, safe, and aligned with human needs**

| **Dimension**                 | **Exam Association**                                               |
| ----------------------------- | ------------------------------------------------------------------ |
| **Transparency**              | Understand how the model works: data, algorithms, training process |
| **Explainability**            | Understand why a specific prediction was made                      |
| **Fairness**                  | Avoid unfair outcomes across groups                                |
| **Controllability**           | Maintain appropriate human control                                 |
| **Veracity**                  | Use accurate and trustworthy information                           |
| **Robustness**                | Perform reliably under changing or difficult conditions            |
| **Safety, privacy, security** | Prevent harm and protect information                               |
| **Governance**                | Policies and oversight for responsible AI use                      |

**High transparency** → **High interpretability**, although simpler, more interpretable models may sometimes trade off predictive capability against more complex models.

### 7.2 - Bias and Variance Recap

| **Problem**                     | **Meaning**                                                         | **Typical Fix**                                                       |
| ------------------------------- | ------------------------------------------------------------------- | --------------------------------------------------------------------- |
| **High bias / Underfitting**    | Model is too simple; poor on training and unseen data               | Add relevant features; use a more capable model                       |
| **High variance / Overfitting** | Model learns training data / noise too closely; poor generalization | Use fewer relevant features; add training data; use data augmentation |

**Goal**: Achieve a good **bias-variance balance** so the model generalizes well to unseen data.

Remember the bias types:
- **Measurement bias** → Faulty measurement or data collection
- **Sampling bias** → Training data is not representative
- **Confirmation bias** → Favoring evidence that supports existing beliefs
- **Observer bias** → Human judgement influences data collection or labeling.

### 7.3 - GenAI Risk Recap

| **Risk**            | **Key Clue**                                                        |
| ------------------- | ------------------------------------------------------------------- |
| **Hallucination**   | Plausible but fabricated or incorrect information                   |
| **Model exposure**  | Sensitive or confidential information is revealed                   |
| **Prompt leaking**  | User prompts, hidden context, or system instructions are exposed    |
| **IP infringement** | Generated content reproduces or closely resembles protected content |

### 7.4 - Human-Centered Design Recap

**Human-centered design (HCD)** places users and their needs at the center of AI development.

Key goals include:
- **Amplifying human decision-making**
- Supporting **fair and unbiased decisions**
- Improving **transparency and explainability**
- Supporting **human and AI learning**
- Promoting **safety, accessibility, and usability**

### 7.5 - Exam Focus

1. **How does the model work? → Transparency**
2. **Why did the model make this prediction? → Explainability**
3. **High bias → Underfitting**
4. **High variance → Overfitting**
5. **Unrepresentative dataset → Sampling bias**
6. **Faulty measurement method → Measurement bias**
7. **Human subjectivity in labeling → Observer bias**
8. **Favoring supporting evidence → Confirmation bias**
9. **Believable but false GenAI output → Hallucination**
10. **Sensitive data revealed → Model exposure**
11. **System instructions or prompts revealed → Prompt leaking**
12. **Design AI around real human needs → Human-centered design**

