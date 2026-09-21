# Question 1

## Original Question

A team of researchers is developing an AI system to assist doctors in diagnosing medical conditions. The system needs to analyze both patient text reports and medical images (such as X-rays and MRIs).

Which model architecture would be most suitable for the given requirements?

## Choices

- A. Multimodal model  
- B. Large language model  
- C. Diffusion model  
- D. Ensemble model

## Correct Answer

A. **Multimodal model**  

## Why?

A **multimodal model** is designed to process and combine information from **multiple data modalities**, such as **text and images**.

In this scenario:
- Patient reports → **Text**
- X-rays and MRIs → **Images**

A multimodal model can analyze both types of input together, making it the best fit.

**Why the others are incorrect:**

- **Large language mode (LLM)** → Primarily designed for **text/language** tasks; not inherently suited to jointly processing medical images and text
- **Diffusion model** → Primarily associated with **generating data**, especially images, rather than combining text and image inputs for diagnosis
- **Ensemble model** → Combines predictions from **multiple models** to improve performance. It does not specifically mean processing multiple types of data.

## Exam Focus

**Multiple input types/modalities (text + images + audio, etc.) → Multimodal model**

Key distinction:

| **Model**            | **Exam Association**                           |
| -------------------- | ---------------------------------------------- |
| **Multimodal model** | Processes **multiple data types/modalities**   |
| **LLM**              | Language understanding and generation          |
| **Diffusion model**  | Generative AI, especially **image generation** |
| **Ensemble model**   | Combines outputs from **multiple models**      |

# Question 2

## Original Question

A company wants to implement a generative AI model using **Amazon SageMaker** to enhance its customer support chatbot. The model needs to be trained on a large dataset of customer interactions to provide real-time responses to customer queries.

Select and order the correct steps from the following list to complete the task. Each step should be selected one time or not at all. **(Select and order THREE.)**

## Choices

- A. Create a training job in Amazon SageMaker.  
- B. Implement the model to the Amazon SageMaker endpoint.  
- C. Upload the dataset to Amazon S3.  
- D. Create an Amazon SageMaker notebook instance.  
- E. Configure the training job to use the dataset from Amazon S3.  
- F. Monitor the endpoint for real-time inference performance.

## Correct Answer

**1. Upload the dataset to Amazon S3.**  
**2. Create a training job in Amazon SageMaker.**  
**3. Configure the training job to use the dataset from Amazon S3.**

## Why?

**Amazon S3** is commonly used to store training datasets for **Amazon SageMaker**. The training workflow therefore begins by making the dataset available in S3, then creating the SageMaker training job and associating the S3 training data with it.

The other options are not required for the requested **training** steps:
- **SageMaker notebook instance** → Useful for interactive development and experimentation, but not mandatory to run a training job.
- **SageMaker endpoint** → Used after training to host a model for **real-time-inference**
- **Monitor the endpoint** → Relevant after deployment, not during the training-data setup process.

A useful flow is:

**Amazon S3 → SageMaker training job → Configure S3 training data → Model deployment/endpoints**

## Exam Focus

- **Store ML training data → Amazon S3**
- **Train a model → SageMaker training job**
- **Real-time inference → SageMaker endpoint**

Remember the lifecycle distinction:

**Data storage → Training → Deployment → Monitoring**

# Question 3

## Original Question

A financial services company is developing a system to optimize its stock trading strategies. The system interacts with the stock market environment, making trades and learning from the outcomes. It receives rewards for profitable trades and penalties for losses, aiming to maximize overall returns.

Which of the following machine learning (ML) approaches is utilized in the scenario?

## Choices

A. Transfer learning  
B. Self-supervised learning  
C. **Reinforcement learning**  
D. Supervised learning

## Correct Answer

**C. Reinforcement learning**

## Why?

**Reinforcement learning (RL)** involves an **agent** interacting with an **environment**, taking actions, and learning from **rewards** or **penalties**.

In this scenario:
- **Agent** → Trading system
- **Environment** → Stock market
- **Actions** → Buy, sell, or other trading decisions
- **Rewards** → Profitable trades
- **Penalties** → Losses
- **Goal** → Maximize cumulative reward/overall returns

Why the others are incorrect:
- **Transfer learning** → Reuses knowledge from a previously trained model for a related task
- **Self-supervised learning** → Learns patterns from unlabeled data by generating supervisory signals from the data itself
- **Supervised learning** → Learns from **labeled input-output examples** rather than rewards from interactions.

## Exam Focus

**Agent + environment + actions + rewards/penalties → Reinforcement learning**

Key exam keywords:

**Reward, penalty, trial and error, environment, agent, maximize cumulative reward → Reinforcement learning**

# Question 4

## Original Question

