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

## Question 31

### Original Question

An AI practitioner has a database of **animal photos**. The AI practitioner wants to automatically **identify and categorize the animals in the photos** without manual human effort.

Which strategy meets these requirements?

### Choices

A. Object detection  
B. Anomaly detection  
C. Named entity recognition  
D. Inpainting

### Correct Answer

**A. Object detection**

### Why?

**Object detection** identifies and locates objects within images and can classify those objects into categories, such as different types of animals.

- **A. Object detection** → Correct. Detects and categorizes objects in images.
- **B. Anomaly detection** → Find unusual or abnormal patterns, not animal categories
- **C. Named entity recognition (NER)** → Extracts entities such as people, organizations, and locations from **text**
- **D. Inpainting** → Fill in or reconstructs missing/removed parts of an image

### Exam Focus

**Identify and categorize objects in images** → **Object detection**

Quick distinction:
- **Object detection** → Find and classify objects in images
- **Anomaly detection** → Detect unusual behavior or outliers
- **NER** → Extract named entities from text
- **Inpainting** → Fill or replace parts of an image

Memory aid:

**"What objects are in this image?"** → **Object detection**

## Question 32

### Original Question

A company wants to create an application by using **Amazon Bedrock**. The company has a **limited budget** and prefers **flexibility without long-term commitment**.

Which Amazon Bedrock pricing model meets these requirements?

### Choices

A. On-Demand  
B. Model customization  
C. Provisioned Throughput  
D. Spot Instance

### Correct Answer

**A. On-Demand**

### Why?

**Amazon Bedrock On-Demand** pricing lets the company pay only for the model usage it consumes, without committing to reserved capacity or long-term throughput.

This is a good fit for workloads that need **flexibility**, have uncertain usage, or want to minimize upfront commitment.

- **A. On-Demand** → Correct. Pay for usage with **no long-term commitment**
- **B. Model customization** → Refers to customizing/fine-tuning models, not the general pricing model for flexible inference.
- **C. Provisioned Throughput** → Reserves model capacity for predictable or high-volume workloads and involves a stronger capacity commitment.
- **D. Spot Instance** → An EC2 purchasing option, not an Amazon Bedrock pricing model

### Exam Focus

**Flexible usage + limited budget + no long-term commitment → Amazon Bedrock On-Demand**

Quick distinction:
- **On-Demand** → Pay per use, flexible
- **Provisioned Throughput** → Reserved model capacity for predictable demand
- **Model customization** → Fine-tuning/customizing models
- **Spot Instances** → Discounted EC2 capacity, not Bedrock pricing

Memory aid:
**"No commitment, pay as you go" → On-Demand**

## Question 33

### Original Question

Which AWS service or feature can help an AI development team **quickly deploy and consume a foundation model (FM) within the team's VPC**?

### Choices

A. Amazon Personalize  
B. Amazon SageMaker JumpStart  
C. PartyRock, an Amazon Bedrock Playground  
D. Amazon SageMaker endpoints

### Correct Answer

**B. Amazon SageMaker JumpStart**

### Why?

**Amazon SageMaker JumpStart** provides access to **pre-trained foundation models and ML models** that can be quickly selected, deployed, and used within a SageMaker environment.

It reduces the effort required to find, configure, and deploy an FM from scratch.

- **A. Amazon Personalize** → Builds personalized recommendation systems, not general-purpose FM deployment.
- **B. SageMaker JumpStart** → Correct. Provides a catalog of **pre-trained models and foundation models** for rapid deployment.
- **C. PartyRock** → A generative AI playground for quickly building applications, but not for deploying FMs into a team's VPC
- **D. SageMaker endpoints** → Host deployed models for inference, but do not provide the curated FM catalog and quick-start deployment capability of JumpStart.

### Exam Focus

**Quickly discover and deploy pre-trained foundation models in SageMaker → SageMaker JumpStart**

Quick distinction:
- **SageMaker JumpStart** → Find and rapidly deploy pre-trained models/FMs
- **SageMaker endpoints** → Host models for inference
- **Amazon Personalize** → Personalized recommendations
- **PartyRock** → No-code/low-code generative AI experimentation

Memory aid:
**"Jump-start model deployment" → SageMaker JumpStart**

## Question 34

### Original Question

How can companies use **large language models (LLMs) securely on Amazon Bedrock**?

### Choices

A. Design clear and specific prompts. Configure AWS Identity and Access Management (IAM) roles and policies by using least privilege access.  
B. Enable AWS Audit Manager for automatic model evaluation jobs.  
C. Enable Amazon Bedrock automatic model evaluation jobs.  
D. Use Amazon CloudWatch Logs to make models explainable and to monitor for bias.

### Correct Answer

**A. Design clear and specific prompts. Configure AWS Identity and Access Management (IAM) roles and policies by using least privilege access.**

### Why?

Secure use of **Amazon Bedrock** includes controlling access to models and AWS resources with **IAM** and following the **principle of least privilege**.

Clear, specific prompts can also reduce unintended model behavior, while IAM policies ensure that users and applications can access only the resources and actions they actually need.

- **A. Clear prompts + least-privilege IAM** → Correct. Combines safer model interaction with proper AWS access control.
- **B. AWS Audit Manager** → Helps with compliance evidence and audits; it does not run Bedrock model evaluation jobs.
- **C. Bedrock model evaluation jobs** → Useful for evaluating model quality and behavior, but not the primary mechanism for securing access.
- **D. CloudWatch Logs** → Useful for monitoring and logging, but does not itself provide model explainability or bias detection.

### Exam Focus

**Secure Amazon Bedrock access → IAM + least privilege**

Key associations:

- **IAM roles/policies** → Control who can invoke models and access resources
- **Least privilege** → Grant only necessary permissions
- **Clear prompts** → Help constrain expected model behavior
- **CloudWatch** → Monitoring/logging
- **Audit Manager** → Compliance/audit evidence
- **Bedrock model evaluation** → Assess model quality and behavior

Memory aid:

**“Secure Bedrock usage” → Least-privilege IAM + well-designed prompts**

## Question 35

### Original Question

A company has terabytes of data in a database that the company can use for business analysis. The company wants to build an **AI-based application that can build a SQL query from input text** that employees provide. The employees have minimal experience with technology.

Which solution meets these requirements?

### Choices

A. Generative pre-trained transformers (GPT)  
B. Residual neural network  
C. Support vector machine  
D. WaveNet

### Correct Answer

**A. Generative pre-trained transformers (GPT)**

### Why?

**Generative pre-trained transformers (GPTs)** can understand **natural language** and generate structured text such as **SQL queries**.

This supports a **text-to-SQL** use case, where an employee can ask a question in plain language and the model generates the corresponding SQL query.

- **A. GPT** → Correct. Suitable for **natural language understanding and code/query generation**
- **B. Residual neural network (ResNet)** → Primarily used for **computer vision and image recognition**
- **C. Support vector machine (SVM)** → Used mainly for classification and regression, not natural-language SQL generation
- **D. WaveNet** → Designed primarily for **audio and speech waveform generation**

### Exam Focus

**Natural language → Generate SQL/code → Generative AI / transformer model**

Quick distinction:
- **GPT / Transformer** → Text generation, code generation, text-to-SQL
- **ResNet** → Image recognition / computer vision
- **SVM** → Classification / regression
- **WaveNet** → Audio generation

Memory aid:
**"Ask in plain English, generate SQL" → GPT / Generative AI**

## Question 36

### Original Question

A company built a **deep learning model for object detection** and deployed the model to production.

Which AI process occurs when the model analyzes a **new image** to identify objects?

### Choices

A. Training  
B. Inference  
C. Model deployment  
D. Bias correction

### Correct Answer

**B. Inference**

### Why?

**Inference** is the process of using a **trained model** to make predictions or generate outputs from new, unseen data.

In this scenario, the object detection model has already been trained and deployed. When it receives a new image and identifies objects, it is performing **inference**.

- **A. Training** → The model learns patterns from training data.
- **B. Inference** → Correct. The trained model analyzes new data and produces predictions.
- **C. Model deployment** → Makes the trained model available for use in production.
- **D. Bias correction** → Refers to reducing unfair or skewed model behavior, not generating predictions.

### Exam Focus

**Trained model + new data + prediction → Inference**

Quick distinction:

- **Training** → Learn from data
- **Deployment** → Put model into production
- **Inference** → Use trained model to make predictions
- **Bias mitigation** → Reduce unfair or skewed outcomes

Memory aid:

**Train → Deploy → Infer**

## Question 37

### Original Question

An AI practitioner is building a model to generate **images of humans in various professions**. The AI practitioner discovers that the **input data is biased** and that specific attributes affect the generated images and create bias in the model.

Which technique will solve the problem?

### Choices

A. Data augmentation for imbalanced classes  
B. Model monitoring for class distribution  
C. Retrieval Augmented Generation (RAG)  
D. Watermark detection for images

### Correct Answer

**A. Data augmentation for imbalanced classes**

### Why?

If the training data underrepresents certain groups or attributes, **data augmentation** can increase the representation of those underrepresented classes and help create a more balanced training dataset.

Reducing imbalance in the input data can reduce the likelihood that the model learns and reproduces biased patterns.
- **A. Data augmentation for imbalanced classes** → Correct. Helps balance the training dataset and mitigate bias caused by underrepresented groups
- **B. Model monitoring for class distribution** → Can **detect or track bias/drift**, but monitoring alone does not correct the biased training data
- **C. RAG** → Adds external retrieved information to a model's context; it does not directly correct class imbalance in image training data
- **D. Watermark detection** → Identifies watermarks or potentially AI-generated content; it does not address training-data bias.

### Exam Focus

**Biased training data caused by class imbalance → Data augmentation / rebalance the dataset**

Quick distinction:
- **Data augmentation** → Mitigate imbalance by increasing training examples
- **Model monitoring** → Detect changes or problems after deployment
- **RAG** → Add external knowledge to generation
- **Watermark detection** → identify marked/generated media

Memory aid:
**Bias starts in imbalanced data → Fix the data distribution**

## Question 38

### Original Question

A company is implementing the **Amazon Titan foundation model (FM)** by using **Amazon Bedrock**. The company needs to **supplement the model with relevant data from the company's private data sources**.

Which solution will meet this requirement?

### Choices

A. Use a different FM.  
B. Choose a lower temperature value.  
C. Create an Amazon Bedrock knowledge base.  
D. Enable model invocation logging.

### Correct Answer

**C. Create an Amazon Bedrock knowledge base.**

### Why?

**Knowledge Bases for Amazon Bedrock** let a foundation model retrieve relevant information from private enterprise data sources and use that information when generating responses.

This is a **Retrieval-Augmented Generation (RAG)** pattern:

**Private data → Knowledge Base → Retrieve relevant context → FM generates response**

- **A. Use a different FM** → Does not solve the requirement to incorporate private company data.
- **B. Lower temperature** → Makes outputs more deterministic, but does not add external knowledge.
- **C. Amazon Bedrock Knowledge Base** → Correct. Connects private data to the FM for grounded responses.
- **D. Model invocation logging** → Records model requests and responses for monitoring/auditing; it does not supply private knowledge to the model.

### Exam Focus

**Supplement an FM with private/company data → Amazon Bedrock Knowledge Bases**

Key associations:

- **Knowledge Base** → Connect private data to an FM
- **RAG** → Retrieve relevant external information before generation
- **Temperature** → Controls randomness
- **Invocation logging** → Monitoring/auditing

Memory aid:

**Need the FM to use company-specific knowledge → Knowledge Base + RAG**

## Question 39

### Original Question

