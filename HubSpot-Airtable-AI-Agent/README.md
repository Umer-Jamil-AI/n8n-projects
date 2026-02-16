# 🔄 HubSpot <-> Airtable Two-Way AI Sync

## 🚀 The Problem
Sales teams live in HubSpot, but Operations teams live in Airtable. Keeping these two systems in sync is usually a manual nightmare, leading to data silos and "dropped balls" in client delivery.

## 🛠 The Solution
A state-aware sync agent that acts as the bridge between Sales and Ops. It doesn't just copy data; it *transforms* it using AI.

### **Workflow Logic (Step-by-Step):**
1.  **State Detection:** Polling trigger detects "Deal Won" status in HubSpot.
2.  **Enrichment:**
    * Fetches company domain.
    * Uses Clearbit/Apollo API (via HTTP Request) to enrich lead data.
3.  **Transformation:** GPT-4o formats the raw sales notes into a clean "Project Brief" for the Ops team.
4.  **Creation:** Creates a linked record in Airtable for the delivery team.
5.  **Feedback Loop:** Updates HubSpot with the "Project Started" timestamp to notify Sales.

## 🧰 Tech Stack
* **CRM:** HubSpot API
* **Database:** Airtable
* **Logic:** Javascript Code Node (for deduplication)
* **AI:** OpenAI (Text Formatting)

## ⚙️ Setup
1.  Import `HubSpot-Airtable-AI-Agent.json`.
2.  Ensure HubSpot Private App Token has `crm.objects.deals.read` scope.
3.  Configure Airtable Personal Access Token.