A company has deployed a machine learning model for fraud detection in its e-commerce platform. The model has been running in production for several months. The company wants to ensure that it continues to perform accurately and reliably.

Which AWS services or features should the company use to monitor the model’s performance and incorporate human review when necessary? **(Select TWO.)**

## Choices

A. **Amazon SageMaker Model Monitor**  
B. **Amazon A2I (Amazon Augmented AI)**  
C. Amazon Bedrock  
D. Amazon SageMaker Ground Truth  
E. Amazon SageMaker Data Wrangler

## Correct Answer

**A. Amazon SageMaker Model Monitor**  
**B. Amazon A2I (Amazon Augmented AI)**

## Why?

**Amazon SageMaker Model Monitor** continuously monitors ML models in production and can detect issues such as **data drift, model quality changes, bias drift, and feature-attribution drift**

**Amazon Augmented AI (A2I)** adds **human review workflows** to ML predictions. It is useful when predictions are uncertain, sensitive, or require manual verification.

Why the others are incorrect:

- **Amazon Bedrock** → Used to build and scale **generative AI applications** using foundation models; it is not the primary service for monitoring SageMaker model performance
- **SageMaker Ground Truth** → Primarily used for **labeling datasets** and creating high-quality training data
- **SageMaker Data Wrangler** → Used to **prepare, clean, transform, and analyze data** for ML.

## Exam Focus

Quick distinction:

| **Service**                 | **Key Exam Association**                                       |
| --------------------------- | -------------------------------------------------------------- |
| **SageMaker Model Monitor** | Monitor production models, detect **drift and quality issues** |
| **Amazon A2I**              | **Human-in-the-loop** review                                   |
| **SageMaker Ground Truth**  | **Data labeling**                                              |
| **SageMaker Data Wrangler** | **Data preparation/transformation**                            |
| **Amazon Bedrock**          | Build **generative AI** applications with foundations models   |

# Question 5

## Original Question

An e-commerce company receives hundreds of invoices from suppliers every day. The finance team spends a significant amount of time manually extracting relevant information from these invoices, such as invoice numbers, line items, and total amounts. The goal is to streamline this process using AI-powered tools.

Which of the following options will meet the requirements?

## Choices

A. Computer vision  
B. Natural Language Processing  
C. **Intelligent Document Processing (IDP)**  
D. Fraud detection

## Correct Answer

**C. Intelligent Document Processing (IDP)**

## Why?

**Intelligent Document Processing (IDP)** uses AI and ML to automatically **extract, classify, and process information from documents** such as invoices, receipts, forms, and contracts.

In this scenario, IDP can extract structured information including:
- **Invoice numbers**
- **Line items**
- **Datas**
- **Supplier information**
- **Total amounts**

Why the others are incorrect:

- **Computer vision** → Broadly analyzes and understands images, but IDP is specifically designed for extracting and processing information from business documents.
- **Natural Language Processing (NLP)** → Focuses on understanding and generating human language; by itself, it does not represent the complete document-processing workflow
- **Fraud detection** → Identifies suspicious or fraudulent activity rather than extracting information from documents.

## Exam Focus

**Extract structured information from invoices, receipts, forms, or documents → Intelligent Document Processing (IDP)**

Key exam keywords:

**Invoices + automatic data extraction + document automation → IDP**

For AWS-specific scenarios, remember that services such as **Amazon Textract** are commonly associated with extracting **text, handwriting, tables, and form data from documents**.

# Question 6

## Original Question

A machine learning specialist is developing an ML model to predict customer churn for a subscription-based service using **Amazon SageMaker**. The specialist is concerned about potential biases in the training data that might affect the model’s performance. The specialist must also ensure that the model’s predictions are transparent and explainable to stakeholders.

Which AWS SageMaker capability helps to meet these requirements?

## Choices

A. Amazon SageMaker Data Wrangler  
B. **Amazon SageMaker Clarify**  
C. Amazon SageMaker JumpStart  
D. Amazon SageMaker Ground Truth

## Correct Answer

**B. Amazon SageMaker Clarify**

## Why?

**Amazon SageMaker Clarify** helps identify **bias** in ML datasets and models and provides **model explainability** capabilities.

It addresses both requirements in the scenario:
- **Bias detection** → Detect potential bias in training data and model predictions
- **Explainability** → Help explain how different features contribute to model predictions, improving transparency for stakeholders

Why the others are incorrect:
- **SageMaker Data Wrangler** → Used for **data preparation, cleaning, transformation, and analysis**
- **SageMaker JumpStart** → Provides **pretrained models, foundation models, and solution templates** to accelerate ML development
- **SageMaker Ground Truth** → Used primarily for **data labeling**.

## Exam Focus

