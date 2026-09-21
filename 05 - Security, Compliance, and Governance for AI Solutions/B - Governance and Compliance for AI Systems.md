## 1 - Regulatory Compliance Standards for AI Systems

### 1.1 - Governance, Risk and Compliance (GRC)

**Governance, Risk, and Compliance (GRC)** is an important area of information security and is especially relevant to AI because AI systems depend heavily on data.

**Data governance** defines the processes and policies governing how data is used, including:
- Role and responsibilities
- Rules for accessing and using data
- Compliance and ethical data usage

Good data governance helps ensure that data used by AI systems meets **legal, regulatory, and ethical requirements**.

**AWS Config** supports governance by continuously tracking the **configuration and configuration changes of AWS resources**. It can help organizations:
- Detect resource **misconfigurations**
- Track configuration changes
- Demonstrate compliance during audits
- Maintain evidence that resources meet required configurations

**Exam association:**
**Track AWS resource configurations and configuration changes → AWS Config**

### 1.2 - Risk Management and Amazon Inspector

**Risk management** focuses on identifying and reducing the likelihood and impact of attacks, breaches, vulnerabilities, and exploitation.

**Amazon Inspector** is a **vulnerability management service** that automatically assesses AWS workloads for vulnerabilities and unintended network exposure.

It can help organizations:
- Identify software vulnerabilities
- Detect network exposure
- Assess security findings
- Assign **risk/severity scores** for prioritization
- Track findings for monitoring, documentation, and audits

This allows organizations to address the **highest-risk vulnerabilities first**.

**Exam association:**
**Scan AWS workloads for vulnerabilities and network exposure → Amazon Inspector**

### 1.3 - Major Compliance Frameworks

Compliance means meeting the requirements established by laws, regulations, and industry standards. Frameworks commonly require organizations to implement and monitor security controls protecting the **confidentiality, integrity, and availability (CIA)** of systems and data

| **Framework / Standard** | **Primary Focus**                                                                      |
| ------------------------ | -------------------------------------------------------------------------------------- |
| **PCI DSS**              | Protecting payment card and cardholder data                                            |
| **NIST**                 | Security standards and guidance, particularly for US government information systems    |
| **HIPAA**                | Privacy and security of **protected health information (PHI)** in the US               |
| **GDPR**                 | Privacy and protection of personal data belonging to individuals in the European Union |

**Key exam mappings:**
**Credit/debit card information → PCI DSS**
**US healthcare / PHI → HIPAA**
**EU personal data / privacy → GDPR**
**US government security guidance → NIST**

### 1.4 - ISO Information Security Standards

The **International Organization for Standardization (ISO)** develops international standards across many industries.

For information security, ISO works with the **International Electrotechnical Commission (IEC)** on the **ISO/IEC 27000 series**.

#### ISO/IEC 27001

**ISO/IEC 27001** defines requirements for establishing, implementing, maintaining, and continually improving an **Information Security Management System (ISMS)**

Organizations can obtain **ISO 27001 certification** by meeting its requirements.

#### ISO/IEC 27002

**ISO/IEC 27002** is a supporting standard that provides **guidelines and best practices for security controls** associated with an ISMS.

A useful distinction:

| **Standard**  | **Purpose**                                                         |
| ------------- | ------------------------------------------------------------------- |
| **ISO 27001** | Requirements for an ISMS; organizations can be certified against it |
| **ISO 27002** | Guidance and best practices for implementing security controls      |

AWS maintains certifications for standards including **ISO 27001, ISO 27017, and ISO 27018**

### 1.5 - SOC Reports

**System and Organization Controls (SOC)** reports assess an organization's internal controls.

| **SOC Report** | **Focus**                                                |
| -------------- | -------------------------------------------------------- |
| **SOC 1**      | Controls relevant to **financial reporting**             |
| **SOC 2**      | Controls related to **trust services/security controls** |
| **SOC 3**      | Public/general-use summary based on SOC 2 information    |

**SOC 3** is useful when organizations need to provide customers or external parties with a publicly distributable description of their security controls.

#### SOC Type 1 vs Type 2

SOC 1 and SOC 2 reports can be issued as **Type 1** or **Type 2**

| **Type**   | **Meaning**                                        |
| ---------- | -------------------------------------------------- |
| **Type 1** | Evaluates controls at a **specific point in time** |
| **Type 2** | Evaluates controls over a **period of time**       |

Memory aid:
**Type 1 → Point in time**
**Type 2 → Period of time**

### 1.6 - AWS Artifact

**AWS Artifact** provides on-demand access to **AWS security and compliance reports, certifications, and agreements**.

It can provide documents related to frameworks such as:
- **ISO**
- **PCI DSS**
- **SOC**

AWS Artifact is especially useful when organizations need **AWS compliance documentation for auditors or regulators**.

However, under the **AWS Shared Responsibility Model**, customers remain responsible for demonstrating the compliance of **their own workloads, configurations, processes, and controls**. AWS Artifact provides AWS's compliance evidence; it does not automatically make a customer's application compliant.

