## 1 - Selecting Foundation Models

### 1.1 - Selecting Foundation Models

When selecting a **foundation model (FM)**, match the model's capabilities to the application's **business requirements**, **performance needs**, and **cost constraints**.

Key selection criteria include:

| **Selection Criterion**  | **What to Consider**                                      | **Typical Exam Scenario**                                                              |
| ------------------------ | --------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| **Modality**             | Types of data the model handles: text, images, audio, etc | Select a model/service compatible with the application's data type                     |
| **Latency**              | How quickly the model returns a response                  | Real-time chatbot → prioritize **low latency**                                         |
| **Multilingual support** | Languages the model understands or generates              | Global/multilingual application → choose a model with built-in multilingual capability |
| **Model size**           | Computational resources required                          | Larger models may provide stronger capabilities but generally require more compute     |
| **Model complexity**     | Sophistication of tasks the model can handle              | Simple task → lighter model; complex reasoning/task → more capable model               |
| **Customization**        | Ability to adapt the model to specific data/tasks         | Domain-specific requirements → consider **fine-tuning** or **few-shot learning**       |
| **Input/output length**  | Amount of context the model can accept and generate       | Large documents or long conversations → require sufficient **context/input length**    |

#### Modality

**Modality** is the type of data a model is designed to process or generate, such as **text, images, or audio**

AWS examples include:
- **Amazon Bedrock foundation models** → generative AI tasks such as chatbots, summarization, and language generation/translation.
- **Amazon Rekognition** → image/video analysis such as object/scene detection, face analysis, and content moderation
- **Amazon Transcribe → speech-to-text**
- **Amazon Polly → text-to-speech**

Choosing the correct modality is essential because the model must support the application's **input and required output type**.

#### Latency

**Latency** is the time required for a model to process a request and return a response

- **Real-time applications**, such as interactive chatbots → **low latency** is important
- **Batch processing**, such as offline analysis → latency is usually less important

There can be a trade-off between **model capability, model size, cost, and response latency**

#### Multilingual Support

Some foundation models support **multiple languages without requiring separate models or additional training**.

Multilingual support is important for applications such as:
- Global customer-service chatbots
- Multilingual content generation
- Translation
- Applications serving users across multiple regions/languages

For multilingual requirements, verify that the selected model supports the **required languages**.

#### Model Size and Complexity

**Model size** affects computational requirements, cost, latency, and deployment considerations

- **Larger models** → generally more computationally demanding and may offer stronger capabilities for complex tasks
- **Smaller models** → generally faster, cheaper, and more resource-efficient

**Model complexity** should match the task:

- **Simple task** → **smaller/lighter model**
- **Complex task** → **more capable/complex model**

Do not automatically choose the largest model; choose one appropriate for the **business requirement and cost/performance trade-off**

#### Customization

Foundation models can sometimes be customized for specific business requirements.

Common techniques include:
- **Fine-tuning** → further trains a model using task- or domain-specific data
- **Few-shot learning** → provides a small number of examples within the prompt to guide the model's behavior without fully retraining it.

Customization ca improve performance for specific use cases but may increase **cost, complexity, and computational requirements**.

#### Input and Output Length

Models have limits on how much information they can process and generate.

Consider:
- **Input length/context window** → how much prompt/context the model can accept.
- **Output length** → how much content the model can generate

This is particularly important for:
- Large-document summarization
- Long conversations
- Complex prompts with significant context

Longer inputs and outputs can also increase **computational requirements, latency, and cost**.

**Selection flow:**
Business requirement → **Modality** → **Latency** → **Language support** → **Model size/complexity** → **Customization** → **Input/output limits** → **Cost/performance**

### 1.2 - Exam Focus

Know how to map application requirements to foundation model selection criteria:
- Text, image, or audio requirement → **Modality**
- Interactive chatbot / immediate response → **Low latency**
- Global application → **Multilingual support**
- Lower compute/cost requirements → **Smaller model**
- Complex tasks → **More capable/complex model**
- Adapt model to domain-specific needs → **Customization / fine-tuning**
- Provide examples in the prompt → **Few-shot learning**
- Process large documents or long conversations → **Large input/context capacity**
- Generate long responses → **Sufficient output length**

Remember that foundation model selection usually involves trade-offs among **performance**, **latency**, **cost**, **computational requirements**, and **task suitability**.

## 2 - Inference Parameters

### 2.1 - Inference Parameters

**Inference parameters** are settings that control how a trained foundation model generates outputs during **inference**.

