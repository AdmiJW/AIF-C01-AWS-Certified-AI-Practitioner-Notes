## 1 - Key Elements of Training Foundation Models

### 1.1 - Key Foundation Model Training Processes

Foundation models go through different training/customization stages depending on whether the goal is to build general knowledge, specialize the model, or keep its knowledge current.

| **Process**                 | **Purpose**                               | **Data**                                    | **Key Idea**                                             |
| --------------------------- | ----------------------------------------- | ------------------------------------------- | -------------------------------------------------------- |
| **Pre-training**            | Build general capabilities                | Massive amounts of **unstructured data**    | Initial general learning                                 |
| **Fine-tuning**             | Customize for a specific task/use case    | High-quality **task-specific labeled data** | Specialization                                           |
| **Continuous pre-training** | Teach the model new information over time | New/domain-specific data                    | Keep knowledge current while retaining previous learning |

#### Pre-training

**Pre-training** is the initial training stage where a foundation model learns from very large datasets.

The model develops broad capabilities such as:
- Understanding language patterns
- Generating coherent responses
- Learning general knowledge and relationships in data

Pre-training is highly **resource-intensive** and is typically performed by large organizations rather than individual customers.

**Memory aid:**
Massive general data → **Pre-training** → General-purpose foundation model

#### Fine-tuning

**Fine-tuning** customizes an already pre-trained foundation model for a particular task or domain.

It uses **high-quality, task-specific labeled datasets** to refine the model's behavior and improve performance for a specific use case.

In **Amazon Bedrock**, fine-tuning involves preparing the training dataset and configuring resources for model customization.

**Important Bedrock characteristic:** A fine-tuned/custom model requires **Provisioned Throughput** for predictable and scalable inference performance

**Memory aid:**
Pre-trained model + Task-specific labeled data → **Fine-tuning** → Specialized model

#### Continuous Pre-training

**Continuous Pre-training** allows a foundation model to learn from additional data while retaining previously learned knowledge

Its main purpose is to:
- Incorporate **new information**
- Keep the model relevant as information changes
- Update knowledge for rapidly changing domains

Example: continuously training a customer-service model on newer support tickets so it learns about recent products, issues, and customer questions.

**Memory aid:**
Existing model + New knowledge → **Continuous pre-training** → Updated model

### 1.2 - Exam Focus

Know the distinction between the three processes:
- **Learn general capabilities from massive datasets → Pre-training**
- **Customize a model for a specific task using labeled data → Fine-tuning**
- **Add new knowledge and keep a model current → Continuous pre-training**
- **Fine-tuned/custom model in Amazon Bedrock → Provisioned Throughput**
- Scenario mentions **specialization or task-specific behavior** → Think **fine-tuning**
- Scenario mentions **new or changing domain knowledge** → Think **continuous pre-training**

## 2 - Methods for Fine-tuning Foundation Models

### 2.1 - Methods for Fine-tuning Foundation Models

Fine-tuning can be performed in different ways depending on whether the goal is to improve **instruction following**, specialize for a **domain**, or reuse knowledge for a **related task**.

| **Method**             | **Purpose**                                                                 | **Best Fit**                                                    |
| ---------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------- |
| **Instruction tuning** | Improve how well a model follows instructions or behaves for specific tasks | Desired response style, task behavior, prompt-response patterns |
| **Domain adaptation**  | Specialize a general-purpose model using industry/domain-specific data      | Healthcare, finance, legal, or other specialized fields         |
| **Transfer learning**  | Reuse knowledge from a pre-trained model for a new, related task            | Related tasks where existing knowledge can accelerate training  |

#### Instruction Tuning

**Instruction tuning** further trains a model using examples of instructions, prompts, and desired responses.

It helps the model:
- Follow instructions more effectively
- Develop a more nuanced understanding of specific tasks
- Produce responses that match desired behavior or style

Example: training a chatbot with examples of empathetic responses so it handles customer complaints more appropriately.

**Memory aid:**
Instructions + Desired responses → **Instruction tuning** → Better instruction following

#### Domain Adaptation

**Domain adaptation** specializes a general-purpose model by further training it on data from a particular **industry, field, or subject area**.

Examples include:
- Healthcare
- Finance
- Legal services
- Technical domains

The goal is to improve the model's understanding of **domain-specific terminology, knowledge, and tasks**

**Memory aid:**
General model + Industry-specific data → **Domain adaptation** → Domain-specialized model

#### Transfer Learning

**Transfer learning** uses knowledge learned by a pre-trained model and applies it to a **new but related task**.

Instead of training a model from scratch, existing learned features and knowledge are reused, which can reduce:
- **Training time**
- **Compute requirements**
- **Cost**

Transfer learning is most effective when the original and new tasks have meaningful **similarities**.

Example: a model trained on general text can be fine-tuned for finance-related text or tasks.

**Memory aid:**
Pre-trained knowledge + Related new task → **Transfer learning**

### 2.2 - Exam Focus

- **Improve instruction following or desired response behavior → Instruction tuning**
- **Specialize a general model for healthcare, finance, legal, etc. → Domain adaptation**
- **Reuse knowledge from an existing model for a related task → Transfer learning**
- **Avoid training from scratch and reduce compute/cost → Transfer learning**
- Transfer learning works best when the **source and target tasks are related**
- Scenario mentions **prompt-response examples with desired behavior** → Think **instruction tuning**

