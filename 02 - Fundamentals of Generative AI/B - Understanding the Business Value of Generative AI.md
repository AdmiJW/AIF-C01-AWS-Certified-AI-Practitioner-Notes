## 1 - Understanding the Advantages and Disadvantages of Generative AI

### 1.1 - Advantages of Generative AI

Generative AI provides several business advantages, especially **adaptability, responsiveness, and simplicity**.

#### Adaptability

A single **foundation model** can perform many different tasks depending on the prompt, such as:
- Writing content
- Summarizing documents
- Generating or debugging code
- Answering questions

Unlike traditional software designed for a narrow task, generative AI can adapt to multiple use cases without requiring a separate application for each one.

#### Responsiveness

Generative AI can provide **near-immediate responses**, making it useful for scenarios such as:
- Customer support assistants
- Coding assistants
- Real-time content generation
- Interactive knowledge applications

This can reduce the **time to value** for users and businesses

#### Simplicity

Because generative AI models understand **natural language**, users can interact with them without needing advanced programming skills.

This lowers the technical barrier for accessing complex AI capabilities.

### 1.2 - Disadvantages and Risks of Generative AI

Generative AI also introduces limitations that must be considered before using it in business-critical workloads.

#### Hallucinations

A **hallucination** occurs when a model generates information that appears plausible but is **incorrect or fabricated**

Generative models predict likely outputs based on learned patterns rather than independently verifying that every generated statement is true.

**Exam association:**
Confident but factually incorrect AI response → **Hallucination**

#### Nondeterminism

**Nondeterminism** means that the same or similar prompt can produce different outputs across multiple runs.

This makes generative AI less suitable for situations requiring **perfectly repeatable and consistent responses**.

Traditional deterministic software:
`Same input → Same output`

Generative AI:
`Same input → Potentially different outputs`

#### Interpretability

Many generative AI models behave like **black boxes**, making it difficult to explain exactly why a particular output was produced.

This is important in use cases where **explainability, auditing, or regulatory accountability** is required.

#### Inaccuracy and Bias

Foundation models can produce inaccurate results because their training data may contain:
- Outdated information
- Incorrect information
- Biased perspectives
- Incomplete representation of certain domains

Organizations should therefore evaluate outputs and apply appropriate **human oversight and validation**

### 1.3 - Selecting the Right Model

Choosing an appropriate model is important for balancing **capability, performance, cost, and risk**

Key factors include:

| **Consideration**      | **Key Question**                                                    |
| ---------------------- | ------------------------------------------------------------------- |
| **Model capabilities** | Does the workload require text only or **multimodal** capabilities? |
| **Performance**        | How quickly must the model respond?                                 |
| **Cost**               | Is the additional capability of a larger model worth the expense?   |
| **Data Security**      | Can the model and service handle the organization's data securely?  |
| **Compliance**         | Does the solution meet applicable regulatory requirements?          |
| **Accuracy**           | Does the model perform well enough for the intended domain?         |

Larger or more capable models are not automatically the best choice. They may have **higher latency and cost** than a smaller model that adequately handles the task.

**Exam principle:**
Choose the **right-sized model for the business requirement**, rather than always selecting the largest or most capable model.

### 1.4 - Security, Constraints, and Compliance

Business adoption of generative AI must account for **security and regulatory requirements**.

Organizations should consider:
- How sensitive data is handled
- Privacy requirements
- Data protection controls
- Industry regulations
- Organizational governance policies

Examples of regulatory frameworks mentioned in the course include **GDPR** and **HIPAA**

For exam scenarios, security and compliance requirements may influence which model, service, or architecture is appropriate.

### 1.5 - Measuring the Business Value of Generative AI

Organizations should measure whether generative AI produces meaningful **business value** rather than adopting it purely for technical capability

Important business metrics include:

| **Metric**                        | **Example**                                                    |
| --------------------------------- | -------------------------------------------------------------- |
| **Efficiency**                    | Reduction in time required to resolve a support ticket         |
| **Conversion rate**               | Increase in purchases after using AI-generated product content |
| **Customer lifetime value (CLV)** | Improved retention through AI-powered personalization          |
| **Accuracy/quality**              | Percentage of responses considered correct or helpful          |
| **Performance**                   | Response time and effectiveness across different workloads     |

Technical performance should therefore be measured alongside **business outcomes**.

**Business value flow:**
AI capability → Improved process/customer experience → Measure outcome → Compare benefit against cost

### 1.6 - Exam Focus

