## 1 - IAM Roles and Policies

### 1.1 - IAM Roles and Policies

**AWS Identity and Access Management (IAM)** controls **who can access AWS resources and what actions they can perform**. This is critical for securing AI workloads that interact with services such as storage, databases, and compute resources.

#### IAM Policies

**IAM policies** define permissions for AWS identities and resources.
- Written as **JSON policy documents**
- **Identity-based policies** can be attached to:
	- IAM users
	- IAM groups
	- IAM roles
- Policies can specify:
	- Allowed or denied **actions**
	- Accessible **resources**
	- **Conditions** under which access is permitted
- Support **fine-grained access control** to limit access to sensitive AI resources.

Policies should grant only the permissions required for the intended task.

#### Role-Based Access Control (RBAC)

**Role-Based Access Control (RBAC)** assigns permissions according to a user's **job function or role**, rather than managing permissions separately for every individual.

Example:

| **Role**                    | **Typical Access**      |
| --------------------------- | ----------------------- |
| Marketing role              | Marketing resources     |
| Developer role              | Application/source code |
| Database administrator role | Database resources      |

A user may have multiple roles depending on their responsibilities

**RBAC advantages:**
- Easier to manage at scale
- Permissions can be reused across many identities
- Access can be removed by removing the associated role

#### Attribute-Based Access Control (ABAC)

**Attribute-Based Access Control (ABAC)** determines access based on **attributes**, often implemented using **tags**.

Attributes may include:
- User attributes
- Resource attributes
- Environment
- Application state

Access decisions can evaluate these attributes using policy conditions.

Example:

**Role tagged** `Environment=Production` → **Access resources tagged** `Environment=Production`

ABAC provides more **dynamic and fine-grained access control** than relying only on fixed roles.

| **Access Model** | **Access Based On** | **Key Benefit**                        |
| ---------------- | ------------------- | -------------------------------------- |
| **RBAC**         | Job role/function   | Simple, scalable permission management |
| **ABAC**         | Attributes/tags     | Dynamic, fine-grained access           |

**RBAC and ABAC can be used together** to strengthen access control.

#### Principle of Least Privilege

The **principle of least privilege** means granting an identity **only the minimum permissions necessary** to perform its required task.

This reduces:
- Unauthorized access to sensitive resources
- Damage caused by compromised identities
- Unnecessary exposure of AI systems and data.

**Exam keyword:**
**Minimum required permissions → Least privilege**

#### Temporary Credentials and IAM Roles

IAM roles can provide **temporary credentials** when a role is assumed.

Temporary access is preferable to long-term credentials such as permanent access keys because:
- Access exists only for the required period.
- Credentials automatically expire
- The potential attack window is reduced if credentials are compromised.

Typical flow:
**Identity → Assume IAM role → Receive temporary credentials → Perform task → Credentials expire**

For AWS workloads and AI applications, prefer **IAM roles and temporary credentials** over storing long-term access keys.

### 1.2 - Exam Focus

- **Control access to AWS resources → AWS IAM**
- **Define permissions using JSON documents → IAM policies**
- **Assign permissions based on job function → RBAC**
- **Control access using tags or other attributes → ABAC**
- **Grant only required permissions → Principle of least privilege**
- **Fine-grained access** → Use specific resources, actions, and policy conditions
- **Temporary AWS access → Assume an IAM role**
- **Prefer temporary credentials** over **long-term access keys** where possible
- **RBAC + ABAC** can be combined for scalable and fine-grained access control

## 2 - Services and Features for Securing AI Systems

### 2.1 - Services and Features for Securing AI Systems

Securing AI systems supports the **CIA triad:**
- **Confidentiality** → Prevent unauthorized access to data
- **Integrity** → Ensure data is not improperly modified
- **Availability** → Ensure systems and data remain accessible when required

Encryption is a primary control for protecting **confidentiality**

#### AWS Key Management Service (AWS KMS)

**AWS Key Management Service (AWS KMS)** is used to **create and control cryptographic keys** used to encrypt and decrypt AWS data.