**Detect ML bias + explain model predictions → Amazon SageMaker Clarify**

Quick distinction:

| **SageMaker Capability** | **Exam Association**                            |
| ------------------------ | ----------------------------------------------- |
| **Clarify**              | **Bias detection + model explainability**       |
| **Data Wrangler**        | Prepare, clean, and transform data              |
| **JumpStart**            | Pretrained models and ready-to-use ML solutions |
| **Ground Truth**         | Data labeling                                   |

**Memory aid:**
- **Clarify** → **"Why did the model predict this, and is it biased?"**

# Question 7

## Original Question

A financial expert is building a model to predict the future value of a portfolio based on historical performance, asset allocation, and market trends. The prediction model will help in making investment decisions and optimizing the portfolio allocation strategy.

Which machine-learning technique should be considered to meet this objective?

## Choices

A. Probability density  
B. Dimensionality reduction  
C. Linear regression  
D. Anomaly detection

## Correct Answer

**C. Linear regression**

## Why?

**Linear regression** is a **supervised learning** technique used to predict a **continuous numerical value** based on one or more input features.

In this scenario:
- Inputs → Historical performance, asset allocation, market trends
- Output → **Future portfolio value**, a continuous value

Why the others are incorrect:
- **Probability density** → Describes how probability is distributed across possible values; it is not the appropriate predictive technique here.
- **Dimensionality reduction** → Reduces the number of input features while preserving important information; it is not primarily used to predict a continuous target
- **Anomaly detection** → Identifies unusual or abnormal observations rather than predicting future numerical values

## Exam Focus

**Predict a continuous numerical value → Regression**

**Model a linear relationship between input features and a numeric target → Linear regression**

Quick distinction:

| **Technique**                | **Exam Association**                         |
| ---------------------------- | -------------------------------------------- |
| **Linear regression**        | Predict **continuous numeric values**        |
| **Dimensionality reduction** | Reduce the number of features/dimensions     |
| **Anomaly detection**        | Find unusual or abnormal data                |
| **Probability density**      | Describe the distribution of possible values |

**Memory aid:**
- **"How much?" / "What value?"** → **Regression**
- **"Which category?"** → **Classification**

# Question 8

## Original Question

A tech company is integrating various generative AI models to enhance its products and services.

Select the correct type of generative AI model to meet each requirement. Each model can be selected one or more times. **(Select FOUR.)**

| Requirement                                                                               |
| ----------------------------------------------------------------------------------------- |
| Generate detailed and contextually accurate **technical documentation** from sparse input |
| Create **photorealistic images from text descriptions** with high detail                  |
| Analyze and generate content involving **text, images, and audio**                        |
| Robust, adaptable model that can be **fine-tuned for many different tasks**               |
|                                                                                           |

## Choices

A. **Large language model (LLM)**  
B. **Stable Diffusion model**  
C. **Large multimodal language model**  
D. **Foundation model**

## Correct Answer

| Requirement                                                                               | Correct Model                       |
| ----------------------------------------------------------------------------------------- | ----------------------------------- |
| Generate detailed and contextually accurate **technical documentation** from sparse input | **Large language model (LLM)**      |
| Create **photorealistic images from text descriptions** with high detail                  | **Stable Diffusion model**          |
| Analyze and generate content involving **text, images, and audio**                        | **Large multimodal language model** |
| Robust, adaptable model that can be **fine-tuned for many different tasks**               | **Foundation model**                |
|                                                                                           |                                     |
|                                                                                           |                                     |

## Why?

**Large language model (LLM)** → Designed for understanding and generating **natural language**. Suitable for documentation, summarization, question answering, and other text-generation tasks.

**Stable Diffusion model** → A **diffusion model** designed for image generation, especially generating detailed images from **text prompts**.

**Large multimodal language model** → Works across **multiple modalities**, such as text, images, and audio. Choose this when a scenario explicitly requires processing or generating more than one data type.

**Foundation model** → A large model trained on broad amounts of data that can be **adapted or fine-tuned for many downstream tasks** rather than being built only for one specific task.

## Exam Focus

Recognize the requirement keywords:

| **Exam keyword / Scenario**                               | **Model**                              |
| --------------------------------------------------------- | -------------------------------------- |
| **Generate text, documentation, summaries**               | **LLM**                                |
| **Generate images from text**                             | **Stable Diffusion / Diffusion Model** |
| **Text + Images + Audio**                                 | **Multimodal model**                   |
| **Broad, reusable, adaptable, fine-tuned for many tasks** | **Foundation model**                   |

**Memory aid:**
- **Text** → **LLM**
- **Text-to-image → Diffusion**
- **Multiple data types → Multimodal**
- **General-purpose base model → Foundation model**

# Question 9

