## 1 - Introducing AWS AI/ML Services

### 1.1 - AWS AI/ML Services Overview

AWS provides a range of **fully managed AI/ML services** that use **pre-trained machine learning models**.

These services allow developers to add AI capabilities to applications **without building or training ML models from scratch**.

Key characteristics:
- **Fully managed** - AWS handles the underlying infrastructure and operational tasks
- Built on AWS infrastructure for **scalability, availability, and reliability**
- Can operate across **multiple Availability Zones (AZ) and AWS Regions**
- Support both:
	- **Real-time processing** - immediate predictions or responses
	- **Batch processing** - process larger datasets asynchronously
- Generally use a **pay-as-you-go pricing model**.

#### Pre-trained AI Services

Pre-trained AWS AI services are designed for specific AI tasks and can be integrated directly into applications.

Examples include:

| **Domain**        | **AWS Service**        | **Primary Purpose**                             |
| ----------------- | ---------------------- | ----------------------------------------------- |
| Vision            | **Amazon Rekognition** | Analyze images and videos                       |
| Document / Vision | **Amazon Textract**    | Extract text and structured data from documents |
| Language          | **Amazon Comprehend**  | Analyze and understand text                     |
| Language          | **Amazon Translate**   | Machine translation                             |
| Speech            | **Amazon Polly**       | Convert text to speech (TTS)                    |
| Speech            | **Amazon Transcribe**  | Convert speech to text (STT)                    |

AWS also provides AI services for:
- Chatbots
- Forecasting
- Search
- Recommendations

### 1.2 - Amazon SageMaker and Amazon Bedrock

Two important AWS services for broader machine learning and generative AI use cases are:

#### Amazon SageMaker

**Amazon SageMaker** provides tools for building, training, and deploying machine learning models.

Unlike pre-trained AI services such as Rekognition or Comprehend, SageMaker is used when more control over the **ML development lifecycle** is required.

#### Amazon Bedrock

**Amazon Bedrock** is an AWS service focused on building **generative AI applications using foundation models (FMs)**

For the exam, distinguish the general roles:
- **Pre-trained AWS AI services** → ready-made AI capabilities for specific tasks
- **Amazon SageMaker** → build, train, and deploy machine learning models
- **Amazon Bedrock** → build generative AI applications using foundation models

### 1.3 - Exam Focus

Remember the mapping between common AI tasks and AWS services:
- **Image/video analysis → Amazon Rekognition**
- **Document data extraction → Amazon Textract**
- **Text analysis → Amazon Comprehend**
- **Language translation → Amazon Translate**
- **Text-to-speech → Amazon Polly**
- **Speech-to-text → Amazon Transcribe**
- **Custom ML Lifecycle → Amazon SageMaker**
- **Generative AI / foundation models → Amazon Bedrock**

The key distinction is whether the application needs a **ready-to-use pre-trained AI capability**, a **custom machine learning workflow**, or a **foundation-model-based generative AI solution**.

## 2 - Vision: Amazon Rekognition

### 2.1 - Amazon Rekognition Overview

**Amazon Rekognition** is a fully managed AWS AI service that uses machine learning to **analyze images and videos**

It can identify and analyze:
- Faces
- Objects
- Scenes
- Text
- Brands
- Activities
- Inappropriate or unsafe content

### 2.2 - Facial Analysis and Recognition

Amazon Rekognition can perform several types of facial analysis.

#### Face Detection and Tracking

Rekognition can:
- Detect faces in images and videos
- Recognize and compare faces
- Track people across video frames

Example use cases include:
- Identifying authorized individuals
- Tracking people appearing in video footage
- Searching for matching faces

#### Facial Attributes and Emotions

Rekognition can analyze facial characteristics such as:
- Estimated age range
- Gender presentation
- Facial expressions

It can also detect apparent emotions such as:
- Happiness
- Sadness
- Anger

> **Exam point:** Amazon Rekognition is the AWS service associated with **image/video analysis and facial analysis**

### 2.3 - Object, Scene, and Activity Detection

Amazon Rekognition can identify different elements within images and videos, including:
- **Objects** - e.g. vehicles, animals, furniture
- **Scenes** - e.g. beaches, forests
- **Text** appearing inside images
- **Brands and logos**
- **Activities** - e.g. running or swimming

This allows applications to automatically understand can categorize visual content