KSM commonly protects:
- **Data at rest**, such as objects stored in **Amazon S3**
- Data used by AWS services that integrate with KMS.

KMS supports different key ownership models:

| **Key Type**             | **Who Manages It?** | **Customer Control/Visibility**                                                                 | **Typical Use**                                 |
| ------------------------ | ------------------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| **Customer managed key** | Customer            | Highest control; configure policies, rotation, aliases, and view metadata                       | Compliance or fine-grained key control          |
| **AWS managed key**      | AWS service         | Limited customer control; customer can view key information but cannot fully administer the key | Convenient encryption managed by an AWS service |
| **AWS owned key**        | AWS                 | No customer management or visibility                                                            | AWS service internal/default encryption         |

**Exam distinction:**
Need maximum control over encryption keys → **Customer managed KMS key**

#### AWS CloudHSM

**AWS CloudHSM** provides dedicated **Hardware Security Modules (HSMs)** for generating and managing cryptographic keys.

Use CloudHSM when an organization requires:
- **Dedicated, single-tenant HSM hardware**
- Greater control over cryptographic operations
- Compliance requirements requiring direct control over HSMs

**KMS vs. CloudHSM**

| **Service**      | **Best Fit**                                                                            |
| ---------------- | --------------------------------------------------------------------------------------- |
| **AWS KMS**      | Managed encryption key service integrated with many AWS services                        |
| **AWS CloudHSM** | Dedicated HSMs and greater customer control for strict security/compliance requirements |

#### Encryption at Rest vs. In Transit

**Encryption at rest** protects stored data

Example:
**Amazon S3 data → Encrypt using AWS KMS keys**

**Encryption in transit** protects data while it travels across networks, typically using **TLS**

**AWS Certificate Manager (ACM)** provisions and manages SSL/TLS certificates used to secure network communications.

**Important distinction:**
**KMS → Encryption keys/data encryption**
**ACM → SSL/TLS certificates**

#### Amazon Macie

**Amazon Macie** is a data security service that helps **discover and classify sensitive data stored in Amazon S3**

Macie can identify information such as:
- Personally identifiable information (**PII**)
- Credit card information
- Phone numbers
- Social Security numbers
- Other sensitive data

Macie uses **machine learning and pattern matching** to discover sensitive data.

It supports:
- **Managed data identifiers** → Built-in identifiers for common sensitive data types
- **Custom data identifiers** → Customer-defined patterns, including **regular expressions (RegEx)**, for organization-specific sensitive data

**Exam keyword:**
**Discover/classify sensitive data in S3 → Amazon Macie**

#### AWS PrivateLink

**AWS PrivateLink** provides **private connectivity between VPCs and supported AWS/services** without requiring traffic to traverse the public internet.

Benefits include:
- Keeps traffic on the **AWS network**
- Reduces exposure to the public internet
- Helps reduce the network **attack surface**
- Supports secure access to AWS services through **VPC endpoints**

**Exam keyword:**
**Privately access supported AWS services without using the public internet → AWS PrivateLink**

#### AWS Shared Responsibility Model

The **AWS Shared Responsibility Model** separates security responsibilities between **AWS** and the **customer**.

| **AWS - Security of the Cloud**                            | **Customer - Security in theCloud**             |
| ---------------------------------------------------------- | ----------------------------------------------- |
| Physical data centers                                      | Customer data                                   |
| Physical infrastructure                                    | IAM permissions                                 |
| Underlying compute, storage, and networking infrastructure | Encryption configuration                        |
| AWS global infrastructure                                  | Application configuration                       |
| Hardware and facilities                                    | OS/network configuration where customer-managed |
|                                                            | Security groups and firewall rules              |

The exact customer responsibility depends on the AWS service being used. **More managed services generally shift more infrastructure-management responsibility to AWS**, while customers remain responsible for areas such as their **data, identities, permissions, and configurations**.

### 2.2 - Exam Focus

