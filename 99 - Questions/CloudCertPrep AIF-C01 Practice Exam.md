## Question 1

### Original Question

Which option describes a characteristic of AI governance frameworks that help build trust and deploy human-centered AI?

### Choices

A. Aligning AI projects with revenue goals and stakeholder expectations  
B. Developing policies and guidelines for data, transparency, responsible AI, and compliance  
C. Driving business transformation and competitive growth through AI  
D. Expanding AI initiatives across business units to maximize long-term value

### Correct Answer

**B. Developing policies and guidelines for data, transparency, responsible AI, and compliance**

### Why?

**AI governance frameworks** establish policies, processes, and controls for developing and using AI responsibly. They commonly address **data governance, transparency, accountability, responsible AI, risk management, and regulatory compliance**.

The other choices focus primarily on business value, growth, or scaling AI rather than governance and trust.

### Exam Focus

**AI governance** → Policies and controls for **responsible AI, transparency, accountability, data governance, and compliance**

Governance focuses on **how AI is managed and controlled**, not simply on maximizing business value.

---

## Question 2

### Original Question

A healthcare organization uses an ML model to flag abnormal lab results. To ensure responsible AI practices, it wants medical professionals to review any prediction the model is uncertain about before the result is sent to patients. Which AWS service meets this requirement?

### Choices

A. Amazon SageMaker Model Monitor  
B. Amazon Augmented AI (Amazon A2I)  
C. Amazon Bedrock Guardrails  
D. Amazon SageMaker Clarify

### Correct Answer

**B. Amazon Augmented AI (Amazon A2I)**

### Why?

**Amazon Augmented AI (Amazon A2I)** adds **human review workflows** to ML predictions. Predictions that meet specified conditions, such as having **low confidence**, can be routed to human reviewers before a final decision is made.

- **SageMaker Model Monitor** → Monitors deployed models for issues such as data/model quality and drift.
    
- **Amazon Bedrock Guardrails** → Controls and filters generative AI inputs and outputs.
    
- **SageMaker Clarify** → Detects bias and explains ML predictions.
    

### Exam Focus

**Human review of ML predictions** → **Amazon A2I**

**Low-confidence prediction → Human reviewer → Final result**

---

## Question 3

### Original Question

A startup is launching an LLM-powered virtual agent and wants to stop users from coaxing it into unsafe actions or leaking its hidden instructions. Which action most directly reduces this risk?

### Choices

A. Reduce the maximum output length on each request  
B. Increase the model's temperature so responses vary more  
C. Raise the Top P value to widen token sampling  
D. Add system instructions in a prompt template that teach the model to recognize and refuse manipulation attempts

### Correct Answer

**D. Add system instructions in a prompt template that teach the model to recognize and refuse manipulation attempts**

### Why?

The scenario describes **prompt injection**, where a user attempts to manipulate an LLM into ignoring its intended instructions, performing unsafe actions, or revealing confidential system prompts.

Strong **system instructions and prompt templates** can define expected behavior and tell the model to reject attempts to override its instructions.

Changing **maximum output length, temperature, or Top P** affects response length or randomness but does not directly protect against prompt injection.

### Exam Focus

**User tries to override instructions or expose system prompts** → **Prompt injection**

Mitigation → Strong **system instructions/prompt templates** that instruct the model to detect and refuse manipulation.

**Temperature / Top P** → Control randomness, not security.

---

## Question 4

### Original Question

Which statement correctly describes embeddings in generative AI?

### Choices

A. Embeddings lower hardware requirements by using a less precise data type for weights and activations  
B. Embeddings search data to find the most helpful information for answering natural-language questions  
C. Embeddings represent data as high-dimensional vectors that capture semantic relationships  
D. Embeddings store and retrieve data for generative AI applications

### Correct Answer

**C. Embeddings represent data as high-dimensional vectors that capture semantic relationships**

### Why?

**Embeddings** convert data such as text, images, or other content into numerical **high-dimensional vectors**. Items with similar meanings tend to have vectors that are close together, enabling **semantic similarity search**.

- A describes **quantization**.
    
- B describes the retrieval process used in systems such as **RAG**, not embeddings themselves.
    
- D describes the role of a **vector database/store**.
    

### Exam Focus

**Embeddings** → Numerical **high-dimensional vectors** representing semantic meaning

**Vector database** → Stores and searches embeddings

**Similar meaning → Similar/nearby vectors**

---

## Question 5

### Original Question

Which two capabilities make Amazon Kendra valuable for enterprise search applications?

### Choices

A. Infrastructure monitoring  
B. Managed relational database hosting  
C. Semantic search  
D. Natural language understanding  
E. Video transcoding

### Correct Answer

**C. Semantic search**  
**D. Natural language understanding**

### Why?

**Amazon Kendra** is an intelligent enterprise search service that uses **machine learning and natural language understanding (NLU)** to understand the intent and context of user queries.

Its **semantic search** capabilities allow it to return relevant information based on meaning rather than relying only on exact keyword matches.

The other options relate to unrelated AWS capabilities.

### Exam Focus

**Enterprise intelligent search** → **Amazon Kendra**

Key capabilities:

- **Semantic search**
    
- **Natural language understanding**
    
- Search based on **meaning and context**, not only keywords
    

---

## Question 6

### Original Question

A company deployed a deep learning model for object detection to production. When the model examines a new image to identify the objects in it, which AI process is taking place?

### Choices

A. Inference  
B. Training  
C. Bias correction  
D. Model deployment

### Correct Answer

**A. Inference**

### Why?

**Inference** occurs when a trained ML model receives new data and generates a prediction or output.

In this case:

**New image → Trained object detection model → Predicted objects**

**Training** is the earlier process where the model learns from training data. Deployment makes the model available for use but is not the process of generating predictions.

### Exam Focus

**Training** → Model learns from data  
**Inference** → Trained model makes predictions on new data  
**Deployment** → Makes the trained model available for inference

---

## Question 7

### Original Question

A company is developing an ML model for loan approvals. It needs to detect bias in the model and also explain the model's predictions. Which solution meets these requirements?

### Choices

A. Amazon SageMaker Clarify  
B. AWS AI Service Cards  
C. Amazon SageMaker Data Wrangler  
D. Amazon SageMaker Model Cards

### Correct Answer

**A. Amazon SageMaker Clarify**

### Why?

**Amazon SageMaker Clarify** helps identify **bias** in ML datasets and models and provides **model explainability** to understand how features influence predictions.

- **AWS AI Service Cards** → Provide transparency information about AWS AI services and their intended use cases and limitations.
    
- **SageMaker Data Wrangler** → Prepares, cleans, and transforms ML data.
    
- **SageMaker Model Cards** → Document important details about ML models for governance and reporting.
    

### Exam Focus

**Detect ML bias + Explain predictions** → **SageMaker Clarify**

**Prepare/transform data** → SageMaker Data Wrangler  
**Document model details** → SageMaker Model Cards  
**AWS AI service transparency documentation** → AWS AI Service Cards

---

## Question 8

### Original Question

A retail store plans to forecast demand for a product over the coming weeks using the Amazon SageMaker AI DeepAR algorithm. Which type of data is required to meet this requirement?

### Choices

A. Text data  
B. Image data  
C. Time series data  
D. Audio data

### Correct Answer

**C. Time series data**

### Why?

**DeepAR** is a supervised learning algorithm designed for **time-series forecasting**. It predicts future values based on historical observations collected over time.

Demand forecasting is therefore a typical DeepAR use case.

Examples include:

- Product demand
    
- Sales
    
- Traffic
    
- Resource usage
    

### Exam Focus

**SageMaker DeepAR** → **Time-series forecasting**

**Historical values over time → Predict future values**

Demand or sales forecasting scenarios are strong indicators of **time-series data**.

---

## Question 9

### Original Question

A company with Amazon Bedrock access wants to control which models specific employees are allowed to use. Which solution meets these requirements?

### Choices

A. Use AWS Identity and Access Management (IAM) service roles to restrict model subscription  
B. Use AWS Identity and Access Management (IAM) policies to restrict model access  
C. Use AWS Security Token Service (AWS STS) to generate temporary credentials for model use  
D. Use Amazon Inspector to monitor model access

