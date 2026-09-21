## 1 - Introducing Basic AI and ML Concepts

### 1.1 - AI/ML vs Traditional Rule-Based Solutions

#### Traditional / Non-ML Solutions

Traditional software uses **explicit rules and predefined constraints** written by programmers.

Example: Password length validation
- Password < 8 characters → "Too short"
- Password > 20 characters → "Too long"
- Otherwise → Accept

Key characteristics:
- **Rule-based**
- **Deterministic** - The same input always produces the same output
- **Predictable**
- **Transparent and easy to explain**
- Logic is explicitly defined by developers

#### Exam tip:

If a problem requires:
- Fixed rules
- Deterministic outputs
- Highly predictable behavior
- Simple predefined logic
then **machine learning is usually unnecessary**. A traditional software solution is generally more appropriate.

### 1.2 - AI / Machine Learning Solutions

Machine learning differs from traditional programming because its behavior is primarily **driven by data rather than explicitly programmed rules**.

Key characteristics:
- Learns patterns from historical data
- Can adapt as data and patterns change
- Outputs may not always be completely deterministic
- Logic is generally less transparent than traditional rule-based software
- Models can still be designed to be **explainable**

ML is useful when the problem involves discovering or learning patterns that would be difficult to express using fixed rules.

### 1.3 - Relationship Between AI, ML, Deep Learning, and Generative AI

The technologies can be viewed as nested concepts:

**Artificial Intelligence (AI)**
	→ **Machine Learning (ML)**
		→ **Deep Learning (DL)**
			→ **Generative AI (GenAI)**

#### Artificial Intelligence (AI)

AI is the broadest category.

Goal: Create systems capable of performing tasks associated with human intelligence

Examples: 
- Understanding language
- Recognizing patterns
- Making decisions

#### Machine Learning (ML)

ML is a **subset of AI**.

Machine learning uses **algorithms and data to allow computers to learn patterns without explicitly programming every rule**.

Instead of defining all logic manually,
`Data → Learning Algorithm → Learned Model`

#### Deep Learning (DL)

Deep learning is a **subset of machine learning**.

It uses **neural networks with multiple interconnected layers** to learn complex patterns from data.

Key characteristics:
- Uses neural networks
- Can automatically learn complex features
- Requires less manual feature engineering
- Effective for large and complex datasets
- Inspired loosely by how neurons in the human brain interact

#### Neural Networks

A neural network typically contains:

`Input Layer → Hidden Layers → Output Layer`

**Input Layer**

Receives the raw input data.

Example for handwritten digit recognition:
- Pixel values from an image

**Hidden Layers**

Perform most of the pattern-learning.

Different layers may learn increasingly complex features.

Example:

`Pixels → Edges → Curves → Shapes → Digit Pattern`

Each hidden layer builds upon information learned by previous layers.

**Output Layer**

Produces the final prediction.

Example:

`Image → Neural Network → "This digit is 7"`

#### Deep Learning Use Cases 

**Computer Vision**

Computer vision allows computers to understand and analyze images and video.

Deep learning is widely used because neural networks can **automatically learn visual features**.

Common tasks:
- **Image Classification** - determine what an image contains
- **Object Detection** - identify and locate objects
- **Image Segmentation** - divide an image into meaningful regions

#### Natural Language Processing (NLP)

Natural Language Processing enables computers to **understand, process, and extract information from human language**.

NLP can work with unstructured information such as:
- Text
- Audio
- Speech
- Other language-related data

Common use cases:
- Language translation
- Virtual assistants
- Voice-command recognition
- Chatbots
- Information extraction
- Sentiment analysis

#### Sentiment Analysis

Determines the emotional tone of text.

Typical classifications:
- Positive
- Negative
- Neutral

Example:

`Customer Review → NLP Model → Positive Sentiment`

#### Generative AI

Generative AI is focused on **creating new content based on patterns learned from existing data**.

Possible outputs include:
- Text
- Images
- Music 
- Video

Traditional ML often focuses on:

`Input → Prediction / Classification`

Generative AI focuses on:

`Input / Prompt → Newly Generated Content`

#### Key Exam Distinctions