- **Create and control encryption keys → AWS KMS**
- **Need maximum control over a KMS key → Customer managed key**
- **Dedicated hardware security modules / strict cryptographic compliance → AWS CloudHSM**
- **Protect stored data → Encryption at rest**
- **Protect network traffic using TLS certificates → AWS Certificate Manager (ACM)**
- **Find and classify PII or other sensitive data in S3 → Amazon Macie**
- **Built-in sensitive-data patterns → Macie managed data identifiers**
- **Organization-specific RegEx detection → Macie custom data identifiers**
- **Private AWS service connectivity without public internet exposure → AWS PrivateLink**
- **AWS secures the underlying cloud infrastructure** → Security **of** the cloud
- **Customer secures data, IAM, encryption settings, and configurations** → Security **in** the cloud

## 3 - Data History

### 3.1 - Data History

AI systems depend on **training data**, so understanding the history of that data is important for **quality, transparency, governance, compliance, and bias detection**.

#### Data Origins

**Data origins** describe where training data came from and how it was prepared before model training.

This can include:
- Where and how the data was collected
- How it was cleaned and curated
- How it was processed or transformed

Understanding data origins helps organizations assess **data quality** and identify potential **biases or issues** that could affect model performance.

#### Data Source Citation

**Data source citation** records and acknowledges the original sources of training data, such as:
- Datasets
- Websites
- Databases
- Other external or internal sources

Source citation supports **transparency** and helps organizations identify applicable **licensing, terms of service, and acceptable-use requirements**.

**Exam distinction:**
**Where the data came from → Data origins**
**Acknowledging/documenting the source → Data source citation**

#### Data Lineage

**Data lineage** tracks the complete history and movement of data throughout its lifecycle.

It can include:

**Collection → Cleansing → Transformation → Movement between systems → Model training**

Data lineage provides traceability and helps organizations create accurate documentation about **data origins and source citations**.

It is important for:
- Governance
- Auditing
- Troubleshooting
- Transparency
- Tracking how training data was prepared and used

#### Data Cataloging

**Data cataloging** organizes information and metadata related to AI assets and datasets

A catalog may contain:
- Dataset information
- Data sources
- Models
- Metadata
- Licensing information
- Terms of service

Cataloging makes this information easier to document, govern, discover, and communicate to **stakeholders and users**

#### Amazon SageMaker Model Cards

**Amazon SageMaker Model Cards** provide a centralized way to document important information about machine learning models for **governance and reporting**

Model cards can document information such as:
- **Data origins and sources**
- Training data details
- How data was used during training
- Model performance metrics
- Potential quality issues and bias
- Model intended use
- Model risk information

This documentation can be shared with **stakeholders and auditors** to improve transparency and demonstrate governance of AI systems.

A useful relationship to remember:
**Data history + model information → SageMaker Model Cards → Governance, transparency, and auditability**

### 3.2 - Exam Focus

- **Where training data originally came from and how it was prepared → Data origins**
- **Credit/document the original dataset, website, or database → Data source citation**
- **Track data from collection through transformation and movement between systems → Data lineage**
- **Organize datasets, metadata, sources, licensing, and model information → Data cataloging**
- **Document model purpose, training data, performance, risk, and governance information → Amazon SageMaker Model Cards**
- **Licensing and terms of service** are important when evaluating whether training data can be legally and appropriately used
- **Data history and lineage** help identify **quality problems, bias, compliance issues, and governance risks**.

## 4 - Secure Data Engineering

### 4.1 - Secure Data Engineering

Before training an AI system, training data should maintain strong **quality and integrity**.

Important data-quality characteristics include:
- **Accuracy** → Data should not contain misinformation, incorrect facts, or unreliable speculation
- **Completeness** → Required information should not be missing
- **Integrity** → Data should be protected against unauthorized or malicious modification

**Data lineage** helps track how data is collected, cleaned, transformed, and modified throughout its lifecycle. This supports verification of **accuracy, completeness, and integrity**

Typical flow:
**Data collection → Cleaning → Transformation → Training → Monitoring**

#### Defense in Depth for Data Protection

A **defense-in-depth** strategy uses multiple security controls rather than relying on a single protection mechanism.