A medical company is customizing a **foundation model (FM)** for diagnostic purposes. The company needs the model to be **transparent and explainable** to meet regulatory requirements.

Which solution will meet these requirements?

### Choices

A. Configure the security and compliance by using Amazon Inspector.  
B. Generate simple metrics, reports, and examples by using Amazon SageMaker Clarify.  
C. Encrypt and secure training data by using Amazon Macie.  
D. Gather more data. Use Amazon Rekognition to add custom labels to the data.

### Correct Answer

**B. Generate simple metrics, reports, and examples by using Amazon SageMaker Clarify.**

### Why?

**Amazon SageMaker Clarify** helps improve **model transparency and explainability** by providing tools to analyze predictions, detect bias, and explain how input features influence model outputs.

This makes it suitable for regulated use cases where organizations need to understand and document model behavior.

- **A. Amazon Inspector** → Identifies software vulnerabilities and unintended network exposure; it does not provide model explainability.
- **B. SageMaker Clarify** → Correct. Provides **bias detection and model explainability** capabilities.
- **C. Amazon Macie** → Discovers and protects **sensitive data in Amazon S3**; it does not explain model predictions.
- **D. Amazon Rekognition Custom Labels** → Used to build custom **image classification/object detection** models, not to provide FM transparency.

### Exam Focus

**Model transparency + explainability + bias analysis → Amazon SageMaker Clarify**

Quick distinction:

- **SageMaker Clarify** → Explainability and bias detection
- **Amazon Inspector** → Vulnerability management
- **Amazon Macie** → Sensitive-data discovery in S3
- **Rekognition Custom Labels** → Custom image analysis

Memory aid:

**“Why did the model make this prediction?” → SageMaker Clarify**

## Question 40

### Original Question

A company wants to deploy a conversational chatbot to answer customer questions. The chatbot is based on a fine-tuned **Amazon SageMaker JumpStart** model. The application must comply with multiple regulatory frameworks.

Which capabilities can the company show compliance for? **(Choose two.)**

### Choices

A. Auto scaling inference endpoints  
B. Threat detection  
C. Data protection  
D. Cost optimization  
E. Loosely coupled microservices

### Correct Answer

**B. Threat detection**  
**C. Data protection**

### Why?

Regulatory compliance commonly focuses on **security contrls** that protect systems and sensitive data. **Amazon SageMaker** provides security and compliance capabilities covering areas such as data protection, IAM, logging, monitoring, and infrastructure security.

- **A. Auto scaling inference endpoints** → Improves scalability and availability, but is not primarily a regulatory compliance control.
- **B. Threat detection** → Correct. Detecting and monitoring potential security threats supports security and compliance requirements
- **C. Data protection** → Correct. SageMaker supports controls such as **encryption, IAM, secure network communication, and activity logging** to protect data.
- **D. Cost optimization** → Focuses on reducing spending, not demonstrating regulatory compliance
- **E. Loosely coupled microservices** → An application architecture pattern, not a compliance capability

### Exam Focus

**Regulatory compliance** → **Think security + data protection**

For this question:
**Threat detection + Data protection → Compliance-related capabilities**

Quick distinction:
- **Threat detection** → Identify security threats
- **Data protection** → Encryption, access control, secure handling of data
- **Auto scaling** → Performance/scalability
- **Cost optimization** → Financial efficiency
- **Loosely coupled architecture** → Application design

Memory aid:
**Compliance question → Look for controls that protect systems and data**

## Question 41

### Original Question

A company is training a **foundation model (FM)**. The company wants to increase the **accuracy of the model up to a specific acceptance level**.

Which solution will meet these requirements?

### Choices

A. Decrease the batch size.  
B. Increase the epochs.  
C. Decrease the epochs.  
D. Increase the temperature parameter.

### Correct Answer

**B. Increase the epochs.**

### Why?

An **epoch** is one complete pass through the training dataset. Increasing the number of epochs gives the model more opportunities to learn patterns from the training data and can improve model accuracy until the desired performance level is reached.

- **A. Decrease the batch size** → Changes how many training examples are processed before each model update, but does not directly guarantee higher accuracy.
- **B. Increase the epochs** → Correct. More training iterations can improve learning and model accuracy.
- **C. Decrease the epochs** → Reduces training and can lead to **underfitting**.
- **D. Increase the temperature** → Temperature is an **inference parameter** that controls output randomness; it does not improve training accuracy.

Too many epochs can eventually cause **overfitting**, so training should be monitored and stopped once the desired validation performance is reached.

### Exam Focus

**Need the model to train longer and improve accuracy → Increase epochs**

Quick distinction:

- **Epochs** → Number of complete passes through training data
- **Batch size** → Number of samples processed before a parameter update
- **Temperature** → Controls randomness during generation/inference
- **Too few epochs** → Underfitting
- **Too many epochs** → Risk of overfitting

Memory aid:

**More epochs → More learning opportunities → Potentially higher accuracy**

## Question 42

### Original Question

A company is building a **large language model (LLM) question-answering chatbot**. The company wants to decrease the number of actions call center employees need to take to respond to customer questions.

Which business objective should the company use to evaluate the effect of the LLM chatbot?

### Choices

A. Website engagement rate  
B. Average call duration  
C. Corporate social responsibility  
D. Regulatory compliance

### Correct Answer

**B. Average call duration**

### Why?

The goal is to make call center employees more **efficient when answering customer questions**. If the chatbot provides useful answers quickly, employees should need fewer manual actions and spend less time handling each call.

Therefore, **average call duration** is a relevant measurable business KPI for evaluating the chatbot's impact.

- **A. Website engagement rate** → Measures website interaction, not call center efficiency.
- **B. Average call duration** → Correct. Reflects how efficiently agents can resolve customer questions.
- **C. Corporate social responsibility** → A broad organizational objective, not a direct chatbot performance metric.
- **D. Regulatory compliance** → Important for governance, but does not measure reduction in employee effort.

### Exam Focus

**AI reduces call-center effort → Measure operational efficiency**

Key association:

**Faster customer-question resolution → Lower average call duration**

Quick distinction:

- **Average call duration** → Call center productivity/efficiency
- **Website engagement** → Digital customer interaction
- **Compliance** → Regulatory/governance requirement
- **CSR** → Broader social/business objective

Memory aid:
**Business objective should directly measure the problem the AI is intended to improve.**

## Question 43

### Original Question

Which functionality does **Amazon SageMaker Clarify** provide?

### Choices

A. Integrates a Retrieval Augmented Generation (RAG) workflow  
B. Monitors the quality of ML models in production  
C. Documents critical details about ML models  
D. Identifies potential bias during data preparation

### Correct Answer

**D. Identifies potential bias during data preparation**

### Why?

**Amazon SageMaker Clarify** helps detect **bias in datasets and ML models** and also provides **model explainability** capabilities.

It can identify potential bias during **data preparation before model training**, as well as evaluate bias after training.

- **A. RAG workflow** → More closely associated with services such as **Amazon Bedrock Knowledge Bases**.
- **B. Monitor model quality in production** → Primarily handled by **Amazon SageMaker Model Monitor**.
- **C. Document model details** → Handled by **Amazon SageMaker Model Cards**.
- **D. Identify potential bias** → Correct. This is a core **SageMaker Clarify** capability.

### Exam Focus

**Bias detection + model explainability → SageMaker Clarify**

Quick distinction:

- **SageMaker Clarify** → Bias detection and explainability
- **SageMaker Model Monitor** → Monitor production model/data quality
- **SageMaker Model Cards** → Document model details and governance information
- **Bedrock Knowledge Bases** → RAG with external/private data

Memory aid:

**Clarify = “Is the model biased, and why did it predict this?”**

## Question 44

### Original Question

A company is developing a new model to **predict the prices of specific items**. The model performed well on the **training dataset**. When the company deployed the model to production, the model's performance decreased significantly.

What should the company do to mitigate this problem?

### Choices

A. Reduce the volume of data that is used in training.  
B. Add hyperparameters to the model.  
C. Increase the volume of data that is used in training.  
D. Increase the model training time.

### Correct Answer

**C. Increase the volume of data that is used in training.**

### Why?

The model performs well on training data but poorly on new production data, which is a classic sign of **overfitting**. The model has learned the training data too closely and does not generalize well to unseen examples.

Using **more diverse training data** can help the model learn broader patterns and improve generalization.

- **A. Reduce training data** → Likely makes overfitting worse because the model has even fewer examples to learn from.
- **B. Add hyperparameters** → Hyperparameters are configuration values; simply adding more does not inherently solve overfitting.
- **C. Increase training data** → Correct. More representative data can reduce overfitting and improve generalization.
- **D. Increase training time** → Can worsen overfitting because the model may fit the training data even more closely.

### Exam Focus

**High training performance + poor performance on unseen/production data → Overfitting**

Common ways to reduce overfitting:

- **Increase training data**
- Use more representative/diverse data
- Apply regularization
- Reduce unnecessary model complexity
- Use early stopping

Key distinction:

**Overfitting** → Good on training data, poor on new data  
**Underfitting** → Poor on both training and new data

Memory aid:

**“Memorizes training data, fails in production” → Overfitting**

## Question 45

### Original Question

An ecommerce company wants to build a solution to determine **customer sentiment** based on **written product reviews**.

Which AWS services meet these requirements? **(Choose two.)**

### Choices

A. Amazon Lex  
B. Amazon Comprehend  
C. Amazon Polly  
D. Amazon Bedrock  
E. Amazon Rekognition

### Correct Answer

**B. Amazon Comprehend**  
**D. Amazon Bedrock**

### Why?

Both **Amazon Comprehend** and **Amazon Bedrock** can be used to analyze text and determine sentiment.

- **A. Amazon Lex** → Used to build **conversational chatbots and voice bots**.
- **B. Amazon Comprehend** → Correct. Provides NLP capabilities including **sentiment analysis**, entity recognition, and key phrase extraction.
- **C. Amazon Polly** → Converts **text to speech**.
- **D. Amazon Bedrock** → Correct. Foundation models can analyze written text and classify or describe its sentiment.
- **E. Amazon Rekognition** → Analyzes **images and videos**, not written reviews.

### Exam Focus

**Sentiment analysis on text → Amazon Comprehend or Amazon Bedrock**

Quick distinction:

- **Amazon Comprehend** → Managed NLP service; sentiment, entities, key phrases
- **Amazon Bedrock** → Generative AI / foundation models; can perform text classification and sentiment analysis
- **Amazon Lex** → Chatbots
- **Amazon Polly** → Text-to-speech
- **Amazon Rekognition** → Image/video analysis

Memory aid:

**Written text + sentiment → Comprehend / Bedrock**

## Question 46

### Original Question

A company wants to use **large language models (LLMs) with Amazon Bedrock** to develop a chat interface for the company's **product manuals**. The manuals are stored as **PDF files**.

Which solution meets these requirements **MOST cost-effectively**?

### Choices

A. Use prompt engineering to add one PDF file as context to the user prompt when the prompt is submitted to Amazon Bedrock.  
B. Use prompt engineering to add all the PDF files as context to the user prompt when the prompt is submitted to Amazon Bedrock.  
C. Use all the PDF documents to fine-tune a model with Amazon Bedrock. Use the fine-tuned model to process user prompts.  
D. Upload PDF documents to an Amazon Bedrock knowledge base. Use the knowledge base to provide context when users submit prompts to Amazon Bedrock.

### Correct Answer

**D. Upload PDF documents to an Amazon Bedrock knowledge base. Use the knowledge base to provide context when users submit prompts to Amazon Bedrock.**

### Why?