### 2.4 - Content Moderation

Amazon Rekognition can detect potentially **inappropriate or unsafe content**

This can be used for:
- Content filtering
- Moderating user-uploaded images or videos
- Detecting categories of unwanted content

#### Custom Moderation Adapter

A **Custom Moderation Adapter** allows the standard moderation capability to be customized for an organization's specific requirements.

General process:
1. Provide a **labeled dataset** representing acceptable or inappropriate content
2. Train the adapter using the labeled examples
3. The model learns patterns associated with the provided categories
4. Use the trained adapter to classify new images according to the organization's moderation requirements

> **Exam distinction**: Use a **Custom Moderation Adapter** when the requirement is specifically to **customize content moderation**

### 2.5 - -Amazon Rekognition Custom Labels

**Amazon Rekognition Custom Labels** allows you to create customized image-analysis models for objects or concepts specific to your use case.

Example:

An organization wants Rekognition to recognize particular product brands that are not adequately handled by the standard model.

General workflow:
- Prepare and label training images
- Store the image dataset in **Amazon S3**
- Use the labeled dataset to train a Custom Labels model
- The trained model analyzes new images and detects the custom objects or concepts

#### Custom Labels vs Standard Rekognition
- **Standard Rekognition** → detects commonly supported faces, objects, scenes, activities, text, and other visual features
- **Rekognition Custom Labels** → trains a model to detect **organization-specific obects or concepts**
- **Custom Moderation Adapter** → customizes **inappropriate-content moderation** for specific moderation requirements

### 2.6 - Exam Focus

Know which Rekognition capability matches the requirement:
- **Analyze images/videos → Amazon Rekognition**
- **Detect or compare faces → Amazon Rekognition**
- **Track people in video → Amazon Rekognition**
- **Analyze facial attributes/emotions → Amazon Rekognition**
- **Detect objects, scenes, text, brands, or activities → Amazon Rekognition**
- **Detect inappropriate content → Rekognition Content Moderation**
- **Customize moderation criteria → Custom Moderation Adapter**
- **Detect custom objects/concepts using your own labeled images → Rekognition Custom Labels**

## 3 - Vision: Amazon Textract

### 3.1 - Amazon Textract Overview

**Amazon Textract** is an AWS AI service that automatically **extracts text and structured data from documents and images**

Think:

> **Textract = Text Extraction**

It reduces the need for manual data entry when processing scanned documents, forms, receipts, and other paperwork.

### 3.2 - What Amazon Textract Can Extract

Amazon Textract can extract information from:
- Scanned documents
- Images
- Forms
- Tables
- Grids

It can identify useful details such as:
- Names
- Dates
- Addresses
- Other structured information contained in documents

Example use cases include:
- Extracting data from receipts
- Processing forms automatically
- Extracting information from medical or prescription documents
- Processing large volumes of business paperwork

> **Exam point:** Use **Amazon Textract** when the requirement involves extracting **text or structured document data** from scanned documents or images

### 3.3 - Synchronous Processing

Amazon Textract supports **synchronous, real-time analysis**

This is best suited for:
- Processing a **single document**
- Cases requiring **immediate results**
- Relatively short documents

Example:
- A user scans a receipt and the application immediately extracts its text and information

#### Key Idea

**Synchronous processing = immediate response for individual documents**

### 3.4 - Asynchronous Processing

Amazon Textract also supports **asynchronous analysis**.

This is suitable for:
- Long-form documents
- Large documents
- High-volume document processing
- Batch-style workloads where immediate results are not required

Example use cases:
- Legal firms processing large numbers of documents
- Healthcare organizations processing hundreds or thousands of records

#### Key Idea

**Asynchronous processing = better suited for large-scale or long-running document analysis.**

### 3.5 - Exam Focus

Remember these mappings:
- **Extract text from scanned documents/images → Amazon Textract**
- **Extract data from forms → Amazon Textract**
- **Extract tables and structured document information → Amazon Textract**
- **Need immediate processing of a single document → Synchronous Textract analysis**
- **Need to process long documents or large volumes → Asynchronous Textract analysis**

Also distinguish Textract from other AWS AI services:
- **Amazon Rekognition** → analyzes general image and video content
- **Amazon Textract** → specifically extracts **text and structured information from documents**

## 4 - Language: Amazon Comprehend

### 4.1 - Amazon Comprehend Overview

