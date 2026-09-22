## Question 1

### Original Question

A company makes forecasts each quarter to decide how to optimize operations to meet expected demand. The company uses ML models to make these forecasts.

An AI practitioner is writing a report about the trained ML models to provide **transparency and explainability** to company stakeholders.

What should the AI practitioner include in the report to meet the transparency and explainability requirements?

### Choices

A. Code for model training  
B. Partial dependence plots (PDPs)  
C. Sample data for training  
D. Model convergence tables

### Correct Answer

**B. Partial dependence plots (PDPs)**

### Why?

**Partial dependence plots (PDP)** help explain how one or more input features influence a model's predictions. They visualize the **average relationship between a feature and the predicted outcome**, making model behavior easier for stakeholders to understand.

- **A. Code for model training** - Shows implementation details, but does not directly explain **why the model makes particular decisions***
- **B. Partial dependence plots (PDPs)** - Correct. Used for **model interpretability and explainability** by showing how features affect predictions
- **C. Sample data for training** - Provides information about the data but does not explain the trained model's decision-making behavior
- **D. Model convergence tables** - Show information about the **training/optimization process**, not how features influence model predictions

### Exam Focus

**Explain how features influence model predictions → Partial Dependence Plots (PDPs)**

Remember:
**PDP = Feature value → Average effect on model prediction**

Key exam keywords: **explainability, interpretability, transparency, feature influence, model behavior**

## Question 2

### Original Question

A law firm wants to build an AI application by using **large language models (LLMs)**. The application will read legal documents and **extract key points** from the documents.

Which solution meets these requirements?

### Choices

A. Build an automatic named entity recognition system.  
B. Create a recommendation engine.  
C. Develop a summarization chatbot.  
D. Develop a multi-language translation system.

### Correct Answer

**C. Develop a summarization chatbot.**

### Why?

A **summarization** application uses an LLM to condense long documents and identify their most important information or **key points**.

- **A. Named entity recognition (NER)** → Extracts specific entities such as **people, organizations, locations, or dates**, not the overall key points of a document
- **B. Recommendation engine** → Suggests relevant items based on preferences, behavior, or similarity. It does not summarize documents
- **C. Summarization chatbot** → Correct. An LLM can read legal documents and generate a concise summary containing the **main points**.
- **D. Multi-language translation system** → Converts text from one language to another rather than extracting or summarizing key information

### Exam Focus

**Extract key points or condense long documents → Summarization**

Quick distinction:
- **Summarization** → Identify and condense the main ideas
- **NER** → Extract named entities such as people, places, and organizations
- **Recommendation** → Suggest relevant items
- **Translation** → Convert text between languages

Key exam keywords: **LLM, summarization, key points, document understanding, text generation**

## Question 3

### Original Question

A company wants to classify human genes into **20 categories** based on gene characteristics. The company needs an ML algorithm to document how the **inner mechanism of the model affects the output**.

Which ML algorithm meets these requirements?

### Choices

A. Decision trees  
B. Linear regression  
C. Logistic regression  
D. Neural networks

### Correct Answer

**A. Decision trees**

### Why?

**Decision trees** are highly **interpretable** models. Their internal decision-making process can be followed from the **root node through decision rules to a leaf node**, making it easy to document how input characteristics lead to a particular classification.

Decision trees also naturally support **multiclass classification**, such as assigning genes to one of 20 categories.

- **A. Decision trees** → Correct. Provides transparent, traceable **if/then decision rules** and supports multiclass classification
- **B. Linear regression** → Primarily used for predicting **continuous numerical values**, not categorical classes
- **C. Logistic regression** → Can perform classification, including multiclass variants, but a decision tree provides a more directly understandable view of the model's **internal decision process**
- **D. Neural networks** → Can handle complex multiclass classification but are generally considered **less interpretable / black-box models**.

### Exam Focus

**Need an interpretable model with traceable decision logic → Decision tree**

Quick distinction:

| **Algorithm**           | **Typical use**                     | **Interpretability**               |
| ----------------------- | ----------------------------------- | ---------------------------------- |
| **Decision Tree**       | Classification / regression         | **High - explicit decision rules** |
| **Linear Regression**   | Continuous value prediction         | High                               |
| **Logistic Regression** | Classification                      | Relatively high                    |
| **Neural network**      | Complex classification / prediction | **Low - often black box**          |

Key exam association:

**"Understand/document how the model's internal mechanism produces an output" → Prefer an interpretable model such as a Decision Tree**

## Question 4

### Original Question

A company has built an **image classification model** to predict plant diseases from photos of plant leaves. The company wants to evaluate **how many images the model classified correctly**.

Which evaluation metric should the company use to measure the model's performance?

### Choices

A. R-squared score  
B. Accuracy  
C. Root mean squared error (RMSE)  
D. Learning rate

### Correct Answer

**B. Accuracy**

### Why?

**Accuracy** measures the proportion of predictions that a classification model gets correct.

**Accuracy = Correct predictions / Total predictions**

- **A. R-squared (R²)** → Used for **regression** to measure how well a model explains variation in continuous target values
- **B. Accuracy** → Correct. Measures the **overall proportion of correctly classified images**
- **C. RMSE** → A **regression metric** that measures prediction error for continuous numerical values
- **D. Learning rate** → A **training hyperparameter**, not an evaluation metric. It controls how much model parameters are updated during training. 

### Exam Focus

**"How many predictions were classified correctly?" → Accuracy**

Quick distinction:

| **Metric**        | **Use**                                           |
| ----------------- | ------------------------------------------------- |
| **Accuracy**      | Overall proportion of correct classifications     |
| **R²**            | Regression goodness of fit                        |
| **RMSE**          | Regression prediction error                       |
| **Learning rate** | Training hyperparameter, not a performance metric |

Key exam association:

**Classification + proportion correct → Accuracy**

## Question 5

### Original Question

A company is using a **pre-trained large language model (LLM)** to build a chatbot for product recommendations. The company needs the LLM outputs to be **short** and written in a **specific language**.