| Concept                           | Main Idea                                                   |
| --------------------------------- | ----------------------------------------------------------- |
| Traditional software              | Uses explicitly programmed rules                            |
| Artificial Intelligence (AI)      | Broad field involving machines performing intelligent tasks |
| Machine Learning                  | Learns patterns from data                                   |
| Deep Learning                     | ML using multilayer neural networks                         |
| Generative AI                     | Generates new content from learned patterns                 |
| Computer Vision                   | Understands images/video                                    |
| Natural Language Processing (NLP) | Understands and processes human language                    |

Remember:

- **Fixed rules + predictable output → Traditional programming**
- **Learning patterns from data → Machine Learning**
- **Complex neural networks → Deep Learning**
- **Creating new text / images / audio / etc. → Generative AI**

---
## 2 - How Do Machines Learn?

### 2.1 - How Machine Learning Works

Machine learning (ML) enables systems to **learn patterns from data** rather than relying entirely on explicitly programmed rules.

Typical process:

`Training Data → ML Algorithm → Trained Model → Predictions on New Data`

During **training**, the algorithm learns relationships and patterns from the provided data.

After training, the resulting **ML model** can make predictions or decisions on **new, unseen data**.

### 2.2 Training and Inference

#### Training

**Training** is the process of providing data to an ML algorithm so that it can learn patterns and create a trained model.

Training data commonly contains:
- **Input variables** - the information given to the model
- **Target variables / labels** - the expected correct result

Example:
- Input → image of an animal
- Target/label → `"Shark"`

The objective is to produce a model that can generalize what it learned to new data.

#### Inference

**Inference** is when a trained model applies what it learned to **new, unseen data** to produce a prediction or result.

Example:

`New shark image → Trained model → "Shark"`

Key distinction:
- **Training** = model learns
- **Inference** = trained model is used

**Exam tip:** Questions may distinguish between resources or activities required during **model training** versus during **inference/production use**.

### 2.3 Foundation Models

A **foundation model (FM)** is a large-scale model trained on **very large and diverse datasets**.

Foundation models:
- Learn broad patterns and capabilities
- Can support many different downstream tasks
- Serve as a base for specialized AI applications
- Can be adapted instead of building a model from scratch

Creating a foundation model from scratch typically requires:
- Very large datasets
- Significant computational resources
- Extensive preprocessing
- Specialized ML expertise
- High financial cost

Therefore, organizations commonly use and customize existing foundations models rather than train their own from scratch.

One way of adapting a foundation model is **fine-tuning**.

### 2.4 - Large Language Models (LLMs)

A **Large Language Model (LLM)** is a type of model trained on very large amounts of text and language-related data.

LLMs commonly use:
- **Deep learning**
- **Transformer architectures**
- Large number of learned **parameters**

LLMs learn complex language patterns and can predict likely sequences of words or tokens.

This enables tasks such as:
- Text generation
- Question answering
- Summarization
- Translation
- Conversational interfaces

### 2.5 Model Parameters

**Parameters** are the model's internal settings that are **learned during training.**

Training adjusts these parameters so that the model becomes better at identifying patterns and producing appropriate outputs.

Conceptually:

`Training Data → Adjust Parameters → Improved Model`

Large AI models can contain billions of parameters.

For the exam, remember:
- Parameters are **learned**
- They represent internal model settings
- Training modifies them based on data

### 2.6 Generative AI Training and Inference

For traditional predictive ML, inference often produces a:
- Classification
- Prediction
- Probability

For generative AI, inference produces **new content** based on patterns learned during training.

Examples:
- Text
- Images
- Audio
- Video

A generative model does not need to have seen the exact requested output during training.

Instead, it can combine learned concepts.

Example:

`Prompt: Generate a pink shark`

The model may combine its learned understanding of:
- Sharks
- Colors
- Image composition
to generate something new.

### 2.7 - Prediction Confidence and Probability

ML models may provide a **probability score** representing confidence in a prediction.

For a binary classification problem:
- Score near **1.0** → high confidence in the positive class
- Score near **0.0** → high confidence in the negative class
- Score near **0.5** → high uncertainty

Example:
`P(Shark) = 0.95`
means the model has high confidence that the image belongs to the shark class.

Important:

