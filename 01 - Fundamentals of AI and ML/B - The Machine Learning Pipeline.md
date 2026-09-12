## 1. Exploring the Machine Learning Pipeline

### 1.1 - Machine Learning Pipeline Overview

The **Machine Learning (ML)** pipeline generally consists of three major stages:

1. **Generate and Prepare data**
	- Fetch data
	- Clean data
	- Prepare data for analysis
2. **Train and evaluate the model**
	- Train the model
	- Tune the model
	- Evaluate model performance
3. **Deploy and monitor**
	- Deploy the model to production
	- Monitor and evaluate its performance
	- Collect additional data and refine the model over time

The ML pipeline is often **iterative**, meaning monitoring results may lead back to collecting more data and retraining the model.

### 1.2 - Data Collection and Cleaning

#### Fetching Data

Data can come from many sources, including:
- **Amazon S3**
- APIs
- Real-time data streams 
- Application or device-generated data
- Existing datasets

The goal is to collect the relevant data required to solve the identified ML problem.

#### Why Data Cleaning is Necessary

Real-world data is often messy and may contain:
- Missing or blank values
- `NaN` (Not a Number) values
- Invalid values
- Inconsistent formats
- Inconsistent units
- Inconsistent data types
- Duplicate records
- Irrelevant data

Data cleaning ensures the dataset is **accurate, consistent, and usable for ML**

#### Common Data Cleaning Techniques

**Missing Values**
- Fill / Impute missing values
- Remove records containing unusable null values

**Standardize data types**
- Ensure a feature consistently uses the appropriate type, such as:
	- Integer
	- Float

**Standardize units and formats**
- Convert measurements to consistent units
- Use consistent date/time formats
- Use consistent currency formats

**Standardize column names**
- Apply a consistent naming convention

**Remove unnecessary data**
- Remove or merge:
	- Duplicate records
	- Irrelevant records

### 1.3 - Exploratory Data Analysis  (EDA)

**Exploratory Data Analysis (EDA)** is performed before applying modeling techniques.

Its purpose is to understand the dataset and identify:
- Patterns
- Relationships between variables
- Anomalies/outliers
- Potential data quality issues

EDA can help:
- Form hypotheses
- Gain insights into the data
- Guide model-selection decisions

#### Common EDA Techniques

**Visualizations**
- Charts
- Graphs

Used to visually identify trends, distributions, relationships, and unusual observations.

**Descriptive Statistics**
- Mean
- Median

Used to summarize important characteristics of the dataset.

### 1.4 - Correlation Matrix

A **correlation matrix** is used to quantify the relationship between variables.

Correlation scores range from:

`-1` to `+1`

#### Interpreting Correlation

| **Correlation** | **Meaning**                  |
| --------------- | ---------------------------- |
| `+1`            | Perfect positive correlation |
| `0`             | No linear relationship       |
| `-1`            | Perfect negative correlation |

**Positive correlation**
- As one variable increases, the other tends to increase

**Negative correlation**
- As one variable increases, the other tends to decrease

**Strength of correlation**
- Determined by the absolute value of the correlation score
- Values closer to `1` or `-1` represent stronger relationships
- Values closer to `0` represent weaker linear relationships

The diagonal of a correlation matrix contains `1`s because every variable is perfectly correlated with itself.

#### Exam Focus
- You generally **do not need to calculate or deeply interpret a correlation matrix**
- Know that a correlation matrix is an **EDA tool used to examine relationships between variables**
- Be able to recognize when it is an appropriate tool for a scenario
- Be careful if it appears as a **distractor in questions about model evaluation;** correlation matrices analyze relationships within data rather than directly evaluating ML model performance.

## 2. What is Feature Engineering?

### 2.1 - What is Feature Engineering?

**Feature engineering** transforms raw data into a format that makes it easier for machine learning models to learn useful patterns.

It is part of the **data preparation stage** of the ML pipeline.

Common feature engineering techniques include:
- Feature selection
- Feature extraction
- Dimensionality reduction
- Categorical encoding
- Normalization
- Standardization

### 2.2 - Feature Selection

**Feature selection** means choosing the most relevant features and removing unnecessary ones.

Removing irrelevant features can:
- Reduce training time
- Simplify the dataset
- Prevent the model from learning irrelevant patterns
- Potentially improve model performance

Example:

For an auto loan prediction model, features such as:
- Vehicle size
- Vehicle color
may be irrelevant to the loan outcome and could potentially be removed.

#### Important Consideration

Features should not be removed arbitrarily.

Before removing features, consider:
- Consulting domain expertise
- Exploratory Data Analysis (EDA)
- Whether the feature has a meaningful relationship with the prediction target