Which solution will align the LLM response quality with the company's expectations?

### Choices

A. Adjust the prompt  
B. Choose an LLM of a different size  
C. Increase the temperature  
D. Increase the Top K value

### Correct Answer

**A. Adjust the prompt**

### Why?

**Prompt engineering** is the most direct way to control the **format, length, language, tone, and style** of an LLM response.

The prompt can explicitly instruct the model to:
- Respond in a specific language
- Keep the answer short or within a word limit
- Use a desired tone or output format.

- **A. Adjust the prompt** → Correct. Directly specifies the desired **language and response length.**
- **B. Choose an LLM of a different size** → Model size affects factors such as capability, cost, and latency, but does not directly enforce a particular language or response length.
- **C. Increase the temperature** → Increases **randomness and creativity**. It does not reliably control language or brevity.
- **D. Increase the Top K value** → Allows the model to choose from a larger set of probable next tokens, generally increasing output diversity rather than enforcing formatting requirements.

### Exam Focus

**Control LLM output format, language, tone, or length → Prompt engineering**

Quick distinction:

| **Technique**         | **Main Effect**                                           |
| --------------------- | --------------------------------------------------------- |
| **Prompt adjustment** | Controls instructions, format, language, tone and length  |
| **Temperature**       | Controls randomness / creativity                          |
| **Top K**             | Limits token selection to the K most likely tokens        |
| **Model size**        | Affects capability, cost, and performance characteristics |

Key exam associations:

**"Make the response short and use a specific language" → Adjust the prompt**

## Question 6

### Original Question 

A company uses **Amazon SageMaker** for its ML pipeline in a production environment. The company has **large input data sizes up to 1 GB** and **processing times up to 1 hour**. The company needs **near real-time latency**.

Which SageMaker inference option meets these requirements?

### Choices

A. Real-time inference  
B. Serverless inference  
C. Asynchronous inference  
D. Batch transform

### Correct Answer

**C. Asynchronous inference**

### Why?

**Amazon SageMaker Asynchronous Inference** is designed for interface requests that have **large payloads** or require **long processing times**, while still providing results much sooner than traditional batch processing.

It supports:
- Payloads up to **1 GB**
- Processing times up to **1 hour**
- Near real-time processing where the client does not need to maintain an open connection while waiting

- **A. Real-time inference** → Best for **low-latency, synchronous** requests with smaller payloads and shorter processing times
- **B. Serverless inference** → Best for intermittent or unpredictable workloads where you do not want to manage infrastructure; not intended for 1 GB payloads and hour-long processing
- **C. Asynchronous inference** → Correct. Designed specifically for **large payloads + long-running inference + near real-time results**
- **D. Batch transform** → Best for **offline batch predictions** where immediate or near rela-time responses are not required.

### Exam Focus

**Large payload + long processing time + near real-time → SageMaker Asynchronous Inference**

Quick distinction:

| **SageMaker Option**       | **Best Use Case**                                           |
| -------------------------- | ----------------------------------------------------------- |
| **Real-time Inference**    | Low-latency, synchronous predictions                        |
| **Serverless Inference**   | Intermittent/unpredictable traffic without managing servers |
| **Asynchronous Inference** | **Large payloads and long-running requests**                |
| **Batch transform**        | Offline predictions for large datasets                      |

Key exam association:
**"Up to 1 GB" + "up to 1 hour" → Asynchronous Inference**

## Question 7

### Original Question

A company is using **domain-specific models**. The company wants to avoid creating new models from the beginning. Instead, the company wants to **adapt pre-trained models** to create models for new, related tasks.

Which ML strategy meets these requirements?

### Choices

A. Increase the number of epochs  
B. Use transfer learning  
C. Decrease the number of epochs  
D. Use unsupervised learning

### Correct Answer

**B. Use transfer learning**

### Why?

**Transfer learning** reuses knowledge learned by a **pre-trained model** and adapts it to a new but related task. This reduces the need to train a model from scratch and can require less data, time, and compute.

- **A. Increase the number of epochs →** Changes how long a model trains but does not reuse knowledge from another trained model
- **B. Use transfer learning** → Correct. Starts with a pre-trained model and adapts it for a related task
- **C. Decrease the number of epochs →** Reduces training iterations but does not provide knowledge transfer
- **D. Use unsupervised learning** → Learns patterns from unlabeled data; it does not specifically mean adapting an existing pre-trained model

### Exam Focus

**Reuse a pre-trained model for a new related task → Transfer learning**

Memory aid:
**Pre-trained model → Adapt/fine-tune → New related task**

Key exam keywords: **pre-trained model, reuse existing knowledge, related task, avoid training from scratch, fine-tuning**

## Question 8

### Original Question

A company is building a solution to **generate images for protective eyewear**. The solution must have **high accuracy** and must **minimize the risk of incorrect annotations**.

Which solution will meet these requirements?

### Choices

A. Human-in-the-loop validation by using Amazon SageMaker Ground Truth Plus  
B. Data augmentation by using an Amazon Bedrock knowledge base  
C. Image recognition by using Amazon Rekognition  
D. Data summarization by using Amazon QuickSight Q

### Correct Answer

**A. Human-in-the-loop validation by using Amazon SageMaker Ground Truth Plus**

### Why?

**Amazon SageMaker Ground Truth Plus** provides managed **data labeling and annotation** with human review. Using **human-in-the-loop validation** helps improve annotation quality and reduce labeling errors, which is especially important when **high accuracy** is required.

- **A. SageMaker Ground Truth Plus** → Correct. Provides high-quality data labeling with **human validation**, helping minimize incorrect annotations
- **B. Amazon Bedrock knowledge base** → Used to connect foundation models to external data for **retrieval-augmented generation (RAG)**, not image annotation or data augmentation
- **C. Amazon Rekognition** → Performs **image and video analysis**, such as detecting objects, faces, and labels, but is not primarily a human annotation validation service.
- **D. Amazon QuickSight Q** → Provides **natural-language business intelligence and analytics**, not image labeling