**Amazon Bedrock Knowledge Bases** support **Retrieval-Augmented Generation (RAG)**. The manuals can be indexed so that, for each user question, only the **most relevant document chunks** are retrieved and added as context to the model.

This is more cost-effective than repeatedly sending entire PDFs or fine-tuning a model.

- **A. Add one PDF to each prompt** → Inefficient and may not retrieve the correct manual for each question.
- **B. Add all PDFs to every prompt** → Expensive because it increases **input tokens** and may exceed the model's context window.
- **C. Fine-tune using the PDFs** → More costly and operationally complex; fine-tuning is not the best approach for simply providing access to changing reference documents.
- **D. Bedrock Knowledge Base** → Correct. Uses **RAG** to retrieve only relevant content and provide it as context.

### Exam Focus

**Chat with private documents / PDFs → Amazon Bedrock Knowledge Bases + RAG**

Memory flow:

**PDF manuals → Knowledge Base → Retrieve relevant chunks → Add context → FM generates answer**

Key distinctions:

- **RAG / Knowledge Base** → Best for grounding responses in external or private documents
- **Fine-tuning** → Change model behavior/style for a task
- **Prompt with all documents** → High token cost and context-window issues
- **Relevant document retrieval** → More efficient and cost-effective

Memory aid:

**“Ask questions about company documents” → Bedrock Knowledge Base**

## Question 47

### Original Question

A social media company wants to use a **large language model (LLM)** for content moderation. The company wants to evaluate the LLM outputs for **bias and potential discrimination** against specific groups or individuals.

Which data source should the company use to evaluate the LLM outputs with the **LEAST administrative effort**?

### Choices

A. User-generated content  
B. Moderation logs  
C. Content moderation guidelines  
D. Benchmark datasets

### Correct Answer

**D. Benchmark datasets**

### Why?

**Benchmark datasets** are prebuilt, standardized datasets designed to evaluate model behavior against known criteria. They require less preparation than collecting, cleaning, labeling, and curating company-specific data.

For evaluating **bias, fairness, and discrimination**, benchmark datasets provide a convenient and repeatable way to test model outputs with minimal administrative effort.

- **A. User-generated content** → Requires collection, filtering, labeling, and privacy considerations.
- **B. Moderation logs** → Useful operational data, but usually requires additional processing and labeling before evaluation.
- **C. Content moderation guidelines** → Define policies and rules, but are not themselves an evaluation dataset.
- **D. Benchmark datasets** → Correct. Provide ready-to-use evaluation data with the **least administrative overhead**.

### Exam Focus

**Evaluate model bias/fairness with minimal setup → Benchmark datasets**

Key associations:

- **Benchmark dataset** → Standardized model evaluation
- **Bias/fairness testing** → Check for discriminatory or uneven outcomes
- **Custom operational data** → More preparation and administrative effort
- **Guidelines/policies** → Define expected behavior, not test data

Memory aid:

**“Least effort for standardized evaluation” → Benchmark dataset**

## Question 48

### Original Question

A company wants to use a **pre-trained generative AI model** to generate content for its marketing campaigns. The company needs to ensure that the generated content aligns with the company's **brand voice and messaging requirements**.

Which solution meets these requirements?

### Choices

A. Optimize the model's architecture and hyperparameters to improve the model's overall performance.  
B. Increase the model's complexity by adding more layers to the model's architecture.  
C. Create effective prompts that provide clear instructions and context to guide the model's generation.  
D. Select a large, diverse dataset to pre-train a new generative model.

### Correct Answer

**C. Create effective prompts that provide clear instructions and context to guide the model's generation.**

### Why?

**Prompt engineering** can guide a pre-trained generative AI model to produce content with a desired **tone, style, format, brand voice, and messaging**.

The prompt can explicitly describe the company's communication style and provide relevant context or examples.

- **A. Optimize architecture and hyperparameters** → Requires model-level changes and is unnecessary when the goal is primarily to control generated content style.
- **B. Add more layers** → Increases model complexity but does not ensure alignment with a specific brand voice.
- **C. Effective prompts** → Correct. Provides instructions and context that guide the model toward the desired tone and messaging.
- **D. Pre-train a new model** → Expensive and unnecessary when an existing pre-trained model can be guided through prompts.

### Exam Focus

**Control generative AI tone, style, brand voice, or output format → Prompt engineering**

Key associations:

- **Prompt engineering** → Guide tone, style, format, and behavior
- **Pre-training** → Build broad model knowledge from large datasets
- **Fine-tuning** → Adapt model behavior using task/domain-specific training data
- **Hyperparameters/model architecture** → Affect model training and capability, not simple brand-style control

Memory aid:

**“Make the output sound like our company” → Prompt engineering**

## Question 49

### Original Question

A loan company is building a **generative AI-based solution** to offer new applicants discounts based on specific business criteria. The company wants to build and use an AI model **responsibly** to minimize **bias** that could negatively affect some customers.

Which actions should the company take? **(Choose two.)**

### Choices

A. Detect imbalances or disparities in the data.  
B. Ensure that the model runs frequently.  
C. Evaluate the model's behavior so that the company can provide transparency to stakeholders.  
D. Use the Recall-Oriented Understudy for Gisting Evaluation (ROUGE) technique to ensure that the model is 100% accurate.  
E. Ensure that the model's inference time is within the accepted limits.

### Correct Answer

**A. Detect imbalances or disparities in the data.**  
**C. Evaluate the model's behavior so that the company can provide transparency to stakeholders.**

### Why?

Responsible AI includes **fairness, transparency, and explainability**. To reduce harmful bias, the company should first examine the data for **imbalances or disparities** that could cause unequal outcomes.

The company should also evaluate and document the model's behavior so stakeholders can understand how the system operates and whether it produces fair outcomes.

- **A. Detect data imbalances/disparities** → Correct. Helps identify potential sources of **bias** before or during model development.
- **B. Run the model frequently** → Frequency of execution does not reduce bias.
- **C. Evaluate model behavior for transparency** → Correct. Supports **responsible AI, explainability, and stakeholder trust**.
- **D. ROUGE** → Primarily evaluates similarity between generated and reference text, especially for summarization. It does not guarantee 100% accuracy or fairness.
- **E. Inference time** → Measures performance and latency, not bias or responsible AI.

### Exam Focus

**Responsible AI + minimize bias → Check data fairness + evaluate model behavior**

Key associations:

- **Bias mitigation** → Detect imbalances/disparities in data
- **Transparency** → Evaluate and explain model behavior
- **ROUGE** → Text generation/summarization evaluation metric
- **Inference latency** → Performance metric, not fairness

Memory aid:

**Responsible AI = Fair data + Transparent model behavior**

## Question 50

### Original Question

A company is using an **Amazon Bedrock base model** to summarize documents for an internal use case. The company trained a **custom model** to improve the summarization quality.

Which action must the company take to use the custom model through Amazon Bedrock?

### Choices

A. Purchase Provisioned Throughput for the custom model.  
B. Deploy the custom model in an Amazon SageMaker endpoint for real-time inference.  
C. Register the model with the Amazon SageMaker Model Registry.  
D. Grant access to the custom model in Amazon Bedrock.

### Correct Answer

**A. Purchase Provisioned Throughput for the custom model.**

### Why?

For the exam scenario, an **Amazon Bedrock custom model** created from a base model requires **Provisioned Throughput** to provide the compute capacity needed to invoke the customized model. AWS documentation for Bedrock customized models identifies Provisioned Throughput as an inference option for custom models.

- **A. Provisioned Throughput** → Correct. Provides dedicated capacity for invoking the custom Bedrock model.
- **B. SageMaker endpoint** → Not required when the model is being used through **Amazon Bedrock**
- **C. SageMaker Model Registry** → Used to catalog, version, and manage ML models in SageMaker, not to invoke a Bedrock custom model
- **D. Grant model access** → Model access permissions apply to available foundation models, but this alone does not provide inference capacity for the customized model.

### Exam Focus

**Use a customized Amazon Bedrock model → Provisioned Throughput**

Quick distinction:
- **On-Demand** → Common for base FM inference with usage-based pricing
- **Provisioned Throughput** → Dedicated model capacity; important exam association for **custom Bedrock models**
- **SageMaker endpoint** → Host SageMaker models for inference
- **Model Registry** → Manage/version ML models

Memory aid:
**Bedrock custom model → Provisioned Throughput**

## Question 51

### Original Question

A company needs to choose a model from **Amazon Bedrock** to use internally. The company must identify a model that generates responses in a **style that the company's employees prefer**.

What should the company do to meet these requirements?

### Choices

A. Evaluate the models by using built-in prompt datasets.  
B. Evaluate the models by using a human workforce and custom prompt datasets.  
C. Use public model leaderboards to identify the model.  
D. Use the model `InvocationLatency` runtime metrics in Amazon CloudWatch when trying models.

### Correct Answer

**B. Evaluate the models by using a human workforce and custom prompt datasets.**

### Why?

The requirement is **subjective response preference**, especially style. The best evaluation method is to use **human evaluators** with **custom prompts that reflect the company's real use cases**.

- **A. Built-in prompt datasets** → Useful for standardized evaluation, but may not reflect the company's specific employee preferences.
- **B. Human workforce + custom prompt datasets** → Correct. Human reviewers can judge qualities such as **tone, style, usefulness, and preference** on company-specific examples.
- **C. Public model leaderboards** → Show general benchmark results, not whether employees prefer a model's response style.
- **D.** `**InvocationLatency**` → Measures inference latency, not response quality or style preference.

### Exam Focus

**Subjective model quality such as tone/style/preference → Human evaluation**

Key associations:

- **Human evaluation** → Style, tone, helpfulness, preference
- **Custom prompt datasets** → Evaluate real company use cases
- **Built-in datasets** → Standardized evaluation
- **CloudWatch** `**InvocationLatency**` → Runtime performance, not response quality

Memory aid:

**“Which model do people prefer?” → Human evaluation + custom prompts**

## Question 52

### Original Question

A student at a university is **copying content from generative AI to write essays**.

Which challenge of responsible generative AI does this scenario represent?

### Choices

A. Toxicity  
B. Hallucinations  
C. Plagiarism  
D. Privacy

### Correct Answer

**C. Plagiarism**

### Why?

**Plagiarism** occurs when someone presents content created by another source as their own without proper attribution.

Copying generative AI output directly into an essay can create academic integrity and attribution concerns.

- **A. Toxicity** → Harmful, offensive, or abusive generated content.
- **B. Hallucinations** → When a model generates false or fabricated information.
- **C. Plagiarism** → Correct. Involves using generated content without appropriate attribution or original authorship.
- **D. Privacy** → Concerns exposure or misuse of personal or sensitive information.

### Exam Focus

**Copying AI-generated content as your own → Plagiarism**

Quick distinction:

- **Plagiarism** → Improper attribution / passing off content as your own
- **Hallucination** → False or invented information
- **Toxicity** → Harmful or offensive content
- **Privacy** → Exposure or misuse of sensitive data

Memory aid:

**“AI wrote it, student submitted it as their own” → Plagiarism**

## Question 53

### Original Question

A company needs to build its own **large language model (LLM)** based on only the company's private data. The company is concerned about the **environmental effect of the training process**.

Which Amazon EC2 instance type has the **LEAST environmental effect** when training LLMs?

### Choices

A. Amazon EC2 C series  
B. Amazon EC2 G series  
C. Amazon EC2 P series  
D. Amazon EC2 Trn series

### Correct Answer

**D. Amazon EC2 Trn series**

### Why?

**Amazon EC2 Trn instances** are powered by **AWS Trainium**, which is purpose-built for **high-performance deep learning and generative AI model training**.

