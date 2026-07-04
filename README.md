# AI-Powered B2B Intent Intelligence Platform

Transform real-time buying signals into actionable sales opportunities using AI Agents.

Automatically:

✓ Monitor market signals

✓ Detect buying intent

✓ Score target accounts

✓ Update CRM

✓ Recommend decision makers

✓ Generate personalized outreach

✓ Notify SDRs instantly

<img width="1024" height="572" alt="image" src="https://github.com/user-attachments/assets/8179bc2e-9ce8-43ae-bf1a-fdc16790c4dc" />

## Live Demo

(Coming Soon)

## Overview

AI-Powered B2B Intent Intelligence Platform is an end-to-end multi-agent workflow that continuously monitors market activity, identifies buying intent, prioritizes target accounts, recommends decision-makers, generates personalized outreach, and updates CRM automatically. It demonstrates how modern AI agents can automate the top of the B2B sales funnel.

## Business Problem

B2B sales teams often discover buying intent too late. Market signals are scattered across multiple sources, require manual research, and rarely translate into timely personalized outreach.

This project automates the journey from signal discovery to AI-generated outreach.

## Key Features

-   Multi-source news monitoring
-   AI signal extraction and normalization
-   Intent scoring engine
-   CRM update
-   Buyer discovery
-   AI outreach generation
-   Telegram alerts

## Tech Stack

  - Workflow: n8n
  - AI: Claude, OpenAI
  - News: Google News RSS, NewsAPI, Hacker News
  - Storage: Google Sheets
  - Notifications: Telegram
  - APIs: REST APIs

## Product Vision:

During my transition into AI Product Management, I wanted to build something that demonstrates workflow automation, CRM integrations, AI agents, and product thinking—not just LLM prompting. This project simulates how modern B2B sales organizations detect buying intent, prioritize accounts, and generate personalized outreach using a modular AI architecture.

##  User Journey

Target Accounts
        │
        ▼
News Collection
        │
        ▼
Signal Normalization
        │
        ▼
Intent Scoring
        │
        ▼
CRM Update
        │
        ▼
Buyer Discovery
        │
        ▼
AI Outreach
        │
        ▼
Telegram Alerts

<img width="1148" height="1108" alt="image" src="https://github.com/user-attachments/assets/1c8cd067-47ac-40fa-aaa5-2c69a82022be" />


## Architecture Diagram

<img width="1512" height="982" alt="image" src="https://github.com/user-attachments/assets/0fae11c5-96ed-45d5-9b6d-330041a301d2" />

## AI Agents
| Agent                | Responsibility               |
| -------------------- | ---------------------------- |
| Signal Discovery     | Find relevant buying signals |
| Signal Extraction    | Extract structured events    |
| Signal Normalization | Standardize data             |
| Intent Scoring       | Calculate buying intent      |
| Buyer Discovery      | Recommend contacts           |
| Personalization      | Generate outreach            |



## Scoring Framework:

| Signal         | Weight |
| -------------- | -----: |
| Funding        |     40 |
| Acquisition    |     35 |
| Partnership    |     25 |
| Expansion      |     15 |
| Hiring         |     10 |
| Product Launch |     20 |

-   Weighted buying signals
-   Time decay
-   Unique signal types only
-   Maximum score = 100
-   Buying stages: Target, Awareness, Consideration, Decision

## Product Decisions:

Google Sheets
→ Rapid MVP iteration without infrastructure overhead

Signal Expiry
→ Prevent stale buying intent from influencing scores

Modular AI Agents
→ Independent prompts improve maintainability

Human-readable CRM
→ Designed for SDR usability

AI only for reasoning-intensive tasks
→ Deterministic logic for rule-based operations; AI reserved for reasoning-intensive tasks.

## Sample Outputs:

-   Signal Store
<img width="1512" height="982" alt="image" src="https://github.com/user-attachments/assets/2e1bbaaa-1274-4c85-9e54-4f55c392a83f" />


-   CRM
<img width="1512" height="982" alt="image" src="https://github.com/user-attachments/assets/30b721ef-a9e7-45b2-bd82-89c8dc7f2d6f" />


-   Telegram alerts
  <img width="335" height="236" alt="image" src="https://github.com/user-attachments/assets/793664a5-36cd-4d51-a756-ffcab06f76ab" />


-   Email draft
<img width="701" height="646" alt="image" src="https://github.com/user-attachments/assets/d7995547-c906-4e8e-874e-7ccc7384e76d" />


-   LinkedIn draft
  <img width="411" height="159" alt="image" src="https://github.com/user-attachments/assets/6c652927-760b-4799-a42c-b6de0fe9580c" />



## Technical Highlights:

30+ n8n nodes

6 AI Agents

3 External APIs

100% Automated

7 Buying Signal Types

Intent Score Engine

CRM Synchronization

Personalized Outreach


## Current Limitations:

-   No historical intent trend visualization
-   Limited contact enrichment sources
-   Rule-based scoring (no ML learning)
-   Google Sheets instead of a database
-   Rule-based scoring
-   Limited news sources
-   No feedback learning
-   No analytics dashboard


## Future Roadmap:
Phase 1
- PostgreSQL
- Redis Cache
- Slack

Phase 2
- Salesforce
- HubSpot
- Pipedrive

Phase 3
- RAG
- Pinecone
- Historical Trends

Phase 4
- ML Intent Scoring
- Feedback Learning
- Reinforcement



## Design Principles

-   Explainable AI
-   Modular architecture
-   Low-cost MVP
-   Human-in-the-loop


## Lessons Learned

-   Specialized agents outperform single prompts.
-   Signal freshness matters.
-   Explainability builds trust.


## Skills Demonstrated

• Product Management

• AI Agent Design

• Workflow Automation

• CRM Integrations

• Prompt Engineering

• Intent Scoring

• API Integrations

• Multi-Agent Systems

• Sales Automation

• n8n

• Claude

• OpenAI

• Google Sheets API

• REST APIs