A probability score indicates the model's **confidence**, but high confidence does not automatically guarantee that the prediction is correct.

### 2.8 - Generalization

**Generalization** is a model's ability to perform well on **new, unseen data** rather than only the data it encountered during training.

Example:

A shark classifier should recognize sharks with:
- Different colors
- Different angles
- Different backgrounds
- Different lighting conditions

A model trained on sufficiently diverse data is more likely to generalize effectively.

A model that cannot handle new variations may produce:
- Lower confidence
- Incorrect predictions
- Poor production performance

### 2.9 - Model Fit

**Model fit** describes how well a model has learned from its training data and how effectively it performs on new data.

The three important model-fit patterns for the exam are:
- **Underfitting**
- **Overfitting**
- **Balanced / good fit**

### 2.10 - Underfitting

**Underfitting** occurs when a model has **not learned enough** from the training data.

Characteristics:
- Model is too simple
- Fails to capture important patterns
- Performs poorly on training data
- Also performs poorly on unseen data

Conceptually:
`Poor Training Performance + Poor Test Performance = Underfitting`

Example analogy:

A student barely studies and performs poorly even when the exam contains familiar questions.

**Exam clue:**
If a model performs poorly even on its **training data**, think **underfitting**.

### 2.11 - Overfitting

**Overfitting** occurs when a model learns the training data **too specifically**, including unnecessary details or noise.

Characteristics:
- Performs very well on training data
- Performs poorly on new, unseen data
- Does not generalize effectively
- Model may be unnecessarily complex

Conceptually:
`Excellent Training Performance + Poor Test Performance = Overfitting`

Example analogy:
A student memorizes exact practice questions instead of understanding the concepts.

**Exam clue:**
If a model performs extremely well on training data but poorly on new data, think **overfitting**.

### 2.12 - Balanced Model / Good Fit

A well-fitted model learns enough useful patterns without memorizing the training data.

Characteristics:
- Good performance on training data
- Good performance on unseen data
- Generalizes effectively
- Captures meaningful patterns without unnecessary complexity

Goal:
`Good Training Performance + Good Test Performance = Good Fit`

Comparison:

| **Model Fit** | **Training Data** | **Unseen Data** |
| ------------- | ----------------- | --------------- |
| Underfitting  | Poor              | Poor            |
| Good fit      | Good              | Good            |
| Overfitting   | Very good         | Poor            |

### 2.13 - Bias and Fairness

A model can be **accurate but still unfair**.

**Bias** occurs when a model systematically produces unfair or skewed outcomes for certain groups.

Good predictive performance does **not** automatically guarantee fairness.

Potential consequences include:
- Discrimination
- Unequal treatment
- Unfair decisions

This is especially important in high-impact areas such as:
- Hiring
- Lending
- Healthcare
- Insurance

### 2.14 - Sources of Bias

#### Biased or Unrepresentative Training Data

If certain groups are underrepresented or overrepresented in training data, the model may learn biased patterns.

Example:
A hiring model trained primarily on resumes from men may unintentionally favor male candidates.

#### Historical Bias

Historical datasets may contain existing social inequalities or discriminatory decisions.

The model can learn and reproduce those patterns.

Example:
If historical lending decisions unfairly rejected certain groups, a model trained on that data may continue the same behavior.

#### Algorithm or Feature Selection

Bias can also be introduced by:
- Model design
- Chosen features
- How strongly certain features are weighted

Example:
A loan model that heavily relies on ZIP code may indirectly discriminate if location strongly correlates with race or income.

#### 2.15 - Key Exam Distinctions

| **Concept**      | **Meaning**                                           |
| ---------------- | ----------------------------------------------------- |
| Training         | Model learns patterns from data                       |
| Inference        | Trained model processes new data                      |
| Input variable   | Data supplied to the model                            |
| Target / label   | Expected correct result                               |
| Foundation model | Large broadly trained model usable for many tasks     |
| LLM              | Large model specializing in language-related patterns |
| Parameter        | Internal model setting learned during training        |
| Generalization   | Ability to perform well on unseen data                |
| Underfitting     | Model learns too little                               |
| Overfitting      | Model learns training data too specifically           |
| Good fit         | Model performs well on both training and unseen data  |
| Bias             | Systematic unfairness in model behavior               |