**Inference** is the stage where a trained model applies its learned knowledge to **new input data** to generate a response.

Adjusting inference parameters change the model's behavior without retraining the model.

Key parameters include:

| **Parameter**     | **Lower Value**                          | **Higher Value**                                  |
| ----------------- | ---------------------------------------- | ------------------------------------------------- |
| **Temperature**   | More predictable and deterministic       | More random, creative, and diverse                |
| **Top-k**         | Smaller candidate token pool             | Larger candidate token pool                       |
| **Top-p**         | Smaller probability-based candidate pool | Larger probability-based candidate pool           |
| **Input length**  | Less information processed               | More information processed; higher resource usage |
| **Output length** | Shorter responses                        | Longer responses; higher resource usage           |

#### Temperature

**Temperature** controls the **randomness and creativity** of generated responses.

It is commonly represented as a value between **0.0** and **1.0**, although supported ranges can vary by model.

- **Low temperature** → more deterministic, predictable responses
- **High temperature** → more creative, varied, and less predictable responses.

Typical scenarios:
- Coding, factual responses, structured output → **lower temperature**
- Story generation, brainstorming, marketing copy → **higher temperature**

Memory aid:
**Low temperature → Predictable**
**High temperature → Creative**

#### Input and Output Length

**Input length** determines how much text or data can be provided to the model.

**Output length** determines how much content the model can generate.

Examples:
- Short input → "Summarize this paragraph"
- Long input → summarizing a multi-page document
- Short output → brief answer
- Long output → detailed generated response

Longer inputs and outputs generally increase:
- **Computational requirements**
- **Latency**
- **Cost**

#### Top-k

**Top-k** limits generation to a specific number of the **most probable next tokens**

For example:

**Top-k = 10** → the model considers only the **10 most likely tokens** for the next token selection.

- **Lower Top-k** → smaller candidate pool → more predictable output
- **Higher Top-k** → larger candidate pool → more diverse output

Memory aid:
**Top-k = Number of candidate tokens**

#### Top-p

**Top-p**, also called **nucleus sampling**, selects tokens from a probability-based set of likely candidates

Instead of choosing a fixed number of tokens, the model considers candidate tokens whose cumulative probabilities fall within the specified **Top-p threshold**.

For example,

**Top-p = 0.9** → consider the most likely tokens until their cumulative probability reaches approximately **90%**.

- **Lower Top-p** → fewer candidate options → more predictable output
- **Higher Top-p** → more candidate options → greater diversity

Memory aid:

**Top-p = Probability-based candidate pool**

#### Top-k vs. Top-p

| **Feature**      | **Top-k**                    | **Top-p**                            |
| ---------------- | ---------------------------- | ------------------------------------ |
| Controls         | Number of candidate tokens   | Probability mass of candidate tokens |
| Selection method | Fixed-size candidate pool    | Dynamic probability-based pool       |
| Lower value      | More restrictive/predictable | More restrictive/predictable         |
| Higher value     | More diverse possibilities   | More diverse possibilities           |

Both parameters influence **token sampling** and therefore the randomness and diversity of generated responses.

With supported models in **Amazon Bedrock**, inference parameters such as **temperature, Top-p, and Top-k** can be configured to control model generation behavior.

### 2.2 - Exam Focus

Know the relationship between inference parameters and model behavior:

- More predictable/deterministic response → **Lower temperature**
- More creative/diverse response → **Higher temperature**
- Restrict model to a fixed number of likely tokens → **Top-k**
- Restrict tokens based on cumulative probability → **Top-p**
- Lower **Top-k / Top-p** → fewer candidate tokens, more predictable output
- Higher **Top-k / Top-p** → more candidate tokens, more diverse output
- Larger input/output lengths → generally **higher cost and computational demand**

Key distriction:

**Temperature → randomness**
**Top-k → number of candidate tokens**
**Top-p → probability-based candidate pool**

Exam memory aid:

**Higher Temperature + Higher Top-k + Higher Top-p → More diverse/creative generation**

## 3 - Retrieval-augmented Generation (RAG)

### 3.1 - Retrieval-Augmented Generation (RAG)

**Retrieval-Augmented Generation (RAG)** is a technique that combines a **foundation model (FM)** with an **external knowledge source** such as a database, document repository, or knowledge base.

Instead of relying only on information learned during model training, RAG retrieves relevant external information and adds it to the model's prompt during **inference**.

#### RAG Flow

User query → Retrieve relevant information → Add retrieved context to prompt → Foundation model generates response

