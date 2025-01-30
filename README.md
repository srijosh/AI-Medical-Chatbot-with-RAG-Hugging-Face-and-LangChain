# AI Medical Chatbot with RAG (Hugging Face & LangChain)

This repository contains a project for an AI Medical Chatbot leveraging Retrieval-Augmented Generation (RAG) with Hugging Face models and LangChain. The chatbot provides intelligent medical responses by retrieving relevant context from a vector database and utilizing an LLM for conversational AI.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Tools and Technologies](#tools-and-technologies)

## Introduction

The AI Medical Chatbot is designed to assist users with medical-related queries by retrieving contextually relevant information from stored documents. It employs Retrieval-Augmented Generation (RAG), combining vector-based search using FAISS and language model inference with Mistral-7B-Instruct from Hugging Face.

## Features

- Retrieval-Augmented Generation (RAG): Enhances response accuracy by retrieving relevant document chunks.

- Hugging Face LLM Integration: Uses mistralai/Mistral-7B-Instruct-v0.3 for generating answers.

- Vector Database with FAISS: Stores and retrieves medical documents efficiently.

- Streamlit Frontend: Provides an interactive chat interface for users.

- Secure API Integration: Manages API keys using .env for Hugging Face endpoints.

## Installation

1. Clone the repository to your local machine:

```
   git clone https://github.com/srijosh/AI-Medical-Chatbot-with-RAG-Hugging-Face-and-LangChain.git
```

2. Navigate to the project directory:

```
   cd AI-Medical-Chatbot-with-RAG-Hugging-Face-and-LangChain
```

3. Install the required dependencies:

```
   pip install -r requirements.txt
```

4. Set up environment variables by creating a .env file (Use .env.sample as a reference for setting up your .env file.)

## Usage

1. Step 1: Create the FAISS Vector Store
   Run the following command to load medical documents, generate embeddings, and store them in FAISS:

```
   python create_memory_for_llm.py
```

2. Step 2: Connect LLM with Memory
   Run the following script to initialize the chatbot with retrieval capabilities:

```
   python connect_memory_with_llm.py
```

3. Step 3: Launch the Chatbot
   Start the Streamlit interface for user interaction:

```
   streamlit run medicalbot.py
```

## Tools and Technologies

- LangChain: Framework for integrating AI models and retrieval mechanisms.

- Hugging Face Transformers: For running LLM inference with Mistral-7B-Instruct.

- FAISS: Vector database for storing and retrieving document embeddings.

- Streamlit: Provides an intuitive UI for chatbot interaction.

- Python dotenv: Manages environment variables securely.
