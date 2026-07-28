# 🤖 AI Personal Assistant (Multi-Agent System)

An AI-powered multi-agent personal assistant built with **n8n** that enables users to manage Gmail, Google Calendar, Google Tasks, and perform AI-powered web research through a single Telegram chat interface.

Rather than relying on one AI agent to handle every request, the system uses an intelligent **Orchestrator Agent** that analyzes each user request and delegates it to the most appropriate specialized agent.

---

# 📌 Overview

Modern productivity is fragmented across multiple applications. Users constantly switch between Gmail, Google Calendar, Google Tasks, and search engines just to complete everyday work.

This project demonstrates how a modular AI architecture can unify these services into a single conversational assistant capable of understanding natural language and executing tasks across multiple platforms.

---

# 🚨 Problem

Managing productivity across several applications introduces unnecessary context switching and reduces efficiency.

Traditional AI assistants also become increasingly difficult to scale because a single agent is responsible for every capability, resulting in:

- Complex prompt engineering
- Reduced maintainability
- Limited scalability
- Poor separation of responsibilities

---

# ✅ Solution

This project implements a **multi-agent architecture** where a central **Orchestrator Agent** acts as the decision-maker.

When a user sends a request through Telegram, the Orchestrator:

1. Understands the user's intent.
2. Selects the appropriate specialized agent.
3. Executes the requested task.
4. Returns the final response to the user.

Specialized agents include:

- 📧 Gmail Agent
- 📅 Google Calendar Agent
- ✅ Google Tasks Agent
- 🌐 Research Agent

Each agent is responsible for only one domain, making the overall system modular, scalable, and easy to extend.

---

# 🎯 Outcome

The assistant provides a single conversational interface capable of managing multiple productivity services.

### Key Benefits

- Eliminates unnecessary application switching
- Simplifies email and calendar management
- Automates task management
- Provides AI-powered web research
- Easily expandable with additional agents
- Demonstrates production-style AI workflow architecture using n8n

---

# 🏗️ System Architecture

The complete workflow consists of an Orchestrator Agent responsible for routing requests to specialized agents.


---

# 🤖 Orchestrator Workflow

The Orchestrator Agent serves as the brain of the system.

Its responsibilities include:

- Understanding user intent
- Routing requests
- Delegating work to specialized agents
- Returning responses back to Telegram

> <img width="1605" height="700" alt="image" src="https://github.com/user-attachments/assets/9b5e4d67-887c-407d-a14b-bf2c4a70f3fb" />


---

# 📧 Gmail Agent

The Gmail Agent is responsible for handling all email-related operations.

### Capabilities

- Send emails
- Retrieve unread replies
- Read messages
- Return responses to the Orchestrator

> <img width="1338" height="624" alt="image" src="https://github.com/user-attachments/assets/d9b1cbe4-4e4f-4bed-8193-5a75c48c3271" />


---

# 📅 Google Calendar Agent

The Calendar Agent manages scheduling operations.

### Capabilities

- Create meetings
- Create calendar events
- Retrieve upcoming events
- Return scheduling information

> <img width="1378" height="641" alt="image" src="https://github.com/user-attachments/assets/154a238f-4d07-4c58-b62e-cf35c6fe2bfd" />


---

# ✅ Google Tasks Agent

The Google Tasks Agent manages personal task automation.

### Capabilities

- Create tasks
- Retrieve existing tasks
- Delete tasks
- Return task information

> <img width="1475" height="678" alt="image" src="https://github.com/user-attachments/assets/307fa5ca-b5f6-4f8c-b7ba-2f9ff6fef2d3" />

---

# 🌐 Research Agent

The Research Agent performs AI-powered external research whenever additional information is required.

### Data Sources

- Web Search
- Wikipedia
- Hacker News

Research results are summarized before being returned to the Orchestrator.

> <img width="1249" height="673" alt="image" src="https://github.com/user-attachments/assets/09959e00-6652-424f-9dd7-4da8701a0445" />

---

# ⚙️ Technologies Used

- n8n
- Groq
- OpenAI / Gemini (compatible)
- Telegram Bot API
- Gmail API
- Google Calendar API
- Google Tasks API
- REST APIs
- HTTP Requests
- JSON

---

# 💬 Example Commands

- Schedule a meeting with John tomorrow at 3 PM.
- Show me today's meetings.
- Create a task to finish my GitHub portfolio.
- Summarize my unread emails.
- Research the latest AI automation trends.


---

# 🚀 Future Improvements

- Voice interaction
- WhatsApp integration
- Long-term memory
- Additional specialized agents
- Slack integration
- Microsoft Outlook integration
- Google Drive integration
- Multi-user authentication

---

# 👨‍💻 About

This project is part of my AI Automation Portfolio, where I build production-ready AI systems using **n8n, APIs, Large Language Models, and workflow automation** to solve real business problems.

The goal is to demonstrate scalable AI architectures that can be deployed in production environments rather than simple proof-of-concept automations.

If you'd like to discuss AI automation, workflow design, or collaboration opportunities, feel free to connect.