This allows the model to answer questions about **private, domain-specific, or recently updated information** that may not exist in its original training data.

#### Knowledge Base

A **knowledge base** is a repository of information that a foundation model can reference during inference.

Examples include:
- Company documents
- FAQs
- Policies and procedures
- Technical manuals
- Research papers
- Business data

The knowledge base provides external context that can help produce more **relevant, accurate, and context-aware responses**.

With **Amazon Bedrock Knowledge Bases**, external data such as documents stored in **Amazon S3** can be used as a source for RAG applications.

#### Why use RAG?

A foundation model may not know:
- Internal company information
- Proprietary procedures
- Recently updated policies
- Current business data
- Specialized domain knowledge

RAG addresses this by retrieving relevant information at query time instead of requiring the model to already contain that knowledge.

This is especially useful when information changes frequently because the external source can be updated independently of the foundation model.

#### Common RAG Use Cases

| **Use Case**                      | **External Knowledge Source**            | **Example**                                           |
| --------------------------------- | ---------------------------------------- | ----------------------------------------------------- |
| **Customer support**              | FAQs, policies, support documentation    | "How do I reset my device?"                           |
| **Technical/product support**     | Product manuals, technical documentation | “What are the material specifications for Product X?" |
| **Research and analysis**         | Databases, reports, research documents   | "What were the market trends in Q3?"                  |
| **Internal enterprise assistant** | Company documents and procedures         | Questions about internal policies or processes        |

#### RAG vs. Model Training

RAG supplements a model's knowledge **during inference** rather than changing the model's underlying trained parameters.

**Foundation model alone** → Answers using knowledge already available to the model
**RAG** → Retrieves external information first, then uses it to generate the answer

This makes RAG useful when an application needs access to **current or organization-specific information** without retraining the foundation model.

### 3.2 - Exam Focus

Remember the core association:

**Retrieve external data + generate an answer → RAG**

Key exam mappings:
- Give a foundation model access to company documents → **RAG**
- Answer questions using current FAQs/policies → **RAG**
- Use external information during inference → **RAG**
- Repository of documents/information used by RAG → **Knowledge base**
- Build a RAG application with AWS foundation models → **Amazon Bedrock Knowledge Bases**
- Source documents may be stored in → **Amazon S3**
- Need updated information without retraining the model → **RAG**

Memory aid:

**RAG = Retrieve → Augment prompt → Generate**

RAG helps foundation models provide **more current, domain-specific, and context-aware responses** by grounding generation in external information.

## 4 - Vector Storage Solutions on AWS

### 4.1 - Vector Storage Solutions on AWS

**Embeddings** are numerical representations of data that capture **semantic meaning**. They can represent text, images, and other data in a form that machine learning models can compare mathematically.

A **vector** is the numerical array that represents an embedding.

**Vector databases** are designed to store, index, and search these embeddings efficiently. Instead of relying only on exact matches, they perform **vector similarity search** to find items that are semantically similar.

**Basic Flow**

Data → Generate embeddings → Store vectors → Perform similarity search → Retrieve relevant results

#### AWS Vector Storage Options

| **AWS Service**                                 | **Vector Storage / Search Use Case**                                             |
| ----------------------------------------------- | -------------------------------------------------------------------------------- |
| **Amazon OpenSearch Service**                   | Combines **vector/semantic search with full-text and keyword search**            |
| **Amazon Aurora PostgreSQL-Compatible Edition** | Relational database that can support vector data and similarity search           |
| **Amazon RDS for PostgreSQL**                   | Supports extensions such as **pgvector** for vector similarity search            |
| **Amazon Neptune**                              | Useful when data is based on **graphs and relationships**                        |
| **Amazon DocumentDB**                           | Document-oriented storage that can support vector search alongside document data |

#### Amazon OpenSearch Service

**Amazon OpenSearch Service** can store and search vector embeddings while also supporting traditional **full-text search**.

This is useful when an application needs a combination of:
- **Semantic/vector search**
- **Keyword-based search**
- Search across large collections of content

Example:

Product descriptions/images → Embeddings → **OpenSearch** → Similarity search → Relevant products

For an e-commerce query such as **"budget laptops"**, vector search can retrieve products that are semantically related even when the exact phrase does not appear in the product description.

#### PostgreSQL-Based Options

**Amazon Aurora PostgreSQL-Compatible Edition** and **Amazon RDS for PostgreSQL** can combine traditional relational data with vector capabilities.

With extensions such as **pgvector**, PostgreSQL can perform **vector similarity search** directly within the relational database.