### Correct Answer

**B. Use AWS Identity and Access Management (IAM) policies to restrict model access**

### Why?

**AWS Identity and Access Management (IAM) policies** define which AWS resources and actions particular users, groups, or roles are permitted to access.

For **Amazon Bedrock**, IAM permissions can restrict employees from invoking particular models or performing particular Bedrock actions.

- **IAM service roles** allow AWS services to perform actions on behalf of users or resources; they are not the primary mechanism described here.
    
- **AWS STS** provides temporary security credentials but does not by itself define model-level permissions.
    
- **Amazon Inspector** is a vulnerability management service and does not manage Bedrock model permissions.
    

### Exam Focus

**Control who can access/invoke Amazon Bedrock models** → **IAM policies**

**IAM** → Authentication/authorization permissions  
**STS** → Temporary credentials  
**Inspector** → Vulnerability management

---

## Question 10

### Original Question

To satisfy regulators, a company must run its Amazon SageMaker AI training and inference in a sealed environment with no internet connectivity. Which solution will meet these requirements?

### Choices

A. Run the SageMaker AI training and inference jobs with network isolation  
B. Associate appropriate IAM roles with the SageMaker AI jobs  
C. Run the SageMaker AI training and inference jobs with SageMaker Experiments  
D. Encrypt the data at rest using encryption for SageMaker geospatial capabilities

### Correct Answer

**A. Run the SageMaker AI training and inference jobs with network isolation**

### Why?

**SageMaker network isolation** prevents containers used for training or inference from making **inbound or outbound network calls**, providing an isolated environment for workloads with strict security or regulatory requirements.

- **IAM roles** control permissions but do not by themselves eliminate network connectivity.
    
- **SageMaker Experiments** tracks and organizes ML experiments.
    
- **Encryption at rest** protects stored data but does not prevent internet or network access.
    

### Exam Focus

**SageMaker workload must have no network/internet connectivity** → **Network isolation**

Remember the distinction:

**IAM** → Controls permissions  
**Encryption** → Protects data  
**Network isolation** → Restricts network connectivity  
**SageMaker Experiments** → Tracks ML experiments

## Question 11

### Original Question

A company wants to use a large language model (LLM) on Amazon Bedrock to label text passages as positive or negative. Which prompt engineering strategy meets this requirement?

### Choices

A. Provide only the new passage to classify, with no examples or additional context  
B. Include a few example passages, each labeled positive or negative, in the prompt  
C. Add a detailed explanation of sentiment analysis and how LLMs work to the prompt  
D. Include the new passage along with a few examples of unrelated tasks such as summarization or translation

### Correct Answer

**B. Include a few example passages, each labeled positive or negative, in the prompt**

### Why?

Providing several labeled examples is **few-shot prompting**. The examples demonstrate the expected task and output format, helping the LLM classify a new passage as **positive or negative** without additional training.

- **A** is closer to **zero-shot prompting** because no examples are provided.
    
- **C** adds unnecessary background instead of demonstrating the classification task.
    
- **D** provides examples unrelated to sentiment classification and would not effectively guide the model.
    

### Exam Focus

**Few-shot prompting** → Provide a small number of **input/output examples** in the prompt.

**Zero-shot prompting** → Give instructions with **no examples**.

For classification tasks where examples are supplied → Think **few-shot prompting**.

---

## Question 12

### Original Question

A telecom company wants an LLM chatbot that gives support agents real-time answers grounded in internal policy documents, at the lowest cost. Which approach fits best?

### Choices

A. Paste all policy documents into every prompt as context  
B. Implement Retrieval Augmented Generation (RAG) over the policy documents  
C. Fine-tune the LLM on the policy documents  
D. Pre-train a new model from scratch on the policy corpus

### Correct Answer

**B. Implement Retrieval Augmented Generation (RAG) over the policy documents**

### Why?

**Retrieval Augmented Generation (RAG)** retrieves relevant information from an external knowledge source at query time and supplies it to the LLM as context.

It is well suited when answers must be:

- **Grounded in company documents**
    
- Based on **current or frequently changing information**
    
- Implemented without the higher cost of training or fine-tuning a model
    

Fine-tuning changes model behavior but is generally not the best approach for injecting frequently updated factual knowledge. Pre-training from scratch is far more resource-intensive.

### Exam Focus

**Ground LLM answers in private/current documents** → **RAG**

Typical flow:

**User query → Retrieve relevant documents → Add context → LLM generates grounded answer**

**RAG** → External knowledge  
**Fine-tuning** → Adapt model behavior/style/task performance  
**Pre-training** → Build/train the foundation model itself

---

## Question 13

### Original Question

A restaurant chain wants to build an ML model to cut daily food waste and increase revenue, and it needs the model's accuracy to keep improving over time. Which solution meets these requirements?

### Choices

A. Use Amazon CloudWatch to examine customer orders  
B. Use Amazon Rekognition to improve the model  
C. Use Amazon SageMaker AI and retrain it on newer data  
D. Use Amazon Personalize and refine it with historical data only

### Correct Answer

**C. Use Amazon SageMaker AI and retrain it on newer data**

### Why?

**Amazon SageMaker AI** supports building, training, deploying, and **retraining ML models**. Retraining with newer data allows the model to learn from changing patterns and maintain or improve its predictive performance over time.

- **CloudWatch** provides monitoring and observability rather than ML model training.
    
- **Amazon Rekognition** focuses on image and video analysis.
    
- Training only on historical data does not account for newer trends and changing behavior.
    

### Exam Focus

**Model must improve/adapt as new data arrives** → **Retrain the model with newer data**

**Amazon SageMaker AI** → Build, train, deploy, and retrain custom ML models.

---

## Question 14

### Original Question

A company generates long-form marketing content with a foundation model and wants to evaluate quality at scale without relying on human reviewers. Which evaluation approach uses another large language model to score the outputs?

### Choices

A. A/B testing with live users  
B. LLM-as-a-judge  
C. BLEU scoring  
D. Benchmark dataset comparison

### Correct Answer

**B. LLM-as-a-judge**

### Why?

**LLM-as-a-judge** uses an LLM to evaluate the outputs of another model according to defined criteria such as **relevance, coherence, correctness, or quality**.

It enables scalable automated evaluation when manually reviewing every generated response would be impractical.

- **A/B testing** measures responses through user behavior or preferences.
    
- **BLEU** compares generated text against reference text using n-gram overlap.
    
- **Benchmark datasets** provide standardized evaluation data but do not specifically mean another LLM performs the scoring.
    

### Exam Focus

**Use another LLM to evaluate generated responses** → **LLM-as-a-judge**

Useful for scalable evaluation of subjective qualities such as:

**Relevance • Coherence • Helpfulness • Quality**

---

## Question 15

### Original Question

A developer wants to quickly create a test case and documentation for some code with the LEAST effort. Which solution meets this requirement?

### Choices

A. Build an application that uses foundation models (FMs)  
B. Research and write the test cases by hand, then add the documentation  
C. Upload the code to an online coding assistant  
D. Use Amazon Q Developer in an integrated development environment (IDE)

### Correct Answer

**D. Use Amazon Q Developer in an integrated development environment (IDE)**

### Why?

**Amazon Q Developer** is a generative AI assistant designed for software development. Within an **IDE**, it can help developers understand code and generate development artifacts such as **tests and documentation**, reducing manual effort.

Building a custom FM application would require significantly more work, while manually creating tests and documentation does not satisfy the **least effort** requirement.

### Exam Focus

**Generative AI assistance for software development** → **Amazon Q Developer**

Look for scenarios involving:

- Code generation
    
- Code explanations
    
- Unit/test generation
    
- Documentation
    
- Developer assistance inside an **IDE**
    

---

## Question 16

### Original Question

A manufacturer wants to train an ML model that flags unusual readings in its equipment sensor data, but it has no labeled examples to learn from. Which ML method meets this requirement?

### Choices