## Original Question

An organization plans to implement an artificial intelligence (AI) system to assess and recommend individuals for eligibility in various public health initiatives and social welfare programs. The system analyzes data from multiple sources, including census data, employment records, and financial information.

The organization needs to streamline the application process and ensure that eligible individuals receive the support they need.

Which core dimension of responsible AI should the organization prioritize to ensure that the machine learning model aligns with ethical principles and provides clarity on how decisions are made?

## Choices

A. Safety  
B. Transparency  
C. Privacy and Security  
D. Fairness

## Correct Answer

**B. Transparency**

## Why?

**Transparency** focuses on making AI systems and their decision-making processes **understandable and explainable** to stakeholders.

The key phrase in the question is:

**"Provides clarity on how decisions are made"**

For a system determining eligibility for public programs, stakeholders should be able to understand how the model reaches its recommendations.

Why the others are incorrect:
- **Safety** → Focuses on preventing harmful or unintended outcomes from AI systems.
- **Privacy and Security** → Focuses on protecting sensitive data and preventing unauthorized access
- **Fairness** → Focuses on preventing unjust bias or discrimination across individuals or groups. It is important in this scenario, but the question specifically emphasizes **clarify of decison-making**.

##  Exam Focus

**Explain how an AI system reaches decisions → Transparency**

Quick distinctions:

| **Responsible AI Dimension** | **Exam Association**                                       |
| ---------------------------- | ---------------------------------------------------------- |
| **Transparency**             | Explainability, visibility into **how decisions are made** |
| **Fairness**                 | Reduce bias and unequal treatment                          |
| **Privacy and Security**     | Protect data and control access                            |
| **Safety**                   | Prevent harmful or unsafe outcomes                         |

**Memory aid:**
- **"How did the AI make this decision?" → Transparency**

# Question 10

## Original Question

A health and wellness startup is developing a mobile app that provides personalized fitness and nutrition recommendations to users. The app collects data on users’ exercise routines, dietary preferences, and health goals.

As part of preparing the data, the team applies **feature engineering** techniques to transform raw user inputs into meaningful variables that improve machine learning (ML) model performance.

The startup aims to leverage a **fully managed AWS service** to suggest tailored workout plans, meal recipes, and supplements based on individual user profiles without managing any underlying infrastructure.

Which AWS service gives the startup the ability to **build, train, and deploy machine learning models at scale**?

## Choices

A. **Amazon SageMaker AI**  
B. Amazon Bedrock  
C. Amazon Q Developer  
D. Amazon Polly

## Correct Answer

**A. Amazon SageMaker AI**

## Why?

**Amazon SageMaker AI** is a fully managed service for the complete ML lifecycle, including **building, training, and deploying machine learning models at scale**.

It supports tasks such as:
- Preparing and transforming ML data
- **Feature engineering**
- Training custom ML models
- Deploying models for inference
- Managing ML workflows without managing the underlying infrastructure

Why the others are incorrect:
- **Amazon Bedrock** → Used primarily to build **generative AI applications with foundation models**, rather than providing the full traditional ML model development and training lifecycle
- **Amazon Q Developer** → Generative AI assistant designed to help with **software development and AWS-related tasks**
- **Amazon Polly** → Converts **text into lifelike speech**.

## Exam Focus

**Build + train + deploy ML models at scale → Amazon SageMaker AI**

Quick distinctions:

| **AWS Service**         | **Exam Association**                                 |
| ----------------------- | ---------------------------------------------------- |
| **Amazon SageMaker AI** | Full **ML lifecycle**: build, train, deploy          |
| **Amazon Bedrock**      | Build **generative AI** apps using foundation models |
| **Amazon Q Developer**  | AI assistant for developers and AWS                  |
| **Amazon Polly**        | **Text-to-speech**                                   |

**Memory aid:**
- **Custom ML lifecycle → SageMaker AI**
- **Foundation models / GenAI appls → Bedrock**

# Question 11

## Original Question

An AI specialist is working with a deep-learning model in **Amazon SageMaker**. The model, which includes a softmax layer, is too large to fit into the memory of a single GPU, and the training dataset is also quite extensive.

The specialist must choose a SageMaker built-in option to optimize the training process and manage the large model and dataset.

Which SageMaker built-in option should the specialist use to handle training of **large model sizes**?

## Choices

A. Managed Spot Training  
B. Model Parallelism  
C. Incremental Training  
D. Pipe Mode

## Correct Answer

**B. Model Parallelism**

## Why?

**Model parallelism** distributes different parts of a large model across **multiple GPUs or compute devices**.

The key clue is:

**"The model is too large to fit into the memory of a single GPU"**

**Model parallelism** solves this by splitting the **model itself** across multiple devices so that very large deep-learning models can be trained.

