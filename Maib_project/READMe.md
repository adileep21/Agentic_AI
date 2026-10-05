# ✈️ TravelMate — Multi-Agent AI Trip Planning System

> An AI-powered multi-agent travel planning system built using **n8n, Ollama, and Tavily** that transforms a natural-language travel request into a personalized, budget-aware itinerary.

---

## 📌 Overview

Planning a trip usually requires searching across multiple websites for transportation, accommodation, activities, prices, and itinerary ideas.

**TravelMate** automates this process using a multi-agent AI architecture.

The user simply describes their trip in natural language, and TravelMate:

1. Understands the travel requirements
2. Researches transportation options
3. Researches accommodation and activities
4. Optimizes the trip according to the budget
5. Generates a complete day-by-day travel report

The system combines **local AI models with real-time web research** to create a practical and personalized travel plan.

---

## 🎯 Objectives

- Accept travel requirements through natural-language input
- Automatically extract important trip information
- Research current transportation options
- Research accommodation and activities
- Consider user preferences and budget
- Generate a day-by-day itinerary
- Calculate estimated trip costs
- Identify missing or uncertain information
- Reduce the amount of manual travel research
- Demonstrate multi-agent AI orchestration using n8n

---

## 🏗️ System Architecture

```text
                         USER
                           │
                           ▼
                  ┌─────────────────┐
                  │   Chat Trigger  │
                  └────────┬────────┘
                           │
                           ▼
            ┌────────────────────────────┐
            │ Agent 1                    │
            │ Requirement Analyzer       │
            │                            │
            │ Model: Gemma 3 1B         │
            └─────────────┬──────────────┘
                          │
                          ▼
            ┌────────────────────────────┐
            │ Agent 2                    │
            │ Transportation Planner     │
            │                            │
            │ Model: Qwen3 4B           │
            │ Tools: Tavily Search       │
            │        Tavily Extract      │
            └─────────────┬──────────────┘
                          │
                          ▼
            ┌────────────────────────────┐
            │ Agent 3                    │
            │ Accommodation & Activities │
            │ Planner                    │
            │                            │
            │ Model: Qwen3 4B           │
            │ Tools: Tavily Search       │
            │        Tavily Extract      │
            └─────────────┬──────────────┘
                          │
                          ▼
            ┌────────────────────────────┐
            │ Agent 4                    │
            │ Budget & Itinerary         │
            │ Optimizer                  │
            │                            │
            │ Model: Qwen3 4B           │
            └─────────────┬──────────────┘
                          │
                          ▼
            ┌────────────────────────────┐
            │ Agent 5                    │
            │ Final Report Generator     │
            │                            │
            │ Model: Gemma 3 1B         │
            └─────────────┬──────────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │  FINAL TRIP PLAN│
                 └─────────────────┘