**Amazon Comprehend** is a fully managed **Natural Language Processing (NLP)** service that uses machine learning to **analyze and understand text**.

It can process text from:
- Amazon Textract
- Documents
- Customer messages
- Reviews
- Other textual data sources

> **Exam point:** Think **Amazon Comprehend = understand and analyze text**.

### 4.2 - Built-in Text Analysis Capabilities

Amazon Comprehend provides several built-in NLP capabilities.

#### Sentiment Analysis

Determines whether text expresses:
- Positive snetiment
- Negative sentiment
- Neutral sentiment

Useful for analyzing:
- Customer reviews
- Feedback
- Support messages

#### Entity Recognition

Identifies entities in text, such as:
- People
- Places
- Organizations
- Other named entities

#### Language Detection

Amazon Comprehend can automatically determine the **language** used in a piece of text.

#### Text Classification

Comprehend can classify text into categories.

Examples include:
- Spam detection
- Categorizing documents or messages

### 4.3 - Tokenization and Parts-of-Speech Tagging

Amazon Comprehend uses NLP techniques to understand the structure of text.

#### Tokenization

**Tokenization** breaks text into smaller units called **tokens**, such as individual words or phrases.

Example:

`I love snorkeling`
becomes
- `I`
- `love`
- `snorkeling`

#### Parts-of-Speech Tagging

**Parts-of-Speech (POS) tagging** identifies the grammatical role of each word.

Example:
- `I` → Pronoun
- `love` → Verb
- `snorkeling` → Noun

### 4.4 - Custom Classification

**Custom Classification** allows Amazon Comprehend to classify text according to categories specific to your organization.

General workflow:
1. Prepare a **labeled training dataset**
2. Provide example documents for each category
3. Train a custom classifier
4. Use the trained classifier to categorize new documents

Example categories:
- Billing issues
- Support issues
- Product issues

> **Exam distinction:** Use **Custom Classification** when predefined Comprehend categories do not meet the business requirement

### 4.5 - Custom Entity Recognition

Amazon Comprehend can also be trained to identify **domain-specific entities** beyond its built-in entity types.

Example for legal documents:
- Effective date
- Party A
- Party B
- Legal terms

This requires a labeled training dataset containing examples of the custom entities.

#### Built-in vs Custom Entities
- **Built-in entity recognition** → common entities such as people, places, and organizations
- **Custom entity recognition** → business- or domain-specific entities

### 4.6 - Real-Time and Asynchronous Processing

Amazon Comprehend supports two processing modes.

#### Real-Time Analysis

Best suited for:
- A single document
- Applications requiring an immediate response

#### Asynchronous Analysis

Best suited for:
- Large documents
- Multiple documents
- High-volume text-processing workloads

> **Exam point:** Similar to Textract, choose **real-time processing** for immediate analysis and **asynchronous processing** for larger-scale workloads

### 4.7 - Amazon Comprehend Medical

**Amazon Comprehend Medical** is specialized for analyzing **unstructured healthcare and clinical text**

Examples include:
- Physician notes
- Discharge summaries
- Test results

It can extract and identify medical information from clinical documents

#### Protected Health Information

Amazon Comprehend Medical can identify **Protected Health Information (PHI)**

The **Detect PHI API** can be used to detect sensitive healthcare information within clinical text.

> **Exam Distinction**:
> **Amazon Comprehend** → general-purpose NLP
> **Amazon Comprehend Medical** → NLP for healthcare and clinical text

### 4.8 - Exam Focus

Remember these mappings:
- **Analyze and understand text → Amazon Comprehend**
- **Sentiment analysis → Amazon Comprehend**
- **Detect people, places, organizations → Entity Recognition**
- **Detect text language → Amazon Comprehend**
- **Classify text into custom categories → Custom Classification**
- **Detect business-specific entities → Custom Entity Recognition**
- **Immediate single-document analysis → Real-time processing**
- **Large-scale/multiple document analysis → Asynchronous processing**
- **Analyze clinical or healthcare text → Amazon Comprehend Medical**
- **Detect protected health information → Comprehend Medical Detect PHI API**

Also remember the common workflow:

**Amazon Textract extracts text → Amazon Comprehend analyzes and understands that text**

## 5 - Language: Amazon Translate

### 5.1 - Amazon Translate Overview