1. **Perform many different tasks with the same underlying model → Adaptability**
2. **Provide fast, interactive responses → Responsiveness**
3. **Interact using natural language instead of programming → Simplicity**
4. **Plausible but fabricated or incorrect response → Hallucination**
5. **Same prompt can produce different responses → Nondeterminism**
6. **Difficulty explaining why a model generated a specific response → Interpretability / black-box problem**
7. **Training data may introduce outdated information or biased perspectives → Inaccuracy and bias risk**
8. **Need text, images, audio, or other data types** → Consider **model modality / capabilities**
9. **More capable model may increase latency and cost** → Balance **performance, capability and cost**
10. **Sensitive or regulated workload** → Evaluate **security, privacy, complicance, and governance**
11. **Measure time saved by AI → Efficiency metric**
12. **Measure whether AI increases purchases → Conversion rate**
13. **Measure whether personalization improves long-term customer retention/value → Customer lifetime value**
14. **Business adoption decision** → Evaluate both **technical performance and measurable business outcomes**

## 2 - Demo: Comparing Multiple Generative AI Models

### 2.1 - Comparing Models in Amazon Bedrock

**Amazon Bedrock** provides access to multiple foundation models through its **model catalog** and allows models to be tested in the **Bedrock playground**.

The playground's **Compare mode** can run the same prompt against multiple models side by side. This helps with **model selection** by comparing factors such as:
- Response quality
- Behavior and style
- **Input tokens**
- **Output tokens**
- **Latency**
- Suitability for the intended workload

**Exam association:**
Compare multiple foundation models before application integration → **Amazon Bedrock playground / model evaluation**

### 2.2 - Hallucination Testing

One test prompt asked models about a deliberately fictitious event.

This is useful for observing whether a model:
- Recognizes that information is unavailable or fictional
- Makes unsupported assumptions
- Generates fabricated details

A confidently fabricated response is an example of **hallucination**.

**Exam keyword:**
Plausible but unsupported/generated false information → **Hallucination**

### 2.3 - Temperature and Top P

**Temperature** and **Top P** are inference parameters that influence how responses are generated.

| **Parameter**   | **Effect**                                            |
| --------------- | ----------------------------------------------------- |
| **Temperature** | Controls randomness in token selection                |
| **Top P**       | Restricts token choices to a probability-based subset |

Generally:
- **Lower values** → More predictable, focused, and consistent responses
- **Higher values** → More varied and creative responses

For workloads requiring more consistency, such as factual or business-oriented responses, lower randomness may be preferable.

For creative tasks, higher randomness can encourage more diverse output.

**Memory aid:**
- Lower Temperature/Top P → **Predictability**
- Higher Temperature/Top P → **Creativity**

These settings influence response variability but do **not guarantee factual correctness**.

### 2.4 - Nondeterminism and Repeated Outputs

Generative AI is generally **nondeterministic**, meaning repeated runs of the same prompt can produce different responses.

Adjusting inference parameters can influence this behavior:
- Lower randomness can make outputs more consistent.
- Higher randomness can produce greater variation.

In the demo, one model configured with low randomness repeatedly produced similar output, while another configured with higher randomness generated different results across runs.

**Exam association:**
Need more consistent responses → Reduce **randomness** using inference settings such as temperature.

### 2.5 - System Prompts

A **system prompt** provides high-level instructions that guide a model's overall behavior throughout an interaction.

It can define:
- Persona or role
- Tone
- Response style
- Formatting expectations
- Application-specific behavioral instructions

Example:
`Respond as a slightly annoyed French waiter.`

The system prompt caused the model to maintain this persona while responding to subsequent user messages.

- **System prompt → Application-level behavior**
- **User prompt → Individual user request**

System prompts are useful for creating a consistent **brand or corporate voice** without changing the underlying foundation model.

### 2.6 - System Prompt vs User Prompt

| **Prompt Type**   | **Main Purpose**                                                     |
| ----------------- | -------------------------------------------------------------------- |
| **System Prompt** | Defines overall model behavior, persona, tone, and application rules |
| **User prompt**   | Specifies the user's immediate request or task                       |

Without strong system-level instructions, application behavior may depend much more heavily on how individual users phrase their prompts.

### 2.7 - From Model Evaluation to Application Integration

Model testing should consider more than response quality alone.

A business may evaluate:

**Model → Output Quality → Token Usage → Latency → Inference Settings → System Prompt Behavior → Application Fit**

Once an appropriate model, inference configuration, and system prompt have been identified, the next stage is **application integration**.

### 2.8 - Exam Focus

1. **Compare foundation models side by side → Amazon Bedrock playground Compare mode**
2. **Measure model response speed → Latency**
3. **Measure amount of text processed/generated → Input and output tokens**
4. **More predictable and consistent responses** → Lower **Temperature / Top P**
5. **More varied and creative responses** → Higher **Temperature / Top P**
6. **Control randomness during inference** → **Temperature**
7. **Limit token selection based on cumulative probability → Top P**
8. **Same prompt may produce different responses → Nondeterminism**
9. **Confidently invent information about a nonexistent event → Hallucination**
10. **Define application persona, tone, or response style → System prompt**
11. **User's immediate request → User prompt**
12. **Create consistent application behavior without retraining the model → System prompt + inference configuration**
13. **After selecting the model and desired settings** → Proceed to **application integration**