### Exam Focus

**High-quality annotations + minimize labeling errors + human review → SageMaker Ground Truth Plus**

Quick associations:
- **SageMaker Ground Truth Plus** → Managed **data labeling / human annotation**
- **Amazon Rekognition** → Analyze and recognize content in **images and videos**
- **Amazon Bedrock Knowledge Bases** → **RAG / retrieve external knowledge**
- **Amazon QuickSight Q** → Natural-language **business intelligence**

Key exam keywords: **human-in-the-loop, data labeling, annotation accuracy, human validation**

## Question 9

### Original Question

A company wants to create a chatbot by using a **foundation model (FM) on Amazon Bedrock**. The FM needs to access encrypted data stored in an **Amazon S3 bucket**. The data is encrypted with **Amazon S3 managed keys (SSE-S3)**.

The FM encounters a failure when attempting to access the S3 bucket data.

Which solution will meet these requirements?

### Choices

A. Ensure that the role that Amazon Bedrock assumes has permission to decrypt data with the correct encryption key.  
B. Set the access permissions for the S3 buckets to allow public access to enable access over the internet.  
C. Use prompt engineering techniques to tell the model to look for information in Amazon S3.  
D. Ensure that the S3 data does not contain sensitive information.

### Correct Answer

**A. Ensure that the role that Amazon Bedrock assumes has permission to decrypt data with the correct encryption key.**

### Why?

- **A. Bedrock role permissions** → Intended answer. Access problems with protected S3 data should be solved through the **IAM/service role**, although explicit key-decryption permission applies to **SSE-KMS**, not SSE-S3
- **B. Public S3 access** → Incorrect and insecure. Bedrock should access S3 through appropriate IAM permissions.
- **C. Prompt engineering** → Cannot grant AWS resource permissions
- **D. Remove sensitive information** → Does not resolve an IAM or S3 access failure.

AWS documents `s3:GetObject` and `s3:ListBucket` as permissions used by Bedrock to retrieve S3 data.

### Exam Focus

**Bedrock cannot access S3 data → Check the Bedrock IAM/service role permissions**

Know the encryption distinction:

| **Encryption** | **Key Management**     | **Extra KMS Decrypt Permission?** |
| -------------- | ---------------------- | --------------------------------- |
| **SSE-S3**     | Amazon S3-managed keys | **No explicit KMS permission**    |
| **SSE-KMS**    | AWS KMS key            | `kms:Decrypt` **may be required** |

Key associations:
- **Bedrock → S3 access** → `s3:GetObject` / `s3:ListBucket`
- **Bedrock** → **SSE-KMS encrypted S3 data** → `kms:Decrypt`
- **Prompt engineering does not grant AWS permissions**

## Question 10

### Original Question

A company wants to use **language models** to create an application for inference on **edge devices**. The inference must have the **lowest latency possible**.

Which solution will meet these requirements?

### Choices

A. Deploy optimized small language models (SLMs) on edge devices.  
B. Deploy optimized large language models (LLMs) on edge devices.  
C. Incorporate a centralized small language model (SLM) API for asynchronous communication with edge devices.  
D. Incorporate a centralized large language model (LLM) API for asynchronous communication with edge devices.

### Correct Answer

**A. Deploy optimized small language models (SLMs) on edge devices.**

### Why?

Running an optimized **small language model (SLM)** directly on the **edge device** minimizes latency because inference happens locally and does not require a network round trip to a centralized service.

SLMs also require fewer compute and memory resources than LLMs, making them better suited for resource-constrained edge environments.

- **A. Optimized SLM on edge devices** → Correct. Provides **local inference**, lower resource requirements, and the lowest network latency
- **B. Optimized LLM on edge devices** → Local inference avoids network latency, but LLMs generally require substantially more compute and memory than SLMs.
- **C. Centralized SLM API** → Requires network communication, which adds latency.
- **D. Centralized LLM API** → Requires network communication and uses a larger model, making it less suitable when minimizing latency is the priority.

### Exam Focus

**Lowest-latency language model inference on edge devices → Deploy an optimized SLM locally**

Quick distinction:

| **Approach**            | **Latency Characteristic**                    |
| ----------------------- | --------------------------------------------- |
| **SLM on edge**         | **Lowest latency; local inference**           |
| **LLM on edge**         | Local, but higher resource requirements       |
| **Centralized SLM API** | Network latency added                         |
| **Centralized LLM API** | Network latency + larger compute requirements |

Key exam associations:

- **Edge inference + lowest latency → Local processing**
- **Limited compute/resources → Small Language Model (SLM)**

Memory aid:
- **SLM + Edge → Small, local, low latency**

## Question 11

### Original Question

A company wants to build an ML model by using **Amazon SageMaker**. The company needs to **share and manage variables for model development across multiple teams**.

Which SageMaker feature meets these requirements?

### Choices

A. Amazon SageMaker Feature Store  
B. Amazon SageMaker Data Wrangler  
C. Amazon SageMaker Clarify  
D. Amazon SageMaker Model Cards

### Correct Answer

**A. Amazon SageMaker Feature Store**

### Why?

**Amazon SageMaker Feature Store** is a centralized repository for storing, managing, sharing and reusing **ML features** across models and teams.

In this question, "variables for model development" refers to **features** used as inputs to ML models.

- **A. SageMaker Feature Store** → Correct. Stores and shares reusable ML features across teams and models.
- **B. SageMaker Data Wrangler** → Used to **prepare, clean, and transform data** for ML.
- **C. SageMaker Clarify** → Used for **bias detection and model explainability**
- **D. SageMaker Model Cards** → Used to **document model details**, such as intended use, risk, evaluation, and governance information

### Exam Focus

**Store, manage, share, and reuse ML features → SageMaker Feature Store**

Quick distinction:

| **SageMaker Feature** | **Main Purpose**                    |
| --------------------- | ----------------------------------- |
| **Feature Store**     | Store and reuse ML features         |
| **Data Wrangler**     | Prepare and transform ML data       |
| **Clarify**           | Detect bias and explain predictions |
| **Model Cards**       | Document and govern ML models       |

Memory aid:
- **Data Wrangler → prepare data**
- **Feature Store → store/share features**
- **Clarify → explain/bias**
- **Model Cards → document models**

## Question 12

### Original Question

A company wants to use **generative AI** to increase developer productivity and software development. The company wants to use **Amazon Q Developer**.

What can Amazon Q Developer do to help the company meet these requirements?

### Choices

A. Create software snippets, reference tracking, and open source license tracking.  
B. Run an application without provisioning or managing servers.  
C. Enable voice commands for coding and providing natural language search.  
D. Convert audio files to text documents by using ML models.

### Correct Answer

**A. Create software snippets, reference tracking, and open source license tracking.**

### Why?

**Amazon Q Developer** is a generative AI assistant designed to help developers **write, understand, debug, and improve code**. It can generate code recommendations ranging from snippets to complete functions.

Amazon Q Developer also provides **code reference tracking** when generated recommendations resemble publicly available code. The reference information can include the associated **open-source license**, helping developers review the origin and licensing of suggested code.

- **A. Code snippets + reference/license tracking** → Correct. These are Amazon Q Developer capabiltiies.
- **B. Run applications without managing servers** → Describes **serverless computing**, such as AWS Lambda, not Amazon Q Developer
- **C. Voice commands** → Not the relevant Amazon Q Developer capability described here.
- **D. Audio-to-text** → Describes **Amazon Transcribe**, not Amazon Q Developer

### Exam Focus

**Generative AI coding assistant → Amazon Q Developer**

Key associations:
- **Generate code / code snippets** → Amazon Q Developer
- **Explain, debug, or improve code** → Amazon Q Developer
- **Code reference tracking** → Amazon Q Developer
- **Open-source license information for referenced code** → Amazon Q Developer
- **Speech-to-text** → Amazon Transcribe
- **Serverless application execution** → AWS Lambda

Memory aid:
**Amazon Q Developer = AI assistant for software development**

## Question 13

### Original Question

A financial institution is using **Amazon Bedrock** to develop an AI application. The application is hosted in a **VPC**. To meet regulatory compliance standards, the VPC is **not allowed access to any internet traffic**.

Which AWS service or feature will meet these requirements?

### Choices

A. AWS PrivateLink  
B. Amazon Macie  
C. Amazon CloudFront  
D. Internet gateway

### Correct Answer

**A. AWS PrivateLink**

### Why?

**AWS PrivateLink** enables private connectivity between a **VPC and supported AWS services**, including **Amazon Bedrock**, without requiring an internet gateway, NAT device, public IP address, VPN, or Direct Connect connection. Amazon Bedrock supports **interface VPC endpoints powered by AWS PrivateLink**.

- **A. AWS PrivateLink** → Correct. Provides **private access to Amazon Bedrock without internet traffic**
- **B. Amazon Macie** → Used to discover and protect **sensitive data in Amazon S3**
- **C. Amazon CloudFront** → A content delivery network (CDN) for distributing content; it does not provide private VPC-to-Bedrock connectivity
- **D. Internet gateway** → Provides VPC connectivity to the internet, which directly conflicts with the requirement

### Exam Focus

**Private VPC access to AWS services without internet access → AWS PrivateLink**

## Question 14

### Original Question

A company wants to develop an educational game where users answer questions such as:

“A jar contains six red, four green, and three yellow marbles. What is the probability of choosing a green marble from the jar?”

Which solution meets these requirements with the **LEAST operational overhead**?

### Choices

A. Use supervised learning to create a regression model that will predict probability.  
B. Use reinforcement learning to train a model to return the probability.  
C. Use code that will calculate probability by using simple rules and computations.  
D. Use unsupervised learning to create a model that will estimate probability density.

### Correct Answer

**C. Use code that will calculate probability by using simple rules and computations.**

### Why?

The problem can be solved with a **deterministic mathematical calculation.** There is no need to train, deploy, or maintain an ML model.

For example:
**Probability = Favorable outcomes / Total outcomes**

Using simple code provides the **least operational overhead** because it avoids ML training, model hosting, monitoring, and maintenance.

- **A. Supervised regression** → Unnecessary for a problem with a known mathematical formula.
- **B. Reinforcement learning** → Used when an agent learns through **actions and rewards**, not simple probability calculations
- **C. Simple code/rules** → Correct. Deterministic computation is sufficient and simplest to operate
- **D. Unsupervised learning** → Used to discover patterns in **unlabeled data**, not calculate known probabilities.

### Exam Focus

**Known rules/formulas + deterministic answer → Use traditional code, not ML**

Quick distinction:
- **Deterministic calculation** → Traditional code
- **Predict continuous values from data** → Regression
- **Learn through rewards/actions** → Reinforcement learning
- **Find hidden patterns in unlabeled data** → Unsupervised learning

Memory aid:
**Simple formula → Simple code → Least operational overhead**

## Question 15

### Original Question

Which metric measures the **runtime efficiency of operating AI models**?

### Choices

A. Customer satisfaction score (CSAT)  
B. Training time for each epoch  
C. Average response time  
D. Number of training instances

### Correct Answer

**C. Average response time**

### Why?

**Average response time** measures how long an AI model takes to process a request and return a result during **inference/operation**. It is therefore a direct measure of **runtime performance and latency**.

- **A. CSAT** → Measures **user satisfaction**, not technical runtime efficiency
- **B. Training time per epoch** → Measures **training efficiency**, not runtime inference performance
- **C. Average response time** → Correct. Measures the model's **inference latency** while operating
- **D. Number of training instances** → Describes training resources or scale, not runtime efficiency.

### Exam Focus

**Runtime/inference efficiency → Average response time / latency**

Quick distinction:
- **Response time / latency** → Runtime inference performance
- **Training time per epoch** → Training performance
- **CSAT** → Business/user experience metric
- **Training instances** → Training infrastructure/resource count

