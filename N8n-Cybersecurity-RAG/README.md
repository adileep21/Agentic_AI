# Cybersecurity RAG Chatbot using n8n

## Project Overview

A Retrieval-Augmented Generation (RAG) based cybersecurity chatbot developed using n8n, Groq, Ollama embeddings, and a cybersecurity document knowledge base.

The chatbot combines document-based retrieval with general LLM knowledge to answer cybersecurity questions while maintaining conversational context.

## Objective

To develop an intelligent cybersecurity chatbot that can:

- Retrieve relevant information from cybersecurity PDF documents.
- Answer general cybersecurity questions using an LLM.
- Maintain conversational context using memory.
- Provide an interactive chatbot interface.

## Technologies Used

- n8n
- Groq
- OpenAI GPT-OSS 120B
- Ollama
- nomic-embed-text
- Simple Vector Store
- RAG
- AI Agent
- Chat Trigger

## Knowledge Base

The chatbot was provided with cybersecurity reference documents covering areas such as:

- Cybersecurity fundamentals
- Security controls
- Network security
- Access control
- Authentication
- Malware protection
- Incident handling
- Risk management
- Business continuity
- Supply-chain security

The documents were processed and stored as vector embeddings for retrieval.

## Workflow Architecture

User
↓
n8n Chat Trigger
↓
AI Agent
├── Groq Chat Model
├── Simple Memory
└── Simple Vector Store
↓
Cybersecurity Knowledge Base

## Workflow Components

### 1. Chat Trigger

Receives user questions through the n8n hosted chat interface and initiates the workflow.

### 2. AI Agent

Acts as the central reasoning component and determines how to respond to user questions using the LLM, memory, and knowledge retrieval tool.

### 3. Groq Chat Model

Provides the language model used by the AI Agent to generate responses and perform reasoning.

### 4. Simple Memory

Maintains conversation context so that follow-up questions can be understood in relation to previous messages.

### 5. Simple Vector Store

Stores the embedded cybersecurity document content and retrieves relevant information when required by the AI Agent.

### 6. Ollama Embeddings

The `nomic-embed-text` model converts the cybersecurity documents into vector embeddings for semantic retrieval.

## RAG Process

1. Cybersecurity PDF documents are loaded into n8n.
2. The documents are converted into text chunks.
3. `nomic-embed-text` generates embeddings for the document content.
4. The embeddings are stored in the Simple Vector Store.
5. When a user asks a question, the AI Agent can query the vector store.
6. Relevant document information is retrieved and used to generate the response.
7. When document information is insufficient, the LLM can use its general knowledge and reasoning.

## Conversational Memory

Simple Memory is connected to the AI Agent to retain recent conversation context.

This allows users to ask follow-up questions without repeating the context of the previous question.

## Chatbot Demonstration

The chatbot was tested using natural cybersecurity questions covering:

- General cybersecurity concepts
- Technical security concepts
- Follow-up questions requiring conversational context

## Live Chat

[Open Cybersecurity RAG Chatbot](PASTE_YOUR_N8N_CHAT_URL_HERE)

> Note: The chatbot must be accessible through the published n8n instance for the live link to work.

## Workflow File

The exported n8n workflow is available here:

[Download n8n Workflow](workflow/Cybersecurity_RAG_Chatbot.json)

## Key Features

- Document-based cybersecurity knowledge retrieval
- AI Agent architecture
- General LLM reasoning
- Conversational memory
- Semantic search using embeddings
- Interactive chat interface
- Modular n8n workflow

## Outcome

The project demonstrates the implementation of a cybersecurity-focused RAG chatbot that combines a document knowledge base, semantic retrieval, LLM reasoning, and conversational memory within a single n8n workflow.