### 2.3 - Feature Extraction

**Feature extraction** creates new features from existing features.

The goal is to derive information that may be more useful to the ML model.

Examples:

**Vehicle age**

`Vehicle Age = Current Year - Vehicle Manufacturing Year`
This may provide more useful information than the manufacturing year itself.

**Price per mile**

`Price per Mile = Vehicle Price / Miles Driven`
This combines existing data into a potentially more meaningful feature.

#### Exam Focus

Feature extraction means:

> **Creating new useful features from existing data**

Do not confuse this with feature selection, which chooses which existing features to keep.

### 2.4 - Dimensionality Reduction

**Dimensionality reduction** reduces the number of features in a dataset while attempting to preserve its important information.

Benefits include:
- Simpler datasets
- Faster model training
- Reduced computational requirements
- Easier handling of datasets with many features

#### Principal Component Analysis (PCA)

**Principal Component Analysis (PCA)** is a common dimensionality reduction technique

PCA combines multiple related features into a smaller number of new features called **principal components**.

Example:

Multiple financial features such as:
- Loan amount
- Vehicle price
- Down payment
could potentially be represented by a single principal component.

Similarly,
- Vehicle age
- Mileage
could be combined into another component representing vehicle depreciation

#### Exam Focus

Know that:

**PCA → Dimensionality reduction**

Its purpose is to **reduce the number of dimensions/features while retaining important information**.

### 2.5 - Categorical Encoding

Many ML algorithms work primarily with **numerical input**.

**Categorical encoding** converts categorical/textual values into numerical representations.

Example:

| **Vehicle Type** | **Encoded Value** |
| ---------------- | ----------------- |
| Truck            | 0                 |
| SUV              | 1                 |
| Sedan            | 2                 |

#### Exam Focus

You do not need to know how to implement different encoding techniques.

Recognize categorical encoding as the appropriate approach when:

> **Categorical or text labels must be converted into numerical values for an ML model**

### 2.6 - Handling Different Feature Scales

Features in a dataset can have very different ranges or units.

Example:
- Age: `40-65`
- Salary: potentially `>100,000`

Without scaling, a feature with much larger numerical values may have excessive influence on certain ML algorithms.

Two important techniques are:
- Normalization
- Standardization

### 2.7 - Normalization

**Normalization** rescales numerical values into a common range, commonly:

`0 to 1`

Example conceptually:

Different features are transformed so that their values all fit within the same range.

#### Why Use Normalization?

It prevents features with larger numerical scales from dominating simply because of their magnitude.

#### Exam Recognition

**Normalization → typically rescales values to a range such as 0 - 1**

### 2.8 - Standardization

**Standardization** transforms feature values so that:
- Mean = `0`
- Standard deviation = `1`

This places features with different original scales onto a more comparable scale.

#### Exam Recognition

Remember the distinction:

| **Technique**       | **Result**                                       |
| ------------------- | ------------------------------------------------ |
| **Normalization**   | Values commonly scaled between `0` and `1`       |
| **Standardization** | Mean becomes `0`, standard deviation becomes `1` |

You do not need to calculate either transformation for the exam.

The key concept is that both techniques help create a **more consistent scale across features**, allowing ML models to learn more effectively.

### 2.9 - Feature Engineering Exam Summary

| **Technique**                | **Purpose**                                                         |
| ---------------------------- | ------------------------------------------------------------------- |
| **Feature Selection**        | Keep relevant features and remove unnecessary ones                  |
| **Feature Extraction**       | Create new features from existing data                              |
| **Dimensionality Reduction** | Reduce the number of features while retaining important information |
| **PCA**                      | Common dimensionality reduction technique                           |
| **Categorical Encoding**     | Convert categorical/text values into numerical values               |
| **Normalization**            | Rescale values, commonly to `0-1`                                   |
| **Standardization**          | Transform data to mean `0` and standard deviation `1`               |
|                              |                                                                     |

## 3. Hyperparameters vs. Parameters

### 3.1 - Parameters vs. Hyperparameters

Both **parameters** and **hyperparameters** affect model performance, but they serve different purposes.

|                          | **Parameters**                               | **Hyperparameters**                          |
| ------------------------ | -------------------------------------------- | -------------------------------------------- |
| How determined           | **Learned automatically** from training data | **Specified before training**                |
| Changed during training? | Yes                                          | Usually remain fixed during one training run |
| Purpose                  | Represent learned relationships in data      | Control how the learning algorithm trains    |
| Examples                 | Weights, biases                              | Learning rate, batch size, epochs            |

#### Exam Focus

