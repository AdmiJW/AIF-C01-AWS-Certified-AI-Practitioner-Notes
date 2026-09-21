## 1 - Working with AWS Generative AI Services

### 1.1 - AWS Generative AI Services

| **Service**             | **Primary Purpose**                                            | **Key Characteristics**                                         | **Best Use Case**                                              |
| ----------------------- | -------------------------------------------------------------- | --------------------------------------------------------------- | -------------------------------------------------------------- |
| **Amazon Bedrock**      | Build generative AI applications using foundation models (FMs) | Fully managed, serverless, single API, multiple model providers | Quickly integrate existing FMs without managing infrastructure |
| **SageMaker JumpStart** | Discover, deploy, and fine-tune pre-trained/open-source models | Dedicated SageMaker endpoints, infrastructure control           | Fine-tune or host specific models with greater control         |
| **Amazon SageMaker**    | Build, train, and deploy custom ML models                      | End-to-end ML platform                                          | Create proprietary/custom models from the ground up            |
| **Amazon Q Developer**  | Generative AI assistant for software development               | Helps write, debug, understand, and upgrade code                | Developer productivity                                         |
| **Amazon Q Business**   | Enterprise generative AI assistant                             | Connects to enterprise data sources                             | Answer questions using organizational data                     |
| **PartyRock**           | No-code generative AI application builder                      | Web-based, powered by Bedrock, widget-driven                    | Learning, rapid prototypes, and proofs of concept              |

#### Amazon Bedrock

**Amazon Bedrock** is a **fully managed, serverless** service for accessing high-performing **foundation models (FMs)** from AWS and third-party model providers through APIs.

AWS manages the underlying infrastructure, allowing developers to focus on building generative AI applications.

Important Bedrock capabilities include:
- **Guardrails** → Apply safety and responsible AI controls
- **Knowledge Bases** → Add enterprise/private data to applications using **Retrieval-Augmented Generation (RAG)**
- **Agents** → Allow generative AI applications to perform multi-step tasks and interact with other systems
- Access to models from providers such as **Anthropic** and **Meta**

Use **Amazon Bedrock** when you need a fast way to integrate existing foundation models without provisioning or managing ML infrastructure.

**Exam association:**
**Serverless access to foundation models through APIs** → **Amazon Bedrock**

#### SageMaker JumpStart

**Amazon SageMaker JumpStart** provides pre-trained and open-source models that can be discovered, deployed, and fine-tuned using SageMaker.

Unlike Bedrock's managed API-based approach, JumpStart can deploy models to **dedicated SageMaker endpoints**, giving you more control over the hosting infrastructure and instance types.

Use JumpStart when you need:
- A particular **open-source model**
- **Fine-tuning** of an existing model
- **Dedicated compute capacity**
- Greater control over the model's hosting environment

**Exam association:**
**Deploy/fine-tune an existing open-source model with infrastructure control** → **SageMaker JumpStart**

#### Amazon SageMaker

**Amazon SageMaker** is an end-to-end machine learning platform for **building, training, evaluating, and deploying custom ML models**.

It is appropriate when existing foundation or pre-trained models do not meet the requirements and an organization needs significant customization.

Relevant SageMaker capabilities include:
- **SageMaker Studio** → Integrated development environment (IDE) for ML.
- **SageMaker Clarify** → Helps detect **bias** and improve model explainability
- **SageMaker Model Monitor** → Monitors deployed models for issues such as changes in model/data quality.

Use SageMaker when building a **custom model from the ground up**, especially with large proprietary datasets or specialized ML requirements.

**Exam association:**
**Build and train your own custom ML model → Amazon SageMaker**

#### Amazon Q

**Amazon Q** is a generative AI-powered assistant designed primarily for workplace productivity.

**Amazon Q Developer** focuses on software development and can assist with:
- Writing code
- Debugging
- Understanding code
- Upgrading or modernizing applications

**Amazon Q Business** provides a conversational assistant that can connect to enterprise data sources such as **SharePoint, Salesforce, and Amazon S3** and answer questions using organizational information.

Use Amazon Q when the requirement is for a **ready-made AI assistant**, rather than building a generative AI application from scratch.