Core exam memory:

- **Poor on training + Poor on new data → Underfitting**
- **Great on training + Poor on new data → Overfitting**
- **Good on training + Good on new data → Good fit / Generalization**
- **Accurate model ≠ Fair model**

## 3 - Different Ways Machines Learn

### 3.1 - Types of Machine Learning

Machines can learn using several different approaches:
- **Supervised learning**
- **Unsupervised learning**
- **Semi-supervised learning**
- **Self-supervised learning**
- **Reinforcement learning**

The main difference is **what kind of training data or feedback is available to the model**.

### 3.2 - Supervised Learning

**Supervised learning** trains a model using **labeled data**.

Each training example contains:
- **Input data**
- The correct **target / label**

Example:
`Shark Image → Label: "Shark"`

The model learns the relationship between inputs and known outputs, then applies that relationship to new data.

Common supervised learning tasks:
- **Classification**
- **Regression**

**Exam clue:**
If the training data includes known correct answers or labels, think **supervised learning**.

### 3.3 - Classification

**Classification** is a supervised learning task where the model predicts a **discrete category or class**

#### Binary Classification

The model chooses between **two possible classes**.

Examples:
- Fraud / Not Fraud
- Yes / No
- True / False
- Spam / Not Spam

#### Multi-class Classification

The model chooses among **more than two classes**

Examples:
- Shark / Coral / Seaweed
- Cat / Dog / Cow
- House / Condo / Townhome

Key distinction:
**Classification predicts categories, not continuous numerical values**

### 3.4 - Regression

**Regression** is a supervised learning task used to predict a **continuous numerical value**.

Examples:
- House price
- Rental price
- Stock price
- Temperature
- Sales amount

Example:

A model can learn the relationship between:
`Number of Bedrooms → Rental Price`
and then estimate the price for a new property.

**Exam clue:**
- Predict a **category** → Classification
- Predict a **number / continuous value** → Regression

### 3.5 - Unsupervised Learning

**Unsupervised learning** works with **unlabeled data**.

There is no predefined target or correct answer.

Instead, the model discovers:
- Patterns
- Relationships
- Groups
- Unusual observations

Common unsupervised learning tasks include:
- **Clustering**
- **Anomaly detection**

**Exam clue:**
If the model must discover structure in data without known labels, think **unsupervised learning**.

### 3.6 - Clustering

**Clustering** groups data points based on similarity.

The model discovers natural groupings without being told what the groups should be.

Examples:
- Grouping customers by purchasing behavior
- Grouping patients with similar health characteristics
- Grouping users based on application usage patterns

The algorithm may identify different clusters without assigning meaningful human-readable names.

A domain expert may later interpret and label those clusters.

Example:
`Patient Data → Model Discovers Clusters → Doctor Interprets Groups`

### 3.7 - Anomaly Detection

**Anomaly detection** identifies data points or patterns that differ significantly from normal behavior.

Examples:
- Suspicious network traffic
- Abnormal heart rate
- Unusual application usage
- Unexpected transaction patterns

Conceptually:
`Normal Pattern → Large Deviation → Possible Anomaly`

Anomaly detection is commonly associated with **unsupervised learning**, especially when examples of abnormal behavior are not already labeled.

### 3.8 - Semi-Supervised Learning

**Semi-supervised learning** combines:
- A **small amount of labeled data**
- A **large amount of unlabeled data**

This is useful when labeling data is:
- Expensive
- Slow
- Difficult
- Impractical at large scale

Example:

Speech recognition dataset:
- Small subset of audio recordings → manually transcribed
- Large remaining dataset → unlabeled audio

The model learns from both.

Conceptually:
`Few Labeled Examples + Many Unlabeled Examples → Semi-Supervised Learning`

**Exam clue**:
If only part of the training dataset has labels, think **semi-supervised learning**.

### 3.9 - Self -Supervised Learning

**Self-supervised learning** allows the model to learn from **unlabeled data by deriving training signals from the data itself**.

The model effectively creates its own learning task.

Examples include:
- Predicting missing words
- Predicting the next word or token
- Reconstructing missing parts of data
- Learning relationships between different parts of the input