**Exam association:**
**Download AWS compliance reports/certifications → AWS Artifact**

### 1.7 - Accountability, Transparency, and AI Regulation

Compliance and responsible AI also depend on **accountability** and **transparency**.

#### Accountability

Accountability ensures that people and organizations can be held responsible for actions involving AI systems.

It can be supported through:
- Detailed **logging and audit trails**
- Identifying **who performed an action, what occurred, when, and where**
- Clearly assigned roles and responsibilities
- Responsibility for legal and regulatory consequences

#### Transparency

**Transparency** means being open with users about how AI systems and their data are used.

Organizations should clearly communicate:
- How user data is collected
- How data is processed
- How long data is retained
- How data may be shared
- Available options for deleting data
- Options for opting out of certain data collection

**Terms of service and privacy notices** can help provide this transparency.

Accountability + Transparency → **Responsible and ethical AI usage**

Governments are increasingly developing regulations specifically addressing AI systems, including issues such as **automated decision-making, accountability, transparency, and bias**

Examples include:
- **European Union AI Act** - regulatory framework governing AI systems within the EU
- **New York City rules concerning automated decision systems/tools** - address concerns such as **bias in automated decision-making**

### 1.8 - Exam Focus

Focus on recognizing the AWS service or compliance framework from scenario keywords:

- **Track configuration changes / detect resource misconfigurations / compliance configuration history → AWS Config**
- **Find vulnerabilities and unintended network exposure → Amazon Inspector**
- **Obtain AWS compliance reports and certifications → AWS Artifact**
- **Payment card data → PCI DSS**
- **Protected health information (PHI) → HIPAA**
- **EU personal data/privacy → GDPR**
- **US government security guidance → NIST**
- **Information Security Management System requirements → ISO 27001**
- **Security control implementation guidance/best practices → ISO 27002**
- **Financial reporting controls → SOC 1**
- **Trust services/security controls → SOC 2**
- **Public/general-use SOC report → SOC 3**
- **Snapshot at a specific time → SOC Type 1**
- **Controls evaluated over a period of time → SOC Type 2**
- **Logs, roles, responsibility for actions → Accountability**
- **Explain data collection, processing, retention, and sharing to users → Transparency**

## 2 - AWS Services for GRC

### 2.1 - AWS Config - Governance and Configuration Tracking

**AWS Config** supports governance by recording and evaluating the **configuration of AWS resources** and tracking changes over time.

It helps organizations:
- Track **configuration changes**
- Detect **misconfigurations**
- Assess resources against compliance requirements
- Provide configuration history for **audits**

For AI workloads, AWS Config can help demonstrate that supporting AWS resources remain configured according to organizational and regulatory requirements.

**Exam association:**
**Track resource configuration changes / detect noncompliant configurations → AWS Config**

### 2.2 - Amazon Inspector - Vulnerability Management

**Amazon Inspector** is a **vulnerability management** service that continuously scans AWS workloads for vulnerabilities and unintended network exposure.

It helps organizations:
- Identify software vulnerabilities
- Detect network exposure
- Assess and classify findings
- Prioritize vulnerabilities based on **severity/risk**
- Track findings for remediation, monitoring, and auditing

The main purpose is to reduce security risk by identifying vulnerabilities that should be addressed first.

**Exam association:**
**Scan workloads for vulnerabilities and network exposure → Amazon Inspector**

### 2.3 - Amazon Detective - Security Investigation

**Amazon Detective** helps security teams **investigate security incidents and determine root cause**.

It automatically collects and analyzes security-related data from AWS sources and presents relationships between resources, users, and events in a centralized view.

Use Detective when the scenario involves:
- Investigating a security finding
- Understanding **how an incident occurred**
- Determining the **root cause**
- Analyzing relationships surrounding suspicious activity

**Exam association:**
**Investigate a security incident / determine root cause → Amazon Detective**

### 2.4 - AWS Audit Manager - Audit Evidence Collection

**AWS Audit Manager** helps continuously assess AWS usage and automatically collect **audit evidence** for governance, risk, and compliance activities.

Key capabilities include:
- Collecting evidence related to security controls
- Managing evidence centrally
- Supporting **internal and external audits**
- Monitoring active assessments
- Searching for evidence required by auditors
- Tracking modifications to evidence to help maintain **evidence integrity**

Audit Manager can help organizations demonstrate compliance with regulations, standards, and compliance frameworks.

#### Audit Manager vs AWS Artifact

| **Service**           | **Primary Purpose**                                                    |
| --------------------- | ---------------------------------------------------------------------- |
| **AWS Audit Manager** | Collect, organize, and manage **audit evidence** from your environment |
| **AWS Artifact**      | Access AWS **compliance reports, certifications, and agreements**      |

Memory aid:
- **Audit Manager → Your audit evidence**
- **Artifact → AWS compliance documents**

### 2.5 - AWS Artifact - Compliance Documentation

**AWS Artifact** provides on-demand access to AWS **security and compliance documents**, including reports and certifications.

Documents can support compliance requirements involving standards such as:
- **ISO**
- **PCI DSS**
- **SOC**