| **Requirement**                                   | **Service**            |
| ------------------------------------------------- | ---------------------- |
| AI assistance for coding and software development | **Amazon Q Developer** |
| AI assistant using enterprise/company data        | **Amazon Q Business**  |

#### PartyRock

**PartyRock** is a **no-code, web-based generative AI application builder powered by Amazon Bedrock**.

Applications can be created using configurable widgets for capabilities such as:
- User input
- AI-generated text
- Image generation

PartyRock is best suited for:
- **Rapid prototyping**
- Education and experimentation
- **Proofs of concept (PoCs)**

It is not the primary choice for building a professional production environment.

**Exam association:**
**No-code generative AI experimentation/prototyping → PartyRock**

### 1.2 - Choosing Between Bedrock, JumpStart, and SageMaker

The key distinction is the amount of **infrastructure control and model customization** required

**Bedrock → Jumpstart → SageMaker**
**Fast managed API → Existing model + hosting control → Full custom ML development**

| **Scenario**                                                       | **Best Choice**         | **Why**                                             |
| ------------------------------------------------------------------ | ----------------------- | --------------------------------------------------- |
| Quickly add Claude/Llama-style capabilities to an application      | **Amazon Bedrock**      | Serverless access to existing FMs                   |
| Fine-tune an open-source model and control its compute environment | **SageMaker JumpStart** | Pre-trained models plus dedicated SageMaker hosting |
| Develop a proprietary model/algorithm from scratch                 | **Amazon SageMaker**    | Full ML development lifecycle                       |
| Provide developers with an AI coding assistant                     | **Amazon Q Developer**  | Ready-made developer assistant                      |
| Let employees query company information conversationally           | **Amazon Q Business**   | Connects generative AI to enterprise data           |
| Quickly create a no-code GenAI prototype                           | **PartyRock**           | Simple Bedrock-powered experimentation              |

A useful decision rule:

- **Use existing FM with minimal infrastructure management → Bedrock**
- **Customize/deploy an existing model with hosting control → JumpStart**
- **Build your own model → SageMaker**

### 1.3 - Benefits of AWS Generative AI Services

AWS-managed generative AI services reduce the complexity of adopting AI

#### Lower Barrier to Entry

Services such as **Amazon Bedrock** expose complex foundation models through APIs, reducing the need for organizations to develop deep ML expertise or manage underlying infrastructure.

**PartyRock** lowers the barrier further by enabling no-code experimentation

#### Faster Time to Market

Managed infrastructure allows teams to move quickly from an idea to a prototype or production application without procuring and configuring specialized hardware.

#### Cost Efficiency

AWS offers consumption-based options where workloads can be charged according to usage.

AWS also provides purpose-built AI chips:
- **AWS Trainium** → Designed to accelerate **ML training** workloads
- **AWS Inferentia** → Designed to accelerate **ML inference** workloads

These chips can provide more cost-efficient alternatives to general-purpose infrastructure for appropriate AI workloads.

#### Security and Data Privacy

Organizations can use AWS generative AI and ML services while maintaining control over proprietary business data.

A key exam concept is that customer inputs and proprietary data used with services such as **Amazon Bedrock** are not used to train the underlying third-party foundation models.

### 1.4 - Scenario-Based Service Selection

Consider three common exam scenarios:

**Application developers need a generative AI chatbot quickly**
→ **Amazon Bedrock**

Reason: They need a **serverless API and existing foundation model**, not infrastructure management

**Researchers want to fine-tune an open-source model using specialized proprietary terminology and control the hosting infrastructure**
→ **SageMaker JumpStart**

Reason: They need an **existing model + fine-tuning + dedicated infrastructure control**

**Data Scientists need to develop a proprietary fraud-detection model from historical company data**
→ **Amazon SageMaker**

Reason: They need the full ML lifecycle to **build and train a custom model from scratch**

The distinction can be remembered as:
- **Bedrock = Speed**
- **JumpStart = Control + Existing models**
- **SageMaker = Deep customization**

### 1.5 - Exam Focus

