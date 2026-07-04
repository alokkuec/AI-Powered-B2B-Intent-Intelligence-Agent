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

``` text
News Sources
      |
Normalize
      |
Deduplicate
      |
Aggregate
      |
AI Signal Discovery
      |
Signal Extraction
      |
Signal Store --> Intent Engine --> CRM
                              |
                       Buyer Discovery
                              |
                      AI Personalization
                              |
                          Telegram
```

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
-   CRM
-   Telegram alerts
-   Email draft
-   LinkedIn draft

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