| **Security Area**          | **AWS Services / Features**                        | **Purpose**                                                                   |
| -------------------------- | -------------------------------------------------- | ----------------------------------------------------------------------------- |
| **Identity access**        | **AWS IAM**                                        | Control who can access data and what actions they can perform                 |
| **Encryption**             | **AWS KMS**                                        | Protect data confidentiality and restrict decryption to authorized identities |
| **Network controls**       | **VPCs, security groups, network ACLs, firewalls** | Restrict network access to data and services                                  |
| **Monitoring and logging** | **AWS CloudTrail, Amazon CloudWatch**              | Provide visibility into activity and security events                          |

**IAM** can apply permissions to users, groups, and roles and use **conditions** to provide fine-grained access.

**AWS KMS** protects confidential data using encryption and ensures that only authorized identities can decrypt protected information

Network controls such as **Amazon VPC, security groups**, and **network ACLs (NACLs)** restrict how systems communicate with data resources.

#### CloudTrail vs. CloudWatch

| **Service**           | **Primary Security Use**                                                                        |
| --------------------- | ----------------------------------------------------------------------------------------------- |
| **AWS CloudTrail**    | Records AWS API activity and helps identify **who performed what action, when, and from where** |
| **Amazon CloudWatch** | Monitors metrics and logs and can generate alarms based on operational or security conditions   |

**Exam distinction:**
**Audit AWS API activity → CloudTrail**
**Monitor metrics/logs and create alarms → CloudWatch**

### 4.2 - Privacy and Compliance

AI systems frequently process sensitive information, making **data privacy** an important part of security and compliance.

#### PII and PHI

**Personally Identifiable Information (PII)** is information that can identify or be linked to an individual

Examples can include names, identification numbers, addresses, and other identifying data.

**Protected Health Information (PHI)** is individually identifiable **health information** that is protected under applicable healthcare privacy requirements such as **HIPAA**.

Protecting sensitive data is important because noncompliance can result in:
- Regulatory penalties
- Legal consequences
- Privacy violations
- Reputational damage

#### NIST

The **National Institute of Standards and Technology (NIST)** publishes cybersecurity, privacy, and risk-management guidance.

The **NIST AI Risk Management Framework (AI RMF)** provides guidance for managing risks associated with AI systems, including concerns around **privacy, security, transparency, and trustworthiness**.

#### HIPAA

The **Health Insurance Portability and Accountability Act (HIPAA)** is a U.S. regulation focused on protecting sensitive health information

Important HIPAA rules include:
- **Privacy Rule**
- **Security Rule**
- **Breach Notification Rule**

**Exam keyword:**
**Protect U.S. health information / PHI → HIPAA**

#### General Data Protection Regulation (GDPR)

The **General Data Protection Regulation (GDPR)** protects the privacy and personal data of individuals in the **European Union/European Economic Area**

GDPR can apply to organizations outside Europe when they process personal data in circumstances covered by the regulation.

**Exam keyword:**
**EU personal-data privacy → GDPR**

#### AWS Privacy Reference Architecture

The **AWS Privacy Reference Architecture (AWS PRA)** provides guidance for designing AWS environments with **privacy-related controls and capabilities**.

It can help organizations architect systems that support:
- Privacy requirements
- Data protection
- Governance
- Compliance objectives

#### Transparency

**Transparency** is important for both responsible AI and privacy compliance

Organizations should clearly communicate:
- What user data is collected
- Why it is collected
- How it is processed
- How it is stored
- How it is protected

This information is commonly communicated through **privacy notices or privacy policies**.

### 4.3 - Exam Focus

- **Ensure training data is correct and reliable → Accuracy**
- **Ensure required data is not missing → Completeness**
- **Detect or trace unauthorized changes to data → Integrity + data lineage**
- **Control user/role access to data → AWS IAM**
- **Encrypt sensitive data → AWS KMS**
- **Restrict network access → VPCs, security groups, NACLs, firewalls**
- **Audit AWS API activity → AWS CloudTrail**
- **Monitor metrics/logs and create alarms → Amazon CloudWatch**
- **Use multiple overlapping security controls → Defense in depth**
- **Information that identifies an individual → PII**
- **Protected identifiable health information → PHI**
- **U.S. healthcare privacy/security requirements → HIPAA**
- **EU personal-data privacy requirements → GDPR**
- **AI risk-management guidance → NIST AI RMF**
- **AWS guidance for implementing privacy controls → AWS Privacy Reference Architecture**
- **Clearly disclose data collection, storage, and processing practices → Transparency**

