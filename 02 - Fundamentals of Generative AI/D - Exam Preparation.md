## 1 - Approaching AIF-C01 Exam Questions

### 1.1 - Core Generative AI Mechanics 

For the **AIF-C01 exam**, focus on how generative AI works conceptually rather than on mathematical details or implementation code.
- **Tokens** → Units of text processed by a model. A word may consist of one or multiple tokens.
- **Transformer architecture** → Foundation of most modern generative AI models and a major driver or recent generative AI advances
- **Embeddings** → Numerical representations of data such as text
- **Vectors** → Embeddings are represented as vectors in a **high-dimensional vector space**, where semantically similar concepts are positioned closer together.

**Exam associations:**

- **Text converted into numerical representations → Embeddings**
- **Relationships/similarity between concepts → Vector space**
- **Architecture underlying modern LLMs → Transformers**

### 1.2 - Common Generative AI Limitations

| **Limitation**               | **Meaning**                                                                             |
| ---------------------------- | --------------------------------------------------------------------------------------- |
| **Hallucination**            | Model generates plausible but incorrect or unsupported information                      |
| **Nondeterminism**           | The same or similar prompt can produce different outputs                                |
| **Limited interpretability** | It can be difficult to explain exactly why a complex model produced a particular result |

When a scenario emphasizes **trust, factual accuracy, consistency, or explainability**, consider these limitations.

### 1.3 - Choosing a Model Modality

Choose the model based on the type of **input and output** required

| **Model Type**    | **Typical Uses**                                                |
| ----------------- | --------------------------------------------------------------- |
| **Text-to-text**  | Summarization, translation, question answering, code generation |
| **Text-to-image** | Marketing assets, illustrations, product mock-ups               |
| **Multimodal**    | Work with multiple data types such as text, images, and audio   |

Examples of text models include **Anthropic Claude** and Amazon Nova models.

Image generation commonly uses **diffusion models**, such as image-generation foundation models available through AWS.

**Exam tip:** Identify the required **modality** before choosing the model.

### 1.4 - Key AWS Services and AI Hardware

#### Amazon Bedrock

Choose **Amazon Bedrock** when the requirement emphasizes:
- **Serverless** generative AI
- Access to foundation models through **APIs**
- Rapid application development
- Minimal infrastructure management

**Bedrock = Managed FMs + APIs + fast deployment**

#### Amazon SageMaker and SageMaker JumpStart

Choose **SageMaker JumpStart** when you need pre-trained or open-source models with greater control over deployment and infrastructure.

Choose **Amazon SageMaker** when you need to:
- Build proprietary models
- Train custom models
- Control ML infrastructure or compute configurations

- **Bedrock → Less infrastructure management**
- **JumpStart/SageMaker → More control and customization**

#### AWS AI Chips

| **Chip**           | **Primary Purpose**                            |
| ------------------ | ---------------------------------------------- |
| **AWS Trainium**   | Cost-effective **model training**              |
| **AWS Inferentia** | Cost-effective, high-performance **inference** |

**Memory aid:**
**Trainium → Training**
**Inferentia → Inference**

### 1.5 - Fine-Tuning vs RAG

This distinction is highly testable.

| **Technique**                            | **Best When**                                                                          |
| ---------------------------------------- | -------------------------------------------------------------------------------------- |
| **Fine-tuning**                          | The model needs to learn specialized behavior, terminology, style, or domain patterns  |
| **Retrieval-Augmented Generation (RAG)** | The model needs access to current, private, or frequently changing factual information |

**Fine-tuning** modifies a model's internal weights.

Use it for scenarios such as:
- Learning a particular **brand voice**
- Adapting to specialized terminology
- Improving performance for a specific domain or task

**RAG** retrieves relevant information at inference time and adds it to the model's context without retraining the model.

Use it when information:
- Changes frequently
- Must remain current
- Exists in enterprise knowledge sources
- Should be incorporated without repeatedly retraining the model.

**Memory aid:**
- **Change model behavior → Fine-tuning**
- **Give model current knowledge → RAG**

### 1.6 - AIF-C01 Question Formats

The exam may use several question styles:
- **Multiple choice / multiple response** → Select the best solution from available choices
- **Ordering** → Arrange stages or processes into the correct sequence
- **Matching** → Match services, concepts, advantages, or disadvantages with their definitions
- **Scenario-based questions** → Identify the service or technique that best satisfies business requirements

For longer scenarios, identify the key requirement first rather than focusing on every technical detail.

For example,

**Serverless + foundation model API + rapid deployment**
**→ Amazon Bedrock**

**Maximum ML infrastructure/model control**
**→ Amazon SageMaker**

### 1.7 - How to Approach Generative AI Exam Questions

Focus on **why a business would choose a particular service or technique**, rather than low-level Python or SDK syntax.

Look for requirement keywords:

| **Scenario Keyword**                               | **Likely Answer**       |
| -------------------------------------------------- | ----------------------- |
| Serverless, FM API, rapid deployment               | **Amazon Bedrock**      |
| Open-source/pre-trained model + deployment control | **SageMaker JumpStart** |
| Build/train proprietary model                      | **Amazon SageMaker**    |
| Learn brand style or specialized terminology       | **Fine-tuning**         |
| Current/private enterprise knowledge               | **RAG**                 |
| Train models efficiently                           | **AWS Trainium**        |
| Run inference efficiently                          | **AWS Inferentia**      |

