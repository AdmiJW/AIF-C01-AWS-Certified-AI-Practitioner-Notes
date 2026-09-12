## 1 - Introducing Amazon SageMaker

### 1.1 - Amazon SageMaker Overview

**Amazon SageMaker** is a fully managed AWS service for building, training, and deploying machine learning (ML) models.

It acts as a **one-stop platform for the ML lifecycle**, supporting the major stages of the ML workflow:
1. Prepare and process data
2. Train and tune models
3. Deploy models for inference

SageMaker also provides **versioning and tracking** capabilities to manage different model iterations.

It supports multiple machine learning approaches, including:
- Supervised learning
- Unsupervised learning
- Reinforcement learning
- Deep learning

#### Key Exam Idea

If a question asks for an AWS service that provides an **end-to-end managed environment for developing, training, and deploying ML models**, the answer is usually **Amazon SageMaker**.

### 1.2 - Amazon SageMaker Studio

**SageMaker Studio** is an integrated development environment (IDE) for machine learning.

It provides a centralized visual interface where developers and data scientists can manage ML projects throughout the development lifecycle.

Key capabilities include:
- **Jupyter Notebooks** for writing and executing ML code
- Tools for **data preparation and visualization**
- Model building, training, and deployment
- Collaboration between multiple users

Think of SageMaker Studio as the **main workspace/interface for working with SageMaker ML projects**.

### 1.3 - SageMaker Canvas

**SageMaker Canvas** provides a **no-code interface** for building and training machine learning models.

Users can create ML models without needing to write programming code.

#### Key Distinction

**SageMaker Studio** → Full ML development environment for developers and data scientists

**SageMaker Canvas** → No-code ML model creation, suitable for users who do not need to write code.

This distinction is important for scenario-based exam questions.

### 1.4 - SageMaker Pipelines

**SageMaker Pipelines** is used to create and automate **machine learning workflows**

A pipeline can contain multiple steps representing different stages of the ML lifecycle, such as:

`Data Preprocessing → Model Training → Hyperparameter Tuning → Deployment`

Pipelines ensure that the steps run in the correct sequence and can provide **versioning and tracking** of ML workflows.

This is useful for creating repeatable and automated ML processes.

#### Key Exam Idea

If a scenario asks how to **automate or orchestrate multiple stages of an ML workflow**, think **SageMaker Pipelines**

### 1.5 - SageMaker Autopilot / AutoML

**SageMaker Autopilot** provides **AutoML (Automated Machine Learning)** capabilities.

AutoML automates tasks such as:
- Selecting appropriate machine learning algorithms/models
- Training candidate models
- Hyperparameter tuning

The user mainly provides:
1. Training data
2. The **target variable** to predict

For example, in an email spam classification dataset, the target variable could be:

`Is_Spam → Yes/No`

Autopilot then performs much of the model-building process automatically with minimal manual intervention.

Autopilot can also be incorporated as a step within a **SageMaker Pipeline**.

### 1.6 - Exam Focus

Know the role of each SageMaker component:

| **Service / Feature**   | **Main Purpose**                          |
| ----------------------- | ----------------------------------------- |
| **Amazon SageMaker**    | End-to-end managed ML service             |
| **SageMaker Studio**    | Integrated ML development environment     |
| **SageMaker Canvas**    | Build ML models without writing code      |
| **SageMaker Pipelines** | Automate and orchestrate ML workflows     |
| **SageMaker Autopilot** | Automatically build/select/tune ML models |

Pay particular attention to scenario questions:
- **Need to build, train, and deploy ML models? → SageMaker**
- **Need an ML development workspace? → SageMaker Studio**
- **Need no-code ML? → SageMaker Canvas**
- **Need automated ML workflow orchestration? → SageMaker Pipelines**
- **Need automatic model selection and hyperparameter tuning? → SageMaker Autopilot / AutoML**

## 2 - Amazon SageMaker Data Wrangler

### 2.1 - Amazon SageMaker Data Wrangler

**Amazon SageMaker Data Wrangler** is a SageMaker feature used to **prepare, clean, transform, and analyze data for machine learning**

It focuses on the **data preparation stage** of the ML lifecycle, before model training

Data Wrangler is available within **Amazon SageMaker Studio** and provides a visual interface for working with data.

It supports multiple data types, including:
- Tabular data
- Images
- Text
- Time series data

It also supports **SQL** for manipulating data

### 2.2 - Data Import and Cleaning

Data Wrangler can import data from AWS data sources such as:
- **Amazon S3**
- **Amazon Redshift**
- **Amazon Athena**

After importing the data, it can help clean common data quality problems such as:
- Missing values
- Duplicate records
- Outliers

The goal is to convert raw data into a form that is suitable for machine learning.

### 2.3 - Feature Engineering

Data Wrangler supports **feature engineering**, which involves transforming existing data or creating new features that may improve model performance.