AWS Artifact provides evidence of **AWS's compliance**, but customers remain responsible for documenting and demonstrating the compliance of their own workloads and controls.

**Exam association:**
**Download AWS compliance reports/certifications → AWS Artifact**

### 2.6 - AWS Trusted Advisor - AWS Best Practices

**AWS Trusted Advisor** evaluates an AWS environment against recommended AWS best practices and provides recommendations for improvement.

It aligns recommendations with the six pillars of the **AWS Well-Architected Framework**:

1. **Operational Excellence**
2. **Security**
3. **Reliability**
4. **Performance Efficiency**
5. **Cost Optimization**
6. **Sustainability**

Trusted Advisor can recommend remediation actions that improve configuration and overall security posture.

**Exam association:**
**AWS best-practice recommendations / Well-Architected guidance → AWS Trusted Advisor**

### 2.7 - AWS CloudTrail and Amazon GuardDuty

#### AWS CloudTrail

**AWS CloudTrail** records **API activity and account activity** in AWS.

Logs can include:
- Who performed an action
- What API action occurred
- When it occurred
- Source IP address
- Whether the API call succeeded or failed

CloudTrail is important for **auditing, accountability, investigation, and compliance**.

**Exam association:**
**Record AWS API calls / determine who performed an action → AWS CloudTrail**

#### Amazon GuardDuty

**Amazon GuardDuty** is an intelligent **threat detection** service that continuously monitors AWS environments for suspicious or malicious activity.

It analyzes multiple AWS data sources and uses **machine learning, anomaly detection, and threat intelligence** to generate security findings.

Use GuardDuty when the scenario involves:
- Detecting malicious activity
- Detecting unusual behavior
- Identifying potential compromised resources or credentials
- Continuous AWS threat monitoring

#### CloudTrail vs GuardDuty

| **Service**    | **Main Purpose**                                            |
| -------------- | ----------------------------------------------------------- |
| **CloudTrail** | **Record** API and account activity                         |
| **GuardDuty**  | **Detect threats** and suspicious activity                  |
| **Detective**  | **Investigate** security incidents and determine root cause |

Memory flow:
**CloudTrail → Record activity → GuardDuty → Detect threats → Detective → Investigate**

### 2.8 - AWS Security Hub - Centralized Security Management

**AWS Security Hub** provides a centralized location for managing and aggregating security findings from AWS security services and supported third-party tools.

It supports:
- **Continuous security monitoring**
- Aggregation of security findings
- Centralized security visibility
- Integration with security services and SIEM tools
- Automated security response workflows
- **Cloud Security Posture Management (CSPM)**
- Security checks against compliance standards

Security Hub can evaluate an AWS environment against security standards and frameworks such as **PCI DSS** and **NIST SP 800-53**.

Think of Security Hub as the **central aggregation and security posture layer** across multiple AWS security services.

| **Service**             | **Key Exam Keyword**               |
| ----------------------- | ---------------------------------- |
| **AWS Config**          | Configuration compliance           |
| **Amazon Inspector**    | Vulnerabilities                    |
| **Amazon Detective**    | Investigation/root cause           |
| **AWS Audit Manager**   | Audit evidence                     |
| **AWS Artifact**        | Compliance documents               |
| **AWS Trusted Advisor** | Best-practice recommendations      |
| **AWS CloudTrail**      | API activity/logging               |
| **Amazon GuardDuty**    | Threat detection                   |
| **AWS Security Hub**    | Centralized security findings/CSPM |

### 2.9 - Exam Focus

Memorize the scenario-to-service mappings:

- **Track resource configuration changes and compliance → AWS Config**
- **Scan workloads for vulnerabilities/network exposure → Amazon Inspector**
- **Investigate an incident and determine root cause → Amazon Detective**
- **Automatically collect and manage evidence for an audit → AWS Audit Manager**
- **Access AWS SOC, ISO, or PCI compliance reports → AWS Artifact**
- **Receive AWS best-practice and Well-Architected recommendations → AWS Trusted Advisor**
- **Record who made an AWS API call and when → AWS CloudTrail**
- **Detect suspicious or malicious AWS activity → Amazon GuardDuty**
- **Aggregate security findings into a centralized dashboard → AWS Security Hub**
- **Assess security posture against standards such as PCI DSS/NIST → AWS Security Hub**

High-value distinction:
**CloudTrail records → GuardDuty detects → Detective investigates → Security Hub aggregates**

For compliance:
**AWS Config → Configuration compliance**
**Audit Manager → Audit evidence**
**AWS Artifact → AWS compliance reports**

## 3 - AWS Dashboard Features for AI Security

### 3.1 - IAM Policies for Amazon Bedrock and SageMaker

**AWS Identity and Access Management (IAM)** policies control which AWS actions users, roles, and services are allowed to perform.

A read-only AI policy may allow actions such as:
- **Amazon Bedrock** `Get` and `List` actions
- Selected **Amazon SageMaker** read actions
- Access across specified AWS resources