The key distinction is:
- **Parameters → learned by the model**
- **Hyperparameters → configured to control model training**

### 3.2 - Model Parameters

During training, the ML algorithm adjusts its **parameters** to reduce prediction errors.

Common examples include:
- **Weights**
- **Biases**

#### Weights

**Weights** determine how strongly different inputs/features influence the model's prediction.

For example, an auto-related model might use:
- Car age
- Price
- Mileage

A feature with a **higher learned weight** generally has greater influence on the model's calculation than one with a lower weight.

The model automatically adjusts these weights during training.

#### Biases

A **bias** is an additional learned value that allows the model to shift its predictions rather than relying only on weighted input values.

Both **weights and biases are learned automatically during training**.

### 3.3 - Hyperparameters

**Hyperparameters** are configuration settings that control the behavior of the learning algorithm.

They are:
- Defined **before training begins**
- Fixed during an individual training run
- Adjustable between training runs
- Tuned to improve model performance

Hyperparameters can affect:
- Training speed
- Learning effectiveness
- Model accuracy
- Underfitting and overfitting

Different algorithms can have different hyperparameters.

Common examples include:
- Learning rate
- Batch size
- Number of epochs

### 3.4 - Learning Rate

The **learning rate** controls how much the model changes its parameters, such as weights and biases, during each update.

#### High Learning Rate

A high learning rate:
- Makes larger parameter updates
- Can train faster
- May **overshoot the optimal solution**
- Can make training unstable or prevent convergence

#### Low Learning Rate

A low learning rate:
- Makes smaller, more gradual updates
- Can provide more precise learning
- Usually requires more training time
- May converge very slowly

#### Exam Focus

Think of learning rate as:

> **How large a step the model takes when adjusting its parameters**

The goal is to find a value that balances **training speed and effective convergence**

### 3.5 - Batch Size

**Batch size** is the number of training examples processed before the model updates its parameters.

#### Larger Batch Size
- Processes more examples before each parameter update
- Typically requires fewer updates
- Can make training computationally efficient
- May capture less fine-grained variation between individual examples

#### Smaller Batch Size
- Uses fewer examples before each update
- Updates parameters more frequently
- Can provide more fine-grained learning
- May take longer to train

#### Exam Recognition

**Batch size → number of training examples processed before a parameter update**

Do not confuse batch size with epochs

### 3.6 - Epochs

An **epoch** is one complete pass through the entire training dataset.

Example:

`10 epochs = model processes the entire training dataset 10 times`

The number of epochs influences how much opportunity the model has to learn from the training data.

#### Too Few Epochs → Underfitting

With too few epochs, the model may not learn enough patterns from the data

**Underfitting**:
- Poor performance on training data
- Poor performance on unseen/test data
- Model has not learned the underlying patterns sufficiently

#### Too Many Epochs → Overfitting

With too many epochs, the model may begin memorizing the training data

**Overfitting**:
- Very good performance on training data
- Poor performance on new/unseen data
- Model fails to generalize

#### Exam Focus

| **Situation**   | **Likely Problem** |
| --------------- | ------------------ |
| Too few epochs  | **Underfitting**   |
| Too many epochs | **Overfitting**    |

### 3.7 - Early Stopping

**Early stopping** can help prevent overfitting by stopping training when model performance stops improving.

It commonly involves:
- Setting a maximum number of epochs
- Monitoring a performance metric
- Defining a **patience period**

#### Patience

**Patience** specifies how many epochs training should continue without improvement before stopping.

Example concept:
If patience is `5`, training may stop after 5 consecutive epochs without meaningful improvement.

#### Exam Focus

**Early stopping → technique used to reduce overfitting by stopping training when further epochs are no longer improving performance**

### 3.8 - Hyperparameter Tuning

**Hyperparameter tuning** is the process of finding hyperparameter values that produce better model performance.

Examples of values that may be tuned:
- Learning rate
- Batch size
- Number of epochs

Because different combinations can produce significantly different results, multiple training runs may be required.

### 3.9 - Grid Search

**Grid search** evaluates combinations of predefined hyperparameter values.

Example:
- Learning rate: `0.01`, `0.1`
- Batch size: `32`, `64`

Grid search tests every specified combination.

#### Advantages
- Systematic
- Can identify strong combinations within the supplied search space

#### Disadvantages
- Computationally expensive
- Time-consuming when many hyperparameters or values are tested

#### Exam Recognition

**Grid search → systematically tests all specified hyperparameter combinations**

### 3.10 - Random Search

**Random search** randomly selects combinations from predefined hyperparameter ranges.