Because Trainium is optimized specifically for ML training, it provides improved **performance per watt**, helping reduce the energy consumption and environmental impact of training large models.

- **A. C series** → Compute-optimized instances for general compute-intensive workloads, not specifically optimized for LLM training.
- **B. G series** → GPU-based instances commonly used for graphics and ML inference/training, but not as specifically optimized for large-scale training as Trainium.
- **C. P series** → GPU instances designed for high-performance ML training, but Trainium instances are purpose-built by AWS for efficient deep learning training.
- **D. Trn series** → Correct. Designed specifically for **energy-efficient, high-performance ML/LLM training**.

### Exam Focus

**Train large ML/LLM models efficiently → EC2 Trn instances / AWS Trainium**

Quick distinction:

- **Trn / Trainium** → ML model **training**
- **Inf / Inferentia** → ML **inference**
- **P series** → GPU-based high-performance ML/HPC workloads
- **G series** → Graphics and GPU-based ML workloads
- **C series** → General compute-intensive workloads

Memory aid:

**Trainium = Training**  
**Inferentia = Inference**

Key exam association:

**LLM training + energy efficiency / lower environmental impact → AWS Trainium (EC2 Trn)**

## Question 54

### Original Question

A company wants to build an interactive application for children that generates new stories based on classic stories. The company wants to use **Amazon Bedrock** and needs to ensure that the **results and topics are appropriate for children**.

Which AWS service or feature will meet these requirements?

### Choices

A. Amazon Rekognition  
B. Amazon Bedrock playgrounds  
C. Guardrails for Amazon Bedrock  
D. Agents for Amazon Bedrock

### Correct Answer

**C. Guardrails for Amazon Bedrock**

### Why?

**Guardrails for Amazon Bedrock** help control foundation model inputs and outputs by applying safety policies and content restrictions.

They can be used to help block or filter **inappropriate topics and harmful content**, which is especially important for child-facing applications.

- **A. Amazon Rekognition** → Analyzes images and videos; it is not used to control Bedrock-generated text content.
- **B. Amazon Bedrock playgrounds** → Used to experiment with models and prompts, not enforce production safety policies.
- **C. Guardrails for Amazon Bedrock** → Correct. Helps enforce **content safety, topic restrictions, and responsible AI controls**.
- **D. Agents for Amazon Bedrock** → Orchestrate tasks and actions across systems; they are not primarily a content-safety mechanism.

### Exam Focus

**Control harmful/inappropriate FM inputs and outputs → Guardrails for Amazon Bedrock**

Key associations:

- **Guardrails** → Content filtering, denied topics, safety controls
- **Playgrounds** → Test and experiment with prompts/models
- **Agents** → Perform multi-step tasks and invoke actions
- **Rekognition** → Image/video analysis

Memory aid:

**“Keep Bedrock responses safe and appropriate” → Guardrails**

## Question 55

### Original Question

A company is building an application that needs to **generate synthetic data based on existing data**.

Which type of model can the company use to meet this requirement?

### Choices

A. Generative adversarial network (GAN)  
B. XGBoost  
C. Residual neural network  
D. WaveNet

### Correct Answer

**A. Generative adversarial network (GAN)**

### Why?

A **Generative Adversarial Network (GAN)** is a generative model that learns the distribution and patterns of existing training data and then creates **new synthetic samples** that resemble the original data.

GANs consist of two competing neural networks:
- **Generator** → Creates synthetic data
- **Discriminator** → Tries to distinguish real data from generated data

Through this competition, the generator learns to produce increasingly realistic synthetic data.
- **A. GAN** → Correct. Commonly used for **synthetic data generation**, especially images and other complex data
- **B. XGBoost** → Primarily used for supervised **classification and regression**
- **C. Residual neural network (ResNet)** → Primarily used for **image recognition and computer vision**
- **D. WaveNet** → Primarily designed for generating **audio waveforms and speech**

### Exam Focus

**Generate synthetic data resembling existing data → Generative Adversarial Network (GAN)**

Key associations:

- **GAN** → Synthetic data / realistic generated samples
- **Generator** → Creates fake/synthetic samples
- **Discriminator** → Distinguishes real from generated samples
- **XGBoost** → Classification/regression
- **ResNet** → Computer vision/image recognition
- **WaveNet** → Audio generation

Memory aid:

**GAN = Generator vs. Discriminator → Realistic synthetic data**

## Question 56

### Original Question

A digital devices company wants to **predict customer demand for memory hardware**. The company does not have **coding experience or knowledge of ML algorithms** and needs to develop a **data-driven predictive model**.

The company needs to perform analysis on **internal data and external data**.

Which solution will meet these requirements?

### Choices

A. Store the data in Amazon S3. Create ML models and demand forecast predictions by using Amazon SageMaker built-in algorithms that use the data from Amazon S3.  
B. Import the data into Amazon SageMaker Data Wrangler. Create ML models and demand forecast predictions by using SageMaker built-in algorithms.  
C. Import the data into Amazon SageMaker Data Wrangler. Build ML models and demand forecast predictions by using an Amazon Personalize Trending-Now recipe.  
D. Import the data into Amazon SageMaker Canvas. Build ML models and demand forecast predictions by selecting the values in the data from SageMaker Canvas.

### Correct Answer

**D. Import the data into Amazon SageMaker Canvas. Build ML models and demand forecast predictions by selecting the values in the data from SageMaker Canvas.**

### Why?

**Amazon SageMaker Canvas** provides a **no-code visual interface** that allows users without ML or programming expertise to build machine learning models and generate predictions.

It is well suited for business users who need to combine data, analyze it, and create predictive models such as **demand forecasts** without writing code.
- **A. SageMaker built-in algorithms** → Can build ML models, but generally require more ML knowledge and development effort.
- **B. SageMaker Data Wrangler** → Primarily used to **prepare, clean, and transform data;** it is not the main no-code tool for building predictive models.
- **C. Amazon Personalize Trending-Now** → Used for **recommendation systems** and identifying trending items, not general demand forecasting
- **D. SageMaker Canvas** → Correct. Provides **no-code ML** for building predictive models and forecasts.

### Exam Focus

**No coding or ML expertise + need to build predictive models → Amazon SageMaker Canvas**

Quick distinction:
- **SageMaker Canvas** → No-code ML model building and predictions
- **SageMaker Data Wrangler** → Data preparation and transformation
- **SageMaker built-in algorithms** → Prebuilt ML algorithms for developers/data scientists
- **Amazon Personalize** → Personalized recommendations

Memory aid:
**Business user + no code + predictive ML → SageMaker Canvas**

## Question 57

### Original Question

A company has installed a security camera. The company uses an **ML model** to evaluate the security camera footage for potential thefts. The company discovers that the model **disproportionately flags people who are members of a specific ethnic group**.

Which type of bias is affecting the model output?

### Choices

A. Measurement bias  
B. Sampling bias  
C. Observer bias  
D. Confirmation bias

### Correct Answer

**B. Sampling bias**

### Why?

**Sampling bias** occurs when the training data is **not representative of the population** that the model will encounter in the real world.

If certain ethnic groups are overrepresented, underrepresented, or represented in an unbalanced way in the training data, the model can learn patterns that produce **disproportionate outcomes** for those groups.

- **A. Measurement bias** → Occurs when data is collected or measured inaccurately or inconsistently.
- **B. Sampling bias** → Correct. Results from **unrepresentative or imbalanced training samples**.
- **C. Observer bias** → Occurs when a person's expectations or judgments influence observations or labels.
- **D. Confirmation bias** → Occurs when people favor evidence that supports their existing beliefs.

### Exam Focus

**Model performs unfairly for a demographic group because of unrepresentative training data → Sampling bias**

Quick distinction:

- **Sampling bias** → Dataset does not represent the real population
- **Measurement bias** → Data collection/measurement method introduces systematic error
- **Observer bias** → Human observer influences labels or observations
- **Confirmation bias** → Preference for information that confirms existing beliefs

Memory aid:

**“Wrong representation in the sample” → Sampling bias**

## Question 58

### Original Question

A company is building a **customer service chatbot**. The company wants the chatbot to **improve its responses by learning from past interactions and online resources**.

Which AI learning strategy provides this **self-improvement capability**?

### Choices

A. Supervised learning with a manually curated dataset of good responses and bad responses  
B. Reinforcement learning with rewards for positive customer feedback  
C. Unsupervised learning to find clusters of similar customer inquiries  
D. Supervised learning with a continuously updated FAQ database

### Correct Answer

**B. Reinforcement learning with rewards for positive customer feedback**

### Why?

**Reinforcement learning (RL)** allows a model or agent to improve its behavior based on **rewards and feedback** from previous actions.

In this scenario, positive customer feedback can act as a **reward signal**, encouraging the chatbot to learn which responses are more effective over time.

- **A. Supervised learning with curated responses** → Requires labeled examples and retraining; it does not inherently learn through ongoing rewards.
- **B. Reinforcement learning** → Correct. Learns from **actions, outcomes, and reward signals** to improve future behavior.
- **C. Unsupervised learning** → Finds patterns or clusters in unlabeled data but does not directly optimize responses from feedback.
- **D. Supervised learning with an updated FAQ** → Updating the knowledge source can improve available information, but it is not a self-improving learning strategy based on rewards.

### Exam Focus

**Learn from interactions + feedback/rewards + improve behavior → Reinforcement learning**

Quick distinction:

- **Supervised learning** → Learn from labeled examples
- **Unsupervised learning** → Discover patterns in unlabeled data
- **Reinforcement learning** → Learn from **rewards and consequences**
- **RLHF** → Reinforcement learning using **human feedback** as part of model alignment

Memory aid:

**Action → Feedback/Reward → Improve future action = Reinforcement learning**

## Question 59

### Original Question

An AI practitioner has built a **deep learning model** to classify the types of materials in images. The AI practitioner now wants to **measure the model performance**.

Which metric will help the AI practitioner evaluate the performance of the model?

### Choices

A. Confusion matrix  
B. Correlation matrix  
C. R² score  
D. Mean squared error (MSE)

### Correct Answer

**A. Confusion matrix**

### Why?

A **confusion matrix** evaluates a **classification model** by comparing predicted classes with actual classes.

It shows how many predictions were:
- Correct classified
- Misclassified
- Assigned to each class

For multiclass image classification, it helps identify **which material classes the model predicts correctly and which classes it confuses**.

- **A. Confusion matrix** → Correct. Used to evaluate **classification performance**
- **B. Correlation matrix** → Shows relationships between numerical variables or features, not classification performance
- **C. R² score** → Used primarily for **regression**
- **D. MSE** → Measures prediction error for **regression** problems

### Exam Focus

**Classification model performance → Confusion matrix**

Quick distinction:
- **Confusion matrix** → Classification results
- R² → Regression goodness of fit
- **MSE** → Regression prediction error
- **Correlation matrix** → Relationships between variables/features

Memory aid:
**Classification + actual vs prediction classes → Confusion matrix**

## Question 60

### Original Question

A company has built a chatbot that can respond to **natural language questions with images**. The company wants to ensure that the chatbot does **not return inappropriate or unwanted images**.

Which solution will meet these requirements?

### Choices

A. Implement moderation APIs.  
B. Retrain the model with a general public dataset.  
C. Perform model validation.  
D. Automate user feedback integration.

### Correct Answer

**A. Implement moderation APIs.**

### Why?

**Moderation APIs** can inspect generated content and detect or block **unsafe, inappropriate, or unwanted images** before they are returned to users.

This provides a direct content-safety control for a generative AI application.

