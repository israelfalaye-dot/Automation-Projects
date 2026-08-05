# AI Investor Portfolio Assistant

An AI-powered investment management system that combines **Vapi**, **n8n**, and **Airtable** to help angel investors manage their startup pipeline, portfolio companies, and annual reporting process using natural language voice commands and intelligent automation.
<!-- Paste Airtable Base Screenshot -->
---

# Overview

## Problem

Managing startup investments involves handling large volumes of emails, startup applications, founder information, portfolio data, and annual reports. As the number of investments grows, manually tracking opportunities, communicating with founders, and maintaining records becomes increasingly inefficient.

Angel investors often switch between multiple tools just to perform simple tasks such as reviewing new startups, updating company records, or checking portfolio information.

---

## Solution

This project provides an AI-powered portfolio management system that centralizes the entire investment workflow.

The solution combines voice AI, workflow automation, and Airtable into a single operating system capable of:

- Receiving startup investment inquiries
- Organizing startup applications automatically
- Managing investment opportunities
- Tracking portfolio companies
- Collecting founder contact information
- Sending automated follow-up emails
- Reminding founders about annual reports
- Retrieving and updating investment data through natural voice conversations

The voice assistant, **Marvin**, allows investors to interact with their portfolio simply by speaking.

---

## Outcome

The result is a streamlined investment management system that reduces repetitive administrative work while providing a faster and more organized experience for managing startup investments.

Instead of navigating multiple dashboards and spreadsheets, investors can retrieve information, update records, and manage their portfolio through a single AI-powered assistant.

---

# System Architecture

The system is built around a modular architecture where each component has a clearly defined responsibility.

- **Vapi** serves as the voice interface, allowing the investor to interact with the system using natural language.
- **n8n** acts as the automation engine, handling business logic, processing requests, and orchestrating workflows.
- **Airtable** functions as the central database, storing startups, opportunities, investments, and primary contacts.
- **AI Models** interpret user requests and generate conversational responses.
- **Email automations** keep founders informed throughout the investment lifecycle.

```
                         User
                          │
                          ▼
                Marvin (Vapi Voice AI)
                          │
                 Voice Conversation
                          │
                          ▼
                     n8n Backend
                          │
        ┌─────────────────┼─────────────────┐
        │                 │                 │
        ▼                 ▼                 ▼
  Retrieve Data     Update Records     Email Automation
        │                 │                 │
        └─────────────────┼─────────────────┘
                          │
                          ▼
                     Airtable Base
                          │
        ┌────────────┬─────────────┬─────────────┬─────────────┐
        ▼            ▼             ▼             ▼
 Startup Intake  Opportunities  Investments  Primary Contacts
```

This modular architecture makes each component independent, making the system easier to maintain, extend, and integrate with additional services in the future.


---

# Complete System Flow

The diagram below illustrates the complete investment lifecycle, from a founder's initial investment inquiry to ongoing portfolio management.

```text
 Founder
    │
    ▼
Investment Pitch Email
    │
    ▼
AI Email Assistant (n8n)
    │
    │ Detects startup investment inquiries
    │
    ▼
Automatic Reply with Startup Intake Form
    │
    ▼
Founder Completes Startup Intake Form
    │
    ▼
Startup Intake Table (Airtable)
    │
    │ Review & Evaluation
    ▼
Opportunities Table
    │
    ├───────────────────────────────────────────────┐
    │                                               │
    │                                               ▼
    │                                 Opportunity Follow-up Automation
    │                                               │
    │                              Sends meeting invitation email
    │                                               │
    └───────────────────────────────────────────────┘
    │
Investment Approved
    │
    ▼
Primary Contact Form
    │
    ▼
Primary Contacts Table
    │
    ▼
Investments Table
    │
    ├───────────────────────────────────────────────┐
    │                                               │
    │                                               ▼
    │                             Annual Report Reminder Automation
    │                                               │
    │                   Automatically reminds founders one month
    │                   before the next reporting date
    │
    └───────────────────────────────────────────────┘
    │
    ▼
Marvin (Voice AI Assistant)
    │
    ├── Retrieve portfolio information
    ├── Search investments
    ├── Search opportunities
    ├── Search startup submissions
    ├── Retrieve primary contacts
    └── Update annual reporting dates
```