Useful when an application already needs:
- SQL
- Relational data
- Transactions
- Vector search

Example use cases include **recommendation systems** and applications that store structured business data alongside embeddings.

#### Amazon Neptune

**Amazon Neptune** is designed for **graph-based data**, where relationships between entities are important.

Use it when the application needs to work with connected data such as:
- Relationships between people or entities
- Knowledge graphs
- Recommendation relationships

Exam association:

**Graph relationships → Amazon Neptune**

#### Amazon DocumentDB

**Amazon DocumentDB** is a document-oriented database suitable for applications that use **JSON-like/document data** and need vector capabilities alongside that data.

Exam association:

**Document-oriented data + vector search → Amazon DocumentDB**

### 4.2 - Exam Focus

Know what vector storage is used for:
- Numerical representation of semantic meaning → **Embedding**
- Numerical array representing an embedding → **Vector**
- Find semantically similar items → **Vector similarity search**
- Store and search embeddings → **Vector database**

Key AWS mappings:
- **Semantic/vector search + keyword/full-text search → Amazon OpenSearch Service**
- **Relational PostgreSQL database + vector search → Aurora PostgreSQL / RDS for PostgreSQL with pgvector**
- **Graph relationships / knowledge graphs → Amazon Neptune**
- **Document-oriented data + vector capabilities → Amazon DocumentDB**

Memory aid:

**Embeddings → Vector database → Similarity search → Relevant context/results**

For exam scenarios, focus on the application's existing data model:

**Search-heavy → OpenSearch**
**Relational → PostgreSQL + pgvector**
**Graph → Neptune**
**Documents → DocumentDB**

## 5 - Cost Tradeoffs for Customization

### 5.1 - Cost Tradeoffs for Foundation Model Customization

Foundation models can be customized using several approaches, including **pre-training, fine-tuning, in-context learning,** and **Retrieval-Augmented Generation (RAG)**.

The right approach depends on the required **cost, control, complexity, scalability, and access to domain-specific data**.

| **Approach**            | **Cost**                                | **Model Retraining?** | **Best Use Case**                               |
| ----------------------- | --------------------------------------- | --------------------- | ----------------------------------------------- |
| **Pre-training**        | Very high                               | Yes, from scratch     | No suitable existing model; maximum control     |
| **Fine-tuning**         | Moderate                                | Yes                   | Adapt an existing model to a specialized task   |
| **In-context learning** | Low                                     | No                    | Guide behavior through prompts/examples         |
| **RAG**                 | Cost-effective / lower than fine-tuning | No                    | Use current, proprietary, or external knowledge |

#### Pre-training

**Pre-training** means creating and training a model from scratch using a very large dataset.

It has the **highest cost** because it requires substantial:
- Compute resources
- Storage
- Training data
- Training time

Pre-training provides a high degree of control over the resulting model but is generally practical only for organizations with significant resources

Best suited when:
- A suitable pre-trained model does not already exist
- The use case requires highly specialized or proprietary model behavior.

Example:

A financial institution creates a model specifically for **proprietary fraud detection**.

#### Fine-tuning

**Fine-tuning** starts with an existing pre-trained model and further trains it using a **smaller, task-specific dataset**.

Because the base model already exists, fine-tuning is generally **less expensive than pre-training**.

Use fine-tuning when the goal is to:
- Adapt a general-purpose model to a specialized domain.
- Modify model behavior for a particular task
- Improve performance on domain-specific examples

Example:

A healthcare organization fine-tunes a language model to better process specialized healthcare-related data

**Memory aid:**
**Pre-trained model + specialized training data → Fine-tuned model**

#### In-Context Learning

**In-context learning** changes model behavior through the **prompt** instead of retraining the model.

Examples or instructions are supplied as part of the input, allowing the model to infer how it should respond.

Because no model training is required, the cost is generally **low**, with costs primarily coming from **inference/token usage**.

Example:

A customer-service chatbot receives example question-and-answer pairs within its prompt to guide its responses.

**Memory aid:**
**Examples in prompt → No retraining**

#### Retrieval-Augmented Generation (RAG)

**RAG** connects a pre-trained foundation model to an **external knowledge source**, such as a knowledge base or vector database.

The model itself is not modified. Instead, relevant information is retrieved at inference time and supplied as additional context.

RAG is useful for:
- **Frequently changing information**
- **Current data**
- **Proprietary business information**
- Large collections of organizational documents

Example:

A retail chatbot retrieves current **product inventory** before generating its response.

