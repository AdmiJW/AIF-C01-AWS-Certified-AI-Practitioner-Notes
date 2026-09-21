## 1 - Basic AI Concepts and Terminologies 

### 1.1 - Original Question

A company is developing a recommendation system for an online shopping platform. The goal is for the assistant to enhance suggestions based on user behavior and feedback over time.

Which AI learning strategy enables this adaptive improvement?

### 1.2 - Choices

- A. **Unsupervised learning** to identify patterns and user preferences
- B. **Supervised learning** with a fixed dataset of past purchases and ratings
- C. **Supervised learning** with an evolving dataset of customer interactions
- D. **Reinforcement learning** with rewards based on customer engagement metrics

### 1.3 - Correct Answer

D. **Reinforcement learning** with rewards based on customer engagement metrics

### 1.4 - Why?

**Reinforcement Learning (RL)** learns by taking actions and receiving **rewards or feedback** based on the outcomes.

In this scenario, the recommendation system continuously improves its suggestions based on how users respond, such as clicks, purchases, or other engagement metrics.

This matches the core idea of reinforcement learning:
`Action → Feedback / Reward → Adjust Behavior → Improve Over Time`

The other options do not directly model continuous improvement through rewards:
- **Supervised learning** learns from labeled examples
- **Unsupervised learning** discovers patterns in unlabeled data
- An evolving supervised dataset may be retrained over time, but it is still not learning directly through a reward-based feedback loop

### 1.5 - Exam Focus

Look for keywords such as:

**Rewards, feedback, actions, trial and error, adaptive behavior, improve over time → Reinforcement Learning**

Quick distinction:
- **Supervised Learning** → Learn from labeled data
- **Unsupervised Learning** → Find patterns in unlabeled data
- **Semi-supervised Learning** → Mix of labeled and unlabeled data
- **Self-supervised Learning** → Generate labels from the data itself
- **Reinforcement Learning** → Learn through actions, rewards, and feedback

## 2 - The Machine Learning Pipeline

### 2.1 - Original Question

A company has developed a **classification model** to identify whether emails are spam or not.

After training and validating the model, the company wants to evaluate its performance using a metric that represents the **overall proportion of correct predictions**

Which evaluation metric should the company use?

### 2.2 - Choices

- A. **R² (R-Squared)**  
- B. **Root Mean Squared Error (RMSE)**  
- C. **F1 Score**  
- D. **Accuracy**

### 2.3 - Correct Answer

D. Accuracy

### 2.4 - Why?

The model is performing **classification**, so classification metrics are required.

**R²** and **RMSE** are mainly used for **regression**, so A and B can be eliminated.

Both **Accuracy** and **F1 Score** are classification metrics, but **Accuracy** specifically measures the **overall proportion of predictions that are correct** 

**F1 Score** instead balances **precision and recall**, making it more useful when false positives and false negatives matter or when the classes are imbalanced.

### 2.5 - Exam Focus

First identify whether the task is **classification or regression**
- **Accuracy** → Overall proportion of correct classification predictions
- **F1 Score** → Balance between precision and recall
- **RMSE** → Regression prediction error
- **R²** → How well a regression model explains variation in the target

Key wording:

**"Overall propertion of correct predictions" → Accuracy**

## 3 - AWS Managed AI/ML Services and Applications

### 3.1 - Original Question

A company is developing a **sentiment analysis tool** to assess customer feedback from various sources.

The goal is to automatically analyze text data and derive insights about **customer emotions and key themes**

Which solution meets these requirements?

### 3.2 - Choices

- A. **Amazon Textract**  
- B. **Amazon Comprehend**  
- C. **Amazon SageMaker**  
- D. **Amazon Rekognition**

### 3.3 - Correct Answer

B. **Amazon Comprehend**  

### 3.4 - Why?

**Amazon Comprehend** is a managed NLP service designed to analyze text and extract insights such as:
- **Sentiment**
- **Key phrases**
- **Entities**
- **Language**

This directly matches the requirement to analyze customer feedback for emotions and themes.

The other options are less suitable:
- **Amazon Textract** → Extracts text and structured data from scanned documents
- **Amazon SageMaker** → Builds, trains, and deploys custom ML models; more complex than needed here
- **Amazon Rekognition** → Analyzes images and videos

### 3.5 - Exam Focus

Match the service to the data type and task:
- **Text sentiment / entities / key phrases → Amazon Comprehend**
- **Extract text from scanned documents → Amazon Textract**
- **Image and video analysis → Amazon Rekognition**
- **Build and deploy custom ML models → Amazon SageMaker**

Key wording:

**"Sentiment analysis", "customer emotions", "key themes", "text insights" → Amazon Comprehend**

## 4 - Unpacking Amazon SageMaker

### 4.1 - Original Question

Which Amazon SageMaker service is designed to streamline the **data preparation process** by allowing users to **visually clean and transform data** for machine learning?

### 4.2 - Choices

- A. **Amazon SageMaker Feature Store**  
- B. **Amazon SageMaker Clarify**  
- C. **Amazon SageMaker Pipelines**  
- D. **Amazon SageMaker Data Wrangler**

### 4.3 - Correct Answer

D. Amazon SageMaker Data Wrangler

### 4.4 - Why?

**SageMaker Data Wrangler** is specifically designed for **data preparation**, including visually cleaning, transforming, and analyzing data before model training.

The other options serve different purposes:
- **Feature Store** → Stores and manages reusable ML features
- **Clarify** → Used for model explainability and bias detection
- **Pipelines** → Automates and orchestrates ML workflows

The key clue in the question is **"visually clean and transform data"**

### 4.5 - Exam Focus

Memorize the role of these SageMaker services:

- **Data preparation / cleaning / transformation** → Data Wrangler
- **Store and reuse features** → Feature Store
- **Workflow automation and orchestration** → Pipelines
- **Bias detection and explainability** → Clarify

Key wording:

**"Prepare data", "clean data", "transform data", "visual data preparation"**  → **SageMaker Data Wrangler**