IAM policies can also include **conditions** that restrict when permissions apply. For example, SageMaker read actions can be permitted only when the request is made **through Amazon Bedrock**.

Key principle:
**IAM → Fine-grained permissions and least-privilege access to AI services**

### 3.2 - Guardrails for Amazon Bedrock

**Guardrails for Amazon Bedrock** provides configurable safeguards for generative AI applications.

Guardrails can help address risks associated with the **OWASP Top 10 for Large Language Model (LLM) Applications**.

Important capabilities include:
- **Prompt/input filtering** → Helps block undesirable or harmful inputs
- **Sensitive information filters** → Detect or filter **PII**, such as Social Security numbers
- **Output controls** → Restrict undesirable model responses
- **Contextual grounding checks** → Evaluate whether responses are supported by provided source information

Contextual grounding is particularly useful for reducing **hallucinations** by checking whether generated responses are grounded in relevant factual context.

**Exam association:**
**Apply safety, content, PII, and grounding controls to Bedrock model interactions → Guardrails for Amazon Bedrock**

### 3.3 - AWS Config Managed Rules

**AWS Config** provides centralized visibility into AWS resource configurations and tracks **configuration changes** over time.

**AWS Config Managed Rules** are predefined rules maintained by AWS that evaluate whether resources comply with desired configurations.

They help with:
- Detecting **noncompliant resources**
- Monitoring configuration changes
- Supporting governance and audits
- Continuously checking security and compliance requirements

**Exam association:**
**Automatically evaluate AWS resource configurations against predefined rules → AWS Config Managed Rules**

### 3.4 - AWS Config Conformance Packs

**AWS Config conformance packs** bundle multiple Config rules and remediation actions into a single deployable compliance framework.

AWS provides **sample conformance pack templates** aligned with established security and compliance standards, such as **PCI DSS**.

This allows organizations to evaluate many related compliance controls consistently across AWS environments.

#### Managed Rules vs Conformance Packs

| **Feature**                 | **Purpose**                                                                            |
| --------------------------- | -------------------------------------------------------------------------------------- |
| **AWS Config Managed Rule** | Evaluates a specific configuration requirement                                         |
| **Conformance Pack**        | Groups multiple Config rules and remediation actions for broader compliance objectives |

Memory aid:
- **Config Rule** → **One compliance check**
- **Conformance Pack → Collection of compliance checks**

### 3.5 - Exam Focus

- **Control permissions for Bedrock / SageMaker resources → IAM policies**
- **Restrict permissions based on how a service is accessed → IAM policy conditions**
- **Filter harmful prompts or model outputs → Guardrails for Amazon Bedrock**
- **Detect/filter sensitive information such as PII → Bedrock Guardrails**
- **Check whether generated answers are supported by source context → Contextual grounding checks**
- **Continuously track AWS resource configurations → AWS Config**
- **Evaluate a resource against a predefined configuration requirement → AWS Config Managed Rules**
- **Apply a collection of compliance rules aligned to frameworks such as PCI DSS → AWS Config conformance packs**

High-value distinction:
- **IAM → Who/what can access AI services**
- **Bedrock Guardrails → What AI inputs/outputs are permitted**
- **AWS Config → Whether AWS resources remain compliantly configured**

## 4 - Data Governance Strategies

### 4.1 - Data Lifecycle and Governance

Effective **data governance** should cover the entire **data lifecycle:**

**Collection → Processing → Classification → Storage → Consumption → Archival/Backup → Disposal**

Governance policies determine how data is collected, processed, retained, shared, and eventually deleted.

Before storing data, organizations should **classify it according to sensitivity and compliance requirements**. Highly sensitive data requires stronger controls because exposure may cause security, financial, legal, or reputational damage.

Common considerations include:
- **Data sensitivity**
- **Privacy requirements**
- **Encryption**
- **Retention periods**
- **Data residency and sovereignty**
- **Secure disposal**

### 4.2 - Data Privacy, Residency, and Sovereignty

**Data residency** refers to requirements concerning the **geographic location where data is stored**.

Compliance frameworks may also define:
- How long data must be retained
- How personal information can be collected and processed
- What security controls must protect that information

For example, **GDPR** establishes privacy requirements for personal data associated with individuals in the European Union.

**Data sovereignty** means that data is subject to the **laws and governance requirements of the jurisdiction in which it is stored or processed**. Some countries impose requirements concerning where certain categories of data must be stored.

Key distinction:

| **Concept**          | **Meaning**                                    |
| -------------------- | ---------------------------------------------- |
| **Data residency**   | Where data is physically/geographically stored |
| **Data sovereignty** | Laws and jurisdiction governing the data       |
| **Data retention**   | How long data must be kept                     |

### 4.3 - Amazon S3 Object Lock

**Amazon S3 Object Lock** protects S3 objects from deletion or overwrite using a **Write Once, Read Many (WORM)** model.

It supports **data immutability**, which is valuable for:
- Regulatory compliance
- Audit records
- Protection against accidental or malicious deletion
- Long-term retention requirements

#### Compliance Mode vs Governance Mode