Compared with grid search, it:
- Does not test every possible combination
- Can find effective combinations more quickly
- Typically requires fewer training runs

#### Exam Recognition

| **Method**        | **Approach**                     |
| ----------------- | -------------------------------- |
| **Grid Search**   | Tests all specified combinations |
| **Random Search** | Samples random ccombinations     |

Random search is useful when exhaustive grid search would be too expensive or time-consuming.

### 3.11 - Amazon SageMaker Automatic Model Tuning

**Amazon SageMaker Automatic Model Tuning** can automate the process of finding effective hyperparameter values.

Instead of manually testing configurations, SageMaker can:
- Run multiple training jobs
- Evaluate different hyperparameter combinations
- Identify configurations that optimize the chosen performance metric

#### Exam Focus

If a question asks for an AWS service or capability that can **automatically optimize model hyperparameters**, look for **Amazon SageMaker Automatic Model Tuning**

### 3.12 - Exam Summary

| **Concept**                          | **Key Point**                                         |
| ------------------------------------ | ----------------------------------------------------- |
| **Parameter**                        | Learned automatically from training data              |
| **Weight**                           | Controls the influence of inputs/features             |
| **Bias**                             | Learned offset that adjusts model predictions         |
| **Hyperparameter**                   | Configuration set before training                     |
| **Learning Rate**                    | Controls size/speed of parameter updates              |
| **Batch Size**                       | Number of examples processed before an update         |
| **Epoch**                            | One complete pass through the training dataset        |
| **Too few epochs**                   | Can cause underfitting                                |
| **Too many epochs**                  | Can cause overfitting                                 |
| **Early stopping**                   | Stops training when performance stops improving       |
| **Patience**                         | Number of unimproved epochs tolerated before stopping |
| **Grid Search**                      | Tests all specified combinations                      |
| **Random Search**                    | Tests randomly selected combinations                  |
| **SageMaker Automatic Model Tuning** | Automates hyperparameter optimization                 |

## 4. Metrics for Classification Models

### 4.1 - Classification Outcomes

Classification models are commonly evaluated using four prediction outcomes:

| **Outcome**             | **Meaning**                                          | **Example**                                 |
| ----------------------- | ---------------------------------------------------- | ------------------------------------------- |
| **True Positive (TP)**  | Model predicts positive, and it is actually positive | Shark correctly identified as a shark       |
| **True Negative (TN)**  | Model predicts negative, and it is actually negative | Seaweed correctly identified as not a shark |
| **False Positive (FP)** | Model predicts positive, but it is actually negative | Fish incorrectly identified as a shark      |
| **False Negative (FN)** | Model predicts negative, but it is actually positive | Shark incorrectly missed                    |

#### Exam Recognition
- **False Positive → false alarm**
- **False Negative → missed positive case**

Which error matters more depends on the business scenario.

### 4.2 - Class Imbalance

**Class imbalance** occurs when one class is much more common than another.

Example:

In fraud detection:
- Legitimate transactions → very common
- Fraudulent transactions → relatively rare

This can make some evaluation metrics, especially **accuracy**, misleading.

A model could predict every transaction as legitimate and still achieve high accuracy if fraudulent transactions are rare.

### 4.3 - Accuracy

**Accuracy** measures the proportion of all predictions that are correct.

Conceptually:

`Correct Predictions / Total Predictions`

It considers both:
- True Positives
- True Negatives

#### Limitation

Accuracy can be misleading with **imbalanced datasets**

Example:
If 90% of samples belong to one class, a model that always predicts that class could achieve approximately 90% accuracy despite performing poorly on the minority class.

#### Exam Focus

Use accuracy when:
- Classes are reasonably balanced
- Overall correctness is the main concern
Be cautious when:
- The dataset is highly imbalanced

### 4.4 - Precision

**Precision** measures how many predicted positive cases are actually positive

Conceptually:

`TP / (TP + FP)`

In other words:

> Of everything the model predicted as positive, how many were actually positive?

High precision means **few false positives**

#### When Precision Matters

Precision is important when **false positives are costly**

Examples:
- Fraud detection where legitimate transactions should not be unnecessarily blocked
- Spam detection where legitimate emails should not be marked as spam

#### Exam Shortcut

**Precision → minimize false positives / false alarms**

If a question emphasizes the cost of incorrectly flagging something as positive, precision is likely important.

### 4.5 - Recall

**Recall**, also called **sensitivity**, measures how many actual positive cases the model successfully identifies.

Conceptually:

`TP / (TP + FN)`

In other words:

> Of all the cases that were actually positive, how many did the model detect?

High recall means **few false negatives**

#### When Recall Matters