1. **Serverless access to foundation models with minimal infrastructure management → Amazon Bedrock**
2. **Guardrails, Knowledge Bases/RAG, and Agents → Amazon Bedrock**
3. **Deploy or fine-tune existing/open-source models with dedicated infrastructure control → SageMaker JumpStart**
4. **Build, train, and deploy a completely custom ML model → Amazon SageMaker**
5. **Bias detection/explainability → Clarify**
6. **Monitor deployed ML models → SageMaker Model Monitor**
7. **AI coding and development assistant → Amazon Q Developer**
8. **Enterprise conversational assistant connected to company data → Amazon Q Business**
9. **No-code generative AI prototyping and education → PartyRock**
10. **ML training acceleration → AWS Trainium**
11. **ML inference acceleration → AWS Inferentia**

**Core decision flow:**
**Need an FM API quickly → Bedrock → Need existing model + hosting control/fine-tuning → JumpStart → Need a custom model from scratch → SageMaker**

## 2 - Demo: Working with Amazon Bedrock

### 2.1 - Integrating Amazon Bedrock into an Application

A generative AI application can use **Amazon Bedrock APIs** from its backend to send user prompts to a foundation model and return generated responses.

Example application flow:
**User → API Gateway → AWS Lambda → Amazon Bedrock → Lambda → API Gateway → User**

- **Amazon API Gateway** receives requests from the application frontend and can handle authorization.
- **AWS Lambda** contains the application logic and calls Amazon Bedrock
- **Amazon Bedrock** sends the request to the selected **foundation model (FM)**.
- Lambda processes and formats the generated response before returning it to the frontend
- Services such as **Amazon DynamoDB** can store information such as chat history.

**Exam idea:** Bedrock is typically integrated into applications programmatically through its **API/SDK**, while other AWS services can handle the surrounding application architecture.

### 2.2 - System Prompts

A **system prompt** provides high-level instructions that define how the foundation model should behave and respond.

It can specify:
- **Persona or role** - e.g., act as an Italian tutor
- **Tone and personality** - e.g., friendly and encouraging
- **Response format** - e.g., Italian response followed by an English learning tip
- **Behavioral rules** - e.g., adapt to the learner's skill level
- **Constraints** - e.g., respond using only 1-3 sentences
- Instructions for handling errors or correcting users

The system prompt is useful for establishing a consistent **application behavior, tone, and corporate voice**.

**System prompt → Defines how the model should behave**
**User prompt/message → Defines what the user is asking**

### 2.3 - Selecting the Foundation Model

When calling Amazon Bedrock, the application specifies the **model ID** for the foundation model it wants to invoke.

For example, an application could select an **Anthropic Claude** model available through Bedrock.

The basic request contains information such as:
**Model ID + System Prompt + User Message + Inference Parameters → Foundation Model Response**

This allows developers to change or select models according to application requirements without building the foundation model themselves.

### 2.4 - Inference Parameters

Applications can configure **inference parameters** that influence how a foundation model generates its response.

#### Temperature

**Temperature** controls the randomness or creativity of generated output.
- **Lower temperature** → More predictable, consistent, deterministic responses
- **Higher temperature** → More varied and creative responses

For example, a temperature such as **0.7** can allow greater variation than a very low temperature.

**Exam keyword:**
**Control creativity/randomness → Temperature**

#### Maximum Tokens

**Max tokens** limits the maximum number of tokens the model can generate in its response.

It is useful for controlling:
- Response length
- Resource consumption
- Potential inference costs

**Exam keyword:**
**Limit generated response length → Max tokens**

### 2.5 - Application Processing Around Bedrock

The foundation model is only one component of a generative AI application. Application code can handle additional tasks before and after the Bedrock API call.

For example, a Lambda function might:
- Receive and validate user requests
- Construct the prompt sent to Bedrock
- Include the **system prompt**
- Select the **model ID**
- Set inference parameters such as **temperature** and **max tokens**
- Invoke Amazon Bedrock
- Parse and format the model response
- Store conversation information in **DynamoDB**
- Retrieve chat history
- Handle application errors

This separation is important:

**Bedrock generates model output; application code handles business logic, storage, formatting, and integration**

### 2.6 - Exam Focus