- **A. Moderation APIs** → Correct. Filter or block inappropriate generated content.
- **B. Retrain with a public dataset** → Does not guarantee safe outputs and may introduce additional unwanted content
- **C. Model validation** → Helps assess model quality and behavior, but does not actively filter every generated image
- **D. User feedback integration** → Can improve the system over time, but does not immediately prevent inappropriate outputs

### Exam Focus

**Prevent unsafe/inappropriate generated content → Content moderation / moderation APIs**

Key associations:

- **Moderation** → Detect and block unsafe content
- **Model validation** → Evaluate model quality before or during deployment
- **User feedback** → Improve future behavior
- **Retraining** → Modify model behavior, but not a direct real-time safety filter

Memory aid:

**“Block inappropriate output before the user sees it” → Moderation**

## Question 61

### Original Question

An AI practitioner is using an **Amazon Bedrock base model** to summarize session chats from the customer service department. The AI practitioner wants to **store invocation logs to monitor model input and output data**.

Which strategy should the AI practitioner use?

### Choices

A. Configure AWS CloudTrail as the logs destination for the model.  
B. Enable invocation logging in Amazon Bedrock.  
C. Configure AWS Audit Manager as the logs destination for the model.  
D. Configure model invocation logging in Amazon EventBridge.

### Correct Answer

**B. Enable invocation logging in Amazon Bedrock.**

### Why?

**Amazon Bedrock model invocation logging** is specifically designed to capture information about model requests and responses, including **input and output data**, for monitoring and auditing purposes.

- **A. AWS CloudTrail** → Records AWS API activity, such as who called an API and when, but it is not the primary feature for storing Bedrock model input/output payloads.
- **B. Bedrock invocation logging** → Correct. Captures model invocation details for monitoring and analysis.
- **C. AWS Audit Manager** → Helps collect evidence for compliance assessments, not model invocation payload logging.
- **D. Amazon EventBridge** → Routes events between services but is not the Bedrock feature used to log model inputs and outputs.

### Exam Focus

**Monitor and store Amazon Bedrock model inputs/outputs → Enable model invocation logging**

Quick distinction:

- **Bedrock invocation logging** → Model request/response data
- **CloudTrail** → AWS API activity and user actions
- **Audit Manager** → Compliance evidence
- **EventBridge** → Event routing

Memory aid:
**“What went into and came out of the FM?” → Bedrock invocation logging**

## Question 62

### Original Question

A company is building an **ML model to analyze archived data**. The company must perform inference on **large datasets that are multiple GBs in size**. The company does **not need to access the model predictions immediately**.

Which Amazon SageMaker inference option will meet these requirements?

### Choices

A. Batch transform  
B. Real-time inference  
C. Serverless inference  
D. Asynchronous inference

### Correct Answer

**A. Batch transform**

### Why?

**Amazon SageMaker Batch Transform** is designed for **offline inference on large datasets** when predictions are **not required immediately**.

It processes data in batches without requiring a persistent inference endpoint.

- **A. Batch transform** → Correct. Best for **large offline datasets** and non-urgent predictions.
- **B. Real-time inference** → Best for **low-latency, synchronous** predictions.
- **C. Serverless inference** → Best for intermittent or unpredictable online inference workloads without managing servers.
- **D. Asynchronous inference** → Best for **large individual payloads or long-running inference requests** when results are needed asynchronously, but still on a request-by-request basis.

### Exam Focus

**Large dataset + offline processing + no immediate prediction needed → SageMaker Batch Transform**

Quick distinction:

- **Batch Transform** → Large offline datasets
- **Real-time Inference** → Immediate, low-latency predictions
- **Serverless Inference** → Intermittent/unpredictable online traffic
- **Asynchronous Inference** → Large payloads / long processing per request

Memory aid:

**“Process a big dataset later” → Batch Transform**

## Question 63

### Original Question

Which term describes the **numerical representations of real-world objects and concepts** that AI and natural language processing (NLP) models use to improve understanding of textual information?

### Choices

A. Embeddings  
B. Tokens  
C. Models  
D. Binaries

### Correct Answer

**A. Embeddings**

### Why?

**Embeddings** are numerical vector representations of data such as **words, sentences, images, or concepts**. They capture semantic meaning so that similar items are positioned close together in vector space.

- **A. Embeddings** → Correct. Numerical representations used for semantic meaning and similarity.
- **B. Tokens** → Individual units of text, such as words, subwords, or characters, that a model processes.
- **C. Models** → Algorithms or systems trained to perform AI tasks; they are not numerical representations of individual concepts.
- **D. Binaries** → General binary data representation and not the NLP concept described.

### Exam Focus

**Numerical vector representation of words, text, images, or concepts → Embeddings**

Quick distinction:

- **Tokens** → Pieces of input text
- **Embeddings** → Numerical vectors representing semantic meaning
- **Vector search** → Compares embeddings to find similar content

Memory aid:

**Token = piece of text → Embedding = meaning represented as numbers**

## Question 64

### Original Question

A research company implemented a chatbot by using a **foundation model (FM) from Amazon Bedrock**. The chatbot searches for answers to questions from a large database of research papers.

After multiple prompt engineering attempts, the company notices that the FM is performing poorly because of the **complex scientific terms** in the research papers.

How can the company improve the performance of the chatbot?

### Choices

A. Use few-shot prompting to define how the FM can answer the questions.  
B. Use domain adaptation fine-tuning to adapt the FM to complex scientific terms.  
C. Change the FM inference parameters.  
D. Clean the research paper data to remove complex scientific terms.

### Correct Answer

**B. Use domain adaptation fine-tuning to adapt the FM to complex scientific terms.**

### Why?

**Domain adaptation fine-tuning** adapts a foundation model to the terminology, language patterns, and knowledge style of a specific domain.

Because prompt engineering has already been tried and the problem is the model's poor understanding of **specialized scientific terminology**, fine-tuning on domain-specific research data is the appropriate solution.

- **A. Few-shot prompting** → Provides examples in the prompt, but prompt engineering has already been insufficient for the specialized terminology.
- **B. Domain adaptation fine-tuning** → Correct. Helps the FM better understand **domain-specific vocabulary and concepts**.
- **C. Change inference parameters** → Parameters such as temperature or Top P affect generation behavior, not the model's understanding of scientific terminology.
- **D. Remove complex terms** → Would remove valuable domain information and reduce the usefulness of the research data.

### Exam Focus

**FM struggles with specialized domain terminology → Domain adaptation fine-tuning**

Quick distinction:

- **Prompt engineering / few-shot** → Guide model behavior using instructions and examples
- **Domain adaptation fine-tuning** → Teach the model specialized terminology and domain patterns
- **Inference parameters** → Control randomness and generation behavior
- **Data cleaning** → Improve data quality, not remove essential domain vocabulary

Memory aid:

**“Model does not understand the domain” → Domain adaptation fine-tuning**

## Question 65

### Original Question

A company wants to use a **large language model (LLM) on Amazon Bedrock** for sentiment analysis. The company needs the LLM to produce **more consistent responses to the same input prompt**.

Which adjustment to an inference parameter should the company make to meet these requirements?

### Choices

A. Decrease the temperature value.  
B. Increase the temperature value.  
C. Decrease the length of output tokens.  
D. Increase the maximum generation length.

### Correct Answer

**A. Decrease the temperature value.**

### Why?

**Temperature** controls the randomness of an LLM's output.

A **lower temperature** makes the model choose more probable tokens, producing responses that are **more deterministic and consistent** for the same input.

- **A. Decrease temperature** → Correct. Produces more predictable and consistent outputs.
- **B. Increase temperature** → Increases randomness and creativity, making responses less consistent.
- **C. Decrease output tokens** → Limits response length, not randomness.
- **D. Increase maximum generation length** → Allows longer responses, but does not improve consistency.

### Exam Focus

**Need consistent / deterministic LLM responses → Lower temperature**

Quick distinction:

- **Low temperature** → More predictable, deterministic
- **High temperature** → More random, creative
- **Max tokens** → Controls response length

Memory aid:

**Lower temperature = Lower randomness**

## Question 66

### Original Question

A company wants to develop a **large language model (LLM) application by using Amazon Bedrock** and customer data that is uploaded to **Amazon S3**. The company's security policy states that each team can access data for **only the team's own customers**.

Which solution will meet these requirements?

### Choices

A. Create an Amazon Bedrock custom service role for each team that has access to only the team's customer data.  
B. Create a custom service role that has Amazon S3 access. Ask teams to specify the customer name on each Amazon Bedrock request.  
C. Redact personal data in Amazon S3. Update the S3 bucket policy to allow team access to customer data.  
D. Create one Amazon Bedrock role that has full Amazon S3 access. Create IAM roles for each team that have access to only each team's customer folders.

### Correct Answer

**A. Create an Amazon Bedrock custom service role for each team that has access to only the team's customer data.**

### Why?

The company should follow the **principle of least privilege** by giving each Amazon Bedrock service role access only to the S3 data required by that specific team.

- **A. Separate Bedrock service role per team** → Correct. Restricts each team's Bedrock access to only its own customer data.
- **B. Specify customer name in requests** → Does not enforce access control. Security must be enforced through **IAM permissions**, not user-provided prompt/request values.
- **C. Redact personal data** → May improve privacy, but does not enforce team-level authorization by itself.
- **D. One Bedrock role with full S3 access** → Violates **least privilege** because the Bedrock service role can access all customer data.

### Exam Focus

**Restrict Bedrock access to specific S3 data → Use IAM service roles with least-privilege permissions**

Key associations:

- **IAM role** → Controls AWS resource access
- **Least privilege** → Grant only the permissions required
- **Per-team access boundaries** → Separate roles/policies for each team's data
- **Prompt/request values** → Do not replace IAM authorization

Memory aid:

**“Each team can access only its own data” → Separate least-privilege IAM roles**

## Question 67

### Original Question

A medical company deployed a **disease detection model on Amazon Bedrock**. To comply with privacy policies, the company wants to prevent the model from including **personal patient information** in its responses. The company also wants to receive **notifications when policy violations occur**.

Which solution meets these requirements?

### Choices

A. Use Amazon Macie to scan the model's output for sensitive data and set up alerts for potential violations.  
B. Configure AWS CloudTrail to monitor the model's responses and create alerts for any detected personal information.  
C. Use Guardrails for Amazon Bedrock to filter content. Set up Amazon CloudWatch alarms for notification of policy violations.  
D. Implement Amazon SageMaker Model Monitor to detect data drift and receive alerts when model quality degrades.

### Correct Answer

**C. Use Guardrails for Amazon Bedrock to filter content. Set up Amazon CloudWatch alarms for notification of policy violations.**

### Why?

**Guardrails for Amazon Bedrock** can enforce content policies on model inputs and outputs, including helping detect and filter **sensitive information such as personally identifiable information (PII)**.

**Amazon CloudWatch** can then be used for monitoring and alarms so the company can receive notifications when relevant policy violations or operational thresholds occur.

- **A. Amazon Macie** → Primarily discovers and protects sensitive data stored in **Amazon S3**; it is not the main tool for filtering Bedrock responses.
- **B. AWS CloudTrail** → Records AWS API activity for auditing, but does not directly filter personal information from model responses.
- **C. Bedrock Guardrails + CloudWatch** → Correct. Guardrails enforce response safety/privacy controls, while CloudWatch provides monitoring and alerting.
- **D. SageMaker Model Monitor** → Detects issues such as **data drift and model quality degradation**, not sensitive-information leakage from Bedrock responses.

### Exam Focus

**Prevent sensitive/PII data in Bedrock responses → Guardrails for Amazon Bedrock**

**Monitor and alert on violations → Amazon CloudWatch**

Quick distinction:

