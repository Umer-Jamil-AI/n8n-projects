# 🎙️ AI Meeting Ops Agent (Fireflies.ai Sync)

## 🚀 The Problem
Project managers spend 20-30% of their week organizing post-meeting notes, assigning tasks in Asana/ClickUp, and sending follow-up emails. Information gets lost in transit.

## 🛠 The Solution
A fully autonomous "Chief of Staff" agent that listens to meetings, extracts action items, and enforces accountability by directly updating project management tools.

### **Workflow Logic (Step-by-Step):**
1.  **Trigger:** Webhook receives meeting transcript completion event from **Fireflies.ai**.
2.  **Extraction:** GPT-4o analyzes the transcript to identify:
    * Decision Points
    * Action Items (Who, What, By When)
    * Sentiment Analysis
3.  **Routing:**
    * **Tasks:** Pushed directly to **Airtable/Asana** with due dates.
    * **Summary:** Drafts a formatted email in **Gmail** to all attendees.
    * **CRM:** Updates **HubSpot** deal stages if the meeting was a sales call.

## 🧰 Tech Stack
* **Voice Intelligence:** Fireflies.ai API
* **Database:** Airtable
* **Communication:** Gmail API
* **LLM:** OpenAI (JSON Mode for structured output)

## ⚙️ Setup
1.  Import `AI-Meeting-Ops-Agent.json`.
2.  Connect your Fireflies.ai API key.
3.  Map the Airtable Base ID for task creation.