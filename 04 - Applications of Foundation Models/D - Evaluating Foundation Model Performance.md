## 1 - Evaluation Approaches for Foundation Models

### 1.1 - Evaluation Approaches for Foundation Models

Evaluating a **foundation model (FM)** helps determine whether it meets expected requirements such as **accuracy, fairness, relevance, and usability**

Two key evaluation approaches are **human evaluation** and **benchmark datasets**.

#### Human Evaluation

**Human evaluation** uses people to access model outputs against criteria such as **relevance, quality, politeness, helpfulness, or usefulness**

Example: Human reviewers rate chatbot responses based on how helpful and appropriate they are.

**Strengths:**
- Provides **nuanced, qualitative feedback**
- Reflects **real-world human expectations**
- Useful when evaluation requires human judgement or context

**Limitations:**
- **Time-consuming**
- **Labor-intensive**
- Can be **subjective**
- Results may vary between evaluators

#### Benchmark Datasets

**Benchmark datasets** are pre-built collections of labeled data or predefined tasks used to evaluate model performance against established standards.

They provide a more **objective** and **scalable** method for assessing characteristics such as **accuracy, bias, and fairness**.

| **Evaluation Method**  | **Key Advantage**               | **Key Limitation**                                           |
| ---------------------- | ------------------------------- | ------------------------------------------------------------ |
| **Human Evaluation**   | Nuanced, context-aware feedback | Subjective and labor-intensive                               |
| **Benchmark Datasets** | Objective, scalable, and faster | May not represent niche or application-specific requirements |

Benchmark datasets generally require **less administrative effort** than human evaluation and can help identify potential **bias** in model outputs.

**Memory aid:**
Human evaluation → **Nuance + human judgement**
Benchmark datasets → **Objective + scalable testing**

### 1.2 - Exam Focus

- **Human judge relevance, helpfulness, or quality → Human evaluation**
- **Predefined labeled data/tasks against industry standards → Benchmark datasets**
- **Nuanced but subjective and labor-intensive → Human evaluation**
- **Faster, scalable, and more objective → Benchmark datasets**
- **Detect accuracy, bias, or fairness systematically → Benchmark datasets**
- **Niche/application-specific evaluation** may require **human evaluation** because generic benchmarks can lack specificity.

## 2 - Performance Metrics

### 2.1 - Performance Metrics

Automated metrics help quantify the **accuracy, relevance, and quality** of foundation model outputs. Common metrics include **ROUGE, BLEU,** and **BERTScore**.

| **Metric**    | **Best Used For**                 | **What It Measures**                                               | **Exam Association**                |
| ------------- | --------------------------------- | ------------------------------------------------------------------ | ----------------------------------- |
| **ROUGE**     | Summarization                     | Overlap between generated and reference text                       | **Recall / summarization**          |
| **BLEU**      | Machine translation               | Similarity between generated translation and reference translation | **Bilingual / translation quality** |
| **BERTScore** | Semantic similarity, paraphrasing | Similarity in meaning using embeddings                             | **Semantic meaning / embeddings**   |

#### ROUGE

**ROUGE (Recall-Oriented Understudy for Gisting Evaluation)** measures the **overlap between generated text and reference text**.

It is commonly used for **summarization** because it emphasizes how much important information from the reference text appears in the generated output.

**ROUGE-N** compares matching **n-grams**:
- **ROUGE-1** → Matching individual words (**unigrams**)
- **ROUGE-2** → Matching two-word sequences (**bigrams**)

For the exam, focus on the general association rather than the calculation details.

**Memory aid:**
**ROUGE → Recall → Summarization**

#### BLEU

**BLEU (Bilingual Evaluation Understudy)** evaluates how closely generated text matches a reference, primarily for **machine translation**.

It compares **word sequences** between the generated translation and reference translation.

BLEU scores typically range from **0 to 1**, where a higher score indicates a closer match to the reference.

**Memory aid:**
**BLEU → Bilingual → Translation**

#### BERTScore

**BERTScore** evaluates generated text using **embeddings** from pretrained **BERT (Bidirectional Encoder Representations from Transformers)** models.

Unlike metrics that mainly compare exact words, BERTScore evaluates **semantic similarity** - whether two pieces of text have similar meaning even when different words are used.

Example:
Reference: *A dog is loyal and friendly*
Generated: *A dog is faithful and sociable*

Although the wording differs, **BERTScore** can recognize that the sentences have similar meanings.