A useful approach is:

**Identify requirement → Determine level of control → Determine whether knowledge or behavior must change → Choose AWS service/technique** 

### 1.8 - Exam Focus

1. **Basic unit processed by an LLM → Token**
2. **Core architecture behind modern LLMs → Transformer**
3. **Numerical representation of semantic meaning → Embedding/vector**
4. **Plausible but false model output → Hallucination**
5. **Same prompt can produce different answers → Nondeterminism**
6. **Summarization, translation, code generation → Text-to-text model**
7. **Image generation** → Commonly **diffusion-based models**
8. **Multiple input/output data types → Multimodal model**
9. **Fast, serverless access to foundation models → Amazon Bedrock**
10. **Existing/open-source model with greater deployment control → SageMaker JumpStart**
11. **Build and train proprietary models → Amazon SageMaker**
12. **Model training hardware → AWS Trainium**
13. **Model inference hardware → AWS Inferentia**
14. **Change model behavior/style or specialized terminology → Fine-tuning**
15. **Add current/private factual information without retraining → RAG**

**Key exam mindset:**
**Don't ask "How is this coded?" → Ask "Why would the business choose this service or technique?"**

## 2 - Approaching the AWS Certified AI Practitioner (AIF-C01) exam (Generative AI)

### 2.1 - Time Management Strategy

The **AIF-C01 exam** has limited time, so avoid spending too long on a single difficult question.

A useful approach is a **two-pass strategy:**
1. **Pass 1** → Answer questions you know quickly
2. **Mark difficult questions for review** rather than getting stuck
3. **Pass 2** → Return to flagged questions with the remaining time

if you cannot confidently narrow down an answer after roughly a minute, make your best choice, **mark it for review**, and continue

This helps protect easy marks and prevents one difficult scenario from consuming too much exam time.

### 2.2 - Read for Exam Keywords

Many AWS questions can be solved by identifying the **business requirement** hidden in the scenario.

Common associations:

| **Keyword / Requirement**                                        | **Likely Direction**                             |
| ---------------------------------------------------------------- | ------------------------------------------------ |
| **Serverless, rapid genAI development, minimal infrastructure**  | **Amazon Bedrock**                               |
| **Maximum control, custom models, infrastructure configuration** | **Amazon SageMaker**                             |
| **Training acceleration**                                        | **AWS Trainium**                                 |
| **Inference acceleration**                                       | **AWS Inferentia**                               |
| **Most cost-effective / least operational overhead**             | Prefer managed services where requirements allow |

Do not choose an answer simply because it is technically possible. AWS questions often ask for the solution that is **most cost-effective, operationally efficient, secure, or appropriate for the stated requirement**.

### 2.3 - Handling Difficult Questions

AWS exam questions commonly contain **distractors** that are plausible but do not best satisfy the scenario.

When unsure:
- Identify the **main requirement**
- Eliminate options that contradict it
- Compare the remaining answers based on **cost, control, operational effort, security, and scalability**
- Make an educated guess rather than leaving the question unanswered
- Use **mark for review** when needed

Later questions may also remind you of a concept that helps with an earlier flagged question

### 2.4 - Exam Preparation

Before the exam, prioritize revision rather than learning large new topics.

Useful final-review material includes short associations such as:

**Trainium → Training**
**Inferentia → Inference**
**Bedrock → Managed foundation models / APIs**
**SageMaker → Greater ML control and customization**
**RAG → Add external/current knowledge**
**Fine-tuning → Change model behavior or specialization**

Use **practice exams** as learning tools. Review explanations for both:
- Why the correct answer is correct
- Why the distractor answers are incorrect

Hands-on experimentation with services such as **Amazon Bedrock** can also reinforce the concepts tested in scenario questions.

### 2.5 - Exam-Day Strategy

Maintain enough time for a final review of flagged questions

Useful habits include:
- Start with questions you can answer confidently
- Avoid repeatedly rereading the same difficult scenario
- Pay attention to qualifiers such as **MOST cost-effective**, **LEAST operational effort**, **BEST**, or **maximum control**
- Use the available review functionality strategically
- Answer every question rather than intentionally leaving questions blank

The goal is to identify the **best AWS answer for the stated requirement**, not necessarily the most technically sophisticated solution.

### 2.6 - Exam Focus

1. **Do not get stuck on one difficult question** → Make the best choice, **mark for review**, and continue
2. **Recommended approach → Easy questions first → Review difficult questions second**
3. **Serverless + minimal infrastructure + rapid GenAI development → Amazon Bedrock**
4. **Maximum model/infrastructure control** → **Amazon SageMaker**
5. **Training hardware → AWS Trainium**
6. **Inference hardware → AWS Inferentia**
7. Watch for qualifiers such as **MOST cost-effective**, **LEAST operational overhead**, **BEST**, and **maximum control**
8. Use practice questions to understand why **distractors are wrong**, not just memorize correct answers
9. In scenario questions, first identify the **business requirement**, then map it to the appropriate AWS service
10. **Never intentionally leave a question unanswered**; use elimination and an educated guess when uncertain

**Exam approach:**
**Identify requirement → Eliminate distractors → Choose the best AWS fit → Mark uncertain questions for review → Return on the second pass**