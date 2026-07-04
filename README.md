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

Loom walkthrough — recording in progress.
See Sample Outputs below for workflow results.

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

At 6sense, I launched Intelligent Workflows — a no-code GTM orchestration platform used by 1,500+ enterprise customers. I wanted to build the underlying signal detection and scoring layer from scratch to understand the implementation depth behind the product decisions I was making as a PM.

This project simulates how enterprise intent platforms detect buying signals, weight them over time, and translate them into personalised outreach — built with n8n, Claude, and Google Sheets as the intentionally lightweight stack.

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
| Agent                | Responsibility               | Why AI(Not Rules)                      |
| -------------------- | ---------------------------- | ---------------------------------------|
| Signal Discovery     | Find relevant buying signals | Ambiguous text requires judgment       |
| Signal Normalization | Standardize data             | Handles varied Claude output formats   |
| Intent Scoring       | Calculate buying intent      | ❌ Pure JS — deterministic by design   |
| Buyer Discovery      | Recommend contacts           | Role matching requires context         |
| Personalization      | Generate outreach            | Creative language generation           |
| Stage Assignment     | Map score to buying Stage    | ❌ Pure rules — explainable by design 



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

- **Sequential signal storage** before history read —
  eliminates race condition in parallel branch design
- **Time decay model** — signals >30 days old weighted
  at 50%, signals >90 days excluded entirely
- **Content-based deduplication** — fingerprint on
  company + headline prevents score inflation across
  runs and sources
- **One headline = one signal** priority rule —
  prevents double-counting from compound headlines
- **Watchlist-scoped history reads** — Signal Store
  filtered to active accounts only, not a full table scan


## Current Limitations:

## Current Limitations

- Google Sheets as signal store — no indexed queries, reads all rows per run (see Roadmap: Phase 1)

- Contact enrichment uses mock data — Apollo and Hunter free tiers restrict people search endpoints

- Signal collection limited to news APIs — LinkedIn hiring/leadership signals require paid enrichment

- No feedback loop — scoring weights are static, not learned from conversion outcomes

- No historical trend visualization — score changes over time not yet surfaced

-   Rule-based scoring (no ML learning)

-   Limited news sources
  


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