Why the others are incorrect:
- **Managed Spot Training** → Reduces training **costs** by using spare EC2 capacity; it does not solve a model-too-large-for-one-GPU problem.
- **Incremental Training** → Continues training from an existing model or checkpoint rather than starting from scratch.
- **Pipe Mode** → Streams training data directly from **Amazon S3** instead of downloading the full dataset first. It is useful for **large datasets**, not for a model that cannot fit into GPU memory.

## Exam Focus

**Model too large for one GPU → Model Parallelism**

**Dataset too large to download efficiently → Pipe Mode**

Quick distinction:

| **SageMaker Option**      | **Exam Association**                               |
| ------------------------- | -------------------------------------------------- |
| **Model Parallelism**     | Split a **large model across GPUs**                |
| **Pipe Mode**             | Stream **large datasets from S3**                  |
| **Managed Spot Training** | Reduce **training cost**                           |
| **Incremental Training**  | Continue training an **existing model/checkpoint** |

**Memory aid:**
- **Large model → Model Parallelism**
- **Large dataset → Pipe Mode**

# Question 12

## Original Question

A healthcare insurance company manually extracts sensitive information from claims forms and accompanying attachments. This manual process has led to significant delays for customers seeking healthcare benefits.

To improve customer service and reduce manual labor, the company wants to **automate the extraction of information from documents** to speed up claims processing.

Which AWS service will help meet the company’s objectives?

## Choices

A. Amazon Comprehend  
B. Amazon Textract  
C. Amazon Personalize  
D. Amazon Lex

## Correct Answer

**B. Amazon Textract**

## Why?

**Amazon Textract** automatically extracts **text, handwriting, tables, and form data** from scanned documents and images.

It is well suited for claims forms because it can identify structured information such as:
- Form fields
- Key-value pairs
- Tables
- Printed text
- Handwritten content

Why the others are incorrect:
- **Amazon Comprehend** → Uses NLP to analyze text for entities, sentiment, key phrases, and other language insights; it is not primarily for extracting document structure
- **Amazon Personalize** → Builds **personalized recommendation** systems
- **Amazon Lex** → Builds **conversational chatbots and voice interfaces**

## Exam Focus

**Extract text, tables, and form fields from scanned documents → Amazon Textract**

Quick distinction:

| **AWS Service**        | **Exam Association**                         |
| ---------------------- | -------------------------------------------- |
| **Amazon Textract**    | Document data extraction, forms, tables, OCR |
| **Amazon Comprehend**  | NLP and text analysis                        |
| **Amazon Presonalize** | Personalized recommendations                 |
| **Amazon Lex**         | Conversational bots                          |

**Memory aid:**
- **Document extraction → Textract**
- **Understand extracted text → Comprehend**

# Question 13

## Original Question

A company has a recommender system that generates **embeddings** from customer interaction data to understand product relationships and user preferences. The goal is to enhance the system with **semantic search** capabilities to retrieve contextually similar product recommendations more efficiently.

Which AWS services are best suited for implementing vector search to optimize and scale the recommendation system? **(Select THREE.)**

## Choices

A. Amazon OpenSearch Service  
B. Amazon Neptune ML  
C. Amazon S3  
D. Amazon DocumentDB (with MongoDB compatibility)  
E. Amazon Redshift  
F. Amazon QuickSight

## Correct Answer

**A. Amazon OpenSearch Service**  
**B. Amazon Neptune ML**  
**D. Amazon DocumentDB (with MongoDB compatibility)**

## Why?

**Amazon OpenSearch Service** supports native **vector search** using embeddings and k-nearest neighbor (k-NN) techniques. It is well suited for **semantic search and recommendation systems**.

**Amazon DocumentDB** supports **vector search** and vector indexes, allowing applications to perform similarity searches over embeddings. AWS specifically lists use cases such as **semantic search, product recommendations, and personalization**.

**Amazon Neptune ML** is useful for recommendation scenarios involving **graph relationships**. It can generate graph-based embeddings using graph neural networks and knowledge-graph embedding models, which can help identify related products or users.

A useful nuance for the exam: **Neptune ML generates and uses graph embeddings**, while AWS's dedicated native vector-similarity capability in the Neptune family is currently associated with **Neptune Analytics**.

The other options are less appropriate:
- **Amazon S3** → Primarily object storage; not traditionally the vector-search engine intended by this question
- **Amazon Redshift** → Primarily a data warehouse for analytics
- **Amazon QuickSight** → Business intelligence and visualization

## Exam Focus

**Embeddings + semantic similarity search → Vector search**