| **Mode**            | **Behavior**                                                                                                      |
| ------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **Compliance mode** | Protected objects cannot be deleted or overwritten during the retention period, even by the AWS account root user |
| **Governance mode** | Users with specific permissions can bypass retention protection when necessary                                    |

Memory aid:
- **Compliance mode → Strictest protection**
- **Governance mode → Authorized bypass possible**

#### Legal Holds

An **S3 Object Lock legal hold** prevents an object from being deleted or overwritten until the hold is explicitly removed.

Unlike a retention period, a legal hold does **not require a predefined expiration date**.

Typical use case:
**Litigation / legal discovery → Legal hold**

### 4.4 - Archival, Backup, and Availability

When data is no longer frequently accessed but must still be retained, it can move into an **archival stage**.

AWS storage options include:
- **S3 Intelligent-Tiering** → Automatically optimizes storage costs based on changing access patterns
- **S3 Glacier storage classes** → Cost-effective storage for long-term archival
- **S3 Glacier Deep Archive** → Very low-cost storage for rarely accessed, long-term data

**AWS backup** provides centralized capabilities for protecting supported AWS resources through backups.

Backups improve **resilience and availability** by allowing organizations to recover data after:
- Accidental deletion
- Corruption
- Security incidents
- Other disasters

**Exam association:**
**Centralized AWS backup management → AWS Backup**

### 4.5 - Responsible Data Disposal

When data is no longer required by the business or applicable compliance requirements, it should be **securely deleted**.

Responsible disposal:
- Reduces unnecessary storage
- Reduces the amount of sensitive information exposed to attack
- Helps meet privacy and retention requirements
- Reduces the potential impact of a future data breach

Data should not simply be kept indefinitely unless there is a valid business or regulatory reason.

### 4.6 - Logging and Monitoring AI Systems

Two important AWS monitoring and auditing services are:

| **Service**           | **Primary Purpose**                                        |
| --------------------- | ---------------------------------------------------------- |
| **Amazon CloudWatch** | Monitor metrics, logs, alarms, and operational performance |
| **AWS CloudTrail**    | Record AWS API and account activity for auditing           |

For AI systems, logging and monitoring should extend beyond infrastructure health.

Important areas to monitor include:
- **Model inputs and outputs** → Detect prompt injection, misuse, and abnormal behavior
- **Performance metrics** → Detect degradation or availability problems
- **Security events** → Failed logins, unauthorized access, or unusual data activity
- **Infrastructure** → Monitor compute, networking, and storage resources
- **Responsible AI concerns** → Monitor for bias and inappropriate system behavior
- **Copyright and intellectual property risks** → Identify potential policy or compliance issues

Monitoring availability-related metrics can also help identify potential attacks such as **Distributed Denial-of-Service (DDoS)** activity.

### 4.7 - Governance for Responsible AI

AI governance must consider more than traditional security controls.

Organizations should monitor AI systems for risks involving:
- **Bias and fairness**
- **Privacy**
- **Data misuse**
- **Copyright and intellectual property**
- **Security threats**
- **Regulatory compliance**

These controls help organizations maintain **responsible AI practices** throughout the AI and data lifecycle.

### 4.8 - Exam Focus

- **Classify data before applying protection controls → Data classification**
- **Where data must be stored geographically → Data residency**
- **Which jurisdiction's laws govern data → Data sovereignty**
- **How long data must be kept → Data retention**
- **Prevent S3 objects from deletion/overwrite using WORM → S3 Object Lock**
- **Retention cannot be bypassed, even by root → Object Lock Compliance mode**
- **Authorized users can bypass retention → Object Lock Governance mode**
- **Preserve data indefinitely for litigation/discovery → Legal hold**
- **Automatically optimize S3 storage by access pattern → S3 Intelligent-Tiering**
- **Long-term, rarely accessed archival data → S3 Glacier / Glacier Deep Archive**
- **Centralized backup and recovery of AWS resources → AWS Backup**
- **Operational metrics, logs, and alarms → Amazon CloudWatch**
- **AWS API and account activity auditing → AWS CloudTrail**

High-value lifecycle:
**Collect → Process → Classify → Securely Store → Consume → Archive/Backup → Delete**

## 5 - Governance Protocols

### 5.1 - Policies, Processes, and Procedures

Governance begins with **policies**, which provide high-level direction for how an organization should operate.

A policy should align information security and AI governance activities with the organization's:
- Mission and values
- Business objectives
- Compliance obligations
- Regulatory requirements

For example, a **privacy policy** may define high-level expectations for protecting customer data and **personally identifiable information (PII)**.

Policies are supported by **processes** and **procedures**.

| **Component** | **Purpose**                                                 |
| ------------- | ----------------------------------------------------------- |
| **Policy**    | Defines high-level direction and expectations               |
| **Process**   | Defines the activities used to achieve the policy objective |
| **Procedure** | Defines the detailed steps for performing a task            |

Memory aid:
- **Policy → What/Why**
- **Process → How at a high level**
- **Procedure → Exact steps**

### 5.2 - Policy Review Cadence

