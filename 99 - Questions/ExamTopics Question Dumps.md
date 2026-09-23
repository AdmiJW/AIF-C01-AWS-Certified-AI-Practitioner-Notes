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

---

→
## Question X
### Original Question
### Choices
### Correct Answer
### Why?
### Exam Focus