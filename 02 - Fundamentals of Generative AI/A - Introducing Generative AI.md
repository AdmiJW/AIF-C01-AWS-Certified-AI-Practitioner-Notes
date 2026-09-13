## 1 - Understanding Generative AI Core Concepts

### 1.1 - Tokenization and Chunking

**Tokenization** converts input text into smaller units called **tokens** that a model can process numerically. A token may be a whole word, part of a word, or a few characters.

Example:
`I am learning generative AI` → `I | am | learn | ing | generative | AI`

**Chunking** splits large documents or datasets into smaller blocks before processing.

- Each **chunk** contains multiple tokens
- Chunks may **overlap** so context is preserved between sections
- Chunking helps keep input within the model's **context window**
- It is especially important when processing large documents for generative AI applications.

**Key Distinction**

| **Concept**      | **Purpose**                                          |
| ---------------- | ---------------------------------------------------- |
| **Tokenization** | Break text into units the model can process          |
| **Chunking**     | Break large content into manageable groups of tokens |

Example chunk sizes such as 300-1,000 tokens are implementation choices, **not fixed AWS limits**

### 1.2 - Embeddings and Vector Space

**Embeddings** are numerical representations of data that capture its **meaning and relationships**.

Embeddings are represented as **vectors** in a high-dimensional **vector space**. Semantically similar content is positioned closer together.

Example:

`I forgot my password`
is likely close in vector space to:

- `How do I log in?`
- `I can't sign in.`

This allows AI systems to identify **semantic similarity** rather than relying only on exact keyword matches.

**Flow:**
Text → **Tokens** → **Embeddings/Vectors** → Semantic relationships

### 1.3 - Transformers and Self-Attention

Modern generative AI models commonly use the **transformer architecture**.

A key transformer mechanism is **self-attention**, which allows the model to determine which parts of the input are most relevant to one another.

For example:

> The trophy didn't fit in the suitcase because it was too small.

Self-attention helps determine that **"it" refers to the suitcase** by considering relationships across the sentence.

Compared with older sequential approaches, transformers are better at capturing **context and long-range relationships** within text.

**Exam association:**
**Transformer → Self-attention → Understand relationships and context across input**

### 1.4 - Foundation Models and Generative AI Model Types

A **foundation model (FM)** is a large model trained on extensive datasets that can perform a broad range of tasks and can be adapted for more specific use cases.

**Amazon Bedrock** provides access to foundation models and capabilities for building and customizing generative AI applications without managing the underlying model infrastructure.

#### Large Language Models

**Large language models (LLMs)** specialize primarily in language-related tasks and commonly generate output by predicting the **next token** based on previous context.

Typical tasks include:
- Text generation
- Summarization
- Translation
- Question answering
- Conversational assistants

#### Multimodal Models

**Multimodal models** can work with more than one type of data, such as:
- Text
- Images
- Audio
- Video

**Exam keyword:**
Multiple input / output modalities → **Multimodal model**

#### Diffusion Models

**Diffusion models** are commonly used for **image generation**.

They generally begin with random noise and progressively **denoise** it according to the prompt until an image is produced.

**Key distinction:**

| **Model/Concept**    | **Typical Behavior**                                         |
| -------------------- | ------------------------------------------------------------ |
| **LLM**              | Predicts/generates tokens                                    |
| **Multimodal model** | Processes multiple data types                                |
| **Diffusion model**  | Generates content such as images through iterative denoising |

### 1.5 - Prompt Engineering and Generative AI Use Cases

**Prompt engineering** is the practice of designing and optimizing model inputs to produce better outputs.

Effective prompts can provide:
- Clear instructions
- Relevant context
- A desired role or **persona**
- Constraints or expected output form

Example:
`Act as a senior developer and review this code for security issues`

Common **generative AI use cases** include:
- Creating new content
- Summarization
- Translation
- Conversational assistants
- Recommendations
- Interactive simulations and learning experiences

Prompt engineering influences model behavior **without retraining the underlying model**

### 1.6 - Exam Focus

1. **Break text into model-processable units → Tokenization**
2. **Split large documents into manageable sections → Chunking**
3. **Preserve relationships between adjacent chunks → Chunk overlap**
4. **Maximum amount of information a model can consider at once → Context window**
5. **Represent semantic meaning numerically → Embeddings**
6. **Similar meanings positioned close together → Vector space**
7. **Core architecture behind many modern generative AI models → Transformer**
8. **Determine relationships and relevant context within input → Self-attention**
9. **Broad pretrained model adaptable to many tasks → Foundation model**
10. **AWS service for accessing and building with foundation models → Amazon Bedrock**
11. **Text generation through next-token prediction → LLM**
12. **Work with text, images, audio, or video together → Multimodal model**
13. **Generate images through iterative denoising → Diffusion model**
14. **Improve model responses by optimizing instructions and context → Prompt engineering**