Key exam association:
**"How fast does the deployed AI model respond?" → Average response time**

## Question 16

### Original Question

A company is building a **contact center application** and wants to gain insights from customer conversations. The company wants to **analyze and extract key information from the audio of customer calls**.

Which solution meets these requirements?

### Choices

A. Build a conversational chatbot by using Amazon Lex.  
B. Transcribe call recordings by using Amazon Transcribe.  
C. Extract information from call recordings by using Amazon SageMaker Model Monitor.  
D. Create classification labels by using Amazon Comprehend.

### Correct Answer

**B. Transcribe call recordings by using Amazon Transcribe.**

### Why?

**Amazon Transcribe** converts **speech in audio recordings into text**, making customer call content available for further analysis and extraction of insights.

For contact center workloads, **Amazon Transcribe Call Analytics** can also help derive information from calls, such as conversation characteristics and customer-agent interactions.

- **A. Amazon Lex** → Used to build **conversational chatbots and voice bots**, not primarily to analyze recorded calls
- **B. Amazon Transcribe** → Correct. Converts **audio/speech to text** so call information can be analyzed
- **C. SageMaker Model Monitor** → Monitors deployed ML models for issues such as **data/model quality drift**, not audio transcription
- **D. Amazon Comprehend** → Performs **NLP on text**, such as sentiment and entity detection, but the audio must first be converted to text

### Exam Focus

**Audio / speech → Text → Amazon Transcribe**

Quick distinction:
- **Amazon Transcribe** → Speech-to-text
- **Amazon Lex** → Conversational chatbots
- **Amazon Comprehend** → Analyze text with NLP
- **SageMaker Model Monitor** → Monitor deployed ML models

Memory aid:
**Customer call audio → Transcribe first → Analyze text afterward**

## Question 17

### Original Question

A company has **petabytes of unlabeled customer data** to use for an advertisement campaign. The company wants to **classify its customers into tiers** to advertise and promote the company's products.

Which methodology should the company use to meet these requirements?

### Choices

A. Supervised learning  
B. Unsupervised learning  
C. Reinforcement learning  
D. Reinforcement learning from human feedback (RLHF)

### Correct Answer

**B. Unsupervised learning**

### Why?

**Unsupervised learning** is used when the dataset is **unlabeled** and the goal is to discover hidden patterns or groups within the data.

For customer segmentation, a **clustering** algorithm can group customers with similar characteristics into different tiers without requiring predefined labels.

- **A. Supervised learning** → Requires **labeled training data** with known target outputs
- **B. Unsupervised learning** → Correct. Finds patterns or clusters in **unlabeled data**, making it suitable for customer segmentation.
- **C. Reinforcement learning** → Trains an agent through **actions and rewards**.
- **D. RLHF** → Uses **human feedback** to improve or align model behavior, commonly associated with generative AI models

### Exam Focus

**Unlabeled data + discover customer groups/segments → Unsupervised learning**

Quick distinction:
- **Supervised learning** → Labeled data → classification/regression
- **Unsupervised learning** → Unlabeled data → clustering/pattern discovery
- **Reinforcement learning** → Actions + rewards
- **RLHF** → Human feedback used to align model behavior

Key exam association:
**Customer segmentation / grouping / tiers from unlabeled data → Clustering → Unsupervised learning**

## Question 18

### Original Question

An AI practitioner wants to use a **foundation model (FM)** to design a search application. The search application must handle queries that contain **text and images**.

Which type of FM should the AI practitioner use to power the search application?

### Choices

A. Multi-modal embedding model  
B. Text embedding model  
C. Multi-modal generation model  
D. Image generation model

### Correct Answer

**A. Multi-modal embedding model**

### Why?

A **multi-modal embedding model** converts different data types, such as **text and images**, into numerical vector representations called **embeddings**.

These embeddings can be compared for similarity, making them ideal for **semantic search** across multiple modalities.

- **A. Multi-modal embedding model** → Correct. Supports embeddings for **text and images**, enabling cross-modal similarity search
- **B. Text embedding model** → Creates embeddings from text only and would not directly handle image queries
- **C. Multi-modal generation model** → Designed to understand and/or generate content across modalities, but is not the best fit when the primary task is **search and similarity matching**
- **D. Image generation model** → Generates images from prompts rather than creating representations for search.

### Exam Focus

**Search using text + images → Multi-modal embedding model**

Key associations:
- **Embedding model** → Convert content into vectors for **semantic search / similarity**
- **Text embedding** → Text only
- **Multi-modal embedding** → Text + images
- **Generation model** → Create new content

Memory aid:
- **Search → Embeddings**
- **Text + Images → Multi-modal embeddings**

## Question 19

### Original Question

A company uses a **foundation model (FM) from Amazon Bedrock** for an AI search tool. The company wants to **fine-tune the model** to be more accurate by using the company's data.

Which strategy will successfully fine-tune the model?

### Choices

A. Provide labeled data with the prompt field and the completion field.  
B. Prepare the training dataset by creating a `.txt` file that contains multiple lines in `.csv` format.  
C. Purchase Provisioned Throughput for Amazon Bedrock.  
D. Train the model on journals and textbooks.

### Correct Answer

**A. Provide labeled data with the prompt field and the completion field.**

### Why?

**Supervised fine-tuning** uses **labeled training examples** that show the model the desired relationship between an input and the expected output.

For supported Amazon Bedrock text-to-text fine-tuning, training data can contain:
- `prompt` → the input provided to the model
- `completion` → the expected output

AWS documents this format for non-conversational fine-tuning tasks. Training datasets are typically supplied as `JSONL`, with one training example per line.

- **A. Labeled prompt/completion data** → Correct. Provides examples that allow the FM to learn the company's desired behavior.
- **B. `.txt` containing CSV data** → Incorrect. Bedrock fine-tuning requires supported dataset formats such as **JSONL**, not arbitrary CSV lines in a text file.
- **C. Provisioned Throughput** → Provides reserved model inference capacity; it does not itself fine-tune a model
- **D. Journals and textbooks** → Generic additional data does not necessarily represent the company's task-specific desired outputs.