Recall is important when **missing a positive case has serious consequences**

Examples:
- Detecting diseases
- Identifying dangerous conditions
- Detecting fraud when missing fraudulent transactions is highly costly

#### Exam Shortcut

**Recall → minimize false negatives / missed positives**

If a question emphasizes that positive cases must not be missed, recall is likely the key metric.

### 4.6 - Precision vs. Recall

Precision and recall focus on different types of errors.

| **Metric**    | **Main Question**                                          | **Tries to Reduce** |
| ------------- | ---------------------------------------------------------- | ------------------- |
| **Precision** | When the model predicts positive, how often is it correct? | False Positives     |
| **Recall**    | Of all actual positives, how many were detected?           | False Negatives     |

#### Easy Exam Memory
- **Precision → avoid false alarms**
- **Recall → avoid missing real positives**

Improving one may sometimes reduce the other, so the correct choice depends on business requirements.

### 4.7 - F1 Score

The **F1 Score** combines precision and recall into a single metric.

It is the **harmonic mean of precision and recall**

F1 score is useful when:
- Both precision and recall matter
- The dataset is imbalanced
- You want one metric that balances false positives and false negatives

A high F1 score indicates that the model achieves a good balance between precision and recall.

#### Exam Focus

If a scenario requires:

> **A balance between precision and recall**

look for:

**F1 score**

### 4.8 - Confusion Matrix

A **confusion matrix** summarizes a classification model's predicted values against the actual values.

It contains:
- True Positives
- True Negatives
- False Positives
- False Negatives

Example structure:

|                        | **Actual Positive** | **Actual Negative** |
| ---------------------- | ------------------- | ------------------- |
| **Predicted Positive** | True Positive       | False Positive      |
| **Predicted Negative** | False Negative      | True Negative       |

Metrics derived from the confusion matrix include:
- Accuracy
- Precision
- Recall
- F1 score

#### Exam Focus

A **confusion matrix is used to evaluate classification models** and understand what types of classification errors they are making.

Do not confuse it with a **correlation matrix**, which examines relationships between variables during data analysis.

### 4.9 - ROC Curve and AUC

The **ROC curve (Receiver Operating Characteristic curve)** evaluates how well a binary classification model distinguishes between classes across different classification thresholds.

It plots:
- **True Positive Rate (TPR)** - related to recall
- **False Positive Rate (FPR)**

This helps visualize the trade-off between correctly detecting positives and incorrectly classifying negatives as positives.

#### AUC

**AUC (Area Under the Curve)** summarizes the ROC curve into a single value.

AUC typically ranges from:

`0 to 1`

A higher AUC indicates a model that is generally better at distinguishing between positive and negative classes.

- AUC closer to `1` → better class discrimination
- AUC around `0.5` → approximately random classification

Different model configurations can be compared using their AUC values

#### Exam Focus

**AUC-ROC → evaluates a classification model's ability to distinguish between classes across different thresholds**

When comparing otherwise similar classifiers:

> **Higher AUC generally indicates better discriminatory performance**

### 4.10 - Classification Metrics Exam Summary

| **Metric / Concept**     | **Key Exam Meaning**                                    |
| ------------------------ | ------------------------------------------------------- |
| **True Positive**        | Positive prediction is correct                          |
| **True Negative**        | Negative prediction is correct                          |
| **False Positive**       | Incorrect positive / false alarm                        |
| **False Negative**       | Missed actual positive                                  |
| **Class imbalance**      | One class greatly outnumbers another                    |
| **Accuracy**             | Overall percentage of correct predictions               |
| **Precision**            | Focuses on reducing false positives                     |
| **Recall / Sensitivity** | Focuses on reducing false negatives                     |
| **F1 Score**             | Balances precision and recall                           |
| **Confusion Matrix**     | Shows TP, TN, FP, and FN                                |
| **ROC Curve**            | Plots true positive rate against false positive rate    |
| **AUC**                  | Measures overall ability to distinguish between classes |

## 5. Metrics for Regression Models

### 5.1 - Mean Absolute Error (MAE)

**Mean Absolute Error (MAE)** measures the average absolute difference between predicted values and actual values.

Conceptually:

`MAE = Average of |Actual - Predicted|`

Example:

If a house-price model has:
`MAE = $20,000`
The model's predictions are, on average, about **$20,000 away from the actual prices**.

#### Exam Focus
- Lower MAE → better predictions
- Easy to interpret because it uses the **same units as the target value**
- Treats all errors proportionally

Use MAE when you want a straightforward measure of the model's **average prediction error**

### 5.2 - Mean Squared Error (MSE)