Useful for:
- **Paraphrasing**
- **Semantic similarity**
- Tasks requiring a more **nuanced understanding of meaning**

**Memory aid:**
**BERTScore → "Bond" between meanings → Semantic similarity**

### 2.2 - Exam Focus

- **Summarization / recall of reference content → ROUGE**
- **Machine translation / bilingual text → BLEU**
- **Semantic similarity using embeddings → BERTScore**
- **Exact or n-gram overlap → ROUGE / BLEU**
- **Similar meaning despite different wording →BERTScore**
- **ROUGE** emphasizes how much reference information is captured
- **BLEU** is strongly associated with **translation quality**
- **BERTScore** uses **BERT embeddings** to compare meaning rather than relying only on exact word matches

## 3 - Business Objective Alignment

### 3.1 - Business Objective Alignment

Foundation model evaluation should consider not only technical metrics, but also whether the model supports **business goals**. Key business-alignment metrics include **productivity, user engagement**, and **task engineering**.

| **Metric**           | **What it meaures**                                                         | **Positive indicator**                                 |
| -------------------- | --------------------------------------------------------------------------- | ------------------------------------------------------ |
| **Productivity**     | How efficiently the model completes tasks and produces high-quality outputs | More useful output with **minimal human intervention** |
| **User Engagement**  | How often and how deeply users interact with the model                      | Frequent interaction, refinement, and feedback         |
| **Task Engineering** | How effectively the model completes specific business-relevant tasks        | Tasks completed **smoothly and accurately**            |

#### Productivity

**Productivity** measures how efficiently a foundation model performs tasks and generates **high-quality outputs with minimal human intervention.**

Higher productivity generally indicates stronger alignment with business objectives.

Low productivity may suggest that:
- Too much manual correction is required.
- The model is not producing useful results efficiently
- The model may not adequately support the intended business use case.

#### User Engagement

**User engagement** measures how often and how deeply users interact with the model.

It can include:
- Frequency of model usage
- Complexity of user prompts
- How actively users refine model responses
- User feedback and modifications

Higher engagement can indicate that users find the model **valuable and useful**.

User refinement and feedback can also help guide the model toward better outcomes.

#### Task Engineering

**Task engineering** evaluates how efficiently the foundation model completes **specific tasks that support business objectives**.

A model that performs required tasks **accurately, reliably, and smoothly** is more likely to align with the organization's intended use case.

**Memory aid:**
**Productivity → Efficiency**
**Engagement → User interaction**
**Task engineering → Task completion**

### 3.2 - Exam Focus

- **Efficient output with minimal human intervention → Productivity**
- **Frequency and depth of user interaction → User engagement**
- **Ability to complete specific business-related tasks → Task engineering**
- Higher **productivity** generally indicates stronger business requirement
- Higher **user engagement** can indicate that the model is providing value.
- Accurate and effective completion of intended tasks → stronger **business objective alignment**

## 4 - Exam Tips

### 4.1 - Evaluating Foundation Model Performance - Summary

| **Concept**            | **Key Exam Association**                                                                                                      |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| **Human evaluation**   | People assess outputs for criteria such as relevance, quality, or helpfulness; **nuanced but subjective and labor-intensive** |
| **Benchmark datasets** | Pre-built labeled datasets used to test against standards; **objective, scalable, and efficient**                             |
| **ROUGE**              | Measures **overlap/recall** between generated and reference text; commonly used for **summarization**                         |
| **BLEU**               | Compares generated and reference word sequences; primarily used for **machine translation**                                   |
| **BERTScore**          | Uses **BERT embeddings** to measure **semantic similarity**                                                                   |
| **Productivity**       | High-quality results with **minimal human intervention**                                                                      |
| **User engagement**    | Frequency and depth of user interaction, refinement, and feedback                                                             |
| **Task engineering**   | How effectively the model completes **specific business-aligned tasks**                                                       |

**Quick memory flow:**

Human evaluation → **Human judgement**
Benchmark datasets → **Objective testing**
ROUGE → **Recall / Summarization**
BLEU → **Bilingual / Translation**
BERTScore → **Semantic similarity**

### 4.2 - Exam Focus

- **Nuanced human judgment → Human evaluation**
- **Standardized, scalable evaluation → Benchmark datasets**
- **Summarization → ROUGE**
- **Machine translation → BLEU**
- **Semantic similarity / embeddings → BERTScore**
- **Efficiency with little human intervention → Productivity**
- **Frequency and depth of interaction → User engagement**
- **Effective completion of business-specific tasks → Task engineering**