### Exam Focus

**Improve an FM for a specific task using labeled company data → Supervised fine-tuning**

Memory aid:
**Prompt = input → Completion = desired output**

Key exam associations:
- **Fine-tuning** → Modify model behavior using training examples
- **Labeled prompt + completion pairs** → Supervised fine-tuning
- **JSONL** → Common Bedrock fine-tuning dataset format
- **Provisioned Throughput** → Inference capacity, not **model training**
- **Company-specific labeled examples** → Better task/domain specialization

## Question 20

### Original Question

A company wants to use **AI to protect its application from threats**. The AI solution needs to check whether an **IP address is from a suspicious source**.

Which solution meets these requirements?

### Choices

A. Build a speech recognition system.  
B. Create a natural language processing (NLP) named entity recognition system.  
C. Develop an anomaly detection system.  
D. Create a fraud forecasting system.

### Correct Answer

**C. Develop an anomaly detection system.**

### Why?

**Anomaly detection** identifies unusual or suspicious patterns that differ from normal behavior. It is well suited for security use cases such as detecting potentially malicious IP addresses, abnormal traffic, or unusual access patterns.

- **A. Speech recognition** → Converts spoken audio into text; unrelated to IP threat detection
- **B. Named entity recognition (NER)** → Identifies entities such as names, organizations, dates, or locations in text
- **C. Anomaly detection** → Correct. Detects **unusual or suspicious behavior** that may indicate a threat
- **D. Fraud Forecasting** → Not the best fit or identifying suspicious IP activity in application security

### Exam Focus

**Suspicious activity / unusual behavior / threat detection → Anomaly detection**

Key exam associations:
- **Anomaly detection** → Find outliers and abnormal behavior
- **NER** → Extract named entities from text
- **Speech recognition** → Audio to text
- **Security monitoring** → Often uses anomaly detection

Memory aid:
**"Does this activity look unusual?" → Anomaly detection**

## Question 21

### Original Question

Which feature of **Amazon OpenSearch Service** gives companies the ability to build **vector database applications**?

### Choices

A. Integration with Amazon S3 for object storage  
B. Support for geospatial indexing and queries  
C. Scalable index management and nearest neighbor search capability  
D. Ability to perform real-time analysis on streaming data

### Correct Answer

**C. Scalable index management and nearest neighbor search capability**

### Why?

Vector databases store **embeddings** as high-dimensional vectors and perform **similarity search** to find the most similar vectors.

**Amazon OpenSearch Service** supports vector search through **k-nearest neighbor (k-NN)** / **nearest neighbor search**, which makes it suitable for applications such as **semantic search**, recommendation systems, and retrieval-augmented generation (RAG).

- **A. Amazon S3 integration** → Useful for storage and data integration, but does not provide the core vector search capability
- **B. Geospatial indexing** → Used for location-based queries, not embedding similarity
- **C. Nearest neighbor search** → Correct. Enables similarity searches across stored vectors.
- **D. Real-time streaming analysis** → Useful for analyzing incoming data, but is not what enables OpenSearch to function as a vector database.

### Exam Focus

**Vector database + similarity search → Nearest neighbor / k-NN search**

Key associations:
- **Embeddings** → Numerical vector representations
- **Vector database** → Store and search embeddings
- **k-NN / nearest neighbor search** → Find similar vectors
- **Amazon OpenSearch Service** → Supports vector search for semantic search and RAG

Memory aid:
**Embedding → Vector index → Nearest neighbor search → Most similar results**

## Question 22

### Original Question

Which option is a use case for **generative AI models**?

### Choices

A. Improving network security by using intrusion detection systems  
B. Creating photorealistic images from text descriptions for digital marketing  
C. Enhancing database performance by using optimized indexing  
D. Analyzing financial data to forecast stock market trends

### Correct Answer

**B. Creating photorealistic images from text descriptions for digital marketing**

### Why?

**Generative AI** is used to **create new content**, such as text, images, audio, video, or code.

Creating **photorealistic images from text prompts** is a classic **text-to-image generative AI** use case.

- **A. Intrusion detection systems** → More closely related to **security analytics** or anomaly detection, not content generation.
- **B. Creating photorealistic images from text descriptions** → Correct. This is a direct **generative AI** use case.
- **C. Optimized indexing** → A database performance task, not a generative AI task.
- **D. Forecasting stock market trends** → Usually a **predictive AI / ML** use case, not generative AI.

### Exam Focus

**Generative AI = create new content**

Common generative AI outputs:

- **Text**
- **Images**
- **Audio**
- **Video**
- **Code**

Quick distinction:

- **Generative AI** → Creates new content
- **Predictive ML** → Forecasts or classifies
- **Anomaly detection** → Finds unusual behavior
- **Optimization/indexing** → Traditional system/database improvement

Memory aid:

**If the model creates something new, it is likely a generative AI use case.**

## Question 23

### Original Question

A company wants to build a generative AI application by using **Amazon Bedrock** and needs to choose a **foundation model (FM)**. The company wants to know **how much information can fit into one prompt**.

Which consideration will inform the company's decision?

### Choices

A. Temperature  
B. Context window  
C. Batch size  
D. Model size

### Correct Answer

**B. Context window**

### Why?

The **context window** is the maximum amount of information a foundation model can process at one time. It includes the prompt and, depending on the model, may also account for conversation history and generated output.

A larger context window allows the model to handle **longer prompts, larger documents, or more conversation history**.

- **A. Temperature** → Controls **randomness and creativity** of model output.
- **B. Context window** → Correct. Determines how much text or tokenized information the model can process in a single interaction.
- **C. Batch size** → Controls how many training or inference samples are processed together; it does not define prompt capacity.
- **D. Model size** → Refers to the number of model parameters and generally affects capability and resource requirements, not directly how much information fits into one prompt.