- **Bedrock Guardrails** → Content filtering, denied topics, PII/sensitive information controls
- **CloudWatch** → Metrics, monitoring, alarms
- **CloudTrail** → AWS API activity/audit history
- **Macie** → Sensitive-data discovery in S3
- **SageMaker Model Monitor** → Model/data quality monitoring

Memory aid:

**Filter unsafe or sensitive Bedrock output → Guardrails**  
**Need alerts → CloudWatch**

## Question 68

### Original Question

A company manually reviews all submitted resumes in **PDF format**. As the company grows, the company expects the volume of resumes to exceed the company's review capacity. The company needs an automated system to **convert the PDF resumes into plain text format** for additional processing.

Which AWS service meets this requirement?

### Choices

A. Amazon Textract  
B. Amazon Personalize  
C. Amazon Lex  
D. Amazon Transcribe

### Correct Answer

**A. Amazon Textract**

### Why?

**Amazon Textract** automatically extracts **text, handwriting, tables, and structured data from scanned documents and PDFs**.

It is the appropriate service for converting resume PDFs into machine-readable text for downstream processing.

- **A. Amazon Textract** → Correct. Extracts text and structured information from documents and PDFs.
- **B. Amazon Personalize** → Builds personalized recommendation systems.
- **C. Amazon Lex** → Builds conversational chatbots and voice interfaces.
- **D. Amazon Transcribe** → Converts **speech/audio to text**, not PDF documents.

### Exam Focus

**Extract text from PDFs, scans, forms, or documents → Amazon Textract**

Quick distinction:

- **Amazon Textract** → Document/PDF → text and structured data
- **Amazon Transcribe** → Audio/speech → text
- **Amazon Lex** → Conversational bots
- **Amazon Personalize** → Recommendations

Memory aid:

**Document → Text = Textract**  
**Speech → Text = Transcribe**

## Question 69

### Original Question

An education provider is building a question and answer application that uses a **generative AI model** to explain complex concepts. The education provider wants to automatically **change the style of the model response depending on who is asking the question**. The education provider will give the model the **age range of the user** who has asked the question.

Which solution meets these requirements with the **LEAST implementation effort**?

### Choices

A. Fine-tune the model by using additional training data that is representative of the various age ranges that the application will support.  
B. Add a role description to the prompt context that instructs the model of the age range that the response should target.  
C. Use chain-of-thought reasoning to deduce the correct style and complexity for a response suitable for that user.  
D. Summarize the response text depending on the age of the user so that younger users receive shorter responses.

### Correct Answer

**B. Add a role description to the prompt context that instructs the model of the age range that the response should target.**

### Why?

**Prompt engineering** can dynamically control an LLM's **tone, complexity, vocabulary, and style** without retraining the model.

By including the user's age range in the prompt and instructing the model to tailor its response appropriately, the application can adapt responses with very little implementation effort.

- **A. Fine-tuning** → Could customize model behavior, but requires additional training data, time, and cost. It is unnecessary for a simple dynamic style requirement.
- **B. Role description in the prompt** → Correct. Provides the model with the target audience and desired response style with minimal implementation effort.
- **C. Chain-of-thought reasoning** → Used to improve reasoning on complex tasks, not primarily to control audience-specific tone or complexity.
- **D. Summarization** → Shortens responses but does not necessarily adjust vocabulary, explanation depth, or style for different age groups.

### Exam Focus

**Dynamically change tone/style/complexity based on user context → Prompt engineering**

Key associations:

- **Role prompting** → Tell the model who it should act as or who the target audience is
- **Prompt context** → Supply dynamic information such as age, role, or expertise
- **Fine-tuning** → More effort; use when deeper model adaptation is needed
- **Chain-of-thought** → Reasoning strategy, not style customization

Memory aid:

**“Explain this differently for different users” → Put the audience details in the prompt**

## Question 70

### Original Question

Which strategy evaluates the **accuracy of a foundation model (FM)** that is used in **image classification** tasks?

### Choices

A. Calculate the total cost of resources used by the model.  
B. Measure the model's accuracy against a predefined benchmark dataset.  
C. Count the number of layers in the neural network.  
D. Assess the color accuracy of images processed by the model.

### Correct Answer

**B. Measure the model's accuracy against a predefined benchmark dataset.**

### Why?

A **benchmark dataset** provides known, labeled examples that can be used to compare the model's predictions with the correct answers.

For an image classification task, the model can be evaluated by measuring how often it correctly classifies images in the benchmark dataset.

- **A. Resource cost** → Measures operational cost, not model accuracy.
- **B. Benchmark dataset** → Correct. Provides a standardized way to measure classification performance.
- **C. Number of neural network layers** → Describes model architecture, not prediction quality.
- **D. Color accuracy** → Not a general metric for image classification performance.

### Exam Focus

**Evaluate model accuracy → Compare predictions against a labeled benchmark dataset**

Key associations:

- **Benchmark dataset** → Standardized model evaluation
- **Accuracy** → Proportion of correct classifications
- **Architecture size/layers** → Model design, not evaluation
- **Cost metrics** → Operational efficiency, not predictive accuracy

Memory aid:

**Known answers + model predictions → Measure accuracy**

## Question 71

### Original Question

An accounting firm wants to implement a **large language model (LLM)** to automate document processing. The firm must proceed **responsibly to avoid potential harms**.

What should the firm do when developing and deploying the LLM? **(Choose two.)**

### Choices

A. Include fairness metrics for model evaluation.  
B. Adjust the temperature parameter of the model.  
C. Modify the training data to mitigate bias.  
D. Avoid overfitting on the training data.  
E. Apply prompt engineering techniques.

### Correct Answer

**A. Include fairness metrics for model evaluation.**  
**C. Modify the training data to mitigate bias.**

### Why?

Responsible AI focuses on areas such as **fairness, bias mitigation, transparency, privacy, and reducing harmful outcomes**.

- **A. Fairness metrics** → Correct. Helps measure whether the model produces unfair or discriminatory outcomes across different groups.
- **B. Adjust temperature** → Controls output randomness and creativity, not fairness or bias.
- **C. Modify training data to mitigate bias** → Correct. Improving the representation and balance of training data can reduce biased model behavior.
- **D. Avoid overfitting** → Important for model generalization, but it does not directly address responsible AI harms such as unfairness or discrimination.
- **E. Prompt engineering** → Helps guide model behavior and output format, but it is not the primary approach for addressing systemic bias in training data.

### Exam Focus

**Responsible AI + reduce unfair outcomes → Measure fairness + mitigate bias in the data**

Key associations:

- **Fairness metrics** → Detect unequal model outcomes
- **Bias mitigation** → Improve or rebalance training data
- **Temperature** → Randomness
- **Overfitting** → Generalization problem
- **Prompt engineering** → Guide model responses

Memory aid:

**Responsible AI = Measure fairness + Reduce bias**

## Question 72

### Original Question

A company is building an **ML model**. The company collected new data and analyzed the data by **creating a correlation matrix, calculating statistics, and visualizing the data**.

Which stage of the ML pipeline is the company currently in?

### Choices

A. Data pre-processing  
B. Feature engineering  
C. Exploratory data analysis  
D. Hyperparameter tuning

### Correct Answer

**C. Exploratory data analysis**

### Why?

**Exploratory Data Analysis (EDA)** is the stage where practitioners examine and understand a dataset before building the model.

Typical EDA activities include:

- Calculating **summary statistics**
- Creating **visualizations**
- Examining **correlations** between variables
- Identifying patterns, distributions, anomalies, and relationships
- **A. Data pre-processing** → Cleans and prepares data, such as handling missing values, duplicates, or formatting.
- **B. Feature engineering** → Creates, transforms, or selects variables that will be used as model inputs.
- **C. Exploratory data analysis** → Correct. Focuses on understanding the data through statistics and visualization.
- **D. Hyperparameter tuning** → Adjusts model configuration values after model development begins.

### Exam Focus

**Statistics + visualizations + correlation analysis → Exploratory Data Analysis (EDA)**

Quick distinction:

- **EDA** → Understand and explore the data
- **Data preprocessing** → Clean and prepare the data
- **Feature engineering** → Create/transform useful model features
- **Hyperparameter tuning** → Optimize model configuration

Memory aid:
**Explore before you build → EDA**

## Question 73

### Original Question

A company has documents that are **missing some words** because of a database error. The company wants to build an ML model that can **suggest potential words to fill in the missing text**.

Which type of model meets this requirement?

### Choices

A. Topic modeling  
B. Clustering models  
C. Prescriptive ML models  
D. BERT-based models

### Correct Answer

**D. BERT-based models**

### Why?

**BERT (Bidirectional Encoder Representations from Transformers)** is well suited for **masked language modeling**, where the model predicts missing words by using the context on both sides of the missing text.

- **A. Topic modeling** → Identifies themes or topics in collections of documents.
- **B. Clustering models** → Groups similar data points without labels.
- **C. Prescriptive ML models** → Recommend actions or decisions, not missing words.
- **D. BERT-based models** → Correct. Can predict **masked or missing tokens** from surrounding context.

### Exam Focus

**Fill in missing words using surrounding context → BERT / masked language modeling**

Quick distinction:

- **BERT** → Understand context bidirectionally; strong for masked-word prediction
- **Topic modeling** → Discover document themes
- **Clustering** → Group similar items
- **Prescriptive ML** → Recommend actions

Memory aid:

**Missing word in a sentence → BERT predicts the mask**

## Question 74

### Original Question

A company wants to display the **total sales for its top-selling products across various retail locations in the past 12 months**.

Which AWS solution should the company use to **automate the generation of graphs**?

### Choices

A. Amazon Q in Amazon EC2  
B. Amazon Q Developer  
C. Amazon Q in Amazon QuickSight  
D. Amazon Q in AWS Chatbot

### Correct Answer

**C. Amazon Q in Amazon QuickSight**

### Why?

**Amazon Q in Amazon QuickSight** provides generative BI capabilities that let users ask questions about business data in **natural language** and automatically generate **visualizations, charts, and insights**.

This makes it appropriate for creating graphs of sales performance across products, locations, and time periods.

- **A. Amazon Q in Amazon EC2** → Not the AWS analytics/visualization solution for generating business graphs.
- **B. Amazon Q Developer** → Helps developers with coding, AWS development, and software tasks.
- **C. Amazon Q in Amazon QuickSight** → Correct. Generates **business intelligence insights and visualizations** from data.
- **D. Amazon Q in AWS Chatbot** → Not the primary service for business data visualization.

### Exam Focus

**Natural-language business analytics + automatically generate charts/graphs → Amazon Q in Amazon QuickSight**

Key associations:

- **Amazon QuickSight** → Business intelligence and dashboards
- **Amazon Q in QuickSight** → Natural-language questions, summaries, and visualizations
- **Amazon Q Developer** → Coding and software development assistance

Memory aid:

**“Ask business questions and create graphs” → Amazon Q in QuickSight**

## Question 75

### Original Question

A company is building a chatbot to improve user experience. The company is using a **large language model (LLM) from Amazon Bedrock** for **intent detection**. The company wants to use **few-shot learning** to improve intent detection accuracy.

Which additional data does the company need to meet these requirements?

### Choices

A. Pairs of chatbot responses and correct user intents  
B. Pairs of user messages and correct chatbot responses  
C. Pairs of user messages and correct user intents  
D. Pairs of user intents and correct chatbot responses

### Correct Answer

**C. Pairs of user messages and correct user intents**

### Why?

**Few-shot learning** provides the LLM with a small number of examples that demonstrate the desired input-to-output relationship.

For **intent detection**:

- **Input** → User message
- **Expected output** → Correct user intent

