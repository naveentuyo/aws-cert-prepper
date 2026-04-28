# AWS Machine Learning & AI Services — Quick Quiz
#
# Total Questions: 20
# Based on: AWS ML and AI Services.md

## Q1. A company wants to analyze customer reviews to determine whether feedback is positive, negative, or neutral. Which AWS service should they use?
- [ ] A) Amazon Rekognition
- [ ] B) Amazon Translate
- [x] C) Amazon Comprehend
- [ ] D) Amazon Textract
### Explanation
Amazon Comprehend is a natural language processing (NLP) service that can understand sentiment (positive, negative, mixed, or neutral) from text. Analyzing customer feedback for sentiment is one of its primary use cases. Rekognition (A) analyzes images and video, not text. Translate (B) converts text between languages. Textract (D) extracts text from scanned documents.
---

## Q2. A company needs to build a chatbot that understands both voice and text input from users. Which AWS service provides the conversational engine for this?
- [x] A) Amazon Lex
- [ ] B) Amazon Polly
- [ ] C) Amazon Transcribe
- [ ] D) Amazon Comprehend
### Explanation
Amazon Lex is the service behind Alexa's conversational engine. It provides automatic speech recognition (ASR) for converting speech to text and natural language understanding (NLU) to recognize user intent, making it the right choice for building chatbots. Polly (B) converts text to speech (output, not input). Transcribe (C) converts speech to text but doesn't understand intent or manage dialogue. Comprehend (D) extracts insights from text but doesn't handle conversation flow.
---

## Q3. A company wants to add lifelike speech output to their mobile application to improve accessibility for visually impaired users. Which AWS service should they use?
- [ ] A) Amazon Lex
- [ ] B) Amazon Transcribe
- [x] C) Amazon Polly
- [ ] D) Amazon Comprehend
### Explanation
Amazon Polly is a text-to-speech service that turns text into lifelike speech, supporting dozens of languages and neural text-to-speech (NTTS) voices. Building accessibility features for visually impaired users is a core use case. Lex (A) builds chatbots. Transcribe (B) converts speech to text (the opposite direction). Comprehend (D) analyzes text for insights.
---

## Q4. A healthcare company needs to extract structured data such as key-value pairs and tables from scanned patient intake forms. Which AWS service is BEST suited?
- [ ] A) Amazon Comprehend
- [ ] B) Amazon Rekognition
- [x] C) Amazon Textract
- [ ] D) Amazon Kendra
### Explanation
Amazon Textract goes beyond simple OCR — it extracts text, handwriting, tables, and structured data (key-value pairs) from scanned documents using machine learning. It understands document layout and relationships, making it ideal for forms like patient intake documents, invoices, and tax forms. Comprehend (A) analyzes text meaning, not document structure. Rekognition (B) analyzes images for objects and faces, not document data extraction. Kendra (D) is an enterprise search service.
---

## Q5. A company wants to replace their traditional keyword-based internal search with a system that understands natural language questions and returns specific answers from company documents stored in S3. Which service should they use?
- [ ] A) Amazon Comprehend
- [x] B) Amazon Kendra
- [ ] C) Amazon Textract
- [ ] D) Amazon Q Business
### Explanation
Amazon Kendra is an intelligent enterprise search service powered by machine learning that understands natural language queries and returns specific answers from data sources like S3, databases, and SharePoint. Unlike keyword-based search, Kendra understands context and intent. Comprehend (A) extracts insights from text but isn't a search engine. Textract (C) extracts data from scanned documents. Amazon Q Business (D) is a generative AI assistant that can answer questions, but Kendra is specifically designed as an enterprise search replacement.
---

## Q6. A data science team needs a fully managed platform to build, train, and deploy custom machine learning models using TensorFlow. Which AWS service should they use?
- [ ] A) Amazon Rekognition
- [ ] B) Amazon Comprehend
- [ ] C) Amazon Kendra
- [x] D) Amazon SageMaker AI
### Explanation
Amazon SageMaker AI is a fully managed platform covering the entire ML workflow — data labeling, model training, tuning, deployment, and monitoring. It supports popular frameworks like TensorFlow and PyTorch, and provides tools like SageMaker Studio (an ML IDE) and SageMaker JumpStart (pre-trained models). Rekognition (A) and Comprehend (B) provide pre-built AI capabilities, not custom model building. Kendra (C) is an enterprise search service.
---