**Amazon Translate** is a fully managed neural machine translation service that automatically **translates text between languages**.

It aims to preserve:
- Meaning
- Tone
- Fluency
- Context and linguistic nuances

> **Exam point:** Think **Amazon Translate = automatic language translation**

Amazon Translate can also support **application localization**, where content is adapted for users in different languages and regions.

### 5.2 - Amazon Translate with Amazon Comprehend

Amazon Translate can be combined with other AWS AI services.

A common workflow is:
1. Use **Amazon Translate** to translate text into a supported language
2. Use **Amazon Comprehend** to analyze the translated text

Example:

For customer reviews written in different languages:

**Customer review → Amazon Translate → Amazon Comprehend → Sentiment analysis**

This can determine whether reviews are:
- Positive
- Negative
- Neutral

### 5.3 - Real-Time and Asynchronous Translation

Amazon Translate supports both **real-time** and **asynchronous** processing

#### Real-Time Translation

Best suited for:
- Immediate translation
- Individual text inputs or documents
- Interactive applications

#### Asynchronous Translation

Best suited for:
- Large collections of documents
- Batch translation workloads
- Cases where an immediate response is not required

Asynchronous translation can process document collections of up to **5 GB**.

### 5.4 - Translation Customization

Amazon Translate provides additional options to control how translations are produced.

#### Custom Terminology

**Custom Terminology** allows specific words or phrases to use predefined tranlsations.

This:
- Overrides the default translation for selected terms
- Does **not** modify or retrain the underlying translation model.

Useful for:
- Product names
- Brand-specific terminology
- Industry terminology
- Organization-specific vocabulary

> **Exam distinction:** Use **Custom Terminology** when specific terms must always be translated in a particular way without retraining the model.

#### Other Translation Settings

Amazon Translate can also support options such as:
- **Brevity** - produces shorter translations when supported
- **Formality** - controls the level of formality in supported languages
- **Profanity masking** - masks profane words in translated output

### 5.5 - Translation Limitations

Machine translation may not always correctly handle:
- Gender-specific language (like Arabic)
- Cultural or linguistic nuances
- Punctuation and formatting conventions
- Context-dependent meanings

Therefore, translated output may still require validation for applications where linguistic accuracy is important.

### 5.6 - Exam Focus

Remember these mappings:
- **Translate text between languages → Amazon Translate**
- **Localize application content → Amazon Translate**
- **Immediate translation → Real-time translation**
- **Large-scale document translation → Asynchronous translation**
- **Force specific translations for selected terms → Custom Terminology**
- **Analyze sentiment after translation → Amazon Translate + Amazon Comprehend**

Key service distinction:
- **Amazon Translate** → translates text between languages
- **Amazon Comprehend** → analyzes and understands the meaning of text

## 6 - Speech: Amazon Polly

### 6.1 - Amazon Polly Overview

**Amazon Polly** is a fully managed AWS AI service that uses deep learning to convert **text into natural-sounding speech**

Common use cases include:
- Audiobooks
- Public announcements
- Voice-enabled applications
- Accessibility features
- Automated narration

> **Exam point**: Think **Amazon Polly = Text-to-Speech (TTS)**

### 6.2 - Real-Time and Batch Speech Synthesis

Amazon Polly supports different processing modes.

#### Real-Time Processing

Used when speech needs to be generated **immediately** from text

Suitable for:
- Interactive applications
- Dynamic voice responses
- On-demand speech generation

#### Batch Processing

Used to process **large amounts of text in bulk**

Suitable for:
- Audiobooks
- Large collections of documents
- Pre-generated audio content

### 6.3 - Voice and Language Customization

Amazon Polly allows you to configure characteristics of the generated speech, including:
- **Language**
- **Voice**
- Different speech-generation engines and voice types

Available voice engines can include:
- Standard
- Neural
- Long-form
- Generative

> **Exam point:** Amazon Polly provides multiple voice options to produce speech appropriate for different applications

### 6.4 - Speech Synthesis Markup Language (SSML)

**Speech Synthesis Markup Language (SSML)** provides greater control over how **Amazon Polly speaks text**

SSML can be used to control:
- Pronunciation
- Pitch
- Speaking rate
- Volume
- Pauses
- Emphasis

For example, SSML can instruct Polly to:
- Pause between sentences
- Emphasize particular words
- Change how quickly something is spoken