### Exam Focus

**How much information can fit into one prompt → Context window**

Quick distinction:

- **Context window** → Maximum input/context capacity
- **Temperature** → Randomness / creativity
- **Batch size** → Number of samples processed together
- **Model size** → Number of parameters / model capacity

Memory aid:

**Longer prompt or more conversation history → Need a larger context window**

## Question 24

### Original Question

A company wants to make a chatbot to help customers solve technical problems without human intervention.

The company chose a **foundation model (FM)** for the chatbot. The chatbot needs to produce responses that **adhere to the company's tone**.

Which solution meets these requirements?

### Choices

A. Set a low limit on the number of tokens the FM can produce.  
B. Use batch inferencing to process detailed responses.  
C. Experiment and refine the prompt until the FM produces the desired responses.  
D. Define a higher number for the temperature parameter.

### Correct Answer

**C. Experiment and refine the prompt until the FM produces the desired responses.**

### Why?

**Prompt engineering** is used to guide a foundation model's **tone, style, format, and behavior**. By iteratively refining the prompt, the company can instruct the chatbot to respond using its preferred brand or support tone.

- **A. Limit output tokens** → Controls **response length**, not tone.
- **B. Batch inference** → Processes multiple inference jobs efficiently; it does not control response style.
- **C. Refine the prompt** → Correct. Prompt instructions can specify the desired **tone, style, and response format**.
- **D. Higher temperature** → Increases **randomness and creativity**, making responses less predictable rather than enforcing a consistent tone.

### Exam Focus

**Control FM tone, style, format, or behavior → Prompt engineering**

Quick distinction:

- **Prompt engineering** → Tone, style, instructions, output format
- **Max tokens** → Output length
- **Temperature** → Randomness / creativity
- **Batch inference** → Process multiple requests offline/at scale

Memory aid:

**“Make the model respond in a specific way” → Refine the prompt**

## Question 25

### Original Question

A company wants to use a **large language model (LLM) on Amazon Bedrock** for **sentiment analysis**. The company wants to classify text passages as **positive or negative**.

Which prompt engineering strategy meets these requirements?

### Choices

A. Provide examples of text passages with corresponding positive or negative labels in the prompt followed by the new text passage to be classified.  
B. Provide a detailed explanation of sentiment analysis and how LLMs work in the prompt.  
C. Provide the new text passage to be classified without any additional context or examples.  
D. Provide the new text passage with a few examples of unrelated tasks, such as text summarization or question answering.

### Correct Answer

**A. Provide examples of text passages with corresponding positive or negative labels in the prompt followed by the new text passage to be classified.**

### Why?

This is **few-shot prompting**. The prompt gives the LLM several labeled examples that demonstrate the desired classification behavior before asking it to classify a new input.

For sentiment analysis, examples such as:

**“I loved the product.” → Positive**  
**“The service was terrible.” → Negative**

help the model understand the expected labels and output format.

- **A. Labeled examples + new input** → Correct. This is **few-shot prompting**.
- **B. Detailed explanation only** → Provides background, but does not demonstrate the desired classification pattern as effectively.
- **C. New passage only** → This is closer to **zero-shot prompting** and provides less guidance.
- **D. Unrelated examples** → Do not help the model learn the sentiment classification task.

### Exam Focus

**Provide multiple examples of input + expected output in the prompt → Few-shot prompting**

Quick distinction:

- **Zero-shot** → Instructions only, no examples
- **One-shot** → One example
- **Few-shot** → Multiple examples
- **Unrelated examples** → Usually not useful for the target task

Key exam association:

**“Examples with labels followed by a new item to classify” → Few-shot prompting**

## Question 26

### Original Question

A security company is using **Amazon Bedrock** to run foundation models (FMs). The company wants to ensure that only authorized users invoke the models.

The company needs to **identify unauthorized access attempts** so it can set appropriate **AWS Identity and Access Management (IAM)** policies and roles for future iterations of the FMs.

Which AWS service should the company use to identify unauthorized users that are trying to access Amazon Bedrock?

### Choices

A. AWS Audit Manager  
B. AWS CloudTrail  
C. Amazon Fraud Detector  
D. AWS Trusted Advisor

### Correct Answer

**B. AWS CloudTrail**

### Why?

**AWS CloudTrail** records AWS API activity, including **who made a request**, **what action was attempted, when it occurred, and whether it succeeded or failed**.

This makes CloudTrail the correct service for identifying **unauthorized access attempts** to Amazon Bedrock and reviewing activity that can inform future **IAM policies and roles**

- **A. AWS Audit Manager** → Helps collect evidence and assess compliance against frameworks; it is not the primary service for tracing individual API access attempts
- **B. AWS CloudTrail** → Correct. Records and audits **AWS API calls and user activity**.
- **C. Amazon Fraud Detector** → Detects potentially fraudulent business activity using ML, not unauthorized AWS API access
- **D. AWS Trusted Advisor** → Provides recommendations for areas such as cost, security, performance, and fault tolerance; it does not provide detailed API activity logs.

### Exam Focus

**Track who accessed AWS services and which API calls were attempted → AWS CloudTrail**

Quick distinction:
- **CloudTrail** → API activity / user actions / audit trail
- **Audit Manager** → Compliance evidence and assessments
- **Trusted Advisor** → AWS best-practice recommendations
- **Fraud Detector** → Fraud detection using ML

## Question 27

### Original Question

A company has developed an **ML model for image classification**. The company wants to deploy the model to production so that a web application can use the model.

The company needs to **host the model and serve predictions without managing any of the underlying infrastructure**.

Which solution will meet these requirements?

### Choices

A. Use Amazon SageMaker Serverless Inference to deploy the model.  
B. Use Amazon CloudFront to deploy the model.  
C. Use Amazon API Gateway to host the model and serve predictions.  
D. Use AWS Batch to host the model and serve predictions.

### Correct Answer

**A. Use Amazon SageMaker Serverless Inference to deploy the model.**

