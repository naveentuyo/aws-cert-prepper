# AWS Machine Learning & AI Services

## Amazon Comprehend

Amazon Comprehend is a natural language processing (NLP) service that uses machine learning to extract insights and relationships from text. It can identify the language of the text, extract key phrases, places, people, brands, or events, understand sentiment (positive, negative, mixed, or neutral), and organize a collection of text files by topic. Common use cases include analyzing customer feedback, content moderation, and extracting medical information from clinical text (via Comprehend Medical).

## Amazon Kendra

Amazon Kendra is an intelligent enterprise search service powered by machine learning. Unlike traditional keyword-based search, Kendra understands natural language queries and returns specific answers from across your data sources (S3, databases, SharePoint, etc.). Think of it as a smart search engine for your organization's internal documents and knowledge bases. It can understand context and intent, making it far more accurate than simple keyword matching.

## Amazon Lex

Amazon Lex is the service behind Alexa's conversational engine. It lets you build conversational interfaces (chatbots) into any application using voice and text. Lex provides automatic speech recognition (ASR) for converting speech to text and natural language understanding (NLU) to recognize the intent behind the text. You define the conversation flow, and Lex handles the heavy lifting of understanding user input and managing dialogue.

## Amazon Polly

Amazon Polly is a text-to-speech service that turns text into lifelike speech. It supports dozens of languages and a variety of realistic voices, including neural text-to-speech (NTTS) voices that sound very natural. Use cases include adding speech to applications, creating audio content from blog posts or articles, and building accessibility features for visually impaired users.

## Amazon Q

Amazon Q is a generative AI-powered assistant designed for work. It comes in multiple flavors:
- **Amazon Q Developer** — helps developers write, debug, test, and transform code. It can also help understand and troubleshoot AWS resources.
- **Amazon Q Business** — connects to your company's data and applications to answer questions, provide summaries, and generate content based on your organization's knowledge.

Amazon Q is trained on AWS best practices and can assist with architecture decisions, troubleshooting, and cost optimization.

## Amazon Rekognition

Amazon Rekognition provides image and video analysis powered by deep learning. It can identify objects, people, text, scenes, and activities in images and videos. It also offers facial analysis and facial search capabilities. Common use cases include content moderation (detecting inappropriate content), identity verification, detecting PPE in workplace safety scenarios, and analyzing media assets at scale.

## Amazon SageMaker AI

Amazon SageMaker AI is a fully managed platform for building, training, and deploying machine learning models at scale. It covers the entire ML workflow — from data labeling and preparation, to model training and tuning, to deployment and monitoring in production. SageMaker provides built-in algorithms, support for popular ML frameworks (TensorFlow, PyTorch, etc.), and tools like SageMaker Studio (an IDE for ML), SageMaker Autopilot (automated model creation), and SageMaker JumpStart (pre-trained model hub).

## Amazon Textract

Amazon Textract goes beyond simple OCR (optical character recognition). It extracts text, handwriting, tables, and structured data from scanned documents using machine learning. It understands the layout and relationships within a document, so it can pull data from forms (key-value pairs) and tables without manual configuration or templates. Great for automating document processing workflows like invoices, receipts, tax forms, and ID documents.

## Amazon Transcribe

Amazon Transcribe is an automatic speech recognition (ASR) service that converts audio to text. It supports real-time transcription and batch processing, speaker identification (diarization), custom vocabularies for domain-specific terms, and automatic language identification. Use cases include transcribing customer service calls, generating subtitles for video content, and creating searchable archives of audio/video content.

## Amazon Translate

Amazon Translate is a neural machine translation service that delivers fast, high-quality language translation. It supports translation between dozens of languages and can handle real-time and batch translation workloads. It also allows custom terminology to ensure brand names, product names, and domain-specific terms are translated consistently. Common use cases include localizing application content, translating user-generated content, and enabling multilingual communication.