## 5 - AI System Security Risks and Threats

### 5.1 - AI System Security Risks and Threats

AI systems can be attacked through their **training data, inputs, outputs, or underlying AWS infrastructure**. Security requires both **threat detection** and **vulnerability/incident management**.

#### Data Poisoning

**Data poisoning** occurs when an attacker injects **false, biased, or malicious data** into training data.

This can cause the model to:
- Learn incorrect patterns
- Produce biased or harmful outputs
- Behave differently from its intended purpose

**Exam keyword:**
**Malicious modification of training data → Data poisoning**

#### Malicious Input and AI Misuse

Attackers may manipulate model inputs to make an AI system behave unexpectedly or perform unintended actions.

Possible outcomes include:
- Generating misinformation
- Producing copyrighted or otherwise restricted content
- Performing malicious tasks
- Bypassing intended model behavior

**Input sanitization** helps detect and remove potentially malicious input before it reaches the model.

Monitoring **model outputs** is also important because unexpected or abnormal outputs can indicate misuse or compromise.

#### Security Misconfiguration

Incorrectly configured security controls can expose AI systems to attack.

Common areas include:
- **IAM permissions**
- **Encryption**
- **Network access controls**
- Other security configurations

Following **least privilege**, encryption best practices, and secure network configuration reduces the risk of exploitation.

### 5.2 - Amazon GuardDuty

**Amazon GuardDuty** is an intelligent **threat detection** service that continuously monitors for suspicious or malicious activity in AWS environments.

It uses technologies including **machine learning and anomaly detection** to identify potential threats.

Use GuardDuty when the scenario involves:
- Detecting suspicious AWS activity
- Identifying anomalous behavior
- Detecting potential compromised resources or credentials
- Continuous threat monitoring

**Exam association:**
**Detect malicious or anomalous AWS activity → Amazon GuardDuty**

For AI systems, GuardDuty should be combined with application-level controls such as **input sanitization and model output monitoring**.

### 5.3 - Amazon Inspector and Vulnerability Management

**Amazon Inspector** is a vulnerability management service that automatically identifies software vulnerabilities and unintended network exposure across supported AWS workloads.

A typical **vulnerability management** process includes:
**Identify → Assess/Classify → Prioritize → Remediate → Monitor**

Amazon Inspector primarily supports the **identification and assessment of vulnerabilities**, helping organizations determine which vulnerabilities require remediation.

#### GuardDuty vs. Inspector

| **Service**          | **Primary Purpose**                                        | **Think**                    |
| -------------------- | ---------------------------------------------------------- | ---------------------------- |
| **Amazon GuardDuty** | Detect active or potential threats and suspicious behavior | **Threat detection**         |
| **Amazon Inspector** | Identify software vulnerabilities and exposure             | **Vulnerability management** |

**Exam distinction:**
**Suspicious malicious activity → GuardDuty**
**Known vulnerabilities in workloads → Inspector**

### 5.4 - Amazon Detective and Incident Response

**Amazon Detective** helps security teams **investigate security findings and incidents** by analyzing relationships and activity across AWS resources.

It is useful after suspicious activity has been detected because it helps determine:
- What happened
- Which resources were involved
- How events are related
- The possible scope and root cause of the incident

**Exam association:**
**Investigate security incidents and findings → Amazon Detective**

A useful security-service flow is:
**GuardDuty detects → Detective investigates → Security team responds**

### 5.5 - Incident Response Lifecycle

Incident response is the structured process used to detect, contain, remove, and recover from security incidents.

A typical lifecycle based on **NIST incident-response guidance** includes:

| **Phase**                  | **Purpose**                                                                |
| -------------------------- | -------------------------------------------------------------------------- |
| **Preparation**            | Establish security controls, processes, threat intelligence, and readiness |
| **Detection & Analysis**   | Monitor activity and determine whether an event is a security incident     |
| **Containment**            | Limit the spread and impact of malicious activity                          |
| **Eradication**            | Remove malware, compromised components, or root causes                     |
| **Recovery**               | Restore systems and services to normal operation                           |
| **Post-Incident Activity** | Review lessons learned and improve future defenses                         |

This process is **iterative**: lessons learned from an incident should improve future preparation and security controls

### 5.6 - Exam Focus

- **Inject malicious data into training data → Data poisoning**
- **Clean or validate potentially malicious model input → Input sanitization**
- **Detect abnormal or unintended model behavior → Monitor model outputs**
- **Detect suspicious or anomalous AWS activity → Amazon GuardDuty**
- **Scan for software vulnerabilities and unintended exposure → Amazon Inspector**
- **Investigate security findings and determine what happened → Amazon Detective**
- **Thread detection → GuardDuty**
- **Vulnerability management → Inspector**
- **Incident investigation → Detective**
- **GuardDuty detects → Detective investigates**
- **Preparation → Detection/Analysis → Containment → Eradication → Recovery → Lessons learned → Incident response lifecycle**
- **Misconfigured IAM, encryption, or network controls** can create exploitable security weaknesses

## 6 - Application and Infrastructure Security for AI Systems

### 6.1 - Application and Infrastructure Security for AI Systems

AI security covers both the **application layer** and the **underlying infrastructure** that stores data, runs models, and exposes AI services to users.

#### OWASP Top 10 for LLM Applications

The **OWASP Top 10 for LLM Applications** identifies common security risks affecting generative AI and large language model applications.

Important examples include:

| **Risk**                     | **Description**                                                                                          |
| ---------------------------- | -------------------------------------------------------------------------------------------------------- |
| **Prompt Injection**         | Malicious prompts manipulate an LLM into ignoring intended instructions or performing unintended actions |
| **Insecure output handling** | LLM output is trusted without validation, potentially enabling attacks such as XSS or code execution     |
| **Training data poisoning**  | Attackers manipulate training data to influence model behavior or introduce vulnerabilities              |

**Exam distinction:**
**Manipulate the model through crafted prompts → Prompt injection**
**Trust unsafe model output without validation → Insecure output handling**
**Tamper with training data → Training data poisoning**

### 6.2 - Amazon Bedrock Guardrails

**Guardrails for Amazon Bedrock** help apply safety and responsible-AI controls to generative AI applications.

Guardrail-style protections can include:
- Filtering undesirable or unsafe inputs and outputs
- Restricting certain topics or content
- Protecting sensitive information
- Applying consistent controls across model interactions

Additional application-level protections can include:
- **Input validation and sanitization**
- Controlled prompt templates
- Access controls
- Rate limiting
- Output validation and scanning

These controls help reduce risks such as **prompt injection, misuse, and unsafe model responses**.

### 6.3 - Security in the ML/AI Lifecycle

Security should be integrated throughout the **ML lifecycle and CI/CD pipeline**, rather than added only after deployment.

A typical secure lifecycle is:
**Data preparation → Build/Test → Evaluate → Stage → Deploy → Monitor → Incident response**

Key activities include:
- **Data preparation** → Validate data and reduce the risk of training data poisoning
- **Build and test** → Perform security testing and validate model behavior
- **Staging** → Scan and test before production deployment
- **Production** → Continuously monitor models and infrastructure
- **Incident response** → Quickly investigate and remediate security issues

This approach aligns with **MLOps** and secure development practices

### 6.4 - Securing AI Repositories and Model Artifacts

AI systems depend on several sensitive assets that should be protected from unauthorized access or modification:
- Training datasets
- Source code
- Model artifacts
- Configuration files
- Model repositories
- Backups of known-good models

Maintaining trusted backups of trained models allows an organization to **roll back** if a deployed model becomes corrupted, compromised, or vulnerable.

**Exam keyword:**
**Recover from a compromised model version → Restore a known-good model artifact**

### 6.5 - AWS WAF

**AWS Web Application Firewall (AWS WAF)** protects web applications from common **Layer 7 application attacks**.