Providing several **user message → intent** examples helps the model learn how to classify new messages into the correct intent.

- **A. Chatbot responses + intents** → Does not show how user messages map to intents.
- **B. User messages + chatbot responses** → Useful for response generation, not intent classification.
- **C. User messages + correct intents** → Correct. Provides labeled examples for few-shot intent detection.
- **D. Intents + chatbot responses** → Shows how to respond to an intent, not how to detect the intent.

### Exam Focus

**Few-shot classification → Provide examples of input + correct label**

For intent detection:

**User message → Intent label**

Quick distinction:

- **Few-shot prompting** → Multiple labeled examples
- **Intent detection** → Classify what the user is trying to accomplish
- **Response generation** → Generate what the chatbot should say back

Memory aid:

**“Detect the intent” → Example user messages paired with their correct intents**

## Question 76

### Original Question

A company is using **few-shot prompting** on a base model that is hosted on **Amazon Bedrock**. The model currently uses **10 examples in the prompt**. The model is invoked **once daily** and is performing well. The company wants to **lower the monthly cost**.

Which solution will meet these requirements?

### Choices

A. Customize the model by using fine-tuning.  
B. Decrease the number of tokens in the prompt.  
C. Increase the number of tokens in the prompt.  
D. Use Provisioned Throughput.

### Correct Answer

**B. Decrease the number of tokens in the prompt.**

### Why?

Amazon Bedrock inference cost is influenced by the number of **input and output tokens** processed. Because the model already performs well, reducing unnecessary few-shot examples or shortening the prompt can lower the **input token count** and therefore reduce cost.

- **A. Fine-tuning** → Adds training/customization cost and is unnecessary for a model invoked only once per day.
- **B. Decrease prompt tokens** → Correct. Fewer input tokens generally reduce inference cost while preserving the existing model.
- **C. Increase prompt tokens** → Increases token usage and therefore cost.
- **D. Provisioned Throughput** → Better suited for predictable, sustained, high-volume usage and would not be cost-effective for one invocation per day.

### Exam Focus

**Reduce Bedrock inference cost → Reduce unnecessary input/output tokens**

Key associations:

- **More tokens** → Higher inference cost
- **Few-shot prompting** → Examples consume prompt tokens
- **Low/infrequent usage** → Prefer On-Demand rather than Provisioned Throughput
- **Provisioned Throughput** → Best for sustained or predictable high-volume workloads

Memory aid:

**“Model works well, but prompt is long” → Reduce prompt tokens**

## Question 77

### Original Question

An AI practitioner is using a **large language model (LLM)** to create content for marketing campaigns. The generated content **sounds plausible and factual but is incorrect**.

Which problem is the LLM having?

### Choices

A. Data leakage  
B. Hallucination  
C. Overfitting  
D. Underfitting

### Correct Answer

**B. Hallucination**

### Why?

A **hallucination** occurs when an LLM generates information that appears **confident, plausible, or factual** but is actually incorrect or fabricated.

- **A. Data leakage** → Information from training or evaluation data improperly appears where it should not, often compromising evaluation or privacy.
- **B. Hallucination** → Correct. The model produces convincing but false information.
- **C. Overfitting** → The model performs well on training data but poorly on unseen data.
- **D. Underfitting** → The model fails to learn the underlying patterns and performs poorly even on training data.

### Exam Focus

**Plausible-sounding but false LLM output → Hallucination**

Quick distinction:

- **Hallucination** → Fabricated or incorrect generated content
- **Overfitting** → Good on training data, poor on new data
- **Underfitting** → Poor learning/performance overall
- **Data leakage** → Improper exposure or contamination of data

Memory aid:

**“Sounds right, but is wrong” → Hallucination**

## Question 78

### Original Question

An AI practitioner trained a **custom model on Amazon Bedrock** by using a training dataset that contains **confidential data**. The AI practitioner wants to ensure that the custom model does **not generate inference responses based on confidential data**.

How should the AI practitioner prevent responses based on confidential data?

### Choices

A. Delete the custom model. Remove the confidential data from the training dataset. Retrain the custom model.  
B. Mask the confidential data in the inference responses by using dynamic data masking.  
C. Encrypt the confidential data in the inference responses by using Amazon SageMaker.  
D. Encrypt the confidential data in the custom model by using AWS Key Management Service (AWS KMS).

### Correct Answer

**A. Delete the custom model. Remove the confidential data from the training dataset. Retrain the custom model.**

### Why?

If confidential information was included in the **training dataset**, the model may have learned patterns or information from that data. The safest way to prevent the model from generating responses based on it is to **remove the confidential data and retrain the model**.

- **A. Remove data and retrain** → Correct. Prevents the new model from being trained on the confidential information.
- **B. Dynamic data masking** → Would only attempt to hide output after generation and does not remove confidential information learned during training.
- **C. Encrypt inference responses** → Encryption protects data in transit or storage; it does not prevent the model from generating confidential information.
- **D. AWS KMS encryption** → Protects model/data confidentiality at rest, but does not remove learned confidential information from model behavior.

### Exam Focus

**Sensitive/confidential data accidentally included in training → Remove the data and retrain the model**

Key associations:

- **Training data problem** → Fix the dataset and retrain
- **Encryption** → Protects data at rest/in transit
- **Masking** → Hides detected output but does not unlearn training data
- **Data removal + retraining** → Prevents future model learning from that confidential data

Memory aid:

**“Bad data went into training” → Remove it, then retrain**

## Question 79

### Original Question

A company has built a solution by using **generative AI**. The solution uses **large language models (LLMs)** to translate training manuals from English into other languages. The company wants to evaluate the **accuracy of the translations** by examining the generated text.

Which model evaluation strategy meets these requirements?

### Choices

A. Bilingual Evaluation Understudy (BLEU)  
B. Root mean squared error (RMSE)  
C. Recall-Oriented Understudy for Gisting Evaluation (ROUGE)  
D. F1 score

### Correct Answer

**A. Bilingual Evaluation Understudy (BLEU)**

### Why?

**BLEU** is an evaluation metric commonly used for **machine translation**. It compares generated translations with one or more reference translations by measuring overlap in words and phrases.

- **A. BLEU** → Correct. Designed primarily to evaluate **machine translation quality**.
- **B. RMSE** → Used for **regression** to measure numerical prediction error.
- **C. ROUGE** → Commonly used to evaluate **text summarization** by comparing generated text with reference summaries.
- **D. F1 score** → Primarily evaluates **classification** by balancing precision and recall.

### Exam Focus

**Evaluate machine translation → BLEU**

Quick distinction:

- **BLEU** → Translation quality
- **ROUGE** → Summarization quality
- **F1 score** → Classification; balance of precision and recall
- **RMSE** → Regression error

Memory aid:

**Bilingual translation → BLEU**

## Question 80

### Original Question

A large retailer receives thousands of customer support inquiries about products every day. The customer support inquiries need to be processed and responded to quickly. The company wants to implement **Agents for Amazon Bedrock**.

What are the key benefits of using Amazon Bedrock agents that could help this retailer?

### Choices

A. Generation of custom foundation models (FMs) to predict customer needs  
B. Automation of repetitive tasks and orchestration of complex workflows  
C. Automatically calling multiple foundation models (FMs) and consolidating the results  
D. Selecting the foundation model (FM) based on predefined criteria and metrics

### Correct Answer

**B. Automation of repetitive tasks and orchestration of complex workflows**

### Why?

**Agents for Amazon Bedrock** help generative AI applications perform **multi-step tasks** by orchestrating foundation models, APIs, data sources, and business logic.

For a retailer handling large volumes of customer inquiries, agents can automate repetitive support workflows such as retrieving information, calling backend systems, and completing actions.

- **A. Generate custom FMs** → Bedrock Agents do not train or create custom foundation models.
- **B. Automate tasks and orchestrate workflows** → Correct. This is a core capability of Bedrock Agents.
- **C. Call multiple FMs and consolidate results** → Not the primary purpose of Bedrock Agents.
- **D. Select an FM based on metrics** → Model selection/evaluation is separate from agent orchestration.

### Exam Focus

**Multi-step GenAI tasks + API/tool calls + workflow automation → Agents for Amazon Bedrock**

Key associations:

- **Bedrock Agents** → Orchestrate tasks and workflows
- **Action groups** → Allow agents to call APIs or perform actions
- **Knowledge Bases** → Provide retrieved context
- **Guardrails** → Control safe model behavior

Memory aid:

**“AI needs to do things, not just answer” → Bedrock Agents**

## Question 81

### Original Question

Which option is a benefit of **ongoing pre-training** when fine-tuning a foundation model (FM)?

### Choices

A. Helps decrease the model's complexity  
B. Improves model performance over time  
C. Decreases the training time requirement  
D. Optimizes model inference time

### Correct Answer

**B. Improves model performance over time**

### Why?

**Ongoing pre-training** continues training a foundation model on additional, often domain-specific, unlabeled data. This can help the model learn new terminology, knowledge, and patterns, improving its performance for a particular domain over time.

- **A. Decrease model complexity** → Ongoing pre-training does not reduce the model's architecture or number of parameters.
- **B. Improve model performance over time** → Correct. Additional relevant training can improve domain knowledge and model effectiveness.
- **C. Decrease training time** → Ongoing pre-training actually requires additional training and compute.
- **D. Optimize inference time** → Pre-training improves model knowledge, not inference latency.

### Exam Focus

**Continue training an FM on additional domain-specific data → Ongoing pre-training**

Key associations:

- **Ongoing pre-training** → Improve domain knowledge and performance
- **Fine-tuning** → Adapt a model to specific tasks or desired outputs
- **Inference optimization** → Focuses on latency/compute, not additional training

Memory aid:

**More relevant pre-training → Better domain understanding over time**

## Question 82

### Original Question

What are **tokens** in the context of generative AI models?

### Choices

A. Tokens are the basic units of input and output that a generative AI model operates on, representing words, subwords, or other linguistic units.  
B. Tokens are the mathematical representations of words or concepts used in generative AI models.  
C. Tokens are the pre-trained weights of a generative AI model that are fine-tuned for specific tasks.  
D. Tokens are the specific prompts or instructions given to a generative AI model to generate output.

### Correct Answer

**A. Tokens are the basic units of input and output that a generative AI model operates on, representing words, subwords, or other linguistic units.**

### Why?

**Tokens** are the basic pieces of text that a generative AI model processes. Depending on the tokenizer, a token can represent a **whole word, part of a word, punctuation, or another text unit**.

- **A. Basic units of model input/output** → Correct. LLMs process and generate text as sequences of tokens.
- **B. Mathematical representations of words/concepts** → Describes **embeddings**, not tokens.
- **C. Pre-trained weights** → These are the learned **parameters** of the model.
- **D. Prompts or instructions** → A prompt is made up of tokens, but it is not itself the definition of a token.

### Exam Focus

**Basic unit of text processed by an LLM → Token**

Quick distinction:

- **Token** → Piece of text
- **Embedding** → Numerical vector representing semantic meaning
- **Parameter/weight** → Learned model value
- **Prompt** → Instructions/input provided to the model

Memory aid:

**Text → Tokens → Model processing**

## Question 83

### Original Question

A company wants to assess the costs that are associated with using a **large language model (LLM)** to generate inferences. The company wants to use **Amazon Bedrock** to build generative AI applications.

Which factor will drive the inference costs?

### Choices

A. Number of tokens consumed  
B. Temperature value  
C. Amount of data used to train the LLM  
D. Total training time

### Correct Answer

**A. Number of tokens consumed**

### Why?

For Amazon Bedrock LLM inference, cost is commonly based on the number of **input and output tokens** processed by the model.