| **AWS Service**               | **Exam Association**                              |
| ----------------------------- | ------------------------------------------------- |
| **Amazon OpenSearch Service** | **Vector/k-NN search**, semantic search           |
| **Amazon DocumentDB**         | Document database with **native vector search**   |
| **Amazon Neptune ML**         | **Graph ML + graph embeddings + recommendations** |
| **Amazon S3**                 | Object storage                                    |
| **Amazon Redshift**           | Data warehousing/analytics                        |
| **Amazon QuickSight**         | BI dashboard and visualization                    |

**Memory aid:**
- **Semantic similarity → Vector search**
- **Graph relationships/recommendations → Neptune ML**
- **Search embeddings directly → OpenSearch / DocumentDB**

# Question 14

## Original Question

A five-star hotel has accumulated a significant volume of customer reviews and feedback forms. The hotel intends to collect these reviews to enhance its services and highlight recurring issues or concerns raised by guests.

The hotel is also interested in analyzing feedback to introduce new amenities, although its primary focus is improving current services and addressing frequent complaints.

Which AWS service should the hotel use to effectively analyze customer feedback and enhance its services?

## Choices

A. Amazon Bedrock  
B. Amazon Kendra  
C. Amazon QuickSight  
D. Amazon Comprehend
## Correct Answer

**D. Amazon Comprehend**

## Why?

**Amazon Comprehend** is a natural language processing (NLP) service used to analyze text and extract insights such as:
- **Sentiment**
- **Key phrases**
- **Entities**
- Topics and recurring patterns

This makes it well suited for analyzing large volumes of customer reviews and identifying common complaints or themes.

Why the others are incorrect:
- **Amazon Bedrock** → Used to build generative AI applications with foundation models
- **Amazon Kendra** → Enterprise search service used to find information across documents and data sources
- **Amazon QuickSight** → Business intelligence and visualization service; it can visualize results but is not the primary NLP service for analyzing raw customer feedback.

## Exam Focus

**Analyze customer reviews, sentiment, key phrases, and entities → Amazon Comprehend**

Quick distinction:

| **AWS Service**       | **Exam Association**                               |
| --------------------- | -------------------------------------------------- |
| **Amazon Comprehend** | NLP, **sentiment analysis, entities, key phrases** |
| **Amazon Bedrock**    | Generative AI and foundation models                |
| **Amazon Kendra**     | Intelligent enterprise search                      |
| **Amazon QuickSight** | BI dashboards and visualization                    |

**Memory aid:**
- **Understand text → Comprehend**
- **Search documents → Kendra**
- **Visualize insights → QuickSight**

# Question 15

## Original Question

A data science team is working on a computer vision project that involves training a deep learning model using a large dataset of labeled images.

Which of the following best practices should the team follow to ensure the **security and integrity** of their training data? **(Select TWO.)**

## Choices

A. Implement role-based access controls to restrict data access to authorized personnel only.  
B. Perform data normalization to standardize the image formats and dimensions.  
C. Use cryptographic hashing techniques to verify the authenticity of the data.  
D. Conduct exploratory data analysis to identify and remove outliers and anomalies.  
E. Leverage versioning and audit trails to track changes to the dataset.

## Correct Answer

**A. Implement role-based access controls to restrict data access to authorized personnel only.**  
**C. Use cryptographic hashing techniques to verify the authenticity of the data.**

## Why?

**Role-based access control (RBAC)** protects training data by ensuring that only **authorized users or roles** can access or modify it. This addresses the **security** requirement.

**Cryptographic hashing** helps verify that data has not been altered. By comparing hashes, the team can detect unauthorized or accidental changes, helping maintain **data integrity**.

Why the other options are not the best answers:
- **Data normalization** → Improves data consistency and model training, but is primarily a **data preprocessing** technique
- **Exploratory data analysis (EDA)** → Helps identify data quality problems, patterns, and outliers, but is not primarily a security control
- **Versioning and audit trails** → Useful for tracking dataset changes and accountability, but the question's selected controls more directly address **access security** and **verification of data integrity**.

## Exam Focus

**Restrict who can access training data → Role-based access control**

**Verify data has not been modified → Cryptographic hashing**

Quick distinction:

| **Technique**                 | **Primary Purpose**           |
| ----------------------------- | ----------------------------- |
| **RBAC**                      | Access control / **security** |
| **Cryptographic hashing**     | Verify **data integrity**     |
| **Data normalization**        | Data preprocessing            |
| **EDA**                       | Data quality and exploration  |
| **Versioning / audit trails** | Track changes and history     |

**Memory aid:**
- **Security → Control access**
- **Integrity → Verify data has not changed**

# Question 16

## Original Question

A company is planning to build a chatbot to analyze customer reviews using **large language models (LLMs)**. The company is evaluating various LLMs to determine how well they classify reviews as **positive, negative, or neutral**, while considering fairness and unbiased predictions.

