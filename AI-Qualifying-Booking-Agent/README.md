# 🎯 AI Sales Development Rep (SDR) & Booking Agent

## 🚀 The Problem
High-performing sales teams waste 30-50% of their time talking to unqualified leads—people who don't have the budget, authority, or immediate need. Manual qualification is slow and lets hot leads go cold.

## 🛠 The Solution
A fully autonomous **AI SDR** that engages raw leads instantly, evaluates them against your Ideal Customer Profile (ICP), and either books a meeting or deflects them—all in under 60 seconds.

### **Workflow Logic (Step-by-Step):**
1.  **Ingestion:** Webhook triggers when a new lead submits a form (Typeform/Website/Facebook Lead Ad).
2.  **AI Analysis (The Brain):**
    * **Prompt Engineering:** GPT-4o analyzes open-ended answers.
    * **Scoring:** Assigns a "Fit Score" (0-100) based on Budget, Authority, Need, and Timing (BANT).
    * **Classification:** Tags the lead as `Qualified`, `Unqualified`, or `Maybe`.
3.  **The Fork (Logic Branching):**
    * ✅ **Qualified (>70 Score):**
        * Syncs to **HubSpot/CRM** as "Deal Stage: Discovery".
        * Sends a customized email with a **Calendly/booking link**.
        * Alerts the Sales Director via **Slack** with a "Hot Lead" notification.
    * ❌ **Unqualified (<40 Score):**
        * Sends a polite "soft letdown" email with free educational resources.
        * Tags in CRM as "Nurture - Low Priority".
    * 🤔 **Maybe (40-70 Score):**
        * Drafts a personalized follow-up question for a human rep to review.

## 🧰 Tech Stack
* **Orchestration:** n8n
* **Forms:** Webhook (Typeform/Gravity Forms)
* **Intelligence:** OpenAI (GPT-4o) for Sentiment & Intent Analysis
* **CRM:** HubSpot / Airtable
* **Alerting:** Slack / Microsoft Teams

## ⚙️ Setup
1.  Import `AI-Qualifying-Booking-Agent.json` into n8n.
2.  **Critical:** Customize the System Prompt in the OpenAI node to define *your* specific qualification criteria (e.g., "Budget must be >$2k").
3.  Map your CRM fields in the HTTP Request/CRM node.
4.  Replace the placeholder Booking URL with your calendar link.