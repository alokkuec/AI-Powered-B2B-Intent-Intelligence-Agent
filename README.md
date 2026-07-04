# AI-Powered B2B Intent Intelligence Agent

## Overview

An end-to-end multi-agent AI workflow built with **n8n** that continuously monitors market signals, identifies buying intent, prioritizes target accounts, recommends decision-makers, generates personalized outreach, and updates a lightweight CRM.

## Business Problem

B2B sales teams often discover buying intent too late. Market signals are scattered across multiple sources, require manual research, and rarely translate into timely personalized outreach.

This project automates the journey from signal discovery to AI-generated
outreach.

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
## Flow

1.  Read Target Accounts
2.  Fetch News
3.  Normalize
4.  Deduplicate
5.  Aggregate by Company
6.  AI Signal Discovery
7.  Signal Extraction
8.  Signal Normalization
9.  Store Signals
10. Calculate Intent
11. Update CRM
12. Buyer Discovery
13. Persona Selection
14. Generate Outreach
15. Telegram Notification

## Architecture Diagram

<img width="1512" height="982" alt="image" src="https://github.com/user-attachments/assets/0fae11c5-96ed-45d5-9b6d-330041a301d2" />


## User Journey

Target Accounts → News Collection → Intent Detection → CRM Update →
Contact Recommendation → Personalized Outreach → SDR Notification

## Scoring Framework

-   Weighted buying signals
-   Time decay
-   Unique signal types only
-   Maximum score = 100
-   Buying stages: Target, Awareness, Consideration, Decision

## Product Decisions

-   Google Sheets as MVP datastore
-   Modular AI agents
-   Human-readable CRM
-   Signal expiry
-   AI only for high-value tasks

## Sample Outputs

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


## Current Limitations

-   Google Sheets instead of a database
-   Rule-based scoring
-   Limited news sources
-   No feedback learning
-   No analytics dashboard

## Future Roadmap

-   PostgreSQL
-   HubSpot/Salesforce sync
-   RAG
-   Vector search
-   Historical trends
-   ML-based scoring
-   SDR feedback loop
-   Dashboard

## Repository Structure

``` text
/workflows
/prompts
/docs
/screenshots
README.md
```

## Design Principles

-   Explainable AI
-   Modular architecture
-   Low-cost MVP
-   Human-in-the-loop

## Lessons Learned

-   Specialized agents outperform single prompts.
-   Signal freshness matters.
-   Explainability builds trust.