The company also wants to remove **sensitive information** before processing to reduce the risk of prompt leaking and accidental exposure of customer data.

Which options will meet the requirements? **(Select TWO.)**

## Choices

A. Amazon Bedrock Model Evaluation  
B. Amazon Bedrock Guardrails  
C. Amazon Comprehend  
D. Amazon SageMaker AI Ground Truth  
E. Amazon Lex

## Correct Answer

**A. Amazon Bedrock Model Evaluation**  
**B. Amazon Bedrock Guardrails**

## Why

**Amazon Bedrock Model Evaluation** helps compare and evaluate foundation models using relevant evaluation criteria and metrics. It is suitable when choosing among models based on qualities such as **accuracy, robustness, and responsible AI considerations**.

**Amazon Bedrock Guardrails** helps apply safeguards to generative AI applications. It can help detect or filter **sensitive information**, restrict undesirable content, and reduce risks associated with inappropriate model inputs or outputs.

Why the others are incorrect:
- **Amazon Comprehend** → Performs NLP tasks such as sentiment analysis, entity detection, and key-phrase extraction, but it is not the primary Bedrock feature for evaluating multiple LLMs or applying generative AI guardrails
- **SageMaker Ground Truth** → Used mainly for **data labeling** and human annotation workflows
- **Amazon Lex** → Used to build **conversational chatbots** using text and voice interfaces, not for model evaluation or sensitive-data safeguards.

## Exam Focus

**Compare/evaluate foundation models → Amazon Bedrock Model Evaluation**

**Apply GenAI safety controls and protect sensitive information → Amazon Bedrock Guardrails**

| **Requirement**                     | **AWS Capability**           |
| ----------------------------------- | ---------------------------- |
| Evaluate and compare LLMs           | **Bedrock Model Evaluation** |
| Responsible AI / evaluation metrics | **Bedrock Model Evaluation** |
| Filter sensitive information        | **Bedrock Guardrails**       |
| Apply GenAI safety policies         | **Bedrock Guardrails**       |
| Label training data                 | **SageMaker Ground Truth**   |
| Build conversational bots           | **Amazon Lex**               |

**Memory aid:**
- **Evaluate the model → Model Evaluation**
- **Protect the application → Guardrails**

# Question 17

## Original Question

A financial organization is planning to integrate **generative AI services** into its workflow to improve customer support with natural language processing capabilities.

The company wants to ensure that its AI models are **transparent, fair, and accountable** and is looking for resources to understand the **ethical implications and responsible use of AI services**.

Which AWS option would be appropriate for this task?

## Choices

A. Amazon Comprehend  
B. AWS Marketplace  
C. AWS AI Service Cards  
D. Amazon Polly

## Correct Answer

**C. AWS AI Service Cards**

## Why?

**AWS AI Service Cards** provide information about the **responsible design and use of AWS AI services**. They help customers understand areas such as:
- Intended use cases
- Model and service limitations 
- Responsible AI considerations
- Fairness and transparency
- Appropriate use and evaluation

They are especially useful when an organization needs guidance on the **ethical and responsible use of AI**.

Why the others are incorrect:
- **Amazon Comprehend →** NLP service for tasks such as sentiment analysis, entity detection, and key phrase extraction
- **AWS Marketplace** → Catalog for discovering and purchasing third-party software and services
- **Amazon Polly** → Converts text into **speech**

## Exam Focus

**Responsible AI guidance + transparency + fairness + limitations of AWS AI services → AWS AI Service Cards**

| **AWS Option**           | **Exam Association**                                              |
| ------------------------ | ----------------------------------------------------------------- |
| **AWS AI Service Cards** | Responsible AI guidance, transparency, intended uses, limitations |
| **Amazon Comprehend**    | NLP and text analysis                                             |
| **AWS Marketplace**      | Discover/buy third-party solutions                                |
| **Amazon Polly**         | Text-to-speech                                                    |

**Memory aid:**
**"How should this AWS AI service be used responsibly?" → AWS AI Service Cards**

# Question 18

## Original Question

A company is incorporating different generative AI technologies to enhance its internal operations and customer interactions. The company must pair each AI application with the appropriate **responsible AI principle** to ensure ethical integration and alignment with responsible AI practices.

Select the responsible AI principle that best matches each description. **(Select THREE.)**

| **AI Application Practice**                                                                                                                                                    | **Choices**                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------- |
| The application ensures that customer support responses are unbiased and fair, avoiding any form of discrimination or prejudice.                                               | (**Safety, Fairness, Transparency, Controllability)**                     |
| The company openly shares information about the AI system’s overall functioning, data sources, and development process used for generating new product design recommendations. | (**Controllability, Explainability, Privacy and security, Transparency)** |
| The application is designed to prevent unauthorized access to sensitive information while generating personalized customer recommendations.                                    | **(Safety, Privacy and security, Controllability, Explainability)**       |
|                                                                                                                                                                                |                                                                           |