Self-supervised learning is important for training modern foundation models and language models because enormous datasets do not need to be manually labeled.

Example:
`"AWS provides cloud ___" → Predict Missing Word`

The correct answer can be derived from the original data itself.

### 3.10 - Semi-Supervised vs Self-Supervised Learning

These are easy to confuse.

| **Approach**    | **Labels**                                          |
| --------------- | --------------------------------------------------- |
| Semi-supervised | Some data has human-provided labels                 |
| Self-supervised | Model derives labels / signals from the data itself |

Remember:

- **Semi-supervised = Some labels already exist**
- **Self-supervised = Data creates its own supervision**

### 3.11 - Reinforcement Learning

**Reinforcement learning (RL)** trains an agent through **interaction and feedback**.

The model:
1. Takes an action
2. Receives feedback
3. Adjusts its future behavior

Feedback commonly takes the form of:
- **Rewards**
- **Penalties**

The objective is to learn actions that maximize cumulative rewards.

Conceptually:
`Action → Environment → Reward/Penalty → Learn → Next Action`

### 3.12 - Reinforcement Learning Examples

Common use cases include:
- Robotics
- Self-driving systems
- Game-playing agents
- Navigation systems
- Recommendation systems

Example recommendation behavior:
- User clicks a product → positive feedback
- User purchases a product → stronger positive feedback
- User repeatedly ignores a recommendation → negative or weak feedback

The system adjusts future recommendations based on these interactions.

**Exam clue:**
If the model learns by **trial and error using rewards or penalties**, think **reinforcement learning**.

### 3.13 - Comparing Machine Learning Approaches

| **Learning Type**      | **Training Signal**                           | **Typical Tasks**                               |
| ---------------------- | --------------------------------------------- | ----------------------------------------------- |
| Supervised             | Fully labeled data                            | Classification, regression                      |
| Unsupervised           | No labels                                     | Clustering, anomaly detection                   |
| Semi-supervised        | Small labeled + large unlabeled dataset       | Tasks where labeling is expensive               |
| Self-supervised        | Labels/signals generated from the data itself | Foundation model and language-model pretraining |
| Reinforcement learning | Rewards and penalties                         | Sequential decision-making                      |

### 3.14 - Key Exam Distinctions

- **Known correct labels → Supervised learning**
- **No labels, discover patterns → Unsupervised learning**
- **Few labeled + many unlabeled examples → Semi-supervised learning**
- **Model creates its own learning signals from data → Self-supervised learning**
- **Rewards and penalties → Reinforcement learning**

For supervised learning:
- **Predict a class → Classification**
- **Predict a continuous number → Regression**

For unsupervised learning:
- **Discover similar groups → Clustering**
- **Find unusual observations → Anomaly detection**

## 4 - Types of Data in AI Models

### 4.1 - Structured Data

**Structured data** follows a predefined and organized format, making it easier for traditional systems and ML algorithms to store, query, and analyze.

Two important forms of structured data are **Tabular data** and **Time series data**.

### 4.2 - Tabular Data

**Tabular data** is organized into **rows** and **columns**, similar to a spreadsheet or relational database table.

Typically:
- **Rows** represent individual records or observations
- **Columns** represent attributes or features

Example:

| **Customer ID** | **Age** | **Income** | **Purchased** |
| --------------- | ------- | ---------- | ------------- |
| 001             | 25      | 50000      | Yes           |
| 002             | 38      | 82000      | No            |

In an ML context:
- Columns can represent **features / input variables**
- A column can also represent the **target variable / label**

Common examples:
- Customer records
- Transaction records
- Employee information
- Product data
- Financial records

**Exam clue:**
Data arranged into defined **rows and columns → Tabular / structured data**

### 4.3 - Time Series Data

**Time series data** consists of observations recorded **over time**, where the order and timing of data points are important.

It is useful for:
- **Forecasting future values**
- Identifying trends
- Detecting patterns over time
- Understanding changes over time

Example:

| **Year** | **Sales** |
| -------- | --------- |
| 2023     | 1,000     |
| 2024     | 1,200     |
| 2025     | 1,450     |

Historical sales can be used to identify trends and predict future sales.