You do not need to memorize individual SSML tags for the exam.

> **Exam point**: Remember that **SSML controls how synthesized speech is pronounced and delivered**

### 6.5 - Pronunciation Lexicons

**Lexicons** allows developers to customize how Amazon Polly **pronounces specific words or phrases**

#### Lexicons vs SSML
- **SSML** → controls speech characteristics such as pauses, emphasis, rate, pitch, and pronunciation within text
- **Lexicons** → define reusable pronunciation rules for **specific words or phrases**

### 6.6 - Exam Focus

Remember these mappings:
- **Convert text to speech → Amazon Polly**
- **Generate natural-sounding spoken audio → Amazon Polly**
- **Generate speech immediately → Real-time processing**
- **Convert large amounts of text to speech → Batch processing**
- **Control pitch, rate, volume, pauses, and emphasis → SSML**
- **Customize pronunciation of specific terms → Pronunciation Lexicons**

Key service distinction:
- **Amazon Translate** → converts text from one language to another
- **Amazon Polly** → converts text into spoken audio

A common workflow could therefore be:

**Source text → Amazon Translate → translated text → Amazon Polly → spoken translated audio**

## 7 - Speech: Amazon Transcribe

### 7.1 - Amazon Transcribe Overview

**Amazon Transcribe** is a fully managed AWS AI service that converts **speech into text** using **Automatic Speech Recognition (ASR)**.

Common use cases include:
- Closed captions
- Subtitles
- Meeting transcription
- Customer service call transcription
- Interviews and lectures

> **Exam point:** Think **Amazon Transcribe = Speech-to-Text (STT)**

### 7.2 - Real-Time and Batch Transcription

Amazon Transcribe supports two main processing modes.

#### Real-Time Transcription

Processes live audio as it is being captured.

Suitable for:
- Meetings
- Conferences
- Live customer support calls
- Applications using microphone input

#### Batch Transcription

Processes **pre-recorded audio or video files**

Suitable for:
- Recorded lectures
- Interviews
- Large collections of audio/video files
- Bulk transcription workloads

### 7.3 - Automatic Language Identification

Amazon Transcribe can automatically identify the **language being spoken** in audio.

This allows applications to transcribe audio without always having to manually specify the source language.

> **Exam point:** Amazon Transcribe can perform **automatic language identification** before or during transcription.

### 7.4 - Personally Identifiable Information Redaction

Amazon Transcribe can identify and remove or redact **Personally Identifiable Information (PII)** from transcription output.

Examples may include:
- Names
- Phone numbers
- Other personal information

This is useful when handling sensitive conversations such as customer service calls.

### 7.5 - Custom Vocabularies

**Custom Vocabularies** improve transcription accuracy for specific words or phrases that the standard model may have difficulty recognizing.

Useful for:
- Brand names
- Acronyms
- Technical terminology
- Domain-specific terms

Examples:
- Amazon EC2
- C++
- Product or company names

> **Exam point:** Use a **Custom Vocabulary** when you need Transcribe to better recognize a known set of specific terms

### 7.6 - Custom Language Models

**Custom Language Models** improve transcription accuracy by adapting Transcribe to the language patterns of a particular domain or industry.

You provide domain-specific text such as:
- Documents
- Previous transcripts
- Industry-specific content

The model learns terminology and language patterns associated with that domain.

Useful for specialized fields containing large amounts of domain-specific language.

#### Custom Vocabulary vs Custom Language Model
- **Custom Vocabulary** → improves recognition of **specific words and phrases**
- **Custom Language Model** → adapts transcription to the **broader terminology and language patterns of a domain**

> **Exam distinction:** If the requirement mentions a small list of difficult terms, think **Custom Vocabulary**. If it involves adapting transcription to an entire specialized field, think **Custom Language Model**.

### 7.7 - Amazon Transcribe Medical

**Amazon Transcribe Medical** is designed specifically for converting **spoken medical information into text**.

It is optimized for medical terminology such as:
- Medications
- Medical conditions
- Procedures
- Clinical terminology

Suitable for healthcare applications that regularly process spoken medical content.

> **Exam distinction:**
> **Amazon Transcribe** → general-purpose speech-to-text
> **Amazon Transcribe Medical** → speech-to-text optimized for healthcare and medical terminology

### 7.8 - Exam Focus