## Correct Answer

|AI Application Practice|Responsible AI Principle|
|---|---|
|Customer support responses are **unbiased and non-discriminatory**|**Fairness**|
|Company openly shares information about the AI system’s **functioning, data sources, and development process**|**Transparency**|
|Application prevents **unauthorized access to sensitive information**|**Privacy and Security**|

## Why?

**Fairness** ensures that AI systems do not produce systematically biased or discriminatory outcomes for individuals or groups.

**Transparency** focuses on providing visibility into how an AI system is developed and operates, including information about **data sources, processes, and system behavior**.

**Privacy and Security** focuses on protecting sensitive information from **unauthorized access, exposure, or misuse**

Key distinctions:

- **Explainability** → Understand **why a specific prediction or output was produced**
- **Transparency** → Understand the broader **system, data sources, development process, and operation**
- **Controllability** → Ability to **control, modify, constrain, or override** AI behavior.
- **Safety** → Prevent harmful or unintended outcomes.

## Exam Focus

**Unbiased / non-discriminatory outcomes → Fairness**

**Visibility into system functioning, data sources, and development → Transparency**

**Memory aid:**
- **Fair treatment → Fairness**
- **See how the system works → Transparency**
- **Protect the data** → **Privacy and Security**

# Question 19

## Original Question

A retail company wants to improve customer engagement by providing **personalized recommendations** to online shoppers. The company decides to leverage generative AI to achieve this goal.

Which characteristics of a generative AI system are relevant for creating personalized product recommendations? **(Select THREE.)**

## Choices

A. Personalization  
B. Simplicity  
C. Scalability  
D. Adaptability  
E. Responsiveness  
F. Data efficiency

## Correct Answer

**A. Personalization**  
**C. Scalability**  
**F. Data efficiency**

## Why?

**Personalization** allows the system to tailor recommendations based on individual user's preferences, behavior, and interaction history

**Scalability** enables the system to serve recommendations to a large and growing number of users without significant degradation in performance

**Data efficiency** helps the system make effective use of available customer data to generate relevant recommendations without requiring excessive additional data.

Why the others are not the best answers:

- **Simplicity** → Can improve usability and implementation, but it is not a core characteristic specifically tied to personalized recommendation generation
- **Adaptability** → Useful for responding to changing user behavior or requirements, but it is not one of the intended characteristics in this question
- **Responsiveness** → Refers more to how quickly a system reacts or returns outputs than to the underlying capability for generating personalized recommendations

## Exam Focus

- **Tailor recommendations to individual users → Personalization**
- **Serve many users efficiently → Scalaility**
- **Make effective use of available training / customer data → Data efficiency**

**Memory aid:**
**Personal recommendations at scale with effective use of data → Personalization + Scalability + Data efficiency**

# Question 20

## Original Question

A healthcare organization is migrating its patient management system to AWS. As part of its compliance and due diligence efforts, it must ensure that the AWS services and solutions it plans to use comply with healthcare regulations such as **HIPAA** and **HITRUST**.

The organization and its independent software vendors (ISVs) also need access to AWS **security and compliance documentation** to demonstrate compliance to auditors.

Which AWS service provides access to the necessary security and compliance reports?

## Choices

A. Amazon Macie  
B. AWS CloudTrail  
C. AWS Security Hub  
D. AWS Artifact

## Correct Answer

**D. AWS Artifact**

## Why?

**AWS Artifact** provides on-demand access to AWS **security and compliance reports, certifications, and agreements**.

It is the correct service when an organization needs documents for:
- **Compliance audits**
- Regulatory due diligence
- AWS certifications and attestations
- Security and compliance reports
- Agreements such as those relevant to regulated workloads

Why the others are incorrect:

- **Amazon Macie** → Discovers and protects **sensitive data in Amazon S3**
- **AWS CloudTrail** → Records **API activity and account events** for auditing and governance
- **AWS Security Hub** → Aggregates and prioritizes **security findings** across AWS services

## Exam Focus

Quick distinction:

| **AWS Service**      | **Exam Association**                           |
| -------------------- | ---------------------------------------------- |
| **AWS Artifact**     | Compliance reports, certifications, agreements |
| **Amazon Macie**     | Discover sensitive data in S3                  |
| **AWS CloudTrail**   | API activity and audit logs                    |
| **AWS Security Hub** | Centralized security findings                  |

**Memory aid:**
**Need proof of AWS compliance → AWS Artifact**