Compared with fine-tuning, RAG can be more cost-effective when the primary requirement is to give the model access to **specialized or frequently updated knowledge** rather than change its underlying behavior.

#### Choosing the Right Customization Method

A useful distinction is whether the requirement involves changing the model's **behavior** or giving it additional **knowledge**.

**Change model behavior for a specialized task → Fine-tuning**
**Provide current or proprietary knowledge → RAG**
**Guide output using examples without retraining → In-context learning**
**Build an entirely new model → Pre-training**

Typical cost order:
**Pre-training → highest cost**
**Fine-tuning → moderate cost**
**RAG / In-context learning → generally lower cost**

Actual cost depends on factors such as model size, data volume, inference usage, storage, and infrastructure.

### 5.2 - Exam Focus

Know the customization method from the scenario:

- Train a foundation model **from scratch → Pre-training**
- Highest compute and training cost → **Pre-training**
- Adapt an existing model using a specialized dataset → **Fine-tuning**
- Modify model behavior for a particular domain/task → **Fine-tuning**
- Provide examples or instructions inside the prompt → **In-context learning**
- No retraining; mainly pay inference costs → **In-context learning**
- Connect an FM to external/current/proprietary data → **RAG**
- Frequently changing knowledge without retraining → **RAG**

Key distinction:

**Fine-tuning** → **changes the model**
**RAG** → **supplies external knowledge to the model**
**In-context learning** → **guides the model through the prompt**
**Pre-training** → **creates the model from scratch**

Memory aid:

**Need behavior change? → Fine-tune**
**Need current knowledge? → RAG**
**Need quick prompt-based guidance? → In-context learning**
**Need a completely new model? → Pre-train**

## 6 - Agents for Multi-step Tasks

### 6.1 - Agents for Multi-step Tasks

**Agents** extend foundation models by enabling them to perform **multi-step workflows** toward a defined goal.

Instead of only generating a response, an agent can:
- Follow instructions
- Retrieve information from data sources
- Call APIs or external tools
- Perform actions across multiple systems
- Use intermediate results to decide the next step

In AWS, **Agents for Amazon Bedrock** help automate and orchestrate complex generative AI workflows with reduced manual intervention.

#### Basic Agent Flow

User request → Understand goal → Retrieve required data → Perform actions/tools → Process results → Generate final response

#### Agents for Amazon Bedrock

**Agents for Amazon Bedrock** can coordinate a sequence of actions required to complete a task.

They can combine foundation models with capabilities such as:
- **Retrieval-Augmented Generation (RAG)** to access company or domain-specific information
- **API calls** to interact with external applications and services
- **Action groups** to define operations the agent can perform
- **Prompt instructions** to guide agent behavior
- **Memory** to maintain relevant context across interactions

The key exam concept is that an agent can do more than answer a question - it can **plan and execute multiple steps** required to achieve a goal.

#### Agents vs. RAG

**RAG** and **agents** solve different problems but can work together

| **Capability**              | **RAG**                 | **Agent**   |
| --------------------------- | ----------------------- | ----------- |
| Retrieve external knowledge | Yes                     | Can use RAG |
| Generate responses          | Yes                     | Yes         |
| Perform multi-step actions  | No, not by itself       | **Yes**     |
| Call APIs/tools             | Not its primary purpose | **Yes**     |
| Automate workflows          | Limited                 | **Yes**     |

Memory aid:
**RAG** → **Retrieve knowledge**
**Agent → Retrieve → Reason/Plan → Act**

#### Example: Customer Order Status

A customer asks:

**"What is the status of my order?"**

An agent could:
1. Retrieve the customer's order details
2. Query the shipping system
3. Analyze the current delivery status
4. Generate a response with the latest information

This workflow can happen automatically without requiring an employee to manually query each system.

#### Common Agent Use Cases

Agents are useful for tasks involving:
- **Multi-step automation**
- Repetitive workflows
- Multiple APIs or systems
- Business data retrieval
- Data-driven actions
- Customer-service automation

Example scenarios include:
- Checking an order and shipment status
- Retrieving account information and performing a requested action
- Looking up information across multiple enterprise systems
- Automating workflows that require several dependent steps

### 6.2 - Exam Focus

Know when to choose **Agents for Amazon Bedrock:**

- Automate a **multi-step workflow → Agents for Amazon Bedrock**
- Foundation model needs to interact with external APIs/tools → **Agent**
- Perform actions across multiple systems → **Agent**
- Reduce manual effort for repetitive workflows → **Agent**
- Retrieve company knowledge as part of a workflow → **Agent + RAG**
- Need only external knowledge retrieval → **RAG**
- Need retrieval plus actions/orchestration → **Agent**