**Mean Squared Error (MSE)** calculates the average of the squared differences between predicted and actual values.

Conceptually:

`MSE = Average of (Actual - Predicted)²`

Because errors are squared, **large errors receive a much larger penalty than small errors**

#### Exam Focus

Use MSE when:
- Large prediction errors should be penalized more heavily
- You want a regression metric that is sensitive to large errors/outliers

Lower MSE generally indicates better model performance.

**MAE vs. MSE**

| **Metric** | **Behavior**                                                   |
| ---------- | -------------------------------------------------------------- |
| **MAE**    | Treats errors proportionally                                   |
| **MSE**    | Penalizes large errors more heavily because errors are squared |

### 5.3 - Root Mean Squared Error (RMSE)

**Root Mean Squared Error (RMSE)** is the square root of MSE.

Conceptually:
`RMSE = √MSE`

Like MSE, RMSE penalizes larger errors more strongly.

However, taking the square root converts the result back into the **same unit as the target variable**, making it easier to interpret.

Example:

For house-price predictions, RMSE would be expressed in currency rather than squared currency units.

#### Exam Focus

RMSE combines two useful properties:
- **Penalizes large prediction errors**
- Produces an error value in the **original units of the prediction**

Lower RMSE generally indicates better model performance

### 5.4 - MAE vs. MSE vs. RMSE

| **Metric** | **Main Characteristic**                                       | **Units**            |
| ---------- | ------------------------------------------------------------- | -------------------- |
| **MAE**    | Average absolute error                                        | Same as target       |
| **MSE**    | Squares errors and strongly penalizes large errors            | Squared target units |
| **RMSE**   | Penalizes large errors but it is easier to interpret than MSE | Same as target       |

#### Exam Recognition
- Need **simple average error → MAE**
- Need to **penalize large errors more heavily → MSE**
- Need large-error sensitivity while retaining **original units → RMSE**

### 5.5 - R-Squared (R²)

**R-Squared (R²)** measures how much of the variation in the target variable can be explained by the model.

In the course context, values are generally interpreted between:
`0 and 1`
- Closer to `1` → model explains more of the variation
- Close to `0` → model explains little of the variation

Example:

`R² = 0.80`
means approximately **80% of the variation in the target variable is explained by the model,** while the remaining 20% is associated with other factors or unexplained variation.

#### Exam Focus

R² measures **how well the model explains variation in the output.**

A higher R² generally means a better fit.

Do not confuse R² with error metrics:
- **MAE / MSE / RMSE → lower is generally better**
- **R² → higher is generally better**

### 5.6 - Operational Performance Metrics

Model quality is not evaluated only by prediction accuracy. Production AL/ML systems may also be evaluated using operational metrics.

#### Average Response Time

**Average response time** measures how long the model takes to produce an output after receiving an input.

It can apply to:
- Predictions
- AI-generated responses
- Inference requests

**Exam Focus**

If a question asks about:
- Runtime performance
- Inference speed
- User-perceived latency
- How quickly the AI responds
Look for:
> **Average Response Time**

#### Training Sessions vs. Epochs

A **training session** refers to one complete execution of the model-training process.

A model might undergo multiple training sessions when:
- New datasets become available
- Hyperparameters are changed
- The model is retrained or improved

Within one training session, the dataset may be processed multiple times.

Each complete pass through the dataset is called an **epoch**.

Example:

`10 epochs`
means the model processes the entire training dataset **10 times during that training session**.

**Exam Focus**

Do not confuse:
- **Training session → one complete model-training run**
- **Epoch → one complete pass through the training dataset within a training run**

#### Customer Feedback and CSAT

**Customer feedback** provides information about how users perceive the AI system.

It can reveal issues such as:
- Poor accuracy
- Slow responses
- Unfair or biased behavior
- Poor user experience

**Customer Satisfaction Score (CSAT)**

**CSAT** measures how satisfied users are with a product or service.

It is a **business / user satisfaction metric**, not a technical runtime-performance metric

**Exam Focus**

If asked:

> Which metric measures how quickly an AI model responds?

Choose **average response time**, not CSAT.

If asked:

> Which metric measures customer satisfaction?

Choose **CSAT**.

#### Return On Investment (ROI)

**Return on Investment (ROI)** measures whether the financial benefits generated by an ML solution justify its costs.

Conceptually:
- Positive ROI → benefits exceed costs
- Negative ROI → costs currently exceed financial returns

ROI can help organizations evaluate the **business value** of an AI or ML project.

**Exam Focus**

Use ROI when the question asks whether:
- An AI project is financially worthwhile
- The business benefits justify the investment
- The ML solution is producing sufficient financial returns