1. **Invoke foundation models from an application → Amazon Bedrock API/SDK**
2. **Serverless application logic that calls Bedrock → AWS Lambda**
3. **Expose/authorize application API requests → Amazon API Gateway**
4. **Store chat history or application data → Amazon DynamoDB**
5. **Define model persona, tone, rules, and response structure → System prompt**
6. **Identify which foundation model to invoke → Model ID**
7. **Increase/decrease creativity and randomness → Temperature**
8. **Restrict maximum generated response length → Max tokens**

**Typical flow:**
**Frontend → API Gateway → Lambda → Bedrock foundation model → Lambda → Frontend**

## 3 - Understanding the Security and Cost of Generative AI in AWS

### 3.1 - Security and Data Privacy in Generative AI

A major enterprise concern with generative AI is **data leakage**. AWS provides controls to help keep proprietary and regulated data secure when using services such as **Amazon Bedrock**.

Key security characteristics include:
- Data can be **encrypted at rest and in transit**.
- **AWS PrivateLink** can provide private connectivity so traffic does not need to traverse the public internet.
- Customer data submitted to Amazon Bedrock is **not used to train the underlying foundation models**.
- AWS infrastructure supports compliance requirements and industry standards relevant to regulated workloads.

**Exam association:**
**Private access to AWS services without using the public internet → AWS PrivateLink**

### 3.2 - Shared Responsibility for Generative AI

Generative AI security follows the AWS **Shared Responsibility Model**

**AWS** is responsible for security **of the cloud**, including the underlying infrastructure, physical facilities, and managed service components.

**The customer** is responsible for security **in the cloud**, including:
- How the AI service is configured and used
- Access permissions
- Application logic
- Data handling
- Prompts and responses
- Protection against inappropriate or malicious inputs

The use of a managed AI service does not remove the customer's responsibility to configure and operate it securely.

### 3.3 - Prompt Attacks and Amazon Bedrock Guardrails

A key generative AI security threat is an **adversarial prompt**, where a user attempts to manipulate the model into ignoring its intended behavior or safety restrictions.

A common example is **jailbreaking** or **prompt injection**, such as instructing a model to ignore previous instructions and reveal restricted information.

**Guardrails for Amazon Bedrock** help enforce safety requirements by applying controls to model inputs and outputs.

Guardrails can help:
- Filter harmful or toxic content
- Block or deny specific topics
- Protect against inappropriate responses
- Detect or mask sensitive information such as **personally identifiable information (PII)**

**Exam association:**
**Apply configurable safety controls to generative AI inputs/outputs → Guardrails for Amazon Bedrock**

### 3.4 - Amazon Bedrock Pricing Models

Generative AI costs depend on factors such as **model choice, token usage, workload volume, and required performance**.

#### On-Demand Pricing

With **on-demand** usage, costs are generally based on actual inference consumption, such as the number of **input and output tokens** processed.

Best suited for:
- Prototypes
- Variable or unpredictable traffic
- New applications
- Workloads that do not require reserved capacity

**On-demand → Pay for what you use**

#### Provisioned Throughput

**Provisioned throughput** provides reserved model capacity for workloads that require more predictable performance and throughput.

It is more appropriate for:
- High-volume production applications
- Consistent workloads
- Applications requiring predictable capacity and responsiveness

| **Requirement**                                                | **Pricing/Capacity Option** |
| -------------------------------------------------------------- | --------------------------- |
| Low or unpredictable usage                                     | **On-demand**               |
| Predictable, high-volume workload requiring dedicated capacity | **Provisioned Throughput**  |

### 3.5 - Region and Model Availability

Not every foundation model is available in every **AWS Region**

Model selection can therefore involve a trade-off between:
- **Model availability**
- **Latency** to application users
- **Data residency or regulatory requirements**
- Application resilience and architecture

A model available in one Region might not be available in another, so organizations should confirm **regional model availability** when designing an application.

For resilient workloads, using multiple Regions can also help improve **availability and disaster recovery**, where supported by the application architecture.

### 3.6 - Cost Optimization and Model Customization

Greater model customization generally introduces additional cost.

Training or deeply customizing models may require:
- Additional compute resources
- Training time
- Storage for customized models
- Ongoing management

