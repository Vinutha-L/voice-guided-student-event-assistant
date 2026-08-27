# Voice-Guided Student Event Information Assistant

A multimodal Generative AI assistant designed to help students quickly access information about student-relevant events such as hackathons, workshops, technical competitions, seminars, fests and other events.

## Problem Statement

Students often need to search through lengthy event brochures and schedules to find specific information such as event dates, venues, registration details and event categories.

Our project aims to make this process faster and more convenient by allowing users to ask questions using either voice or text.

## Proposed Solution

The system combines Speech-to-Text, Retrieval-Augmented Generation (RAG), Large Language Models and Text-to-Speech.

The user provides a question through voice or text. For voice input, the speech is converted into text. The system then retrieves relevant information from the uploaded event document and generates a concise, context-grounded response. The response can also be converted into speech.

## Key Features

- Voice-based input
- Text-based input
- Document-based question answering
- Semantic retrieval using RAG
- Generative AI-powered responses
- Text-to-Speech output
- Information retrieval from uploaded event documents

## AI Models Used

### 1. Speech-to-Text

**Model:** `whisper-large-v3-turbo`  
**Platform:** Groq

Converts the user's spoken question into text.

### 2. Document & Query Embeddings

**Model:** `all-MiniLM-L6-v2`  
**Platform:** Hugging Face / Sentence Transformers

Converts document chunks and user queries into numerical vector representations for semantic similarity search.

### 3. Language Reasoning Core

**Model:** `qwen/qwen3.6-27b`  
**Platform:** Groq

Uses the retrieved context to generate a concise response grounded in the available event information.

### 4. Text-to-Speech

**Model:** `facebook/mms-tts-eng`  
**Platform:** Hugging Face Inference API

Converts the generated response into speech.

**Fallback:** gTTS

## System Workflow

User Voice/Text Query  
↓  
Speech-to-Text  
↓  
Query Embedding  
↓  
Semantic Retrieval from Event Documents  
↓  
LLM Response Generation  
↓  
Text Response  
↓  
Text-to-Speech  
↓  
Voice Response

## Technologies Used

- Python
- Google Colab
- Groq
- Hugging Face
- Sentence Transformers
- Retrieval-Augmented Generation (RAG)
- Large Language Models
- Speech-to-Text
- Text-to-Speech

## How to Run

1. Open the `.ipynb` notebook in Google Colab.
2. Install the required dependencies.
3. Add your own API credentials through Colab Secrets.
4. Upload an event brochure or document.
5. Run the notebook cells.
6. Ask questions using voice or text.

> **Note:** API keys and authentication credentials are not included in this repository. Users must provide their own credentials.

## Team Members

- Vinutha L
- Greeshma J Gore
- Dhanya B M