Common examples:
- Sales over time
- Stock prices
- Temperature readings
- Website traffic
- Energy consumption
- Product demand

**Exam clue:**
If observations are ordered by **time**, especially for **forecasting or trend analysis**, think **time series data**.

### 4.4 - Unstructured Data

**Unstructured data** does not follow a predefined tabular schema or consistent organizational format. 

It generally cannot be represented naturally as conventional rows and columns and may require specialized AI/ML techniques for analysis.

Common examples include:
- Text
- Emails
- Documents
- Social media posts
- Medical notes
- Images
- Videos
- Audio recordings

### 4.5 - Common Unstructured Data Types

#### Text

Examples:
- Emails
- Documents
- Social media posts
- Medical notes

Text may vary significantly in:
- Length
- Language
- Format
- Content

AI techniques such as **Natural Language Processing (NLP)** can be used to process text.

**Images and Videos**

Images and videos contain visual information without predefined fields describing their contents.

AI techniques such as **computer vision** can be used to analyze them.

Examples:
- Photos
- Medical images
- Surveillance footage
- Videos

**Audio**

Raw audio does not inherently contain structured labels describing what is being spoken or heard.

Examples:
- Voice recordings
- Conversations
- Music
- Other sound recordings

AI can process audio for tasks such as speech recognition.

### 4.6 - Structured vs Unstructured Data

| **Data Type** | **Structure**                                 | **Examples**                         |
| ------------- | --------------------------------------------- | ------------------------------------ |
| Tabular       | Rows and columns with predefined fields       | Customer records, transactions       |
| Time series   | Values associated with ordered points in time | Sales, stock prices, sensor readings |
| Unstructured  | No predefined tabular structure               | Text, images, video, audio           |

Both **tabular data** and **time series data** are forms of **structured data**.

Key exam distinctions:
- **Rows + columns → Tabular data**
- **Ordered observations over time → Time series data**
- **Text, images, video, audio → Unstructured data**
- **Forecasting trends over time → Time series is likely relevant**

## 5 - Exam Tips

### 5.1 - Core AI Hierarchy

For the exam, remember the relationship:

`AI → Machine Learning → Deep Learning → Generative AI`

#### Artificial Intelligence (AI)

Broad field focused on systems that mimic aspects of human intelligence.

Examples:
- Understanding language
- Recognizing patterns
- Making decisions

#### Machine Learning (ML)

Subset of AI that uses **algorithms and data to learn patterns** rather than relying entirely on explicit programming.

#### Deep Learning (DL)

Subset of ML that uses **multi-layer neural networks** to learn complex patterns.

#### Generative AI

Subset within deep learning focused on **creating new content**.

Examples:
- Text
- Images
- Music
- Video

### 5.2 - Natural Language Processing

**Natural Language Processing (NLP)** enables machines to understand process, generate, and respond to human language.

Common NLP tasks:
- Text generation
- Translation
- Summarization
- Sentiment analysis
- Autocomplete
- Conversational assistants

### 5.3 - Training vs Inference

Models first go through **training** to learn patterns from data.

After training, they perform **inference** on new, unseen data.

Remember,

**Training = Learning**
**Inference = Using what was learned**

Example:
`Training Images → Train Model → New Image → Inference → Prediction`

### 5.4 - Choosing the Learning Type

#### Supervised Learning

Use when training data contains:
- Inputs
- Correct labels / outputs

Suitable for:
- Classification
- Spam detection
- Image classification
- Regression

**Exam clue:** Labeled dataset → **Supervised learning**

#### Unsupervised Learning

Use when data has **no labels** and the objective is to discover patterns.

Suitable for:
- Clustering
- Customer segmentation
- Anomaly detection

**Exam clue:** Unlabeled data + discover groups/patterns → **Unsupervised learning**

#### Semi-Supervised Learning

Uses:
- A small amount of labeled data
- A large amount of unlabeled data

Useful when manual labeling is expensive or impractical.

Example:
- Some audio recordings have transcripts
- Most audio recordings are unlabeled

**Exam clue:** Some labeled + lots of unlabeled data → **Semi-supervised learning**

#### Self-Supervised Learning

The model creates its own training signals from **unlabeled data**.

It can learn by predicting missing or hidden information.