A. Logistic regression  
B. Decision tree  
C. Autoencoders  
D. Linear regression

### Correct Answer

**C. Autoencoders**

### Why?

**Autoencoders** can be used for **unsupervised anomaly detection**. They learn to reconstruct normal input data. When unusual data is provided, the reconstruction error is typically larger, which can indicate an anomaly.

This makes them useful when there are **no labeled examples of abnormal events**.

- **Logistic regression** → Supervised classification
    
- **Decision trees** → Commonly supervised classification or regression
    
- **Linear regression** → Predicts continuous numerical values
    

### Exam Focus

**Anomaly detection + No labeled data** → **Autoencoders**

Typical concept:

**Normal data → Train autoencoder → High reconstruction error → Possible anomaly**

---

## Question 17

### Original Question

What is the difference between discriminative and generative AI models?

### Choices

A. Discriminative models are more accurate than generative models  
B. Discriminative models need more data than generative models  
C. Discriminative models classify or predict, while generative models create new content  
D. Discriminative models are faster than generative models

### Correct Answer

**C. Discriminative models classify or predict, while generative models create new content**

### Why?

**Discriminative models** learn to distinguish between categories or predict an output from input data.

**Generative models** learn patterns in data and can create **new content**, such as text, images, audio, or code.

|Model Type|Main Purpose|
|---|---|
|**Discriminative**|Classify or predict|
|**Generative**|Generate new content|

### Exam Focus

**Discriminative AI** → **Classification/prediction**

**Generative AI** → **Creates new content**

Example:

**Spam vs. not spam** → Discriminative  
**Generate an email** → Generative

---

## Question 18

### Original Question

A company's image-generation model keeps producing pictures unrelated to the prompts, and the team wants to adjust its prompting to cut down on these. Which technique helps?

### Choices

A. Add few-shot example images  
B. Use zero-shot prompts  
C. Use negative prompts that state what to exclude  
D. Make the prompts more open-ended

### Correct Answer

**C. Use negative prompts that state what to exclude**

### Why?

A **negative prompt** explicitly specifies elements, characteristics, or content that the model should **avoid generating**.

For image generation, negative prompting can help reduce unwanted or irrelevant elements and better constrain the generated output.

- **Few-shot examples** can demonstrate desired behavior but do not directly specify unwanted content.
    
- **Zero-shot prompting** simply provides no examples.
    
- **Open-ended prompts** provide less constraint and can increase irrelevant outputs.
    

### Exam Focus

**Tell a generative model what NOT to produce** → **Negative prompting**

Example concept:

**Prompt** → What you want  
**Negative prompt** → What you want the model to exclude

---

## Question 19

### Original Question

A team builds and trains ML models in Amazon SageMaker Studio notebooks, keeping its data in an Amazon S3 bucket. It needs to control how data moves between Amazon S3 and the notebooks. Which solution meets this requirement?

### Choices

A. Configure SageMaker to use S3 Glacier Deep Archive  
B. Use Amazon Macie to monitor SageMaker Studio  
C. Configure SageMaker to use a VPC with an Amazon S3 endpoint  
D. Use Amazon Inspector to monitor SageMaker Studio

### Correct Answer

**C. Configure SageMaker to use a VPC with an Amazon S3 endpoint**

### Why?

Running **SageMaker** resources within a **VPC** and using an **Amazon S3 VPC endpoint** allows traffic between SageMaker and Amazon S3 to remain within the AWS network rather than requiring access through the public internet.

- **S3 Glacier Deep Archive** is a low-cost archival storage class.
    
- **Amazon Macie** discovers and helps protect sensitive data, particularly in Amazon S3.
    
- **Amazon Inspector** identifies software vulnerabilities and unintended network exposure in supported workloads.
    

### Exam Focus

**Private connectivity from SageMaker to Amazon S3** → **VPC + S3 VPC endpoint**

Remember:

**VPC endpoint** → Private access to supported AWS services without traversing the public internet.

---

## Question 20

### Original Question

An edtech company is building an app where students type a question or snap a photo of one, and the app returns a written answer with an explanation. Which type of model should power the app?

### Choices

A. Diffusion model  
B. Large multimodal language model  
C. Text-to-speech model  
D. Computer Vision model

### Correct Answer

**B. Large multimodal language model**

### Why?

A **large multimodal language model** can process multiple input modalities, such as **text and images**, while generating a text response.

The application must understand either:

**Typed question → Text understanding**

or

**Photo of question → Image understanding**

and then generate a **written explanation**.

- **Diffusion models** are primarily associated with generating images and other media.
    
- **Text-to-speech models** convert text into spoken audio.
    
- **Computer vision models** can analyze images but do not inherently provide the full text reasoning and generation capability required here.
    

### Exam Focus

**Text + Image inputs → Text response/reasoning** → **Multimodal model**

**Multimodal** means a model can work with more than one type of data, such as:

**Text • Images • Audio • Video**

## Question 21

### Original Question

A bank is building an AI application on Amazon Bedrock. The application sits in a VPC that, to satisfy regulators, must be cut off from all internet traffic. Which AWS service or feature meets these requirements?

### Choices

A. Amazon CloudFront  
B. Internet gateway  
C. AWS PrivateLink  
D. Amazon Macie

### Correct Answer

**C. AWS PrivateLink**

### Why?

**AWS PrivateLink** provides private connectivity between a VPC and supported AWS services without sending traffic over the public internet.

For **Amazon Bedrock**, private connectivity can be established through **VPC interface endpoints powered by AWS PrivateLink**, which is useful for workloads with strict security or regulatory requirements.

- **CloudFront** is a content delivery network.
    
- An **internet gateway** provides internet connectivity, which conflicts with the requirement.
    
- **Amazon Macie** discovers and helps protect sensitive data in Amazon S3.
    

### Exam Focus

**Private access to AWS services from a VPC without internet traffic** → **AWS PrivateLink / VPC interface endpoint**

**Regulated or isolated VPC + Amazon Bedrock** → Think **PrivateLink**

---

## Question 22

### Original Question

A model performs well on training data but poorly on evaluation data. What is the most likely cause?

### Choices

A. The model is underfit  
B. The model needs more training epochs  
C. The model is overfit  
D. There is data leakage between the train and test sets

### Correct Answer

**C. The model is overfit**

### Why?

**Overfitting** occurs when a model learns the training data too closely, including noise or specific patterns that do not generalize well to unseen data.

Typical pattern:

**High training performance + Poor evaluation/test performance = Overfitting**

An **underfit** model would generally perform poorly on both training and evaluation data.

### Exam Focus

**Good training performance + Poor test/evaluation performance** → **Overfitting**

**Underfitting** → Poor performance on both training and unseen data.

**Overfitting** → Model memorizes training patterns and fails to generalize.

---

## Question 23

### Original Question

Which large language model (LLM) parameter sets how many candidate next tokens the model considers at each generation step?

### Choices

A. Maximum tokens  
B. Batch size  
C. Temperature  
D. Top K

### Correct Answer

**D. Top K**

### Why?

**Top K** restricts token sampling to the **K most probable next tokens** at each generation step.

For example, if **Top K = 10**, the model considers only the 10 highest-probability candidate tokens before selecting the next token.

- **Maximum tokens** → Limits response length.
    
- **Batch size** → Number of inputs processed together.
    
- **Temperature** → Controls randomness in token selection.
    

### Exam Focus

**Top K** → Number of highest-probability tokens considered

**Top P** → Smallest set of tokens whose cumulative probability reaches a threshold

**Temperature** → Controls randomness

**Maximum tokens** → Controls maximum output length

---

## Question 24

### Original Question

When designing prompts for a generative AI model, which two practices are important?

### Choices

A. Include relevant examples when they help  
B. Use ambiguous wording to encourage creativity  
C. Maximize prompt length regardless of relevance  
D. Provide clear context and instructions  
E. Omit instructions and rely on model defaults

### Correct Answer

**A. Include relevant examples when they help**  
**D. Provide clear context and instructions**

### Why?

Effective prompt engineering generally involves providing **clear instructions, relevant context, and useful examples** when needed.