## Q7. A media company needs to automatically detect inappropriate content in user-uploaded images and videos. Which AWS service should they use?
- [x] A) Amazon Rekognition
- [ ] B) Amazon Comprehend
- [ ] C) Amazon Textract
- [ ] D) Amazon Polly
### Explanation
Amazon Rekognition provides image and video analysis powered by deep learning, including content moderation to detect inappropriate or unsafe content. This is one of its primary use cases for media companies. Comprehend (B) analyzes text, not images. Textract (C) extracts data from documents. Polly (D) converts text to speech.
---

## Q8. A company needs to transcribe recorded customer service calls to text, including identifying which speaker said what. Which AWS service supports this?
- [ ] A) Amazon Polly
- [ ] B) Amazon Lex
- [x] C) Amazon Transcribe
- [ ] D) Amazon Translate
### Explanation
Amazon Transcribe is an automatic speech recognition (ASR) service that converts audio to text. It supports speaker identification (diarization), which labels who said what in a conversation — exactly what's needed for customer service call transcription. Polly (A) does text-to-speech (the opposite). Lex (B) builds chatbots. Translate (D) translates text between languages.
---

## Q9. A global e-commerce company needs to translate product descriptions into dozens of languages while ensuring brand names remain untranslated. Which AWS service supports this?
- [ ] A) Amazon Comprehend
- [ ] B) Amazon Polly
- [ ] C) Amazon Lex
- [x] D) Amazon Translate
### Explanation
Amazon Translate is a neural machine translation service supporting dozens of languages. Critically, it allows custom terminology to ensure brand names, product names, and domain-specific terms are translated consistently (or left untranslated). Comprehend (A) analyzes text sentiment and entities. Polly (B) converts text to speech. Lex (C) builds chatbots.
---

## Q10. A developer wants an AI assistant that can help them write, debug, and transform code while also troubleshooting AWS resources. Which service provides this?
- [x] A) Amazon Q Developer
- [ ] B) Amazon SageMaker AI
- [ ] C) Amazon Comprehend
- [ ] D) Amazon Kendra
### Explanation
Amazon Q Developer is a generative AI-powered assistant specifically designed to help developers write, debug, test, and transform code. It can also help understand and troubleshoot AWS resources and is trained on AWS best practices. SageMaker (B) is for building custom ML models. Comprehend (C) is NLP for text analysis. Kendra (D) is enterprise search.
---

## Q11. A company wants to extract medical information such as diagnoses, medications, and dosages from clinical notes. Which AWS service is specifically designed for this?
- [ ] A) Amazon Textract
- [x] B) Amazon Comprehend Medical
- [ ] C) Amazon Kendra
- [ ] D) Amazon Transcribe
### Explanation
Amazon Comprehend Medical is a specialized version of Amazon Comprehend designed to extract medical information from clinical text, including diagnoses, medications, dosages, and medical conditions. Textract (A) extracts structured data from scanned documents but doesn't understand medical terminology contextually. Kendra (C) is enterprise search. Transcribe (D) converts speech to text.
---

## Q12. A company wants to verify the identity of users by comparing a selfie photo against an ID document photo. Which AWS service provides facial comparison capabilities?
- [ ] A) Amazon Textract
- [ ] B) Amazon Comprehend
- [x] C) Amazon Rekognition
- [ ] D) Amazon SageMaker AI
### Explanation
Amazon Rekognition offers facial analysis and facial search capabilities, including comparing faces across images for identity verification. This is a common use case for onboarding and KYC (Know Your Customer) workflows. Textract (A) extracts text from documents. Comprehend (B) analyzes text. SageMaker (D) builds custom models but Rekognition provides this capability out of the box.
---

## Q13. A company wants to connect their generative AI assistant to internal company data sources like SharePoint and Confluence to answer employee questions. Which AWS service is designed for this?
- [ ] A) Amazon Kendra
- [ ] B) Amazon Comprehend
- [x] C) Amazon Q Business
- [ ] D) Amazon SageMaker AI
### Explanation
Amazon Q Business is a generative AI-powered assistant that connects to your company's data and applications (SharePoint, Confluence, etc.) to answer questions, provide summaries, and generate content based on your organization's knowledge. Kendra (A) provides enterprise search but doesn't generate content or summaries. Comprehend (B) analyzes text. SageMaker (D) builds custom ML models.
---