## 3 - Preparing Data to Fine-tune a Foundation Model

**High-quality data** is essential for effective foundation model fine-tuning. Poor-quality data can produce **biased, inaccurate, or unreliable outputs**.

Good preparation ensures the training data is relevant to the intended use case and representative of real-world scenarios.

| **Data Preparation Concept** | **Purpose**                                                        |
| ---------------------------- | ------------------------------------------------------------------ |
| **Data curation**            | Select and organize relevant, accurate, high-quality data          |
| **Data governance**          | Ensure data quality, privacy, accuracy, and ethical use            |
| **Data representativeness**  | Cover diverse scenarios and reduce bias                            |
| **Data labeling**            | Add tags or categories that help the model learn patterns          |
| **RLHF**                     | Use human feedback to align model responses with human preferences |

#### Data Curation

**Data curation** involves selecting, organizing, and filtering training data so that it is:
- Relevant
- Accurate
- High quality
- Free from unnecessary noise and redundancy

Example: when fine-tuning a model for **legal text**, unrelated content such as fiction or general blogs should be removed

**Memory aid:**
Select + Filter + Organize relevant data → **Data curation**

#### Data Governance

**Data governance** refers to the **policies, processes, and practices** used to manage training data responsibly.

It helps organizations ensure:
- **Data quality and accuracy**
- Compliance with **privacy regulations**
- **Ethical data use**
- Appropriate data handling practices

For fine-tuning, governance is especially important when training data contains sensitive, regulated, or proprietary information.

#### Data Size and Representativeness

A larger dataset can provide richer training information, but **more data is not automatically better**

The most important factors are:
- **Quality** - data should be accurate and useful
- **Representativeness** - data should cover a sufficiently wide range of relevant scenarios

Poorly representative data can introduce or reinforce **model bias**

**Key distinction:**
**Quality + representativeness > raw data quantity**

#### Data Labeling

**Data labeling** means annotating training data with **tags, categories, or expected outputs** so the model can learn specific patterns.

Example:
Email 1 → **Spam**
Email 2 → **Not Spam**

Labeled datasets are particularly important for supervised fine-tuning tasks.

#### Reinforcement Learning from Human Feedback (RLHF)

**Reinforcement Learning from Human Feedback (RLHF)** aligns a model's behavior with **human preferences**.

A typical flow is:

Model responses → **Human evaluation/ranking** → **Reward model** → Model optimization

Human evaluators assess or rank model responses. This feedback is used to train a **reward model**, which learns to predict how desirable a generated response is.

The foundation model can then be optimized using this reward signal to generate responses that better align with human preferences.

### 3.2 - Exam Focus

- **Select, filter, and organize relevant high-quality data → Data curation**
- **Policies and processes for quality, privacy, accuracy, and ethical data use → Data governance**
- **More data is not always better** → Prioritize **quality and representativeness**
- **Cover diverse scenarios and reduce bias → Representative data**
- **Annotate examples with tags or categories → Data labeling**
- **Use direct human preferences to improve model responses → RLHF**
- **Predict the quality/desirability of model responses from human feedback → Reward model**
- Remember: **High-quality data is the backbone of effective fine-tuning**

## 4 - Exam Tips

### 4.1 - Training & Fine-Tuning Recap

| **Concept**                 | **Exam Association**                                                                                  |
| --------------------------- | ----------------------------------------------------------------------------------------------------- |
| **Pre-training**            | Learn general capabilities from vast amounts of **unstructured data**                                 |
| **Fine-tuning**             | Customize a pre-trained model using **task-specific data**                                            |
| **Continuous pre-training** | Learn **new information** while retaining previously learned knowledge                                |
| **Instruction tuning**      | Improve ability to **follow explicit instructions**                                                   |
| **Domain adaptation**       | Further train a general model on **industry/domain-specific data**                                    |
| **Transfer learning**       | Apply knowledge from a pre-trained model to a **new, related task**                                   |
| **Data curation**           | Select and organize **relevant, accurate, high-quality data**                                         |
| **Data governance**         | Policies and processes for **quality, accuracy, privacy, and ethical data use**                       |
| **Data size**               | Total amount of training data; **more is not always better**                                          |
| **Data representativeness** | Ensure training data reflects the diversity and characteristics of the intended real-world population |
| **Data labeling**           | Add **tags/categories** to help the model learn patterns                                              |
| **RLHF**                    | Use **human feedback** to train a **reward model** and improve responses                              |

Key flow:

**Pre-training → Continuous pre-training / Fine-tuning → Task or domain specialization**

For fine-tuning data, prioritize:

**Quality + Relevance + Representativeness > Raw Quantity**

### 4.2 - Exam Focus

- **Massive unstructured data + general capabilities → Pre-training**
- **Task-specific customization → Fine-tuning**
- **Keep model knowledge current → Continuous Pre-training**
- **Follow instructions better → Instruction tuning**
- **Healthcare, finance, legal, etc. specialization → Domain adaptation**
- **Reuse knowledge for a related task → Transfer learning**
- **Select and organize good training data → Data curation**
- **Policies, privacy, ethics, and data quality controls → Data governance**
- **Reflect real-world diversity and reduce bias → Data representativeness**
- **Annotate data with tags/categories → Data labeling**
- **Human preferences + reward model → RLHF**