#### Cost per User

**Cost per user** measures the average cost of providing an AI or ML service to each user.

Conceptually:
`Cost per User = Total Cost / Number of Users`

The metric is useful for:
- Budgeting
- Cost optimization
- Evaluating scalability
- Comparing operating costs as usage grows

**Exam Focus**

If a question asks about:

> How much does it cost to provide the AI service to each individual customer?

Look for:

**Cost per User**

### 5.7 - Regression Metrics Exam Summary

| **Metric**                | **Key Exam Meaning**                                                |
| ------------------------- | ------------------------------------------------------------------- |
| **MAE**                   | Average absolute prediction error                                   |
| **MSE**                   | Average squared error; penalizes large errors heavily               |
| **RMSE**                  | Square root of MSE; penalizes large errors and uses original units  |
| **R²**                    | Measures how much variation in the target is explained by the model |
| **Average Response Time** | Measures inference / runtime speed                                  |
| **Training session**      | One complete model-training run                                     |
| **Epoch**                 | One complete pass through the training dataset                      |
| **CSAT**                  | Measures customer satisfaction                                      |
| **ROI**                   | Measures financial return relative to investment                    |
| **Cost per User**         | Average cost of serving one user                                    |

#### Key Exam Direction

For regression error metrics:
`Lower MAE / MSE / RMSE = Better`

For R²:
`Higher R² = Generally Better`

## 6. Fundamentals of ML Operations

### 6.1 - What is MLOps?

**Machine Learning Operations (MLOps)** is a set of practices used to manage the **entire machine learning lifecycle**

It connects and manages stages such as:
- Data preparation
- Model development and training
- Model packaging
- Testing and validation
- Deployment
- Monitoring
- Model updates and retraining

The goal of MLOps is to make ML workflows more:
- Automated
- Consistent
- Reliable
- Repeatable
- Efficient

### 6.2 - Automation and Standardization

MLOps automates many stages of the ML lifecycle, including:
- Model development
- Model packaging
- Testing
- Deployment

Automation helps:
- Reduce manual work
- Save time
- Reduce human errors
- Create repeatable processes
- Streamline ML workflows

#### Exam Focus

If a scenario asks how to make ML development and deployment **repeatable and less dependent on manual processes**, MLOps automation is a key solution

### 6.3 - Version Control

MLOps uses **version control** for both:
- Models
- Datasets

Versioning helps track exactly which model and data versions were used.

It also helps ensure that the same model can be consistently deployed across environments such as:
- Development
- Testing
- Staging
- Production

#### Rollbacks

Version control also allows teams to **roll back** to an earlier model version.

This is useful when:
- A new model performs worse
- A deployment introduces unexpected problems
- A previous stable model needs to be restored

#### Exam Focus

**Version control → reproducibility, consistency, traceability, and rollback capability**

### 6.4 - Continuous Model Deployment

ML models often need updates because:
- New training data becomes available
- Hyperparameters are adjusted
- Model performance needs improvement

With an MLOps pipeline, updated models can automatically go through:

`Training → Testing → Validation → Deployment`

This reduces or eliminates manual intervention.

#### Exam Focus

MLOps supports **continuous integration and continuous deployment (CI/CD)** concepts for machine learning.

The key idea is:

> Updated models can be automatically validated and deployed through a standardized pipeline

### 6.5 - Model Monitoring

The ML lifecycle does not end after deployment.

MLOps continuously **monitors models in production** to ensure that they continue behaving as expected.

Metrics that may be monitored include:
- Accuracy
- Average response time
- Other model performance metrics
- Operational performance

Monitoring helps detect when:
- Model performance decreases
- Predictions become less accurate
- Response times increase
- A deployed model behaves unexpectedly

#### Exam Focus

**Model monitoring → evaluate production model behavior and performance over time.**

If a model performs well during development but needs to be checked after deployment, monitoring is the relevant MLOps practice.

### 6.6 - MLOps Lifecycle

A simplified MLOps lifecycle can be viewed as:

`Data → Train → Test/Validate → Deploy → Monitor → Update/Retrain`

The process is **continuous and iterative**.

Monitoring may reveal that the model needs:
- New data
- Retraining
- Hyperparameter tuning
- A new model version

The updated model then passes through the pipeline again.

### 6.7 - MLOps Exam Summary