Key distinction:

**RAG → gives the model additional knowledge**
**Agents → enable the model to take actions and orchestrate multi-step tasks**

Memory aid:

**Agent = Goal → Plan → Retrieve → Act → Respond**

## 7 - Exam Tips

### 7.1 - Design Considerations Quick Review

| **Concept**                    | **Exam Association**                                                                                                      |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------- |
| **Foundation model selection** | Consider **cost, modality, latency, model size/complexity, multilingual support, customization, and input/output limits** |
| **Temperature**                | Low → deterministic; High → creative/diverse                                                                              |
| **Top-k**                      | Number of most likely candidate tokens considered                                                                         |
| **Top-p**                      | Probability-based pool of candidate tokens considered                                                                     |
| **Input/output length**        | Longer → greater **cost, latency, and compute requirements**                                                              |
| **RAG**                        | Retrieve external knowledge and add it to the prompt before generation                                                    |
| **Knowledge base**             | Repository of company documents, FAQs, research, etc. used by RAG                                                         |
| **Vector database**            | Stores embeddings and performs **similarity search**                                                                      |
| **Amazon OpenSearch Service**  | Vector/semantic search combined with keyword/full-text search                                                             |
| **Amazon Neptune**             | Graph-based data and relationships                                                                                        |
| **Pre-training**               | Train from scratch → **highest cost**                                                                                     |
| **Fine-tuning**                | Train an existing model on task-specific data → **moderate cost**                                                         |
| **In-context learning**        | Guide behavior with prompts/examples → **no model retraining**                                                            |
| **RAG customization**          | Supply external/current knowledge without modifying model parameters                                                      |
| **Agents for Amazon Bedrock**  | Automate and orchestrate **multi-step workflows**                                                                         |

#### Key Inference Parameter Pattern

**Lower Temperature / Top-p / Top-k → More restricted and predictable output**
**Higher Temperature / Top-p / Top-k → More varied and diverse output**

Remember the distinction:

**Temperature → randomness**
**Top-k → number of candidates**
**Top-p → probability-based candidate pool**

#### RAG and Vector Search

**RAG flow:**

Query → Retrieve relevant information → Augment prompt → Generate response

RAG is especially useful when the model needs **current, proprietary, or domain-specific information**

A typical AWS flow could be:

**Documents in Amazon S3 → Knowledge base/vector store → Retrieve relevant context → Amazon Bedrock FM → Response**

Vector databases store **embeddings**, which enable retrieval based on **semantic similarity** rather than only exact keyword matches.

#### Customization Cost Tradeoffs

A useful relative cost pattern is:

**Pre-training → highest cost**
**Fine-tuning → moderate cost**
**RAG / in-context learning → generally lower cost**

Choose based on the requirement:

**New model from scratch → Pre-training**
**Change specialized model behavior → Fine-tuning**
**Provide current/external knowledge → RAG**
**Guide output using examples in the prompt → In -context learning**

#### Agents

**Agents for Amazon Bedrock** are designed for applications requiring **multi-step actions**, such as retrieving information, calling APIs, processing results, and completing business workflows.

Key distinction:

**RAG → Retrieve knowledge**
**Agent → Orchestrate actions and multi-step workflows**

Agents can also **use RAG** as part of a larger workflow

### 7.2 - Exam Focus

Prioritize these scenario mappings:
- Text vs. image vs. audio requirement → **Model modality**
- Real-time application → **Low latency**
- Creative generation → **Higher temperature**
- Predictable/factual generation → **Lower temperature**
- Fixed number of candidate tokens → **Top-k**
- Probability-based candidate tokens  → **Top-p**
- Current/company-specific information → **RAG**
- Repository supplying RAG information → **Knowledge base**
- Semantic similarity search → **Vector embeddings/vector database**
- Semantic + keyword search → **Amazon OpenSearch Service**
- Graph relationships → **Amazon Neptune**
- Train model from scratch → **Pre-training**
- Adapt existing model using training data → **Fine-tuning**
- Examples provided in prompt → **In-context learning**
- External knowledge without retraining → **RAG**
- Multi-step workflow/API orchestration → **Agents for Amazon Bedrock**

Final memory chain:

**Select FM → Configure inference → Add RAG if external knowledge is needed → Store/search embeddings with vector storage → Choose customization method → Use agents for multi-step actions**
