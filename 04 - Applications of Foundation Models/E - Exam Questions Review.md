## 1 - Design Considerations for Foundation Models

### 1.1 - Original Question

Which factors should you prioritize when selecting a pre-trained **foundation model (FM)** for **real-time language translation**?

### 1.2 - Choices

A. Model size and complexity  
B. Latency and multi-lingual capabilities  
C. Input/output length  
D. Retrieval-augmented generation capability

### 1.3 - Correct Answer

**B. Latency and multi-lingual capabilities**

### 1.4 - Why?

For **real-time language translation**, the model must produce translations quickly and support the required languages.
- **Latency** → Critical for real-time applications because responses must be generated with minimal delay.
- **Multi-lingual capabilities** → Ensure the foundation model can understand and translate effectively across multiple languages
- **Model size and complexity** → Can affect performance and resource requirements, but are not the primary considerations for this scenario
- **Input/output length** → More relevant when handling long prompts or responses, such as **text summarization**
- **Retrieval-Augmented Generation (RAG)** → Connects an FM to external knowledge sources such as databases or document repositories; it does not directly improve real-time translation.

### 1.5 - Exam Focus

**Real-time application** → Prioritize **low latency**
**Language translation** → Prioritize **multi-lingual capabilities**
**Long documents / summarization** → Consider **input/output length**
**Need external or up-to-date knowledge** → Consider **RAG**

**Exam keyword mapping:**
Real-time + translation → **Latency + multi-lingual capabilities**

## 2 - Prompt Engineering Techniques

### 2.1 - Original Question

Which prompt engineering technique involves breaking down complex problems into **sequential reasoning steps** to improve the model's response accuracy?

### 2.2 - Choices

A. Prompt templates  
B. Few-shot prompting  
C. Chain-of-thought prompting  
D. Negative prompting

### 2.3 - Correct Answer

**C. Chain-of-thought prompting**

### 2.4 - Why?

**Chain-of-thought (CoT) prompting** encourages the model to approach a complex problem through a sequence of logical intermediate steps, which can improve accuracy for reasoning-heavy tasks.

- **Prompt templates** → Predefined prompt structures used for **consistency and repeatability**, not sequential reasoning.
- **Few-shot prompting** → Provides several examples to demonstrate the expected task or output pattern
- **Chain-of-thought prompting** → Uses **step-by-step reasoning** to solve complex problems
- **Negative prompting** → Specifies what the model should **avoid including** in its reponse

### 2.5 - Exam Focus

**Step-by-step / sequential reasoning → Chain-of-thought prompting**
**Provide several examples → Few-shot prompting**
**Reusable predefined structure → Prompt template**
**Specify what should not appear in output → Negative prompting**

**Exam keyword mapping:**
Complex problem + logical reasoning steps → **Chain-of-thought prompting**

## 3 - Training and Fine-tuning Foundation Models

### 3.1 - Original Question

Which fine-tuning method involves customizing a foundation model for a **specific field or industry**, such as legal or medical applications?

### 3.2 - Choices

A. Transfer learning  
B. Instruction tuning  
C. Domain adaptation  
D. Continuous pre-training

### 3.3 - Correct Answer

**C. Domain adaptation**

### 3.4 - Why?

**Domain adaptation** customizes a general-purpose foundation model using data from a **specific domain**, such as healthcare, finance, or law.

- **Transfer learning** → Adapts knowledge learned from one task to a **new related task**
- **Instruction learning** → Further trains a model to **follow instructions** more effectively
- **Domain adaptation** → Specializes a model for a **particular industry, field, or subject area**
- **Continuous pre-training** → Continues training on additional data so the model can learn new information while retaining existing capabilities

### 3.5 - Exam Focus

**Specific industry or field → Domain adaptation**
**New related task → Transfer learning**
**Better at following explicit instructions → Instruction tuning**
**Continue learning from additional data → Continuous pre-training**

**Exam keyword mapping:**
Legal, medical, finance, or other specialized field → **Domain adaptation**

## 4 - Evaluating Foundation Model Performance

### 4.1 - Original Question

A company needs a **scalable, objective, and automated** method to evaluate text generation models based on **semantic similarity and linguistic quality**. Which approach is the best choice?

### 4.2 - Choices

A. ROUGE  
B. BLEU  
C. BERTScore  
D. Human evaluation

### 4.3 - Correct Answer

**C. BERTScore**

### 4.4 - Why?

**BERTScore** evaluates generated text using **contextual embeddings**, allowing it to measure **semantic similarity** rather than relying only on exact word overlap.

- **ROUGE** → Commonly used for **text summarization**; measures overlap between generated and reference text but has limited semantic understanding
- **BLEU** → Commonly used for **machine translation**; focuses mainly on n-gram overlap between generated and reference text
- **BERTScore** → Measures **semantic similarity using embeddings**, making it suitable for objective, automated evaluation of generated text
- **Human evaluation** → Can access nuance and quality well, but is **subjective, less consistent, and difficult to scale**

### 4.5 - Exam Focus

**Semantic similarity using contextual embeddings → BERTScore**
**Text summarization / overlap with reference text → ROUGE**
**Machine translation / n-gram overlap → BLEU**
**Nuanced but subjective and difficult to scale → Human evaluation**

**Exam keyword mapping:**
Scalable + automated + semantic similarity → **BERTScore**