## 2 - Demo: Working with Generative AI

### 2.1 - Amazon Q for Generative AI Assistance

**Amazon Q** is a generative AI assistant that can help users create, understand, and modify technical content such as application code.

In the demo, Amazon Q generated **Python code** for a website running in an **AWS Lambda** function based on a natural-language prompt.

Amazon Q can also:
- Explain generated code
- Provide implementation guidance
- Generate step-by-step instructions for AWS tasks
- Modify previous outputs based on follow-up requests.

**Exam association:**
AI-powered assistance for AWS development and technical tasks → **Amazon Q**

### 2.2 - Prompt Engineering and Iterative Refinement

The quality of generative AI output depends heavily on the **clarity and specificity of the prompt**.

A more effective prompt provides details such as:
- Required programming language
- Desired application behavior
- Visual or functional requirements
- Constraints
- Preferred implementation method

For example, changing a vague request for a cat image into a specific request to use **SVG (Scalable Vector Graphics)** produced an output closer to the intended result.

Generative AI interactions can also maintain **conversation context**. This means a user can provide follow-up instructions without repeating the entire original prompt.

**Typical refinement flow:**
Initial prompt → Generated output → Evaluate result → Add clarification → Improved output

This iterative process is a key part of **prompt engineering.**

### 2.3 - Generative AI as an Assistant, Not just a Generator

Generative AI can support multiple stages of a development task rather than only producing content.

In this example, Amazon Q was used to:
- Generate application code
- Explain what the code does
- Modify code based on new requirements
- Provide AWS configuration guidance

This demonstrates how generative AI can improve **developer productivity** through natural-language interaction

The generated output should still be **reviewed and validated** before being used, especially for production workloads.

### 2.4 - Exam Focus

1. **AWS generative AI assistant for development and AWS-related guidance → Amazon Q**
2. **More specific instructions generally produce more relevant output → Prompt engineering**
3. **Improve an initial AI response through follow-up instructions → Iterative prompt refinement**
4. **Continue modifying output without restating everything → Conversation/context awareness**
5. **Generate, explain, and modify code using natural language** → Common **generative AI developer-assistant use case**
6. **Generated AI output should be checked before production use → Human review and validation**

## 3 - Understanding the Foundation Model Lifecycle

### 3.1 - Foundation Model Lifecycle

The **foundation model lifecycle** describes the stages used to create, adapt, evaluate, deploy, and continuously improve a foundation model.

It is an **iterative lifecycle**, not a one-time process.

**Lifecycle flow:**
**Data Selection → Model Selection → Pre-training → Fine-tuning → Evaluation → Deployment → Feedback/Monitoring → Improvement**

### 3.2 - Data Selection

**Data selection** determines the information used to train the model

Foundation models typically require large and diverse datasets containing sources such as:
- Books and articles
- Websites
- Code
- Other structured or unstructured content

Important considerations include **data quality, diversity, relevance, and bias**

Poor-quality or biased training data can negatively affect model outputs.

**Exam association:**
Problems originating from biased or poor-quality training information → Review **training data/data selection**

### 3.3 - Model Selection

**Model selection** involves choosing a model appropriate for the application's requirements.

Consider factors such as:
- Task complexity
- Model capabilities
- Performance
- Speed/latency
- Resource requirements

A smaller model may be suitable when **speed and efficiency** are priorities, while a larger model may be selected for more complex tasks.

### 3.4 - Pre-training

During **pre-training**, a model learns general patterns from a very large dataset.

For language models, this includes learning:
- Language structure and patterns
- Relationships between concepts
- Code patterns
- **Next-token prediction**

Pre-training foundation models requires significant **compute resources, time, and cost**.

Because of this, organizations commonly start with an existing **pre-trained foundation model** rather than training one from scratch.

**Key distinction:**
**Pre-training** → Builds broad, general-purpose capabilities from massive datasets.

### 3.5 - Fine-Tuning

**Fine-tuning** adapts an existing pre-trained model for a more specific task or domain.

The model is trained further using a **smaller, task- or domain-specific dataset**.

Examples include adapting a model to:
- Organization-specific terminology
- Industry-specific knowledge or patterns
- Particular tasks
- Desired communication styles

| **Stage**        | **Main Purpose**                       | **Typical Data**             |
| ---------------- | -------------------------------------- | ---------------------------- |
| **Pre-training** | Learn broad, general capabilities      | Massive, diverse dataset     |
| **Fine-tuning**  | Adapt the model to a specific use case | Smaller, specialized dataset |

**Exam keyword:**
Customize an existing model using task-specific training data → **Fine-tuning**