- **A. Number of tokens consumed** → Correct. More input/output tokens generally increase inference cost.
- **B. Temperature value** → Controls randomness and creativity, not the main pricing driver.
- **C. Training data size** → Relevant to model training or customization, not standard inference cost.
- **D. Training time** → Affects training costs, not the cost of generating individual inference responses.

### Exam Focus

**Amazon Bedrock inference cost → Number of tokens processed**

Key associations:

- **Input tokens** → Prompt/context sent to the model
- **Output tokens** → Generated response
- **More tokens** → Higher inference cost
- **Temperature** → Randomness, not pricing

Memory aid:

**Bedrock LLM inference cost = Token usage**

## Question 84

### Original Question

A company is using **Amazon SageMaker Studio notebooks** to build and train ML models. The company stores the data in an **Amazon S3 bucket**. The company needs to **manage the flow of data from Amazon S3 to SageMaker Studio notebooks**.

Which solution will meet this requirement?

### Choices

A. Use Amazon Inspector to monitor SageMaker Studio.  
B. Use Amazon Macie to monitor SageMaker Studio.  
C. Configure SageMaker to use a VPC with an S3 endpoint.  
D. Configure SageMaker to use S3 Glacier Deep Archive.

### Correct Answer

**C. Configure SageMaker to use a VPC with an S3 endpoint.**

### Why?

A **VPC endpoint for Amazon S3** allows SageMaker Studio resources inside a VPC to access S3 **privately without routing traffic through the public internet**.

This gives the company greater control over the network path and data flow between **SageMaker Studio and Amazon S3**.

- **A. Amazon Inspector** → Identifies software vulnerabilities and unintended network exposure; it does not manage S3-to-SageMaker data flow.
- **B. Amazon Macie** → Detects and classifies sensitive data in S3; it does not provide private connectivity to SageMaker.
- **C. VPC with S3 endpoint** → Correct. Enables controlled, private connectivity between SageMaker Studio and S3.
- **D. S3 Glacier Deep Archive** → Low-cost archival storage intended for rarely accessed data, not active ML data access.

### Exam Focus

**Private/controlled SageMaker-to-S3 data access → VPC + S3 VPC endpoint**

Key associations:

- **VPC endpoint** → Private access to supported AWS services
- **S3 endpoint** → Access S3 without public internet routing
- **Amazon Macie** → Sensitive data discovery in S3
- **Amazon Inspector** → Vulnerability management
- **S3 Glacier Deep Archive** → Long-term archival storage

Memory aid:

**SageMaker in VPC + private S3 access → S3 VPC endpoint**

## Question 85

### Original Question

A company has a **foundation model (FM)** that was customized by using **Amazon Bedrock** to answer customer queries about products. The company wants to validate the model's responses to new types of queries. The company needs to **upload a new dataset that Amazon Bedrock can use for validation**.

Which AWS service meets these requirements?

### Choices

A. Amazon S3  
B. Amazon Elastic Block Store (Amazon EBS)  
C. Amazon Elastic File System (Amazon EFS)  
D. AWS Snowcone

### Correct Answer

**A. Amazon S3**

### Why?

**Amazon Bedrock** uses **Amazon S3** to store and access datasets for tasks such as model customization and evaluation.

The company can upload the new validation dataset to an S3 bucket and provide Bedrock with access to that data.

- **A. Amazon S3** → Correct. Common storage location for Bedrock training, validation, and evaluation datasets.
- **B. Amazon EBS** → Block storage for EC2 instances, not the standard storage source for Bedrock datasets.
- **C. Amazon EFS** → Shared file storage for compute workloads, not the typical Bedrock dataset source.
- **D. AWS Snowcone** → Edge storage and data transfer device, not used directly for Bedrock validation datasets.

### Exam Focus

**Store datasets for Amazon Bedrock model customization/evaluation → Amazon S3**

Key associations:

- **Amazon S3** → Bedrock training/validation datasets
- **Amazon EBS** → Block storage for EC2
- **Amazon EFS** → Shared file system
- **AWS Snowcone** → Edge computing/data transfer

Memory aid:

**Bedrock dataset storage → Amazon S3**

## Question 86

### Original Question

Which prompting attack directly exposes the configured behavior of a **large language model (LLM)**?

### Choices

A. Prompted persona switches  
B. Exploiting friendliness and trust  
C. Ignoring the prompt template  
D. Extracting the prompt template

### Correct Answer

**D. Extracting the prompt template**

### Why?

**Prompt template extraction** is an attack where a user attempts to make the LLM reveal its hidden or system-level instructions.

Because the prompt template defines the model's **configured behavior, rules, constraints, and response style**, exposing it can reveal how the application is designed to operate.

- **A. Prompted persona switches** → Attempts to make the model adopt a different role or persona.
- **B. Exploiting friendliness and trust** → Uses social-engineering-style prompts to influence model behavior.
- **C. Ignoring the prompt template** → Attempts to override existing instructions rather than reveal them.
- **D. Extracting the prompt template** → Correct. Attempts to expose the hidden instructions controlling the LLM.

### Exam Focus

**Attack attempts to reveal hidden/system instructions → Prompt template extraction**

Quick distinction:

- **Prompt extraction** → Reveal hidden instructions
- **Prompt injection** → Override or manipulate instructions
- **Persona switching** → Make the model adopt an unintended role

Memory aid:

**“Show me your hidden instructions” → Prompt template extraction**

## Question 87

### Original Question

A company wants to use **Amazon Bedrock**. The company needs to review which security aspects the company is responsible for when using Amazon Bedrock.

Which security aspect will the company be responsible for?

### Choices

A. Patching and updating the versions of Amazon Bedrock  
B. Protecting the infrastructure that hosts Amazon Bedrock  
C. Securing the company's data in transit and at rest  
D. Provisioning Amazon Bedrock within the company network

### Correct Answer

**C. Securing the company's data in transit and at rest**

### Why?

Under the **AWS Shared Responsibility Model**, AWS is responsible for **security of the cloud**, while the customer is responsible for **security in the cloud**.

For Amazon Bedrock, the customer is responsible for protecting its own data, including configuring appropriate **encryption, IAM permissions, and access controls**.

- **A. Patching Amazon Bedrock** → AWS manages the underlying managed service and its infrastructure.
- **B. Protecting Bedrock infrastructure** → AWS is responsible for physical infrastructure, hardware, networking, and managed service infrastructure.
- **C. Securing company data** → Correct. The customer is responsible for protecting its data and configuring appropriate security controls.
- **D. Provisioning Bedrock within the company network** → Bedrock is a managed AWS service; customers do not provision its underlying infrastructure.

### Exam Focus

**AWS Shared Responsibility Model:**

- **AWS** → Security **of** the cloud
- **Customer** → Security **in** the cloud

Key associations:

- **AWS responsibility** → Physical infrastructure, hardware, managed service maintenance
- **Customer responsibility** → Data protection, IAM, encryption configuration, access permissions
- **Amazon Bedrock** → Fully managed service; customers do not patch its infrastructure

Memory aid:

**Your data and permissions = Your responsibility**

## Question 88

### Original Question

A social media company wants to use a **large language model (LLM)** to summarize messages. The company has chosen a few LLMs that are available on **Amazon SageMaker JumpStart**. The company wants to compare the **generated output toxicity** of these models.

Which strategy gives the company the ability to evaluate the LLMs with the **LEAST operational overhead**?

### Choices

A. Crowd-sourced evaluation  
B. Automatic model evaluation  
C. Model evaluation with human workers  
D. Reinforcement learning from human feedback (RLHF)

### Correct Answer

**B. Automatic model evaluation**

### Why?

**Automatic model evaluation** can assess multiple LLMs using predefined metrics with minimal manual effort. For comparing measurable characteristics such as **toxicity**, automated evaluation provides the lowest operational overhead.

- **A. Crowd-sourced evaluation** → Requires coordinating external human reviewers and adds administrative effort.
- **B. Automatic model evaluation** → Correct. Uses automated metrics to compare model outputs efficiently.
- **C. Human-worker evaluation** → Useful for subjective qualities such as tone or preference, but requires more time and operational effort.
- **D. RLHF** → A model alignment/training technique, not primarily an evaluation method for comparing toxicity.

### Exam Focus

**Compare measurable LLM qualities with least operational effort → Automatic model evaluation**

Quick distinction:

- **Automatic evaluation** → Low overhead; objective/measurable metrics
- **Human evaluation** → Subjective qualities such as style, helpfulness, preference
- **RLHF** → Improve/align model behavior using human feedback
- **Crowd-sourced evaluation** → Human evaluation with additional coordination overhead

Memory aid:

**“Evaluate many models cheaply and automatically” → Automatic model evaluation**

## Question 89

### Original Question

A company is testing the security of a **foundation model (FM)**. During testing, the company wants to **get around the safety features and make harmful content**.

Which security technique is this an example of?

### Choices

A. Fuzzing training data to find vulnerabilities  
B. Denial of service (DoS)  
C. Penetration testing with authorization  
D. Jailbreak

### Correct Answer

**D. Jailbreak**

### Why?

A **jailbreak** is an attempt to bypass a generative AI model's built-in **safety controls, restrictions, or guardrails** so the model produces content that would normally be blocked.

- **A. Fuzzing training data** → Tests systems with unusual or malformed inputs to uncover vulnerabilities; it is not specifically about bypassing LLM safety behavior.
- **B. DoS** → Attempts to make a system unavailable by overwhelming its resources.
- **C. Penetration testing** → Authorized security testing is a broad practice, but the specific technique described here is a jailbreak.
- **D. Jailbreak** → Correct. Attempts to circumvent model safety mechanisms and trigger restricted output.

### Exam Focus

**Bypass an FM/LLM's safety controls to generate restricted content → Jailbreak**

Quick distinction:

- **Jailbreak** → Bypass model safety restrictions
- **Prompt injection** → Manipulate model instructions or context
- **DoS** → Disrupt service availability
- **Fuzzing** → Test unexpected/malformed inputs for vulnerabilities

Memory aid:

**“Break out of the model's safety rules” → Jailbreak**

## Question 90

### Original Question

A company needs to use **Amazon SageMaker** for model training and inference. The company must comply with regulatory requirements to run SageMaker jobs in an **isolated environment without internet access**.

Which solution will meet these requirements?

### Choices

A. Run SageMaker training and inference by using SageMaker Experiments.  
B. Run SageMaker training and inference by using network isolation.  
C. Encrypt the data at rest by using encryption for SageMaker geospatial capabilities.  
D. Associate appropriate AWS Identity and Access Management (IAM) roles with the SageMaker jobs.

### Correct Answer

**B. Run SageMaker training and inference by using network isolation.**

### Why?

**Amazon SageMaker network isolation** prevents training and inference containers from making **outbound network calls**, helping organizations run ML workloads in environments that must not have internet access.

- **A. SageMaker Experiments** → Used to organize, track, and compare ML experiments, not isolate network access.
    
- **B. Network isolation** → Correct. Restricts containers from accessing external networks or the internet.
    
- **C. Encryption at rest** → Protects stored data but does not prevent internet connectivity.
    
- **D. IAM roles** → Control AWS permissions, but do not by themselves block network access.
    

### Exam Focus

**SageMaker training/inference + no internet access → Network isolation**

Quick distinction:

- **Network isolation** → Block outbound network/internet access
    
- **IAM roles** → Control permissions to AWS resources
    
- **Encryption** → Protect data at rest/in transit
    
- **SageMaker Experiments** → Track ML experiments
    

Memory aid:

**“Run SageMaker with no internet” → Network isolation**