Built-in transformations include:
- **Scaling** numerical values
- **Encoding categorical variables**
- Creating **derived features**

For the exam, associate Data Wrangler with both **data cleaning** and **feature transformation**

### 2.4 - Exploratory Data Analysis (EDA)

Data Wrangler can also perform **Exploratory Data Analysis (EDA)**.

EDA helps users understand the structure and quality of a dataset before training a model.

Data Wrangler provides tools to:
- Visualize data
- Summarize data
- Identify patterns or potential data quality issues

This helps determine whether the dataset is ready for model training.

### 2.5 - Exam Focus

The main exam association is:
**Cleaning, preparing, or transforming ML data → SageMaker Data Wrangler**

Remember the typical workflow:
`Import Data → Clean Data → Feature Engineering → Explore / Analyze Data`

Key distinctions:
- **SageMaker Data Wrangler** → Prepare and transform data
- **SageMaker Autopilot** → Automate model selection and tuning
- **SageMaker Pipelines** → Automate the overall ML workflow
- **SageMaker Canvas** → Build ML models using a no-code interface

## 3 - Amazon SageMaker Feature Store

### 3.1 - Amazon SageMaker Feature Store

**Amazon SageMaker Feature Store** is a centralized repository for **storing, managing, retrieving, and sharing machine learning features**.

A **feature** is an input variable used by an ML model. During **feature engineering**, raw data is transformed into useful features.

Without a feature store, teams may repeatedly recreate the same features for different models, causing duplicated work and inconsistent definitions.

### 3.2 - Why Feature Store Is Used

Feature Store allows teams to **reuse previously created features** across multiple ML projects.

This helps:
- Reduce duplicated feature engineering work
- Maintain consistent feature definitions
- Share features across teams and models
- Centralize feature management

Features can be created directly in SageMaker Feature Store or prepared using **SageMaker Data Wrangler** and then published to the Feature Store.

Typical flow:
`Raw Data → Data Wrangler → Feature Engineering → Feature Store → ML Models`

### 3.3 - Data Wrangler vs Feature Store

These two services are related but serve different purposes

**SageMaker Data Wrangler** is mainly used to **clean, prepare, and transform data**

**SageMaker Feature Store** is mainly used to **store and reuse the resulting ML features**

Example:

Data Wrangler creates a feature such as:
`Customer_Average_Monthly_Spending`

Instead of recreating this feature for every new model, it can be stored in **Feature Store** and reused later.

### 3.4 - Exam Focus

The strongest exam association is:
**Store, centralize, share, or reuse ML features → SageMaker Feature Store**

Remember the distinction:

**Data preparation / feature engineering** → SageMaker Data Wrangler
**Centralized feature storage and reuse** → SageMaker Feature Store

If an exam question mentions avoiding **recreating the same features across multiple ML models**, think **SageMaker Feature Store**

## 4 - Demo: Amazon SageMaker Console Walkthrough

### 4.1 - SageMaker Studio Console Overview

This topic is mainly a **console walkthrough** and is **not expected to be directly tested** in the exam.

The important takeaway is understanding where the major SageMaker capabilities fit within **SageMaker Studio**

SageMaker Studio acts as a centralized environment for accessing tools used throughout the ML lifecycle.

### 4.2 - Key SageMaker Studio Applications and Features

**JupyterLab** is used to write, run, and work with code for ML development.

**SageMaker Canvas** provides a no-code interface for building ML models.

Under the data-related features:
- **Data Wrangler** → Data preparation, cleaning, and transformation
- **Feature Store** → Centralized storage and reuse of ML features

Other important capabilities include:
- **AutoML / Autopilot** → Automates model selection and hyperparameter tuning
- **Experiments** → Track and compare ML experiments
- **Training and evaluation jobs** → Train and access models
- **SageMaker Pipelines** → Orchestrate ML workflows
- **Model management** → Register, deploy, and share models

### 4.3 - SageMaker JumpStart

**SageMaker JumpStart** provides access to **prebuilt and pretrained models** that can be quickly used or customized

It can include models from external providers and model hubs such as **Hugging Face**.

For the exam, associate JumpStart with:

**Quickly getting started using existing pretrained models instead of building a model from scratch**

### 4.4 - Model Deployment

SageMaker Studio also provides capabilities for managing deployed models and **endpoints**.

An **endpoint** is commonly used to host a trained model so applications can send requests to it for inference.

Typical flow:
`Train Model → Deploy Model → Endpoint → Generate Predictions`

### 4.5 - Exam Focus

You do **not** need to memorize the SageMaker console layout or navigation steps.
Focus instead on recognizing the purpose of the main SageMaker features:
- **JupyterLab** → Code-based ML development
- **Canvas** → No-code ML
- **Data Wrangler** → Prepare and transform data
- **Feature Store** → Store and reuse features
- **Autopilot / AutoML** → Automated model selection and tuning
- **Pipelines** → ML workflow orchestration
- **JumpStart** → Prebuilt and pretrained models
- **Endpoints** → Host deployed models for inference