For many applications, using an existing foundation model with effective **prompt engineering** may be more cost-efficient than training or heavily customizing a model.

A useful progression is:
**Prompt engineering → Model customization/fine-tuning → Custom model training**

Move toward greater customization only when the business requirement justifies the additional complexity and cost.

### 3.7 - Monitoring Model Performance

AI models should be monitored after deployment because their effectiveness can change as real-world data changes.

**Model drift** occurs when model performance degrades because the patterns in production data differ from those the model originally learned.

Monitoring helps organizations determine whether:
- The model remains accurate and useful
- Performance is degrading
- An expensive model is still delivering sufficient business value
- Retraining, replacement, or configuration changes are required

**Exam association:**
**Performance degrades as real-world data changes → Model drift**

### 3.8 - Responsible AI

**Responsible AI** is the practice of designing, developing, and deploying AI systems in ways that promote characteristics such as:
- **Fairness**
- **Safety**
- **Transparency**
- **Accountability**
- Reduced bias

Organizations should understand not only what a model produces, but also its **intended use, limitations, and lifecycle**

Documentation such as **AI service cards/model documentation** can provide information about:
- Intended use cases
- Model or service characteristics
- Known limitations
- Responsible AI considerations

Maintaining information about the **model and model version** used in an application supports traceability and accountability.

### 3.9 - Model Lifecycle and Human Oversight

Foundation models can change over time. A model or model version may eventually become **legacy, deprecated, or retired**

Organizations should track the model lifecycle and plan for:
- Model version changes
- Testing newer versions
- Application compatibility
- Migration before model retirement

For **high-stakes decisions**, AI should often support rather than completely replace human decision-making.

A **human-in-the-loop** approach introduces human review or approval where errors could have significant consequences.

Examples include decisions involving:
- Finance
- Healthcare
- Legal matters
- Other high-impact outcomes

### 3.10 - Exam Focus

1. **Keep AWS service traffic off the public internet → AWS PrivateLink**
2. **Customer prompts/data are not used to train underlying Bedrock foundation models** → Key **Amazon Bedrock data privacy** concept
3. **AWS secures underlying infrastructure; customer secures configuration and usage → Shared Responsibility Model**
4. **Attempt to manipulate a model into bypassing instructions or safety controls → Prompt injection / jailbreaking**
5. **Filter harmful content, restricted topics, or sensitive information → Guardrails for Amazon Bedrock**
6. **Variable or low-volume GenAI workload → On-demand pricing**
7. **High-volume workload requiring predictable capacity → Provisioned Throughput**
8. **Model availability differs by geographical location** → Check **AWS Region Availability**
9. **Cheaper alternative to unnecessary model training/customization → Prompt engineering with an existing FM**
10. **Model performance degrades as production data changes → Model drift**
11. **Fair, safe, transparent, and accountable AI → Responsible AI**
12. **Track model purpose, limitations, and versions** → Supports **transparency, provenance, and accountability**
13. **High-stakes AI decision** → Consider **human-in-the-loop oversight**

**Security + cost decision flow:**
**Encrypt & isolate data → Apply Guardrails → Choose on-demand or Provisioned Throughput → Monitor performance/drift → Track model versions → Maintain responsible human oversight**

## 4 - Demo: Securing Generative AI in AWS

### 4.1 - Amazon Bedrock Guardrails

**Guardrails for Amazon Bedrock** let you apply safety and policy controls to generative AI applications.

Guardrails can evaluate both **user inputs** and **model outputs** and take configured actions when content violates defined rules.

Common use cases include:
- Blocking harmful content
- Preventing discussion of specific topics
- Filtering profanity or custom words
- Protecting **personally identifiable information (PII)**
- Detecting prompt attacks
- Reducing unsupported or ungrounded responses

**Exam association:**
**Apply reusable safety controls to Bedrock model interactions → Guardrails for Amazon Bedrock**

### 4.2 - Content Filters and Thresholds

Bedrock Guardrails can apply **content filters** to harmful content categories and prompt attacks.

Filters use configurable **strength/threshold levels** that determine how aggressively content is blocked