Governance policies are **living documents** and should be reviewed regularly as AI systems, business requirements, and regulations evolve.

Policy reviews may consider areas such as:
- **Model performance**
- **Data management**
- **Model training**
- **Human safety**
- **Responsible AI**
- Compliance and regulatory changes

The appropriate review frequency should depend on the organization's **risk profile, scale, and complexity**.

Possible review schedules include:
- Monthly
- Quarterly
- Semiannually
- Annually

Higher-risk or rapidly changing AI systems may require more frequent review.

### 5.3 - Stakeholder Representation

AI governance should involve a **diverse set of stakeholders** rather than relying only on technical teams.

Relevant participants may include:
- Technical teams
- Organizational leadership
- Legal and compliance teams
- Subject matter experts
- Internal and external experts
- Verified end users or customer representatives

Broad stakeholder participation helps identify technical, legal, ethical, operational, and user-impact risks.

### 5.4 - Technical and Non-Technical Reviews

AI systems should be reviewed from both **technical** and **non-technical** perspectives.

| **Review Type**          | **Focus**                                                       |
| ------------------------ | --------------------------------------------------------------- |
| **Technical review**     | Model performance, data quality, algorithms, system behavior    |
| **Non-technical review** | Legal, regulatory, compliance, policy, and governance concerns. |

A **technical review** may examine whether the model is accurate, reliable, and functioning as intended.

A **non-technical review** evaluates whether the AI solution complies with organizational policies, applicable regulations, and responsible AI requirements.

### 5.5 - Testing AI Systems

**Testing** validates that an AI system produces expected outputs and behaves as intended before deployment.

Testing can help identify:
- Incorrect or unexpected outputs
- Performance issues
- Bias
- Safety concerns
- Other undesirable model behavior

Testing is an important control before releasing an AI solution into production.

### 5.6 - Intervention and Escalation

Organizations should define clear governance processes for **when and how humans intervene** when reviews or testing identify problems.

Examples include:
- Detecting **AI bias**
- Identifying unsafe model behavior
- Discovering regulatory violations
- Finding unacceptable model performance
- Detecting inappropriate or harmful outputs

Clear decision-making and escalation procedures allow organizations to address problems before they create larger operational, legal, or reputational risks.

This supports **human oversight** and responsible AI governance.

### 5.7 - Exam Focus

- **High-level governance direction and expectations → Policy**
- **Activities used to achieve a policy objective → Process**
- **Detailed step-by-step instructions → Procedure**
- **Policies should be regularly reviewed** → Based on **risk, complexity, and organizational needs**
- **Model performance, data quality, algorithms → Technical review**
- **Legal, regulatory, compliance, and policy concerns → Non-technical review**
- **Validate model behavior before deployment → Testing**
- **Include technical, legal, leadership, SME, and end-user perspectives → Diverse stakeholder participation**
- **Define actions when bias or unsafe behavior is detected → Intervention / escalation procedures**
- **Human involvement in problematic AI decisions → Human oversight**

High-value hierarchy:

**Policy → Process → Procedure**

High-value governance flow:

**Create policy → Review regularly → Involve stakeholders → Perform technical / non-technical reviews → Test → Intervene when necessary**

## 6 - Governance Frameworks

### 6.1 - Generative AI Security Scoping Matrix

The **Generative AI Security Scoping Matrix** helps organizations determine appropriate security responsibilities across the AI lifecycle.

It considers controls such as:
- **Identity and Access Management (IAM)**
- Application security
- Infrastructure security
- Privacy
- Data protection

The matrix uses **Scopes 1-5**. As the scope increases, the organization has **more control over the AI solution**, but also assumes **greater security responsibility**.

| **Scope**   | **AI Use Case**                                  | **Organization's Control** |
| ----------- | ------------------------------------------------ | -------------------------- |
| **Scope 1** | Public consumer application                      | Very low                   |
| **Scope 2** | Enterprise application                           | Low                        |
| **Scope 3** | Application using a pre-trained foundation model | Moderate                   |
| **Scope 4** | Fine-tuned/customized model                      | High                       |
| **Scope 5** | Self-trained model built from scratch            | Highest                    |

Memory aid:
**Higher scope → More control → More security responsibility**

### 6.2 - Scope 1 - Public Consumer Applications

**Scope 1** covers public generative AI applications where the organization does not control:
- The underlying model
- Training data
- Model development

Examples include public AI applications such as **Amazon PartyRock** or other externally provided generative AI tools

The AI provider manages most of the underlying model and infrastructure security.

### 6.3 - Scope 2 - Enterprise Applications

**Scope 2** covers vendor-provided **enterprise AI applications** that are tailored for organizational use.

An example is **Amazon Q**, which can integrate with enterprise environments and organizational data

These applications may perform tasks such as:
- Summarizing business information
- Drafting content
- Assisting employees using company data

Compared with Scope 1, organizations have more business integration and customization, but the vendor still controls the underlying AI model.

### 6.4 - Scope 3 - Pre-Trained Foundation Models