Remember these mappings:
- **Speech-to-text → Amazon Transcribe**
- **Live speech transcription → Real-time transcription**
- **Pre-recorded audio/video → Batch transcription**
- **Automatically determine spoken language → Automatic Language Identification**
- **Remove sensitive personal information → PII Redaction**
- **Improve recognition of specific terms → Custom Vocabulary**
- **Adapt transcription to specialized industry language → Custom Language Model**
- **Medical speech-to-text → Amazon Transcribe Medical**

Also remember the key comparison:
- **Amazon Polly** → Text → Speech
- **Amazon Transcribe** → Speech → Text

These two services essentially perform **opposite conversions**.

## 8 - Chatbots: Amazon Lex

### 8.1 - Amazon Lex Overview

**Amazon Lex** is a fully managed AWS service for building **conversational interfaces and chatbots** using voice and text.

It uses the same underlying conversational AI technology associated with **Amazon Alexa**.

Amazon Lex can:
- Accept text or voice input
- Convert speech to text
- Understand user requests
- Collect required information
- Trigger backend actions to fulfill requests

> **Exam point:** Think **Amazon Lex** = **conversational chatbots and voice bots**

### 8.2 - Intents

An **intent** represents the **goal or action the user wants to accomplish**.

Example:

A customer says:
`I want to order a coffee.`

The intent could be:
`OrderCoffee`

Other examples:
- Book a hotel
- Check an account balance
- Schedule an appointment
- Order food

> **Exam point:** **Intent = what the user wants to do**

### 8.3 - Slots

**Slots** are variables used to collect the information needed to fulfill an intent.

For a coffee-ordering chatbot, slots might include:
- Coffee size
- Coffee type
- Quantity

Example:
**Intent:** Order coffee
**Slot:** Size = Large

Amazon Lex can ask follow-up questions to obtain missing slot values before fulfilling the request.

> **Exam point:** **Slots = information required to complete an intent**.

### 8.4 - Intent Fulfillment with AWS Lambda

Amazon Lex can integrate with **AWS Lambda** to fulfill an intent.

Typical workflow:
1. User interacts with an Amazon Lex chatbot
2. Lex determines the **intent**
3. Lex collects the required **slots**
4. The slot values are passed to an **AWS Lambda function**
5. Lambda processes the request or interacts with external systems/APIs
6. The requested action is completed

Example:

**Customer → Amazon Lex → Intent + Slots → AWS Lambda → Restaurant system/API**

Lambda can perform actions such as:
- Accessing databases
- Calling external APIs
- Creating orders
- Making reservations
- Retrieving account information

### 8.5 - Integration with Amazon Connect

Amazon Lex can integrate with **Amazon Connect** to build conversational bots for **contact centers and customer service applications**.

This can enable automated voice interactions in call centers.

> **Exam mapping:**
> **Chatbot / conversational interface → Amazon Lex**
> **Contact center → Amazon Connect**
> **Automated contact-center bot → Amazon Lex + Amazon Connect** 

### 8.6 - Integration with Amazon Comprehend

Amazon Lex can be combined with **Amazon Comprehend** for deeper analysis of customer conversations.

#### Sentiment Analysis

Amazon Comprehend can determine whether customer input is:
- Positive
- Negative
- Neutral

This can help identify whether customers are satisfied or frustrated.

#### Entity Recognition

Comprehend can identify important entities such as:
- Names
- Locations
- Organizations
- Product Information

This can provide additional insights from chatbot conversations.

### 8.7 - Exam Focus

Remember these mappings:
- **Build text or voice chatbots → Amazon Lex**
- **User's requested action → Intent**
- **Information needed to perform the action → Slots**
- **Execute backend logic or call APIs → AWS Lambda**
- **Build contact-center bots → Amazon Lex + Amazon Connect**
- **Analyze customer sentiment → Amazon Comprehend**
- **Identify entities in conversations → Amazon Comprehend**

Key distinction:
- **Amazon Lex** → understands conversational input and manages chatbot interactions.
- **AWS Lambda** → performs the backend action needed to fulfill the intent.
- **Amazon Comprehend** → analyzes text for insights such as sentiment and entities.

## 9 - Forecasting: Amazon Forecast

### 9.1 - Amazon Forecast Overview

**Amazon Forecast** is a fully managed machine learning services that uses **historical time-series data to predict future outcomes**.