A stricter threshold blocks a broader range of potentially harmful content, while a less restrictive setting blocks only content classified with higher confidence as harmful.

**Exam idea:** The filtering threshold controls the **sensitivity of content moderation**, not the creativity of the model.

- **Guardrail threshold** → Safety filtering sensitivity
- **Temperature** → Model creativity/randomness

### 4.3 - Denied Topics

**Denied topics** allow an application to prevent conversations about specific subjects.

A defined topic can include:
- A **topic name**
- A description or definition of what the topic covers
- Example phrases related to the topic
- Actions to take when the topic appears in inputs or outputs

For example, an organization could configure a guardrail to prevent its chatbot from discussing a prohibited product, competitor, or subject

**Exam association:**
**Prevent an AI application from discussing a particular subject → Denied topics in Bedrock Guardrails**

### 4.4 - Word and Profanity Filters

Guardrails can also block specific language using:
- **Profanity filters**
- **Custom blocked words or phrases**

Custom word filtering is useful when an organization has specific terms that must not appear in prompts or generated responses.

The distinction is:

- **Denied topic → Blocks a broader subject or semantic topic**
- **Word filter → Blocks specific words or phrases**

### 4.5 - Protecting Sensitive Information

Bedrock Guardrails can detect and control **personally identifiable information (PII)**

They can be configured for predefined PII categories and can also use **regular expression (regex) patterns** for organization-specific sensitive data formats.

This can help protect information such as identifiers or other sensitive values from being exposed through generative AI interactions

**Exam association:**
**Detect or protect PII in prompts/responses → Bedrock Guardrails sensitive information filters**

### 4.6 - Grounding Checks

Guardrails can perform **grounding checks** to help determine whether generated answers are sufficiently supported by available source information

This helps reduce the risk of **hallucinations**, where a model produces plausible-sounding but unsupported or incorrect information.

**Grounding checks → Help evaluate whether responses are supported by source/context**

They do not guarantee that every model response will be factually correct.

### 4.7 - Using Guardrails in an Application

After creating a guardrail, it can be associated with a Bedrock model invocation

Application configuration typically includes:
**Model ID + System Prompt + Inference Configuration + Guardrail Configuration**

The guardrail configuration identifies the guardrail using information such as its:
- **Guardrail ID**
- **Guardrail version**

The application can then invoke the foundation model while automatically applying the configured guardrail policies.

Typical flow:
**User → API Gateway → Lambda → Bedrock + Guardrail → Lambda → User**

The **guardrail** decides whether the content complies with configured policies, while the application's own code can control how blocked responses and errors are presented to the user.

### 4.8 - Guardrails vs Application Error Handling

Guardrails and application error handling have different responsibilities.

| **Component**               | **Responsibility**                                                              |
| --------------------------- | ------------------------------------------------------------------------------- |
| **Bedrock Guardrail**       | Detects and blocks content according to configured safety policies              |
| **Application/Lambda code** | Determines how blocked requests, errors, and messages are presented to the user |
| **System prompt**           | Defines normal model behavior, persona, tone, and response instructions         |

A system prompt alone should not be treated as a replacement for dedicated safety controls.

- **System prompt → Model behavior**
- **Guardrail → Enforced safety/policy controls**
- **Application code → User-facing handling and business logic**

### 4.9 - Exam Focus

1. **Apply safety and policy controls to Bedrock inputs and outputs → Amazon Bedrock Guardrails**
2. **Block harmful content or prompt attacks → Content filters**
3. **Prevent conversation about an entire subject → Denied topics**
4. **Block exact terms or profanity → Word/profanity filters**
5. **Detect or protect sensitive personal data → PII filters / sensitive information controls**
6. **Detect organization-specific sensitive patterns → Regular expressions (regex)**
7. **Help reduce unsupported/hallucinated responses → Grounding checks**
8. **Identify a guardrail programmatically → Guardrail ID + version**
9. **Determine persona, tone, and normal model behavior → System prompt**
10. **Handle how blocked/error responses appear to users → Applications/Lambda error-handling logic**

**Key distinction:**
**System prompt = behavior instructions**
**Guardrail = safety enforcement**
**Application code = business logic and error handling**