Examples can demonstrate the expected format or behavior, while clear context reduces ambiguity.

The other options can decrease response quality by adding irrelevant information, creating ambiguity, or failing to communicate the desired task.

### Exam Focus

Good prompt engineering:

- **Clear instructions**
    
- **Relevant context**
    
- **Relevant examples**
    
- Specific desired output or constraints
    

Avoid **ambiguity, irrelevant content, and unnecessary prompt length**.

---

## Question 25

### Original Question

A company uses Retrieval Augmented Generation (RAG) with Amazon Bedrock and Stable Diffusion to create product images, but the results are random and miss requested details. The team wants the images to follow the prompts more closely. Which change helps?

### Choices

A. Set a fixed random seed  
B. Increase the classifier-free guidance (CFG) scale  
C. Increase the number of generation steps  
D. Increase the negative prompt weight

### Correct Answer

**B. Increase the classifier-free guidance (CFG) scale**

### Why?

The **classifier-free guidance (CFG) scale** controls how strongly an image-generation model follows the text prompt.

A higher CFG value generally makes the generated image adhere more closely to the supplied prompt, although excessively high values can reduce image quality.

- A **fixed random seed** improves reproducibility but does not inherently improve prompt adherence.
    
- More generation steps can improve refinement but are not the primary control for how strongly the model follows the prompt.
    
- Negative prompts specify content to avoid.
    

### Exam Focus

**Make generated image follow the prompt more closely** → Increase **CFG scale**

**Random seed** → Reproducibility  
**Generation steps** → Iterative image refinement  
**Negative prompt** → Specify unwanted elements

---

## Question 26

### Original Question

A bank is building an ML model to predict the likelihood that a loan applicant will default. The model uses applicant data such as income, credit score, employment length, and existing debt. The historical dataset includes a label indicating whether each past applicant ultimately defaulted. Which ML technique meets these requirements?

### Choices

A. Supervised learning  
B. Unsupervised learning  
C. Semi-supervised learning  
D. Reinforcement learning

### Correct Answer

**A. Supervised learning**

### Why?

**Supervised learning** trains a model using data that contains both input features and known **labels**.

Here, applicant characteristics are the input features, while whether the applicant **defaulted or did not default** is the label.

This is a **classification** problem.

### Exam Focus

**Labeled training data** → **Supervised learning**

**Default / No default** → **Binary classification**

Quick distinction:

**Supervised** → Labeled data  
**Unsupervised** → No labels  
**Reinforcement learning** → Rewards and penalties from interactions

---

## Question 27

### Original Question

A news app runs sentiment analysis with a large language model (LLM) on Amazon Bedrock and wants the same input to yield steadier results. Which inference parameter should it change?

### Choices

A. Increase the maximum generation length  
B. Reduce the maximum number of output tokens  
C. Decrease the temperature value  
D. Increase the temperature value

### Correct Answer

**C. Decrease the temperature value**

### Why?

**Temperature** controls randomness during token selection.

A **lower temperature** makes the model favor higher-probability tokens, resulting in more **consistent and deterministic** responses.

A higher temperature increases randomness and creativity.

Changing output length does not directly make responses more consistent.

### Exam Focus

**More consistent / predictable output** → **Lower temperature**

**More creative / diverse output** → **Higher temperature**

Think:

**Low temperature = Stable**  
**High temperature = Creative**

---

## Question 28

### Original Question

A business wants to automatically read incoming support emails and route each one into a topic such as billing, technical issues, or account changes. Which AI concept does this scenario represent?

### Choices

A. Forecasting  
B. Computer Vision  
C. Natural Language Processing (NLP)  
D. Speech Recognition

### Correct Answer

**C. Natural Language Processing (NLP)**

### Why?

**Natural Language Processing (NLP)** enables machines to understand, analyze, and classify human language.

Reading support emails and assigning them to categories such as **billing, technical issues, or account changes** is a form of **text classification**, which is an NLP task.

### Exam Focus

**Understand or classify written language** → **NLP**

Common NLP tasks:

- Sentiment analysis
    
- Text classification
    
- Entity recognition
    
- Summarization
    
- Translation
    

**Email → Topic category** → **NLP text classification**

---

## Question 29

### Original Question

A company has built an image classification model and wants a web application to call it for real-time predictions. The company needs a fully managed way to host the model and serve those predictions that scales automatically with demand. Which solution meets these requirements?

### Choices

A. Use Amazon SageMaker Serverless Inference to deploy the model  
B. Use Amazon CloudFront to deploy the model  
C. Use AWS Batch to host the model and serve predictions  
D. Use Amazon API Gateway to host the model and serve predictions

### Correct Answer

**A. Use Amazon SageMaker Serverless Inference to deploy the model**

### Why?

**Amazon SageMaker Serverless Inference** provides a fully managed inference option that automatically provisions and scales compute capacity based on incoming requests.

It is suitable for **real-time inference workloads with intermittent or unpredictable traffic** where the company does not want to manage inference infrastructure.

- **CloudFront** is a content delivery network.
    
- **AWS Batch** is designed for batch computing jobs rather than low-latency real-time inference.
    
- **API Gateway** can expose APIs but does not itself host an ML model.
    

### Exam Focus

**Managed ML inference + Automatically scales with demand** → **SageMaker Serverless Inference**

Useful distinction:

**Real-time endpoint** → Persistent endpoint for sustained low-latency traffic  
**Serverless Inference** → Automatically scales, good for intermittent/unpredictable traffic  
**Batch Transform** → Offline batch predictions

---

## Question 30

### Original Question

Which prompt-based attack is specifically aimed at revealing a model's hidden system instructions?

### Choices

A. Extracting the prompt template  
B. Prompted persona switching  
C. Jailbreaking  
D. Prompt injection

### Correct Answer

**A. Extracting the prompt template**

### Why?

**Prompt extraction** or **prompt template extraction** attempts to make a model reveal its hidden **system prompt, instructions, or prompt template**.

The related concepts differ:

- **Prompt injection** → Malicious instructions attempt to override or manipulate existing instructions.
    
- **Jailbreaking** → Attempts to bypass the model's safety restrictions.
    
- **Persona switching** → Attempts to make the model adopt another identity or behavioral role.
    

### Exam Focus

**Reveal hidden system instructions/prompt** → **Prompt extraction**

**Override instructions** → Prompt injection  
**Bypass safety controls** → Jailbreaking  
**Force alternative identity/persona** → Persona switching

## Question 31

### Original Question

A company analyzes confidential documents with a third-party model on Amazon Bedrock and is worried about data privacy. Which statement explains how Amazon Bedrock keeps that data private?

### Choices

A. User inputs and model outputs are anonymized and then shared with the third-party model providers  
B. User inputs are kept confidential, but model outputs are shared with the third-party model providers  
C. User inputs and model outputs are redacted before they are shared with the third-party model providers  
D. User inputs and model outputs are not shared with any third-party model providers

### Correct Answer

**D. User inputs and model outputs are not shared with any third-party model providers**

### Why?

**Amazon Bedrock** is designed so that customer prompts and model outputs are not shared with third-party foundation model providers for them to use.

This is important for workloads involving **confidential or sensitive enterprise data**.

The other answers incorrectly state that prompts or responses are anonymized, redacted, or otherwise passed to model providers for their use.

### Exam Focus

**Amazon Bedrock data privacy** → Customer **inputs and outputs are not shared with third-party model providers**

Think:

**Private enterprise data + Bedrock** → Prompts and responses remain protected.

---

## Question 32

### Original Question

A company uses Amazon Bedrock for a customer support chatbot and notices costs increasing. The team discovers that full conversation histories are included in every prompt. Which aspect of the token-based pricing model explains this?

### Choices

A. Cost is determined by the time the model spends processing each request  
B. Cost increases with the total number of input and output tokens processed per request  
C. Cost is based on the number of API calls regardless of content  
D. Cost depends on the number of concurrent users

### Correct Answer

**B. Cost increases with the total number of input and output tokens processed per request**

### Why?

Many foundation models on **Amazon Bedrock** use **token-based pricing**.