Common forecasting use cases include:
- Future sales
- Product demand
- Inventory requirements
- Business trends

> **Exam point:** Think **Amazon Forecast = predict future values from historical time-series data**.

### 9.2 - Training Data

Amazon Forecast requires historical data to train a forecasting model.

Typical training data can include:
- Historical sales
- Product demand
- Market trends
- Market share
- Other time-series data

The dataset can be stored in **Amazon S3** and used to train the forecasting model.

Typical workflow:
1. Collect historical time-series data
2. Store the dataset in Amazon S3.
3. Use the data to train an Amazon Forecast model
4. Generate predictions for future periods
5. Use the forecasts to support business decisions.

### 9.3 - Forecast Uncertainty

Forecasts are predictions rather than guaranteed values.

Amazon Forecast can provide a **range of possible future values**, representing the uncertainty or variability associated with the prediction.

This helps businesses understand not only the expected outcome, but also the possible range around that forecast.

### 9.4 - Exam Focus

Remember these mappings:
- **Predict future demand → Amazon Forecast**
- **Predict future sales → Amazon Forecast**
- **Forecast inventory requirements → Amazon Forecast**
- **Use historical time-series data to predict future values → Amazon Forecast**
- **Store training datasets → Amazon S3**
- **Forecast ranges → represent uncertainty in future predictions**

Key distinction:
- **Amazon Forecast** → predicts **future numerical values or trends** from historical data.
- It is not used for general text, image, or speech analysis.

## 10 - Personal Assistants: Amazon Kendra

### 10.1 - Amazon Kendra Overview

**Amazon Kendra** is an intelligent enterprise search service that helps users find **accurate and relevant information across an organization's data sources**.

It is similar to having a search engine designed specifically for internal company information.

> **Exam point:** Think **Amazon Kendra = intelligent enterprise search across company data**

### 10.2 - Natural Language Search

Amazon Kendra uses **Natural Language Processing (NLP)** to understand queries written in normal conversational language.

Users can ask questions naturally, such as:
`When is the annual company meeting?`

Kendra attempts to understand the **meaning and context** of the question rather than relying only on exact keyword matches.

This enables it to return more relevant answers from organizational documents.

### 10.3 - Data Sources

Amazon Kendra can search information across multiple repositories and enterprise data sources.

Example include:
- **Amazon S3**
- **Amazon RDS**
- **Microsoft SharePoint**
- **Google Drive**
- Other supported document and data repositories

Kendra can crawl or connect to these sources and index their content for search.

### 10.4 - Enterprise Search Workflow

A typical Amazon Kendra workflow is:
1. Connect Kendra to organizational data sources
2. Kendra crawls and indexes the available information
3. A user asks a question using natural language
4. Kendra analyzes the **intent and context** of the query
5. It searches the indexed content
6. It returns the most relevant answer or information

Example:

**Question:** `When is the annual company meeting?`

Kendra searches relevant internal documents and returns the information that best answers the question.

### 10.5 - Exam Focus

Remember these mappings:
- **Enterprise search across company data → Amazon Kendra**
- **Search internal documents using natural-language questions → Amazon Kendra**
- **Understand query context instead of only exact keywords → Amazon Kendra**
- **Search across sources such as S3, RDS, SharePoint, and Google Drive → Amazon Kendra**

Key distinction:
- **Amazon Kendra** → searches and retrieves relevant information from **enterprise data sources**
- **Amazon Comprehend** → analyzes text to extract insights such as sentiment and entities.
- **Amazon Lex** → builds conversational chatbots that interact with users.

## 11 - Recommendations: Amazon Personalize

### 11.1 - Amazon Personalize Overview

**Amazon Personalize** is a fully managed machine learning service used to create **real-time personalized recommendations**.

It can personalize experiences based on user behavior such as:
- Clicks
- Purchases
- Ratings
- Browsing activity
- Previous interactions

> **Exam point:** Think **Amazon Personalize = personalized recommendations based on user behavior**.

### 11.2 - Recipes

Amazon Personalize uses **recipes**, which are predefined algorithms designed for different recommendation use cases.

Each recipe is optimized for a specific type of personalization task.

### 11.3 - USER_PERSONALIZATION

**USER_PERSONALIZATION** recommends items to a user based on that user's previous behavior.

It can use signals such as:
- Clicks
- Purchases
- Ratings
- Viewed items