In **Scope 3**, the organization develops its own application but uses an existing **pre-trained foundation model (FM)**.

Examples include foundation models accessed through **Amazon Bedrock**.

The organizations typically:
- Builds the AI application
- Integrates the foundation model through **APIs**
- Controls application behavior and surrounding workloads
- Does not train the underlying foundation model from scratch

**Exam association:**
**Build your own app using an existing foundation model → Scope 3**

### 6.5 - Scope 4 - Fine-Tuned or Customized Models

**Scope 4** involves customizing an existing model using organization-specific data.

Examples include:
- **Amazon Bedrock model customization**
- **Amazon SageMaker JumpStart** models that are further customized

Fine-tuning allows a model to produce responses more closely aligned with specific organizational requirements, terminology, styles, or tasks.

Example:

Training with existing physician documentation so the model generates documentation consistent with organizational conventions.

Compared with Scope 3, Scope 4 introduces additional responsibility because the organization influences the model's behavior through **custom training data**.

**Exam association:**
**Customize an existing foundation model with your own data → Scope 4**

### 6.6 - Scope 5 - Self-Trained Models

**Scope 5** represents models that an organization develops and trains **from scratch**, rather than starting from an existing foundation model.

The organization has maximum control over:
- Model architecture
- Training
- Training data
- Deployment
- Security controls
- Model lifecycle

This also creates the **highest level of security and governance responsibility**

**Exam association:**
**Build and train the model from scratch → Scope 5**

High-value progression:
**Public app → Enterprise app → Pre-trained FM → Fine-tuned FM → Self-trained model**

### 6.7 - Attack Surface and AI Data Flows

Effective AI risk management requires understanding the **attack surface** and how data moves through the AI system.

Important data flows may include:
**Training data → Model → AI application → User prompt → Model response → Application response**

Security teams should understand interactions among:
- Training data
- Foundation/pre-trained models
- Application databases
- User prompts
- Model completions
- End-user responses

This helps identify where security controls should be implemented.

**Data origin and data lineage** are especially important because organizations need to understand where training data came from and how it has been transformed or used.

### 6.8 - Transparency Standards

**Transparency** is a core principle of responsible AI.

Organizations should provide clear information about:
- The AI system's intended purpose
- Model limitations
- Relevant training data information
- Model development processes
- How the AI system works at an appropriate level for users

This information should be made accessible to relevant users and stakeholders.

Transparency helps users understand what an AI system **can and cannot reliably do**.

### 6.9 - Feedback and Stakeholder Collaboration

AI governance should include feedback from a **diverse group of stakeholders**, such as:
- Developers
- Legal and compliance teams
- Leadership
- Subject matter experts
- End users

Organizations should establish clear **feedback channels** so risks and issues can be identified throughout the AI lifecycle.

Cross-functional collaboration is particularly useful for identifying issues involving:
- Bias
- Privacy
- Security
- Regulatory compliance
- User impact

### 6.10 - Training for Responsible AI

Teams involved in AI development should receive **ongoing training** on:
- Responsible AI practices
- Ethical AI development
- Security requirements
- Governance policies
- Regulatory and compliance changes

Continuous education helps ensure that employees understand their responsibilities as AI technologies and regulations evolve.

### 6.11 - Types of AI Bias

AI systems can exhibit several forms of **bias** that may result in unfair or inaccurate outcomes.

| **Bias Type**         | **Meaning**                                                           | **Example**                                                                         |
| --------------------- | --------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| **Algorithmic bias**  | Algorithms produce systematically unfair or discriminatory outcomes   | Hiring system disproportionately selecting candidates from one demographic          |
| **Confirmation bias** | Data or model behavior reinforces existing assumptions or stereotypes | Image generator repeatedly associating an occupation with one gender or demographic |
| **Selection bias**    | Training data does not adequately represent the target population     | Training only on online survey responses while excluding offline participants       |

#### Algorithmic Bias

**Algorithmic bias** occurs when the model or algorithm produces unfair or discriminatory results.

It can affect high-impact use cases such as:
- Hiring
- Lending
- Healthcare
- Automated decision-making

#### Confirmation Bias

**Confirmation bias** occurs when training data or model behavior reinforces existing stereotypes or assumptions.

For generative AI, this may appear when the model repeatedly associates specific occupations, roles, or characteristics with particular demographic groups.

#### Selection Bias

**Selection bias** occurs when training data is collected from a sample that is **not representative of the broader population**.

This can cause the model to produce inaccurate or misleading conclusions when deployed to a broader group.

### 6.12 - Exam Focus

- **Framework for determining security responsibility based on how an AI solution is built → Generative AI Security Scoping Matrix**
- **Public AI application with no model/training-data control → Scope 1**
- **Vendor-provided enterprise AI application → Scope 2**
- **Build your own application using a pre-trained foundation model → Scope 3**
- **Fine-tune/customize an existing model using organizational data → Scope 4**
- **Build and train a model from scratch → Scope 5**
- **More AI development control → More security responsibility**
- **Understand where data originates and how it moves through the system → Data lineage and data flow analysis**
- **Publish intended use, development details, and limitations → Transparency**
- **Include technical, legal, leadership, and end-user input → Stakeholder collaboration**
- **Unfair outcomes caused by model algorithms → Algorithmic bias**
- **Reinforcement of existing stereotypes or assumptions → Confirmation bias**
- **Non-representative training dataset → Selection bias**