## 5 - Amazon SageMaker Deployments

### 5.1 - SageMaker Model Deployment

When a model is deployed in **Amazon SageMaker**, it can be exposed for inference so applications can send input data and receive predictions.

SageMaker supports several inference options, and the exam commonly tests **which deployment type best matches a workload**.

### 5.2 - Real-Time Inference

**Real-time inference** provides **synchronous predictions**

The client sends a request and waits for the model to return the prediction immediately.

Best suited for applications that require:
- **Low latency**
- **Immediate responses**
- **Consistent or predictable traffic**

Common use cases include:
- Chatbots
- Recommendation systems
- Real-time fraud detection

#### Key Exam Idea

If an application needs an **immediate prediction**, choose **real-time inference**

### 5.3 - Asynchronous Inference

**Asynchronous inference** allows an application to submit a request without waiting for an immediate response.

The model processes the request in the background, and the result can be retrieved later.

It is useful when:
- Requests take longer to process
- Payloads are large
- Workloads are unpredictable

Typical use cases include:
- Large file processing
- Complex ML models
- Image processing
- Video processing

#### Key Distinction

- **Real-time inference** → Client waits for an immediate result
- **Asynchronous inference** → Request is processed in the background and the result is retrieved later

### 5.4 - Batch Transform

**Batch Transform**, also called **batch inference**, is used to generate predictions for **large datasets in batches**.

It runs asynchronously and is suitable when predictions do not need to be returned immediately.

Example:
`Large Dataset → Batch Transform → Predictions for Entire Dataset`

Typical use cases include overnight processing or periodically generating predictions for large datasets.

Use Batch Transform when:
- There is a **large volume of data**
- Processing happens periodically
- **Latency is not important**

### 5.5 - Serverless Inference

**Serverless inference** runs ML models without requiring you to manage dedicated inference infrastructure.

SageMaker automatically allocates and scales compute resources based on incoming requests.

It is well suited for:
- Sporadic traffic
- Variable or unpredictable workloads
- Development and prototyping
- Applications where keeping dedicated infrastructure running would be inefficient

Serverless inference can help reduce cost because resources are not continuously provisioned for workloads with infrequent usage.

### 5.6 - Choosing an Inference Option

The key difference between the deployment options is the **workload pattern and latency requirement**

| **Inference Type**  | **Best for**                      | **Key Characteristic**                                |
| ------------------- | --------------------------------- | ----------------------------------------------------- |
| **Real-time**       | Interactive applications          | Immediate, low-latency response                       |
| **Asynchronous**    | Long-running or large requests    | Process now, retrieve result later                    |
| **Batch Transform** | Large offline datasets            | Process many records together                         |
| **Serverless**      | Sporadic or unpredictable traffic | Automatically scales without dedicated infrastructure |

### 5.7 - Exam Focus

Expect scenario questions asking you to choose the correct inference method.

- **Need an immediate prediction with low latency? → Real-time inference**
- **Request takes a long time or involves large files? → Asynchronous inference**
- **Need predictions for a large dataset, such as overnight processing? → Batch Transform**
- **Traffic is sporadic or unpredictable and you want to avoid managing infrastructure? → Serverless inference**

The most important distinction is:
`Immediate request/response → Real-time`
`Long-running request → Asynchronous`
`Large offline dataset → Batch Transform`
`Variable or infrequent traffic → Serverless`

## 6 - Exam Tips

### 6.1 - SageMaker Key Services Recap

**Amazon SageMaker** is a fully managed service for building, training and deploying ML models.

Key features to remember:
- **SageMaker Studio** → IDE for ML development
- **Data Wrangler** → Prepare, clean, and transform data
- **Feature Store** → Store and reuse ML features
- **SageMaker Pipelines** → Automate and orchestrate ML workflows
- **AutoML / Autopilot** → Automate model selection and hyperparameter tuning

Typical workflow:
`Data Wrangler → SageMaker Pipelines → AutoML → Deployment`

### 6.2 - SageMaker Deployment Recap

Know which inference option fits each workload:

| **Deployment Type**        | **Best Use**                                  |
| -------------------------- | --------------------------------------------- |
| **Real-time inference**    | Low-latency, immediate predictions            |
| **Asynchronous inference** | Long-running or complex requests              |
| **Batch Transform**        | Large datasets where latency is not important |
| **Serverless inference**   | Variable or unpredictable workloads           |

### 6.3 - Exam Focus

Prioritize matching the scenario to the correct SageMaker feature:

- **Clean / prepare data** → Data Wrangler
- **Store / reuse features** → Feature Store
- **Automate ML workflow** → Pipelines
- **Automatically select / tune models** → AutoML / Autopilot
- **Immediate response** → Real-time inference
- **Long processing time** → Asynchronous inference
- **Large offline dataset** → Batch transform
- **Variable / sporadic traffic** → Serverless inference