## Q14. A company needs to generate subtitles for video content in the original spoken language. Which AWS service should they use first?
- [ ] A) Amazon Translate
- [x] B) Amazon Transcribe
- [ ] C) Amazon Polly
- [ ] D) Amazon Comprehend
### Explanation
Amazon Transcribe converts audio to text, which is the first step in generating subtitles — you need the spoken words as text before anything else. It supports real-time transcription and automatic language identification. Translate (A) would be a second step if you need subtitles in other languages. Polly (C) converts text to speech. Comprehend (D) analyzes text meaning.
---

## Q15. A company wants to automate invoice processing by extracting vendor names, amounts, and line items from scanned PDF invoices. Which AWS service is BEST suited?
- [x] A) Amazon Textract
- [ ] B) Amazon Comprehend
- [ ] C) Amazon Rekognition
- [ ] D) Amazon Kendra
### Explanation
Amazon Textract extracts text, tables, and structured data (key-value pairs) from scanned documents like invoices, understanding layout and relationships without manual templates. It can pull vendor names, amounts, and line items automatically. Comprehend (B) analyzes text meaning but doesn't extract structured document data. Rekognition (C) analyzes images for objects and faces. Kendra (D) is enterprise search.
---

## Q16. Which AWS service would you use to automatically create ML models from your data without writing code, using a feature called Autopilot?
- [ ] A) Amazon Rekognition
- [ ] B) Amazon Kendra
- [x] C) Amazon SageMaker AI
- [ ] D) Amazon Comprehend
### Explanation
Amazon SageMaker AI includes SageMaker Autopilot, which automatically creates ML models from your data without requiring you to write ML code. It handles data exploration, feature engineering, algorithm selection, and hyperparameter tuning. Rekognition (A) provides pre-built image analysis. Kendra (B) is enterprise search. Comprehend (D) provides pre-built NLP.
---

## Q17. A company needs to detect whether workers on a construction site are wearing required personal protective equipment (PPE). Which AWS service can do this?
- [ ] A) Amazon Comprehend
- [ ] B) Amazon Textract
- [x] C) Amazon Rekognition
- [ ] D) Amazon Polly
### Explanation
Amazon Rekognition can detect PPE (hard hats, face covers, hand covers) in images and video, making it ideal for workplace safety monitoring on construction sites. Comprehend (A) analyzes text. Textract (B) extracts data from documents. Polly (D) converts text to speech.
---

## Q18. A company wants to build a voice-controlled ordering system for a restaurant. Which combination of AWS services would they need for understanding voice commands AND responding with speech?
- [ ] A) Amazon Transcribe and Amazon Translate
- [x] B) Amazon Lex and Amazon Polly
- [ ] C) Amazon Comprehend and Amazon Textract
- [ ] D) Amazon Kendra and Amazon Rekognition
### Explanation
Amazon Lex provides the conversational engine with ASR (speech-to-text) and NLU (understanding intent) for processing voice commands, while Amazon Polly provides text-to-speech for responding with lifelike voice output. Together they create a complete voice-controlled interface. Transcribe + Translate (A) handles transcription and translation, not conversation. Comprehend + Textract (C) analyze text and documents. Kendra + Rekognition (D) handle search and image analysis.
---

## Q19. A news organization wants to automatically identify the language of incoming articles from global correspondents before routing them for translation. Which AWS service can identify the language of text?
- [x] A) Amazon Comprehend
- [ ] B) Amazon Translate
- [ ] C) Amazon Transcribe
- [ ] D) Amazon Lex
### Explanation
Amazon Comprehend can identify the language of text as one of its core NLP capabilities. While Amazon Translate (B) also detects source language during translation, Comprehend is the dedicated NLP service for text analysis tasks like language identification. Transcribe (C) identifies spoken language in audio. Lex (D) builds chatbots.
---

## Q20. A company wants to use pre-trained ML models from a model hub to quickly start a machine learning project without building from scratch. Which SageMaker feature provides this?
- [ ] A) SageMaker Autopilot
- [ ] B) SageMaker Studio
- [x] C) SageMaker JumpStart
- [ ] D) SageMaker Ground Truth
### Explanation
SageMaker JumpStart is a pre-trained model hub that provides access to hundreds of pre-built models, allowing teams to quickly start ML projects without building from scratch. Autopilot (A) automatically creates models from your data. Studio (B) is an IDE for ML development. Ground Truth (D) is a data labeling service.
---