Example:

If a user frequently browses certain books, Amazon Personalize can recommend other books that the user is likely to enjoy

> **Exam mapping: Recommend items specifically for an individual user → USER_PERSONALIZATION**

### 11.4 - PERSONALIZED_RANKING

**PERSONALIZED_RANKING** reorders a given list of items so that the items most relevant to a particular user appear first.

Example:

A search returns multiple products, but Amazon Personalize ranks them differently for each user based on their preferences.

> **Exam mapping: Re-rank existing items for a specific user → PERSONALIZED_RANKING**

### 11.5 - PERSONALIZED_ACTIONS

**PERSONALIZED_ACTIONS** recommends the **next best action** for a user based on previous interactions.

Examples of actions include:
- Sign up for a price alert.
- Subscribe to a service
- Complete a purchase
- Perform another relevant next step

> **Exam mapping: Recommend what the user should do next → PERSONALIZED_ACTIONS**

### 11.6 - POPULAR_ITEMS

**POPULAR_ITEMS** recommends items based on **overall user behavior** rather than the preferences of one individual

This is useful for:
- Trending products
- Popular content
- Most-viewed items

> **Exam mapping: Recommend trending or popular items across users → POPULAR_ITEMS**

### 11.7 - RELATED_ITEMS

**RELATED_ITEMS** recommends items that are associated with another item.

These relationships may come from items that users:
- View together
- Purchase together
- Interact with together

Example:

A user viewing a soccer net may also be recommended a soccer ball.

> **Exam mapping: "Customer who viewed/bought this also..." → RELATED_ITEMS**

### 11.8 - USER_SEGMENTATION

**USER_SEGMENTATION** groups users into segments based on their **affinity for particular items or categories**

Example:

A fitness platform might segment users into:
- Casual gym-goers
- Fitness enthusiasts

These segments can then be used for more targeted recommendations or campaigns.

> **Exam mapping: Group users according to interests or affinities → USER_SEGMENTATION**

### 11.9 - Exam Focus

Remember the recipe mappings:

- **Recommend items for one user → USER_PERSONALIZATION**
- **Reorder a list based on user preference → PERSONALIZED_RANKING**
- **Recommend the next best user action → PERSONALIZED_ACTIONS**
- **Recommend trending items → POPULAR_ITEMS**
- **Recommend similar or complementary items → RELATED_ITEMS**
- **Group users based on affinity → USER_SEGMENTATION**

Key distinction:
- **Amazon Personalize** → generates personalized recommendations
- **Amazon Forecast** → predicts future numerical values or demand
- **Amazon Kendra** → searches enterprise information

## 12 - Exam Tips

### 12.1 - AWS AI/ML Services Summary

Key AWS AI/ML services to recognize for the exam:

| **Service**            | **Primary Purpose**                                             |
| ---------------------- | --------------------------------------------------------------- |
| **Amazon Rekognition** | Analyze images and videos                                       |
| **Amazon Textract**    | Extract text and structured data from documents                 |
| **Amazon Comprehend**  | Analyze and understand text using NLP                           |
| **Amazon Translate**   | Translate text between languages                                |
| **Amazon Polly**       | Convert **text → speech**                                       |
| **Amazon Transcribe**  | Convert **speech → text**                                       |
| **Amazon Lex**         | Build conversational chatbots and voice assistants              |
| **Amazon Forecast**    | Predict future values using historical time-series data         |
| **Amazon Kendra**      | Intelligent enterprise search across documents and data sources |
| **Amazon Personalize** | Generate personalized recommendations                           |

### 12.2 - Key Customization Features

Remember these important service-specific features:
- **Rekognition Custom Labels** → detect custom objects/concepts
- **Rekognition Custom Moderation Adapter** → customize content moderation
- **Transcribe Custom Vocabulary** → improve recognition of specific terms
- **Transcribe Custom Language Model** → improve transcription for a specialized domain

### 12.3 - Exam Quick Recall
- **Image/Video understanding → Rekognition**
- **Document extraction → Textract**
- **Text understanding/sentiment → Comprehend**
- **Translation → Translate**
- **Text-to-speech → Polly**
- **Speech-to-text → Transcribe**
- **Chatbot → Lex**
- **Future prediction → Forecast**
- **Enterprise search → Kendra**
- **Recommendations → Personalize**