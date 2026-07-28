# 🤖 AI Personal Assistant (Multi-Agent System)

> An AI-powered multi-agent personal assistant built with **n8n** that manages Gmail, Google Calendar, Google Tasks, and web research through a single Telegram chat interface.

---

# 📖 Overview

This project demonstrates a production-style **multi-agent AI system** built with **n8n**, AI models, and Google Workspace APIs.

Rather than relying on a single AI agent to perform every task, the assistant uses an intelligent **Orchestrator Agent** that understands the user's request and delegates it to specialized agents responsible for individual services.

Users interact with the system through Telegram using natural language, allowing them to manage emails, calendars, tasks, and perform web research without switching between multiple applications.

The modular architecture makes the system easier to maintain, highly scalable, and simple to extend with additional agents in the future.

---

# 🚨 Problem

Modern productivity is spread across multiple applications.

Users constantly switch between Gmail, Google Calendar, Google Tasks, and search engines just to complete simple everyday tasks.

This creates:

- Constant context switching
- Slower task completion
- Reduced productivity
- Increased cognitive load

Traditional AI assistants also become difficult to maintain because one agent is responsible for every task, making them harder to scale as new capabilities are added.

---

# 💡 Solution

This project implements a **multi-agent architecture** where a central **Orchestrator Agent** acts as the intelligent decision-maker.

When a request is received through Telegram, the orchestrator:

1. Understands the user's intent
2. Selects the appropriate specialized agent
3. Executes the requested action
4. Returns the response back to the user

### Specialized Agents

- 📧 Gmail Agent
- 📅 Google Calendar Agent
- ✅ Google Tasks Agent
- 🌐 Web Research Agent

Each agent operates independently, making the system modular, reliable, and easy to extend.

---

# 🎯 Outcome

The assistant provides a single conversational interface for managing multiple productivity tools.

### Business Value

- Reduces context switching between applications
- Simplifies email, calendar, and task management
- Provides AI-powered web research on demand
- Improves productivity through workflow automation
- Demonstrates a scalable multi-agent architecture
- Makes future feature expansion significantly easier

---

# ✨ Features

- Multi-agent AI architecture
- Intelligent task routing
- Telegram conversational interface
- Gmail integration
- Google Calendar integration
- Google Tasks integration
- AI-powered web research
- Natural language command processing
- Workflow automation with n8n
- API integrations with Google Workspace
- Modular and scalable system design

---

# ⚙️ How It Works

```text
User
   │
   ▼
Telegram
   │
   ▼
Orchestrator Agent
   │
   ├────────► Gmail Agent
   ├────────► Calendar Agent
   ├────────► Tasks Agent
   └────────► Web Research Agent
                    │
                    ▼
             Response returned
                    │
                    ▼
                 Telegram
```

The Orchestrator Agent serves as the brain of the system. Instead of performing every task itself, it determines which specialized agent should handle the request, resulting in a cleaner, more maintainable architecture.

---

# 🛠️ Technologies Used

| Category | Technologies |
|----------|--------------|
| Workflow Automation | n8n |
| AI Models | OpenAI, Gemini |
| Messaging | Telegram Bot API |
| Productivity | Gmail API, Google Calendar API, Google Tasks API |
| Integrations | REST APIs, HTTP Requests |
| Data Format | JSON |

---

# 💬 Example Commands

```text
Schedule a meeting with John tomorrow at 3 PM.

Show me today's meetings.

Create a task to finish my GitHub portfolio.

Summarize my unread emails.

Research the latest AI automation trends.
```

---

# 📂 Project Files

```text
AI-Personal-Assistant/
│
├── README.md
├── orchestrator-agent.json
├── gmail-agent.json
├── calendar-agent.json
├── google-tasks-agent.json
├── web-research-agent.json
└── assets/
    ├── architecture.png
    ├── workflow.png
    └── demo.gif
```

---

# 🚀 Future Improvements

- Voice interaction
- WhatsApp integration
- Long-term memory
- Additional specialized agents
- More productivity integrations
- Persistent conversation history
- User authentication
- MCP (Model Context Protocol) support

---

# 👤 Author

**Israel Falaye**

AI Automation Engineer passionate about building production-ready AI systems, intelligent agents, and business automation solutions using n8n, APIs, and Large Language Models.

If you found this project interesting, feel free to ⭐ the repository.