If the entire conversation history is repeatedly included in each request, the number of **input tokens** increases. Generated responses also contribute **output tokens**.

Therefore:

**Longer prompt history → More input tokens → Higher cost**

### Exam Focus

**Foundation model cost** → Often based on **input tokens + output tokens**

**Long conversation history** → More tokens → Higher inference cost

Reducing unnecessary context can help reduce cost.

---

## Question 33

### Original Question

Which scenario is a practical use case for generative AI?

### Choices

A. Tracking website traffic and user behavior with an analytics dashboard  
B. Using an ML model to forecast product demand  
C. Using a rule-based recommendation engine to suggest products  
D. Using a chatbot to give human-like responses to customer queries in real time

### Correct Answer

**D. Using a chatbot to give human-like responses to customer queries in real time**

### Why?

**Generative AI** creates new content such as text, images, audio, or code.

A chatbot that generates **natural, human-like responses** to customer questions is a typical generative AI use case.

The other options involve analytics, traditional predictive ML, or rule-based systems rather than generation of new content.

### Exam Focus

**Generate human-like text/content** → **Generative AI**

Common use cases:

- Chatbots
    
- Summarization
    
- Content generation
    
- Code generation
    
- Image generation
    

---

## Question 34

### Original Question

In generative AI, what are tokens?

### Choices

A. The hidden layers of the neural network  
B. The instructions or prompts given to the model  
C. The basic units of input and output, such as words or subwords  
D. The vector representations of words or concepts

### Correct Answer

**C. The basic units of input and output, such as words or subwords**

### Why?

**Tokens** are the basic units that a language model processes. A token can represent a whole word, part of a word, punctuation, or another text unit.

LLMs process prompts and generate responses as sequences of tokens.

- **D** describes **embeddings**, not tokens.
    
- A prompt consists of tokens but is not itself the definition of a token.
    

### Exam Focus

**Tokens** → Basic units processed by an LLM

**Embeddings** → Numerical vector representations

**More tokens** → More model processing and potentially higher cost.

---

## Question 35

### Original Question

A hospital wants an AI application that reads structured patient records, extracts the relevant clinical details, and produces concise summaries. Which solution fits?

### Choices

A. Use Amazon Personalize to model patient engagement and pass the output to a general model  
B. Use Amazon Kendra to index the records for search, then apply a template  
C. Use Amazon Textract to digitize scanned documents, then run keyword extraction  
D. Use Amazon Comprehend Medical to extract medical entities and relationships, then apply rule-based logic to format the summaries

### Correct Answer

**D. Use Amazon Comprehend Medical to extract medical entities and relationships, then apply rule-based logic to format the summaries**

### Why?

**Amazon Comprehend Medical** is designed to extract medical information from clinical text, including **medical conditions, medications, procedures, anatomy, and relationships**.

That extracted information can then be processed and formatted into concise summaries.

- **Amazon Personalize** provides personalized recommendations.
    
- **Amazon Kendra** provides intelligent enterprise search.
    
- **Amazon Textract** extracts text and structured data from scanned documents but does not provide specialized medical understanding.
    

### Exam Focus

**Extract medical entities and relationships from clinical text** → **Amazon Comprehend Medical**

**Extract text/forms/tables from scanned documents** → Amazon Textract

**Enterprise search** → Amazon Kendra

---

## Question 36

### Original Question

A company acquires International Organization for Standardization (ISO) accreditation to manage AI risks and to use AI responsibly. What does this accreditation reflect about the company?

### Choices

A. All AI systems that the company uses are ISO certified.  
B. All AI application team members are ISO certified.  
C. All members of the company are ISO certified.  
D. The company's development framework is ISO certified.

### Correct Answer

**D. The company's development framework is ISO certified.**

### Why?

An organizational **ISO accreditation/certification** related to AI management reflects that the organization's **management processes, governance framework, and development practices** conform to the relevant standard.

It does not mean that every employee or every individual AI system is independently ISO certified.

### Exam Focus

**ISO AI certification/accreditation** → Indicates the organization's **AI management or development framework** meets defined standards.

It does **not** mean:

- Every employee is certified
    
- Every AI application is independently certified
    

---

## Question 37

### Original Question

Which of the following is NOT a stage of the foundation model (FM) lifecycle?

### Choices

A. Deployment  
B. Pre-training  
C. Fine-tuning  
D. Marketing

### Correct Answer

**D. Marketing**

### Why?

Typical stages of the **foundation model lifecycle** include developing or **pre-training** the model, adapting it through techniques such as **fine-tuning**, evaluating it, and **deploying** it for inference.

**Marketing** is a business activity and is not part of the technical FM lifecycle.

### Exam Focus

Typical FM lifecycle concepts:

**Pre-training → Evaluation/Adaptation → Fine-tuning → Deployment → Inference**

**Marketing** → Not an FM lifecycle stage.

---

## Question 38

### Original Question

A company is deploying AI agents on Amazon Bedrock that need to access multiple backend systems on behalf of users. The company wants each agent to authenticate with its own identity rather than sharing a single set of credentials. Which AWS feature meets this requirement?

### Choices

A. AWS Secrets Manager  
B. AWS CloudTrail  
C. Amazon Macie  
D. Amazon Bedrock AgentCore Identity

### Correct Answer

**D. Amazon Bedrock AgentCore Identity**

### Why?

**Amazon Bedrock AgentCore Identity** provides identity and authentication capabilities for AI agents, allowing agents to securely access downstream services and resources using appropriate identities and authorization.

- **AWS Secrets Manager** stores and manages secrets.
    
- **AWS CloudTrail** records AWS API activity for auditing.
    
- **Amazon Macie** discovers and protects sensitive data in Amazon S3.
    

### Exam Focus

**AI agent identity and authentication for accessing other systems** → **Amazon Bedrock AgentCore Identity**

**Secrets storage** → Secrets Manager  
**API auditing** → CloudTrail  
**Sensitive S3 data discovery** → Macie

---

## Question 39

### Original Question

A gaming community platform uses Amazon Bedrock Guardrails to screen harmful user inputs and model outputs. Which two content categories can the guardrails filter?

### Choices

A. Gambling  
B. Hate  
C. Politics  
D. Violence

### Correct Answer

**B. Hate**  
**D. Violence**

### Why?

**Amazon Bedrock Guardrails** provides configurable content filtering for categories of harmful content, including **hate** and **violence**.

Guardrails can evaluate both **user inputs and foundation model responses** to help enforce responsible AI policies.

### Exam Focus

**Amazon Bedrock Guardrails** → Control undesirable or harmful model inputs and outputs.

Key exam associations include content such as:

- **Hate**
    
- **Violence**
    
- Sexual content
    
- Insults
    
- Misconduct
    

Think **content safety and responsible AI controls**.

---

## Question 40

### Original Question

A student submits essays by copying text produced by a generative AI tool without attribution. Which responsible AI challenge does this illustrate?

### Choices

A. Toxicity  
B. Privacy  
C. Hallucinations  
D. Plagiarism

### Correct Answer

**D. Plagiarism**

### Why?

**Plagiarism** occurs when someone presents content created by another source as their own without appropriate attribution.

Submitting AI-generated text as original work without disclosure or attribution is therefore a plagiarism and responsible AI concern.

- **Toxicity** → Harmful, offensive, or abusive content
    
- **Privacy** → Improper exposure or use of personal/sensitive information
    
- **Hallucination** → AI generates incorrect or fabricated information
    

### Exam Focus

**AI-generated content submitted without attribution** → **Plagiarism**

Key distinctions:

**Hallucination** → False or fabricated output  
**Toxicity** → Harmful/offensive output  
**Privacy** → Improper handling of sensitive data  
**Plagiarism** → Using generated or copied content without proper attribution

## Question 41

### Original Question

A company deployed an AI assistant on Amazon Bedrock to handle customer service requests. It wants to measure how effectively the assistant resolves customer issues without escalation. Which metric best captures this?

### Choices

A. BLEU score  
B. Perplexity  
C. Model parameter count  
D. Task completion rate

### Correct Answer