### Why?

**Amazon SageMaker Serverless Inference** allows a company to deploy ML models and serve inference requests **without provisioning or managing servers**.

It is well suited for workloads with **intermittent or unpredictable traffic** and automatically manages the underlying compute infrastructure.

- **A. SageMaker Serverless Inference** → Correct. Hosts the model and serves predictions with **no infrastructure management**.
- **B. Amazon CloudFront** → A **content delivery network (CDN)** used to cache and distribute content, not host ML models for inference.
- **C. Amazon API Gateway** → Expose APIs, but does not itself host an ML model or run inference.
- **D. AWS Batch** → Designed for **batch computing jobs**, not low-latency model serving for a web application

### Exam Focus

**Deploy ML model + server predictions + no server management → SageMaker Serverless Inference**

Quick distinction:
- **SageMaker Serverless Inference** → Serverless ML inference
- **API Gateway** → Expose/manage APIs
- **CloudFront** → Content delivery/CDN
- **AWS Batch** → Batch processing workloads

Memory aid:
**"Inference without managing servers" → SageMaker Serverless Inference**

## Question 28
### Original Question

An AI company periodically evaluates its systems and processes with the help of **independent software vendors (ISVs)**. The company needs to receive **email notifications when an ISV's compliance reports become available**.

Which AWS service can the company use to meet this requirement?

### Choices

A. AWS Audit Manager  
B. AWS Artifact  
C. AWS Trusted Advisor  
D. AWS Data Exchange

### Correct Answer

**B. AWS Artifact**

### Why?

**AWS Artifact** provides on-demand access to **AWS compliance reports and agreements**. It is the AWS service associated with retrieving compliance documentation and related reports.

For exam purposes, when the scenario mentions **compliance reports**, certifications, or audit documentation, think **AWS Artifact**.

- **A. AWS Audit Manager** → Helps automate the collection of evidence for **audits and compliance assessments**.
- **B. AWS Artifact** → Correct. Provides access to **compliance reports and agreements**.
- **C. AWS Trusted Advisor** → Provides recommendations for areas such as cost optimization, security, performance, and resilience.
- **D. AWS Data Exchange** → Used to discover and subscribe to **third-party datasets**, not compliance documentation.

### Exam Focus

**Access/download compliance reports and agreements → AWS Artifact**

Quick distinction:
- **AWS Artifact** → Compliance reports and agreements
- **AWS Audit Manager** → Automate audit evidence collection
- **AWS Trusted Advisor** → Best-practice recommendations
- **AWS Data Exchange** → Third-party data products

## Question 29

### Original Question

A company wants to use a **large language model (LLM)** to develop a conversational agent. The company needs to prevent the LLM from being manipulated with common **prompt engineering attacks** to perform undesirable actions or expose sensitive information.

Which action will reduce these risks?

### Choices

A. Create a prompt template that teaches the LLM to detect attack patterns.  
B. Increase the temperature parameter on invocation requests to the LLM.  
C. Avoid using LLMs that are not listed in Amazon SageMaker.  
D. Decrease the number of input tokens on invocations of the LLM.

### Correct Answer

**A. Create a prompt template that teaches the LLM to detect attack patterns.**

### Why?

A well-designed **prompt template** can include instructions that help the model recognize and resist **prompt injection**, malicious instructions, and attempts to override intended behavior.

- **A. Prompt template with attack-detection instructions** → Correct. Adds defensive guidance against common prompt manipulation techniques.
- **B. Increase temperature** → Increases randomness and variability; it does not improve prompt-injection resistance.
- **C. Use only SageMaker-listed LLMs** → Model hosting location does not inherently prevent prompt attacks.
- **D. Decrease input tokens** → Limits prompt length but does not reliably stop malicious instructions.

### Exam Focus

**Protect an LLM from prompt manipulation → Use defensive prompt engineering / prompt templates**

Key associations:

- **Prompt injection** → Malicious instructions designed to override model behavior
- **Prompt template / system instructions** → Help constrain model behavior
- **Temperature** → Controls randomness, not security
- **Token limits** → Control input/output size, not prompt-injection protection

Memory aid:

**“Prevent prompt attacks” → Add explicit defensive instructions and guardrails**

## Question 30

### Original Question

A company is using the **Generative AI Security Scoping Matrix** to assess security responsibilities for its solutions. The company has identified four different solution scopes based on the matrix.

Which solution scope gives the company the **MOST ownership of security responsibilities**?

### Choices

A. Using a third-party enterprise application that has embedded generative AI features.  
B. Building an application by using an existing third-party generative AI foundation model (FM).  
C. Refining an existing third-party generative AI foundation model (FM) by fine-tuning the model by using data specific to the business.  
D. Building and training a generative AI model from scratch by using specific data that a customer owns.

### Correct Answer

**D. Building and training a generative AI model from scratch by using specific data that a customer owns.**

### Why?

The more of the generative AI stack a company **builds, trains, and operates itself**, the more security responsibility it owns.

Training a model **from scratch** means the company is responsible for a wider range of controls, including the **training data, model development, model behavior, infrastructure choices, access controls, and operational security**.

- **A. Third-party application with embedded GenAI** → Least customer ownership because most of the AI stack is managed by the vendor.
- **B. Existing third-party FM** → More responsibility than using a package application, but the underlying FM is still managed by the provider.
- **C. Fine-tuning a third-party FM** → Greater responsibility because the company manages its own fine-tuning data and customization.
- **D. Build and train from scratch** → Correct. Gives the company the **greatest ownership and security responsibility** across the model lifecycle.

### Exam Focus

**More customization and ownership of the GenAI stack → More security responsibility**

Typical progression:

**Third-party GenAI app → Use existing FM → Fine-tune FM → Train model from scratch**

Security ownership generally **increases from left to right**

Memory aid:

**"Build more yourself" → "Own more security responsibility"**


---

→
## Question X
### Original Question
### Choices
### Correct Answer
### Why?
### Exam Focus