AWS WAF uses **web ACLs (web access control lists)** containing rules that allow, block, or monitor web requests.

It can help protect against threats such as:
- **Cross-site scripting (XSS)**
- **SQL injection**
- Malicious HTTP requests
- Known attack patterns

**Exam association:**
**Filter malicious HTTP/web requests → AWS WAF**

### 6.6 - AWS Shield

**AWS Shield** protects applications against **Distributed Denial-of-Service (DDoS)** attacks that attempt to overwhelm resources and reduce availability.

AWS Shield integrates with services such as:
- **Amazon CloudFront**
- **Amazon Route 53**
- Other supported AWS networking and application services

**AWS Shield Advanced** provides enhanced DDoS protection and access to specialized AWS DDoS response support

#### AWS WAF vs. AWS Shield

| **Service**    | **Primary Protection**                                    |
| -------------- | --------------------------------------------------------- |
| **AWS WAF**    | Application-layer web attacks and malicious HTTP requests |
| **AWS Shield** | **DDoS attacks** affecting availability                   |

**Exam distinction:**
**XSS / SQL injection / malicious web requests → AWS WAF**
**DDoS protection → AWS Shield**

### 6.7 - Amazon Cognito

**Amazon Cognito** provides **customer identity and access management (CIAM)** for web and mobile applications.

It can manage:
- User sign-up
- User sign-in
- Authentication
- Application access
- User identity management

Security capabilities can include:
- Detection of suspicious authentication activity
- Protection against compromised credentials
- Additional verification for higher-risk sign-ins
- Authentication event logging

Cognito can also integrate with services such as **AWS WAF** to strengthen application protection.

**Exam distinction:**
**AWS workforce / resource permissions → IAM**
**Customer sign-up and sign-in for web / mobile applications → Amazon Cognito**

### 6.8 - Infrastructure Security for AI Systems

AI infrastructure should protect **data storage, compute resources, networks, and edge systems**

#### Protecting Stored Data

Use encryption to protect the **confidentiality of data at rest**.

**AWS KMS** can manage cryptographic keys used to encrypt sensitive data

**Stored AI data → Encryption → AWS KMS**

#### Protecting Compute Resources

Use **AWS IAM** to restrict access to compute platforms and other AWS resources.

Apply:
- **Least privilege**
- Role-based permissions
- Fine-grained access controls

This reduces the risk of unauthorized users modifying AI infrastructure or models.

#### Securing Edge Devices

**Edge devices** can have increased exposure because they may communicate with external networks or operate outside centralized cloud environments

Use **network segmentation** to isolate edge systems from sensitive internal resources

Network segmentation helps:
- Limit lateral movement by attackers
- Reduce the attack surface
- Prevent compromised edge devices from providing access to sensitive network segments

### 6.9 - Exam Focus

- **Manipulate an LLM using malicious instructions → Prompt injection**
- **Trust model output without validating it → Insecure output handling**
- **Modify training data maliciously → Training data poisoning**
- **Apply generative AI safety controls in Amazon Bedrock → Guardrails for Amazon Bedrock**
- **Integrate security throughout model development and deployment → Secure MLOps / CI/CD lifecycle**
- **Recover from a corrupted model** → Restore a **known-good model artifact**
- **Protect web applications from XSS, SQL injection, and malicious HTTP requests → AWS WAF**
- **Protect against DDoS attacks → AWS Shield**
- **Enhanced DDoS protection and response assistance → AWS Shield Advanced**
- **Customer sign-up/sign-in for web and mobile applications → Amazon Cognito**
- **AWS resource permissions → AWS IAM**
- **Encrypt stored AI data → AWS KMS**
- **Limit attacker movement from edge systems → Network segmentation**
- **WAF = web application attacks; Shield = DDoS; Cognito = customer authentication**

## 7 - Exam Tips

### 7.1 - Practice Question 1

#### Original Question

A healthcare organization is developing an AI-based solution to assist in patient diagnostics. The solution will access sensitive healthcare data, and the organization needs to ensure compliance with data protection regulations.