**D. Task completion rate**

### Why?

**Task completion rate** measures how often the AI assistant successfully completes the intended business task, such as resolving a customer issue without requiring escalation.

- **BLEU score** measures similarity between generated and reference text, often for translation.
    
- **Perplexity** measures how well a language model predicts text.
    
- **Model parameter count** describes model size, not business effectiveness.
    

### Exam Focus

**Did the AI successfully complete the intended task?** → **Task completion rate**

For business-facing AI applications, look for metrics tied directly to the **desired outcome**, not just model internals.

---

## Question 42

### Original Question

A company wants a chatbot for employee policy questions; policies change often and answers must reflect updates in near real time. Which solution fits?

### Choices

A. Create a Retrieval Augmented Generation (RAG) workflow with Amazon Bedrock Knowledge Bases  
B. Fine-tune a large language model (LLM) on the policy text with Amazon SageMaker AI  
C. Build a custom application with Amazon Q Business  
D. Continuously pre-train an LLM on the policy documents

### Correct Answer

**A. Create a Retrieval Augmented Generation (RAG) workflow with Amazon Bedrock Knowledge Bases**

### Why?

**RAG** is ideal when source information changes frequently because the model retrieves the latest relevant documents at inference time rather than relying only on knowledge embedded during training.

**Amazon Bedrock Knowledge Bases** can provide the retrieval layer for grounding responses in current company documents.

- **Fine-tuning** is better for adapting model behavior or style than for frequently changing factual knowledge.
    
- **Continuous pre-training** is more expensive and unnecessary for this use case.
    
- **Amazon Q Business** can support enterprise question answering, but the option that directly matches the stated need for frequently updated grounding is **RAG with Bedrock Knowledge Bases**.
    

### Exam Focus

**Frequently changing enterprise knowledge + near-real-time answers** → **RAG**

**Amazon Bedrock Knowledge Bases** → Managed retrieval for grounding foundation model responses.

---

## Question 43

### Original Question

A logistics company ingests several gigabytes of shipment records each day and uses them to train an ML model that predicts next-day delivery volumes. The company only needs predictions generated once per day on the full set of accumulated data. Which type of inference best meets this requirement?

### Choices

A. Serverless inference  
B. Real-time inference  
C. Asynchronous inference  
D. Batch inference

### Correct Answer

**D. Batch inference**

### Why?

**Batch inference** is designed for generating predictions over a large dataset when immediate responses are not required.

The company processes several gigabytes of data and only needs predictions **once per day**, making batch processing the most appropriate option.

- **Real-time inference** → Low-latency, immediate predictions.
    
- **Serverless inference** → On-demand inference with automatic scaling.
    
- **Asynchronous inference** → Useful for long-running individual requests or large payloads where responses do not need to be immediate.
    

### Exam Focus

**Large dataset + scheduled predictions + no real-time requirement** → **Batch inference**

**Real-time** → Immediate response  
**Asynchronous** → Long-running requests  
**Batch** → Process many records together offline

---

## Question 44

### Original Question

A company invested in a generative AI solution to automate report writing. Which metric best measures whether this investment delivered financial value?

### Choices

A. Number of model parameters  
B. Return on investment (ROI)  
C. Training data volume  
D. Model accuracy

### Correct Answer

**B. Return on investment (ROI)**

### Why?

**Return on investment (ROI)** measures the financial value generated relative to the cost of the AI solution.

For example, it can account for benefits such as:

- Reduced labor costs
    
- Increased productivity
    
- Faster report creation
    
- Increased revenue
    

Model size, training data volume, and accuracy are technical metrics and do not directly measure financial return.

### Exam Focus

**Did the AI investment generate financial value?** → **ROI**

Think:

**Business value / financial impact** → ROI  
**Technical performance** → Accuracy or other model metrics

---

## Question 45

### Original Question

A property company wants to estimate the sale price of homes from features such as floor area, location, and number of bedrooms. Which algorithm should it use to meet this requirement?

### Choices

A. K-nearest neighbours (k-NN)  
B. Logistic regression  
C. K-means  
D. Linear regression

### Correct Answer

**D. Linear regression**

### Why?

**Linear regression** is used to predict a **continuous numerical value**, such as a house price.

The model can use features such as floor area, location-related variables, and bedroom count to estimate a numerical sale price.

- **Logistic regression** → Classification.
    
- **K-means** → Unsupervised clustering.
    
- **k-NN** can be used for regression in some cases, but **linear regression** is the standard exam answer for predicting continuous numeric values.
    

### Exam Focus

**Predict a continuous numerical value** → **Regression**

**House price prediction** → **Linear regression**

**Classification** → Predict a category  
**Regression** → Predict a number

---

## Question 46

### Original Question

A company needs a foundation model that can accept both text and images as input and produce text output. Which FM selection criterion determines whether a model supports this?

### Choices

A. Temperature range  
B. Context window size  
C. Modality  
D. Training dataset size

### Correct Answer

**C. Modality**

### Why?

**Modality** describes the types of data a model can accept or generate, such as **text, images, audio, or video**.

A model that accepts text and images and generates text is a **multimodal model**.

- **Temperature** controls randomness.
    
- **Context window size** determines how much information the model can process in one interaction.
    
- **Training dataset size** does not directly determine supported input and output types.
    

### Exam Focus

**Supported input/output data types** → **Modality**

**Text + Image input** → **Multimodal model**

---

## Question 47

### Original Question

A development team is building a customer support assistant on Amazon Bedrock. The assistant must remember account details from earlier in the conversation, reference relevant help articles, and follow company guidelines. Which concept describes managing all of this information that is fed to the foundation model?

### Choices

A. Prompt engineering  
B. Model distillation  
C. Continuous pre-training  
D. Context engineering

### Correct Answer

**D. Context engineering**

### Why?

**Context engineering** is the broader process of deciding what information should be supplied to a foundation model at inference time.

This can include:

- Conversation history
    
- User or account information
    
- Retrieved documents
    
- System instructions
    
- Tool outputs
    

**Prompt engineering** focuses more narrowly on how instructions and prompts are phrased, while context engineering manages the wider set of information made available to the model.

### Exam Focus

**Manage all information supplied to an FM** → **Context engineering**

Examples:

**System instructions + Conversation history + Retrieved documents + User data**

**Prompt engineering** → How the prompt is written  
**Context engineering** → What information is included

---

## Question 48

### Original Question

An energy provider wants to monitor voltage levels across a power grid in rural regions. It plans to record voltage readings continuously and store them in Amazon RDS, then analyze how the readings fluctuate throughout each day to build an AI model that predicts potential power outages. Which type of data should the provider collect for this task?

### Choices

A. Text data  
B. Audio data  
C. Time series data  
D. Tabular data

### Correct Answer

**C. Time series data**

### Why?

The key characteristic is that voltage readings are recorded **continuously over time** and analyzed for patterns and fluctuations.

This makes the data **time series data**, even if the values are physically stored in a relational database such as Amazon RDS.

The important distinction is the **nature of the data**, not the storage system.

### Exam Focus

**Measurements recorded over time** → **Time series data**

Examples:

- Voltage readings
    
- Stock prices
    
- Sensor measurements
    
- Daily sales
    
- Traffic levels
    

**Stored in a table/database** does not automatically make the analytical data type merely "tabular."

---

## Question 49

### Original Question

A team generates images with an Amazon Nova Canvas model and needs to keep specific items out of the results. Which solution meets this requirement?

### Choices

A. Use a negative prompt  
B. Switch to another foundation model (FM)  
C. Use a more detailed prompt  
D. Use a higher temperature value

### Correct Answer

**A. Use a negative prompt**

### Why?

A **negative prompt** tells an image-generation model which elements should **not appear** in the generated image.

This is the direct technique for excluding unwanted objects, styles, or characteristics.

- Switching models is unnecessary.
    
- A more detailed positive prompt may help describe desired content but does not directly specify exclusions.
    
- Higher temperature generally increases variation rather than enforcing exclusions.
    

### Exam Focus

**Specify what an image model should NOT generate** → **Negative prompt**