High-value scope memory aid:

**1 Public → 2 Enterprise → 3 Pre-trained → 4 Fine-tuned → 5 Self-trained**
**Scope ↑ → Control ↑ → Responsibility ↑**

## 7 - Exam Tips

### 7.1 - Practice Question 1

#### Original Question

A global company is developing an AI-based system that will process sensitive customer data across multiple regions. The legal and compliance teams need to ensure that the system complies with data protection laws and regulations.

Which **two** considerations should the company prioritize to meet legal and regulatory requirements?

#### Choices

A. Compliance with data privacy regulations  
B. Data sovereignty requirements  
C. Optimizing AI model performance  
D. Increasing cloud storage capacity for data processing

#### Correct Answer

**A. Compliance with data privacy regulations**  
**B. Data sovereignty requirements**

#### Why?

**Data privacy regulations** directly govern how sensitive and personal data is collected, processed, stored, and protected. Examples include **GDPR, HIPAA,** and other applicable regulatory frameworks.

**Data sovereignty** concerns the legal jurisdiction and control that applies to data, including requirements that certain data be stored or processed within particular geographic boundaries.

- **C s incorrect:** Model performance is important technically but does not directly satisfy legal or regulatory requirements.
- **D is incorrect:** Storage capacity is an infrastructure concern rather than a compliance requirement.

### 7.2 - Practice Question 2

#### Original Question

A company is deploying a large language model for customer support and needs full accountability and traceability of all API calls made by users and AWS services interacting with the model.

The company needs to record both successful and failed API calls and retain the activity for auditing and compliance.

Which AWS service should be used?

#### Choices

A. Amazon CloudWatch  
B. AWS Config  
C. AWS CloudTrail  
D. AWS Lambda

#### Correct Answer

**C. AWS CloudTrail**

#### Why?

**AWS CloudTrail** records AWS **API and account activity**, including information such as:
- API action performed
- User or identity making the request
- Time of the request
- Source IP address
- Successful and failed API activity

This makes CloudTrail appropriate for **auditability, accountability, and compliance**

| **Service**    | **Primary Purpose**                                     |
| -------------- | ------------------------------------------------------- |
| **CloudTrail** | Record API/account activity                             |
| **CloudWatch** | Metrics, logs, monitoring, and alarms                   |
| **AWS Config** | Track resource configurations and configuration changes |
| **AWS Lambda** | Run event-driven code                                   |

Memory aid:
**CloudTrail → Who did what and when**

### 7.3 - Practice Question 3

#### Original Question

A company is implementing an information security management system and needs to understand the difference between **ISO 27001** and **ISO 27002**.

Which statement best describes the difference?

#### Choices

A. ISO 27001 is a set of recommended practices for security controls, while ISO 27002 outlines requirements for risk assessment.  
B. ISO 27001 specifies requirements for establishing, implementing, and maintaining an ISMS, while ISO 27002 provides guidelines for implementing security controls.  
C. ISO 27001 focuses on payment card transactions, while ISO 27002 explains how to deploy secure containers.  
D. ISO 27001 is a code of practice for information security, while ISO 27002 is a management framework for an ISMS.

#### Correct Answer

**B. ISO 27001 specifies requirements for establishing, implementing, and maintaining an ISMS, while ISO 27002 provides guidelines for implementing security controls.**

#### Why?

**ISO 27001** defines requirements for establishing, implementing, maintaining, and continually improving an **Information Security Management System (ISMS)**. Organizations can be certified against ISO 27001.

**ISO 27002** provides supporting **guidance and best practices for information security controls**.

- **A is incorrect**: It reverses the roles of ISO 27001 and ISO 27002
- **C is incorrect**: Payment card security is associated with **PCI DSS**
- **D is incorrect**: ISO 27001 is the certifiable ISMS requirements standard; ISO 27002 provides supporting security-control guidance.

Memory aid:
**ISO 27001 → Requirements**
**ISO 27002 → Guidance**

### 7.4 - Exam Focus

Memorize these high-value associations:
- **Privacy laws and protection of personal data → Data privacy regulations**
- **Where data must be stored / jurisdiction governing data → Data sovereignty**
- **Record AWS API activity for auditing → AWS CloudTrail**
- **Monitor metrics and alarms → Amazon CloudWatch**
- **Track AWS resource configuration changes → AWS Config**
- **ISMS requirements / certifiable standard → ISO 27001**
- **Security control guidance and best practices → ISO 27002**

Also recognize the major compliance mappings:

**Payment card data → PCI DSS**
**Protected health information → HIPAA**
**EU personal data/privacy → GDPR**
**US security governance → NIST**
**Financial reporting controls → SOC 1**
**Trust services/security controls → SOC 2**