Which regulation should the organization comply with to protect patient data in the United States?

#### Choices

A. General Data Protection Regulation (GDPR)  
B. Health Insurance Portability and Accountability Act (HIPAA)  
C. Payment Card Industry Data Security Standard (PCI DSS)  
D. National Institute of Standards and Technology (NIST)

#### Correct Answer

**B. Health Insurance Portability and Accountability Act (HIPAA)**

#### Why?

**HIPAA** is a U.S. regulation that protects **protected health information (PHI)** and establishes privacy and security requirements for healthcare information

- **A. GDPR** → Focuses on protecting personal data of individuals in the **European Union/EEA**
- **C. PCI DSS** → Security standard for organizations that store, process, or transmit **payment card data**
- **D. NIST** → U.S. government organization that publishes security and risk-management frameworks and guidance; it **is not a regulation**

**Exam clue:**
**Healthcare + patient data + United States → HIPAA**

### 7.2 - Practice Question 2

#### Original Question

A company is planning to deploy a generative AI application on AWS to handle customer service requests. The application will process large amounts of customer data, and the company needs to ensure that only authorized users and services can access the system.

Which AWS service should be used to manage user access to the generative AI application?

#### Choices

A. AWS Identity and Access Management (IAM)  
B. AWS Key Management Service (AWS KMS)  
C. Elastic Load Balancing (ELB)  
D. AWS Systems Manager

#### Correct Answer

**A. AWS Identity and Access Management (IAM)**

#### Why?

**AWS IAM** manages **identities, roles, permissions, and access to AWS resources**, ensuring that only authorized users and services can perform permitted actions.

- **B. AWS KMS** → Manages cryptographic keys and supports **encryption/decryption**
- **C. Elastic Load Balancing** → Distributes incoming traffic across resources to improve **availability and scalability**
- **D. AWS Systems Manager** → Provides operational management and visibility for AWS resources, but it is not the primary service for defining AWS identity permissions

**Exam clue:**
**Who can access an AWS resource and what they can do → IAM**

### 7.3 - Practice Question 3

#### Original Question

A company is deploying a large language model for customer support. Developers are concerned about **prompt injection** and need a way to enforce input controls before prompts are sent to the model.

Which AWS feature can help mitigate these generative AI safety risks?

#### Choices

A. AWS Web Application Firewall (AWS WAF)  
B. AWS Key Management Service (AWS KMS)  
C. Guardrails for Amazon Bedrock  
D. Amazon S3

#### Correct Answer

**C. Guardrails for Amazon Bedrock**

#### Why?

**Guardrails for Amazon Bedrock** provide configurable safeguards for generative AI applications, including controls for **undesirable content, denied topics, sensitive information, and model inputs/outputs**

Application-level protections such as **input validation, sanitization, and controlled prompting** can be combine with Bedrock guardrails to reduce prompt-related risks

- **A. AWS WAF** → Protects web applications from malicious HTTP traffic and attacks such as **SQL injection** and **XSS**; it is not an LLM-specific prompt safety control
- **B. AWS KMS** → Protects data through **encryption and cryptographic key management**
- **D. Amazon S3** → Provides **object storage** and does not directly mitigate prompt injection.

**Exam clue:**
**Generative AI safety controls in Amazon Bedrock → Guardrails for Amazon Bedrock**

### 7.4 - Exam Focus

- **U.S. healthcare data / PHI → HIPAA**
- **EU personal-data privacy → GDPR**
- **Payment card information → PCI DSS**
- **Security frameworks and guidance → NIST**
- **Users, roles, permissions, and AWS resource access → AWS IAM**
- **Encryption and cryptographic keys → AWS KMS**
- **Traffic distribution and availability → Elastic Load Balancing**
- **Generative AI safety controls → Guardrails for Amazon Bedrock**
- **Web attacks such as XSS and SQL injection → AWS WAF**

A useful exam strategy is to identify the **scenario keyword** first:

**Healthcare → HIPAA**
**Access permissions → IAM**
**Encryption → KMS**
**Prompt/model safety → Bedrock Guardrails**
**Web application attacks → WAF**