**Positive prompt** → What to include  
**Negative prompt** → What to exclude

---

## Question 50

### Original Question

A design team uses an image-generation foundation model (FM) on Amazon Bedrock and wants to control how detailed or abstract each generated image is. Which model parameter should they adjust?

### Choices

A. Batch size  
B. Model checkpoint  
C. Generation step  
D. Token length

### Correct Answer

**C. Generation step**

### Why?

For diffusion-based image generation, **generation steps** control how many iterative denoising/refinement steps the model performs when creating the image.

More steps can generally provide more opportunity for the image to become **refined and detailed**, while fewer steps can produce less-refined outputs.

- **Batch size** controls how many images or inputs are processed together.
    
- **Model checkpoint** refers to a saved model state.
    
- **Token length** is primarily associated with textual input/output length, not image refinement.
    

### Exam Focus

**Image refinement/detail during diffusion generation** → **Generation steps**

Useful distinction:

**Generation steps** → Refinement/detail  
**CFG scale** → How strongly the image follows the prompt  
**Negative prompt** → What to exclude  
**Random seed** → Reproducibility

## Question 51

### Original Question

A bank needs its generative AI chatbot to stay factual for regulatory reasons. Which solution helps stop the underlying foundation model (FM) from producing hallucinated answers?

### Choices

A. Use AWS Audit Manager to prepare IT audit and compliance reports  
B. Configure Amazon Bedrock Guardrails to evaluate user inputs and model responses  
C. Use Amazon Inspector to scan workloads for vulnerabilities  
D. Use AWS Config to query compliance metadata using natural language

### Correct Answer

**B. Configure Amazon Bedrock Guardrails to evaluate user inputs and model responses**

### Why?

**Amazon Bedrock Guardrails** can evaluate both user inputs and model responses and apply safeguards to help enforce responsible AI requirements.

For factuality-related use cases, Guardrails can help detect and filter undesirable or unsupported responses as part of the application's safety controls.

- **AWS Audit Manager** supports audit evidence collection and compliance reporting.
    
- **Amazon Inspector** identifies software vulnerabilities.
    
- **AWS Config** tracks and evaluates AWS resource configurations.
    

### Exam Focus

**Control and evaluate FM inputs/outputs for responsible AI** → **Amazon Bedrock Guardrails**

**Audit/compliance evidence** → AWS Audit Manager  
**Vulnerability scanning** → Amazon Inspector  
**Resource configuration compliance** → AWS Config

---

## Question 52

### Original Question

A company will use instruction-based fine-tuning to adapt a foundation model (FM) to its domain. How should it prepare the training data?

### Choices

A. Assemble a large unlabeled domain corpus and continue pre-training  
B. Collect human preference rankings of model outputs  
C. Create instruction-and-response (question-and-answer) pairs for the domain  
D. Build a vector index of the documents for retrieval

### Correct Answer

**C. Create instruction-and-response (question-and-answer) pairs for the domain**

### Why?

**Instruction-based fine-tuning** trains a model using examples that demonstrate how it should respond to particular instructions.

The training dataset should therefore contain:

**Instruction/question → Desired response**

- A large unlabeled corpus is associated with **continued pre-training**.
    
- Human preference rankings are associated with preference-based alignment techniques.
    
- A vector index is used for **RAG**, not fine-tuning.
    

### Exam Focus

**Instruction fine-tuning** → **Instruction-response pairs**

**Unlabeled domain corpus** → Continued pre-training  
**Vector index** → RAG  
**Human preference rankings** → Preference-based model alignment

---

## Question 53

### Original Question

An education company trains a custom large language model (LLM) for teenagers and wants the output to match their style, including creative spelling and shorthand. Which metric should it use to assess the output against reference examples?

### Choices

A. Bilingual Evaluation Understudy (BLEU) score  
B. Perplexity  
C. BERTScore  
D. F1 score

### Correct Answer

**A. Bilingual Evaluation Understudy (BLEU) score**

### Why?

**BLEU** compares generated text against one or more reference texts using **n-gram overlap**.

Because the company wants generated text to resemble known reference examples, including their spelling and phrasing patterns, BLEU can measure how closely the generated wording matches those references.

- **Perplexity** measures how well a language model predicts a sequence of tokens.
    
- **BERTScore** focuses more on semantic similarity using contextual embeddings.
    
- **F1 score** is commonly used for classification and information retrieval tasks.
    

### Exam Focus

**Compare generated text to reference wording using n-gram overlap** → **BLEU**

**BLEU** → Lexical/reference similarity  
**BERTScore** → Semantic similarity  
**Perplexity** → Language-model prediction confidence  
**F1** → Balance of precision and recall

---

## Question 54

### Original Question

A company uses a generative AI assistant to help its support team and wants to measure operational efficiency gains. Which metric should it track?

### Choices

A. Model perplexity  
B. BERTScore  
C. Efficiency measured as reduction in average handle time per case  
D. ROUGE score

### Correct Answer

**C. Efficiency measured as reduction in average handle time per case**

### Why?

The company wants to measure **operational efficiency**, so it should use a business metric directly tied to the amount of time employees spend resolving cases.

A reduction in **average handle time (AHT)** demonstrates that the generative AI solution allows support staff to complete work faster.

The other choices are model or text-quality evaluation metrics rather than operational business metrics.

### Exam Focus

**Operational efficiency of AI** → Measure a real business outcome such as **reduced average handle time**

Distinguish:

**Model quality metrics** → BLEU, ROUGE, BERTScore, perplexity  
**Business impact metrics** → Time saved, productivity, cost reduction, ROI

---

## Question 55

### Original Question

A team wants a low-cost, hands-on way to experiment with and learn about generative AI applications. Which solution is MOST cost-effective?

### Choices

A. Amazon Q Business  
B. Amazon Q Developer  
C. Amazon SageMaker JumpStart  
D. Amazon Bedrock PartyRock

### Correct Answer

**D. Amazon Bedrock PartyRock**

### Why?

**Amazon Bedrock PartyRock** provides a hands-on environment for experimenting with generative AI applications without needing to build and manage substantial infrastructure.

It is designed for quickly learning and prototyping generative AI concepts and applications.

- **Amazon Q Business** is an enterprise generative AI assistant.
    
- **Amazon Q Developer** focuses on software development.
    
- **SageMaker JumpStart** provides pretrained models and ML solutions but involves a broader ML development environment.
    

### Exam Focus

**Learn and experiment with generative AI quickly and cheaply** → **Amazon Bedrock PartyRock**

**Amazon Q Business** → Enterprise/business assistant  
**Amazon Q Developer** → Developer/coding assistant  
**SageMaker JumpStart** → Pretrained ML models and solutions

---

## Question 56

### Original Question

A healthcare company wants to use generative AI to answer patients' medical questions. Which AWS service should it use to support responsible AI for the application?

### Choices

A. AWS Trusted Advisor  
B. Amazon Inspector  
C. Amazon Rekognition  
D. Amazon Bedrock Guardrails

### Correct Answer

**D. Amazon Bedrock Guardrails**

### Why?

**Amazon Bedrock Guardrails** helps implement responsible AI controls by applying safeguards to generative AI **inputs and outputs**.

It can help control harmful or undesirable content and enforce application-specific policies, which is especially important for sensitive applications such as healthcare.

- **AWS Trusted Advisor** provides AWS environment recommendations.
    
- **Amazon Inspector** identifies vulnerabilities.
    
- **Amazon Rekognition** performs image and video analysis.
    

### Exam Focus

**Responsible AI controls for Bedrock applications** → **Amazon Bedrock Guardrails**

Think:

**Content filtering + Safety controls + Input/output evaluation** → Guardrails

---

## Question 57

### Original Question

Which prompting approach is used to harden a model against prompt injection attacks?

### Choices

A. Chain-of-thought prompting  
B. Adversarial prompting  
C. Few-shot prompting  
D. Zero-shot prompting

### Correct Answer

**B. Adversarial prompting**

### Why?

**Adversarial prompting** deliberately tests a model with malicious, misleading, or manipulative inputs to discover weaknesses.