Commonly associated with:
- Language-model training
- Autocomplete
- NLP

**Exam clue:** Model derives labels/training signals from the data itself → **Self-supervised learning**

#### Reinforcement Learning

The model learns by interacting with an environment and receiving:
- Rewards
- Penalties

Suitable for:
- Recommendation systems
- Robotics
- Self-driving systems
- Sequential decision-making

**Exam clue:** Rewards / penalties / trial and error → **Reinforcement learning**

### 5.5 - Learning Type Quick Comparison

| **Learning Type** | **Key Signal**                       | **Typical Example**        |
| ----------------- | ------------------------------------ | -------------------------- |
| Supervised        | Fully labeled data                   | Spam classification        |
| Unsupervised      | No labels                            | Customer segmentation      |
| Semi-supervised   | Few labeled + many unlabeled         | Speech recognition         |
| Self-supervised   | Model derives its own labels/signals | Language-model pretraining |
| Reinforcement     | Rewards and penalties                | Recommendation systems     |

### 5.6 - Classification vs Regression

Both are commonly **supervised learning** tasks.

#### Classification

Predicts a **category**.

Examples:
- Spam / Not Spam
- Fraud / Not Fraud
- Cat / Dog / Bird

#### Regression

Predicts a **continuous numerical value**

Examples:
- House price
- Sales amount
- Temperature

Remember:
**Category → Classification**
**Continuous number → Regression**

### 5.7 - Model Fit

Three important model-fit states:

#### Underfitting

The model does **not learn enough** from the training data.

Results:
- Poor performance on training data
- Poor performance on unseen data

**Exam clue:** Poor even on training data → **Underfitting**

#### Overfitting

The model learns the training data **too specifically**, including noise and unnecessary details.

Results:
- Very good performance on training data
- Poor performance on unseen data

**Exam clue:** Great training performance + poor unseen-data performance → **Overfitting**

#### Good / Balanced Fit

The model learns meaningful patterns without memorizing the training data.

Results:
- Good training performance
- Good unseen-data performance
- Good **generalization**

Goal:
`Learn enough, but not too much`

### 5.8 - Generalization

**Generalization** is the ability of a model to perform well on **new, unseen data**.

A robust model should:
- Learn meaningful patterns
- Avoid memorizing training examples
- Handle variations not seen exactly during training

Good model fit should lead to good generalization.

### 5.9 - Foundation Models

A **foundation model (FM)** is a large model that has already been trained on **vast amounts of data**. 

Foundation models:
- Learn broad capabilities
- Can support many tasks
- Can work with different types of data
- Can be adapted for specialized use cases

Instead of training a large model from scratch, organizations can often start with an existing foundation model and customize it.

### 5.10 - Fine-Tuning

**Fine-tuning** adapts a pre-trained model for a more specific task or domain.

Process:
`Pre-trained Foundation Model → Additional Task-Specific Training → Customized Model`

Fine-tuning typically uses a **smaller, specialized dataset**.

**Exam clue:** Further training an existing pre-trained model on task-specific data → **Fine-tuning**

### 5.11 - Large Language Models

A **Large Language Model (LLM)** is a type of foundation model specialized in understanding and generating human language.

Common capabilities:
- Text generation
- Translation
- Summarization
- Question answering
- Sentiment analysis

Remember:
**Foundation model** = broad category of large pre-trained models
**LLM** = foundation model focused on language

### 5.12 - High-Priority Exam Memory

- **AI → ML → Deep Learning → Generative AI**
- **Training → Learn from data**
- **Inference → Use trained model on new data**
- **Labeled data → Supervised**
- **No labels + discover patterns → Unsupervised**
- **Few labels + many unlabeled → Semi-supervised**
- **Generate supervision from the data itself → Self-supervised**
- **Rewards and penalties → Reinforcement learning**
- **Category prediction → Classification**
- **Continuous value prediction → Regression**
- **Poor training + poor test performance → Underfitting**
- **Great training + good test performance → Overfitting**
- **Good training + good test performance → Good fit / generalization**
- **Large pre-trained multi-purpose model → Foundation model**
- **Further task-specific training of a pre-trained model → Fine-tuning**
- **Language-focused foundation model → LLM**