| **MLOps Concept**           | **Key Exam Meaning**                                            |
| --------------------------- | --------------------------------------------------------------- |
| **MLOps**                   | Practices for managing the entire ML lifecycle                  |
| **Automation**              | Reduces manual work and errors                                  |
| **Standardization**         | Creates consistent and repeatable ML processes                  |
| **Model version control**   | Tracks different versions of models                             |
| **Dataset version control** | Tracks which data was used to develop models                    |
| **Consistency**             | Ensures appropriate model versions are used across environments |
| **Rollback**                | Restore a previous model if a new version causes problems       |
| **Continuous deployment**   | Automatically test, validate, and deploy updated models         |
| **Monitoring**              | Track production model performance and operational metrics      |
| **Retraining**              | Update a model using new data or configurations                 |

#### Key Exam Idea

Think of MLOps as the practices that turn ML development into a **repeatable production process:**

> **Automate → Version → Deploy → Monitor → Improve**

## 7. Exam Tips

### 7.1 - Machine Learning Pipeline

The ML process can be viewed in three broad stages:
1. **Generate and prepare data**
2. **Train and fine-tune the model**
3. **Deploy and monitor the model**

Early-stage data preparation includes:
- Fetching data
- Cleaning data
- Exploratory Data Analysis (EDA)
- Feature engineering

### 7.2 - Exploratory Data Analysis (EDA)

**EDA** helps understand a dataset before modeling

Common techniques include:
- Summarizing data using statistics such as averages
- Visualizing data with charts and graphs
- Identifying patterns and anomalies
- Formulating questions or hypotheses
- Using a **correlation matrix** to examine relationships between variables

#### Correlation Matrix

Correlation values generally range from `-1` to `+1`:
- Positive value → positive relationship
- Negative value → negative relationship
- Values closer to `±1` → stronger relationship

### 7.3 - Feature Engineering

**Feature engineering** transforms raw data into more useful inputs for ML models.

Key techniques:

| **Technique**                | **Purpose**                                                         |
| ---------------------------- | ------------------------------------------------------------------- |
| **Feature selection**        | Keep the most relevant existing features                            |
| **Feature extraction**       | Create new features from existing data                              |
| **Dimensionality reduction** | Reduce the number of features while retaining important information |
| **Scaling**                  | Put numerical features onto comparable scales                       |
| **Categorical encoding**     | Convert categorical values into numerical representations           |

### 7.4 - Parameters vs. Hyperparameters

This is a **high-priority exam topic**.

|               | **Hyperparameters**               | **Parameters**              |
| ------------- | --------------------------------- | --------------------------- |
| Determined by | User/tuning process               | Model                       |
| When          | Set before a training run         | Learned during training     |
| Purpose       | Control the learning process      | Directly affect predictions |
| Examples      | Learning rate, batch size, epochs | Weights, biases             |

Hyperparameters can be optimized using techniques such as:
- **Grid search**
- **Random search**

Parameters such as weights and biases are automatically adjusted by the training algorithm.

#### Exam Shortcut

> **Hyperparameters are configured; parameters are learned**

### 7.5 - Classification Metrics

Use these metrics for **classification problems**:

| **Metric**               | **Key Meaning**                                         |
| ------------------------ | ------------------------------------------------------- |
| **Accuracy**             | Proportion of all predictions that are correct          |
| **Precision**            | Of predicted positives, how many were actually positive |
| **Recall / Sensitivity** | Of actual positives, how many were correctly identified |
| **F1 Score**             | Balances precision and recall                           |

#### Exam Shortcut
- Avoid false positives → **Precision**
- Avoid false negatives → **Recall**
- Balance precision and recall → **F1 Score**
- Overall correctness → **Accuracy**

### 7.6 - Regression Metrics

Regression models predict **continuous numerical values** and are commonly evaluated by comparing predicted and actual values.

Important metrics include:

| **Metric** | **Key Meaning**                                                      |
| ---------- | -------------------------------------------------------------------- |
| **MAE**    | Average absolute prediction error                                    |
| **RMSE**   | Error metric that penalizes larger errors and retains original units |
| **R²**     | How much variation in the target is explained by the model           |

#### Exam Shortcut
- **Classification problem → Accuracy, Precision, Recall, F1**
- **Regression problem → MAE, MSE/RMSE, R²**

### 7.7 - Final Exam Reminders

Focus especially on recognizing the correct concept for a scenario:
- **EDA** → understand data before modeling
- **Correlation matrix** → relationships between variables
- **Feature Engineering** → improve model inputs
- **Parameters** → learned during training
- **Hyperparameters** → control training behavior
- **Grid / Random Search** → Hyperparameter tuning
- **Classification metrics** → evaluate categorical predictions
- **Regression metrics** → evaluate numerical predictions

The most important distinction from this module is:

> **Know whether a scenario involves data preparation, model training configuration, classification evaluation, or regression evaluation**