These tests can include simulated **prompt injection** attempts so developers can identify vulnerabilities and strengthen the model or application's safeguards.

- **Chain-of-thought prompting** encourages intermediate reasoning.
    
- **Few-shot prompting** provides examples.
    
- **Zero-shot prompting** provides instructions without examples.
    

### Exam Focus

**Test/harden a model against malicious prompts** → **Adversarial prompting**

**Few-shot** → Examples provided  
**Zero-shot** → No examples  
**Adversarial prompting** → Test resistance to attacks and manipulation

---

## Question 58

### Original Question

What is the primary purpose of Amazon Q Business?

### Choices

A. To monitor infrastructure  
B. To store large datasets  
C. To train custom ML models  
D. To provide AI-powered business assistance over company data

### Correct Answer

**D. To provide AI-powered business assistance over company data**

### Why?

**Amazon Q Business** is a generative AI-powered assistant designed for organizational use. It can connect to enterprise information and help employees find information, answer questions, and complete work using **company data**.

It is not primarily an infrastructure monitoring, data storage, or custom model training service.

### Exam Focus

**Generative AI assistant over enterprise/company data** → **Amazon Q Business**

**Amazon Q Developer** → Software development assistance  
**Amazon Q Business** → Employee/business knowledge assistance

---

## Question 59

### Original Question

A newsroom is piloting a generative AI writing aide. Pilot traffic is light, performance is not a concern, and future usage is unpredictable; the newsroom wants the lowest cost. Which solution meets these requirements?

### Choices

A. Use Amazon Bedrock with Provisioned Throughput  
B. Use GPU-powered Amazon EC2 instances  
C. Use Amazon SageMaker JumpStart  
D. Use Amazon Bedrock with On-Demand pricing

### Correct Answer

**D. Use Amazon Bedrock with On-Demand pricing**

### Why?

**Amazon Bedrock On-Demand** pricing lets the company pay for model inference based on actual usage without committing to dedicated capacity.

This is well suited to a pilot with:

- **Low traffic**
    
- **Unpredictable usage**
    
- No strict throughput requirements
    
- A priority on minimizing upfront or idle-capacity costs
    

**Provisioned Throughput** is more suitable when predictable or guaranteed throughput is required.

### Exam Focus

**Low/unpredictable FM usage + pay only for usage** → **Bedrock On-Demand**

**Predictable/high-volume usage requiring dedicated capacity** → **Provisioned Throughput**

---

## Question 60

### Original Question

A media platform plans to use a large language model for content moderation and wants to check its outputs for bias and unfair treatment of particular groups. Which data source allows this assessment with the least administrative effort?

### Choices

A. Benchmark datasets  
B. Moderation logs  
C. User-generated content  
D. Internal content moderation guidelines

### Correct Answer

**A. Benchmark datasets**

### Why?

**Benchmark datasets** provide standardized, curated examples that can be used to evaluate model behavior consistently, including performance related to **bias and fairness**.

They generally require less administrative effort than collecting, cleaning, labeling, and validating large amounts of production or user-generated data.

- **Moderation logs** require processing and interpretation of operational data.
    
- **User-generated content** may require substantial collection, labeling, privacy review, and cleaning.
    
- **Internal guidelines** define policies but are not themselves an evaluation dataset.
    

### Exam Focus

**Evaluate model bias/fairness with minimal data preparation** → **Benchmark datasets**

**Benchmark dataset** → Standardized model evaluation  
**Production/user data** → More representative of real usage, but usually requires more preparation and governance

## Question 61

### Original Question

An online store's chatbot must filter harmful content from both user prompts and its responses. Which Amazon Bedrock feature fits?

### Choices

A. Amazon Bedrock Guardrails  
B. Amazon Bedrock Knowledge Bases  
C. Amazon Bedrock Agents  
D. Amazon Bedrock custom models

### Correct Answer

**A. Amazon Bedrock Guardrails**

### Why?

**Amazon Bedrock Guardrails** applies safety controls to both **user inputs and model outputs**. It can filter harmful or undesirable content and enforce responsible AI policies.

- **Knowledge Bases** → Ground model responses in external data using RAG.
    
- **Agents** → Orchestrate tasks and interact with tools/APIs.
    
- **Custom models** → Adapt foundation models for specific use cases.
    

### Exam Focus

**Filter harmful user prompts + model responses** → **Amazon Bedrock Guardrails**

**Knowledge Bases** → RAG/grounding  
**Agents** → Task orchestration and tool use  
**Guardrails** → Safety and content filtering

---

## Question 62

### Original Question

A pharmaceutical company will train its own large language model (LLM) on private data and wants to limit the carbon footprint of training. Which Amazon EC2 instance type has the LEAST environmental impact for training LLMs?

### Choices

A. Amazon EC2 Trn series  
B. Amazon EC2 P series  
C. Amazon EC2 G series  
D. Amazon EC2 C series

### Correct Answer

**A. Amazon EC2 Trn series**

### Why?

Amazon EC2 **Trn instances** use **AWS Trainium**, which is purpose-built for high-performance deep learning training with improved **price performance and energy efficiency** compared with general-purpose compute options.

- **P instances** → GPU-based accelerated computing and ML workloads.
    
- **G instances** → Graphics and inference-oriented workloads.
    
- **C instances** → Compute-optimized general workloads.
    

### Exam Focus

**Efficient deep learning / LLM training on AWS** → **AWS Trainium / EC2 Trn instances**

Useful association:

**Trainium → Training**  
**Inferentia → Inference**

---

## Question 63

### Original Question

A travel agency builds an AI agent that can search flight availability, book tickets, and process payments by calling the airline's APIs. Which agentic AI capability allows the agent to interact with these external systems?

### Choices

A. Tool usage  
B. Model fine-tuning  
C. Prompt caching  
D. Memory management

### Correct Answer

**A. Tool usage**

### Why?

**Tool usage** allows an AI agent to call external APIs, applications, databases, or other systems to perform actions beyond generating text.

In this case, the agent can use tools to:

**Search flights → Book ticket → Process payment**

- **Fine-tuning** adapts model behavior.
    
- **Prompt caching** reduces repeated prompt-processing overhead.
    
- **Memory management** helps retain relevant information across interactions.
    

### Exam Focus

**Agent calls APIs or external systems** → **Tool usage**

**Memory** → Retain information  
**Tools** → Take actions / access external systems  
**Planning** → Determine steps needed to accomplish a goal

---

## Question 64

### Original Question

While evaluating a classification model in Amazon SageMaker AI, an AI practitioner needs a metric that gives the ratio of correctly classified items to the total number of items classified, whether correctly or incorrectly. Which metric meets this requirement?

### Choices

A. Recall  
B. Accuracy  
C. Precision  
D. F1 score

### Correct Answer

**B. Accuracy**

### Why?

**Accuracy** measures the proportion of all predictions that the model classified correctly.

It considers both correctly predicted positive and negative examples relative to the **total number of predictions**.

- **Precision** → Of predicted positives, how many were actually positive.
    
- **Recall** → Of actual positives, how many were correctly detected.
    
- **F1 score** → Harmonic mean of precision and recall.
    

### Exam Focus

**Correct predictions ÷ Total predictions** → **Accuracy**

Quick distinction:

**Accuracy** → Overall correctness  
**Precision** → Correctness of positive predictions  
**Recall** → Ability to find actual positives  
**F1** → Balance between precision and recall

---

## Question 65

### Original Question

A company needs a generative AI model for an app that must answer users in real time. Which model characteristic matters most?

### Choices

A. Inference speed  
B. Training time  
C. Innovation speed  
D. Model complexity

### Correct Answer

**A. Inference speed**

### Why?

**Inference speed** determines how quickly a trained model generates a response after receiving user input.

For a **real-time application**, low inference latency is critical to providing users with fast responses.

**Training time** matters during model development but does not directly determine how quickly users receive responses after deployment.

### Exam Focus

**Real-time generative AI responses** → Prioritize **inference speed / low latency**

**Training time** → How long model development takes  
**Inference speed** → How quickly deployed model produces outputs