### 3.6 - Model Evaluation

Before deployment, the model should be **evaluated** to determine whether it meets application requirements

Evaluation can consider:
- **Accuracy/quality**
- **Hallucinations**
- **Toxicity or harmful output**
- Reliability
- Other task-specific benchmarks

Evaluation is important for both **model performance** and **responsible AI**.

### 3.7 - Deployment and Feedback Loop

During **deployment**, the model is integrated into an application or service so that users can interact with it.

Deployment does not end the lifecycle. The model should be continuously **monitored** in production.

Monitoring and feedback may reveal:
- Poor or incorrect responses
- User dissatisfaction
- Latency or performance issues
- New data requirements
- Areas requiring additional customization

This information forms a **feedback loop** that can lead to updated data, further fine-tuning, reevaluation, and redeployment.

**Feedback loop:**
**Deploy → Monitor → Collect Feedback → Improve → Evaluate → Redeploy**

### 3.8 - Exam Focus

1. **First consider the quality, diversity, and bias of training information → Data selection**
2. **Choose a model based on task, capability, speed, and resource requirements → Model selection**
3. **Train on massive datasets to learn general patterns → Pre-training**
4. **Adapt an existing model using a smaller specialized dataset → Fine-tuning**
5. **Check quality, hallucinations, toxicity, and other benchmarks → Evaluation**
6. **Integrate the model into an application for users → Deployment**
7. **Observe production behavior and collect user/performance data → Monitoring and feedback**
8. **Foundation model development is not one-and-done → Iterative lifecycle/feedback loop**
9. **Pre-training vs. fine-tuning** → Pre-training creates **broad capabilities**; fine-tuning creates **task/domain specialization**
10. **High cost and compute requirements of training from scratch** → Often start with an existing **pre-trained foundation model**

## 4 - Demo: Working with the Foundation Model Lifecycle - Model Selection

### 4.1 - PartyRock for Model Experimentation

**PartyRock** is an AWS no-code environment for learning and experimenting with **generative AI**.

It can be used to:
- Build generative AI applications without writing code
- Experiment with different foundation models
- Practice **prompt engineering**
- Generate text and images
- Perform basic data analysis.

For the foundation model lifecycle, PartyRock is useful for exploring the **model selection** stage

### 4.2 - Comparing Foundation Models

**Model selection** involves testing candidate models to determine which best fits a specific workload.

Different models can receive the **same prompt** and produce different outputs. A useful comparison evaluates factors such as:
- Output quality
- Accuracy or relevance
- Tone and style
- Strengths and weaknesses
- Suitability for the intended task

In the demo, the same input was sent to two different models so their responses could be compared under identical conditions.

**Exam association:**

Choosing the best foundation model for a workload → **Evaluate multiple models against the same requirements**

Specific model versions used in a demo are less important than understanding the **model comparison process**

### 4.3 - PartyRock Widgets and Application Flow

PartyRock applications are built using connected **widgets**.

The comparison workflow consisted of:

**User Input → Multiple AI Models → Evaluation/Judge**

The same user prompt was passed to each candidate model, allowing their outputs to be compared consistently.

This illustrates an important evaluation principle: use the **same task and criteria** when comparing models.

### 4.4 - Automated Model Evaluation

An additional AI-powered component can act as an **evaluator or judge**

In the demo, the evaluator:
- Reviewed outputs from both models
- Applied evaluation criteria
- Identified strengths and weaknesses
- Assigned comparative scores
- Selected an overall preferred model

Prompt engineering was used to define **how the evaluator should judge the responses**.

An automated evaluator can make comparisons more scalable, but evaluation results should still be interpreted carefully rather than assumed to be objectively correct.

### 4.5 - Prompt Engineering in Model Evaluation

**Prompt engineering** is important not only for generating content but also for defining evaluation behavior.

A well-designed evaluator prompt can specify:
- The evaluator's role
- Required evaluation criteria
- Scoring rules
- Desired response format
- How a winner should be determined.

**Flow:**
Same prompt → Candidate models → Compare outputs → Score against criteria → Select appropriate model

### 4.6 - Exam Focus

1. **No-code AWS environment for experimenting with generative AI → PartyRock**
2. **Test several foundation models to determine the best fit → Model selection**
3. **Send the same prompt to multiple models** → Enables a fairer **model comparison**
4. **Compare quality, relevance, strengths, weaknesses, and task suitability → Model evaluation criteria**
5. **Use another model to critique and score candidate outputs → Automated evaluation / model-as-a-judge**
6. **Define how an evaluator should assess responses → Prompt engineering**
7. **Model selection should be based on workload requirements, not simply model size or popularity**
8. **PartyRock demo model names/versions** → Examples only; focus on the **selection and evaluation process**