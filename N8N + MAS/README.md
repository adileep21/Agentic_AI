# n8n Multi-Agent Cybersecurity System

A sequential multi-agent cybersecurity system built using **n8n, Groq, Tavily, and Simple Memory**. The system processes cybersecurity queries through three specialized AI agents.

## Architecture

Chat Trigger → Threat Analysis Agent → Risk Analysis Agent → Response & Recommendations Agent → Final Response

## Agents

- **Threat Analysis Agent** — Identifies threats, attack vectors, vulnerabilities, and potential consequences.
- **Risk Analysis Agent** — Evaluates security, business, and operational risks and prioritizes them.
- **Response & Recommendations Agent** — Generates mitigation actions, security controls, incident response actions, and preventive measures.

## Tools & Technologies

- **n8n** — Workflow orchestration
- **Groq** — LLM (`openai/gpt-oss-20b`)
- **Tavily Search** — External cybersecurity research
- **Simple Memory** — Maintains conversation context
- **Chat Trigger** — User-facing chatbot interface

## Key Features

- Sequential multi-agent processing
- Specialized agent roles
- Dynamic handoff between agents
- External research using Tavily
- Conversational memory
- Production chat interface
## Demo

**Production Chat:** [Hosted URL](http://localhost:5678/webhook/7edb5c1b-58f0-4b64-9425-9753c0ca036a/chat)