This workflow creates a fully connected investment management system where startup sourcing, portfolio management, founder communication, and reporting are automated from end to end. Every stage of the investment lifecycle is connected through Airtable and orchestrated by n8n, while Marvin provides a natural voice interface for interacting with the entire system.

---

# Airtable Implementation

Airtable serves as the central data layer for the entire system. It stores startup submissions, investment opportunities, portfolio companies, and founder contact information while powering the interfaces, forms, and automations used throughout the investment lifecycle.

## Database

The Airtable base is organized into four core tables that represent each stage of the investment pipeline.

- Startup Intake
- Opportunities
- Investments
- Primary Contacts


---

## Interfaces

Custom Airtable Interfaces provide a clean workspace for reviewing and managing portfolio data.

### Startup Intake Dashboard

Displays all newly submitted startups awaiting review.

<img width="1786" height="915" alt="image" src="https://github.com/user-attachments/assets/37e18968-1ac7-44ea-93d0-1fc1faf82576" />


### Opportunities Dashboard

Displays startups currently being evaluated for investment.

<img width="1838" height="988" alt="image" src="https://github.com/user-attachments/assets/b7aeed28-6741-4631-9c79-94d9659f22dc" />


### Investment Portfolio Dashboard

Displays all active investments, annual reporting dates, and portfolio information.

<img width="1837" height="999" alt="image" src="https://github.com/user-attachments/assets/0d4c86dd-9bd8-4441-9997-207822d82e4d" />

---

## Forms

Two Airtable Forms simplify information collection throughout the investment process.

### Startup Intake Form

Founders complete this form after receiving the automated response to their investment inquiry. Submitted information is automatically stored in the **Startup Intake** table.

<img width="1732" height="899" alt="image" src="https://github.com/user-attachments/assets/89a08d8f-b97d-4a0e-b481-61b97c3ad6f9" />


### Primary Contact Form

Once an investment progresses, founders complete this form to provide the company's primary contact information.

Submitted responses are automatically stored in the **Primary Contacts** table.

<img width="1844" height="935" alt="image" src="https://github.com/user-attachments/assets/f2d34b02-028e-442c-bf46-01bbc9ee242e" />


---

## Automations

Two Airtable Automations eliminate repetitive manual follow-up.

### Opportunity Follow-up

When a startup is moved into the **Opportunities** table, Airtable automatically sends an email inviting the founder to schedule a meeting to discuss the investment opportunity.

<img width="1085" height="890" alt="image" src="https://github.com/user-attachments/assets/fb164a1e-48d4-4962-8bb4-ba49edf0e4a4" />


### Annual Report Reminder

One month before a company's annual reporting date, Airtable automatically emails the founder requesting their annual report.

<img width="845" height="882" alt="image" src="https://github.com/user-attachments/assets/2fc2e90d-cfad-4164-93fe-fa40b374b57a" />

---

# Tech Stack

| Category | Technology |
|-----------|------------|
| Voice AI | Vapi |
| Workflow Automation | n8n |
| Database | Airtable |
| AI Model | OpenAI |
| Programming | JavaScript |
| Integration | Webhooks |
| Email | Gmail |

---

# Repository Structure

```text
AI-Investor-Portfolio-Assistant/
├── README.md
└── workflow.json
```

---

## Future Improvements

- Portfolio analytics dashboard
- Investment performance summaries
- Calendar integration for founder meetings
- Automated investment memos
- Multi-user authentication
- Investor reporting dashboard

---

Built by **Kola**.



