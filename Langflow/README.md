# CyberFlow- LangFlow Cybersecurity Smart Chatbot

An AI-powered cybersecurity assistant built using LangFlow and Groq. The chatbot can answer questions across cybersecurity domains and maintain conversational context using Message History.

## Tools & Technologies

- LangFlow
- Groq API
- OpenAI Compatible Model
- `openai/gpt-oss-20b`
- Message History

## Workflow

1. **Chat Input**  
   Receives the user's cybersecurity question.

2. **Message History – Retrieve**  
   Retrieves previous conversation context from the current session.

3. **Prompt Template**  
   Provides the cybersecurity assistant instructions and incorporates previous conversation context.

4. **Groq Language Model**  
   Generates the response using `openai/gpt-oss-20b` through the Groq OpenAI-compatible API.

5. **Chat Output**  
   Displays the generated response to the user.

6. **Message History – Store**  
   Stores the conversation response so it can be referenced in subsequent questions.

## Model Configuration

- Provider: OpenAI Compatible
- Base URL: `https://api.groq.com/openai/v1`
- Model: `openai/gpt-oss-20b`

## Key Features

- Broad cybersecurity question answering
- Conversational memory
- Context-aware follow-up questions
- Groq-powered inference
- LangFlow visual workflow
