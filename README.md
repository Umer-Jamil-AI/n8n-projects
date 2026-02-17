# ⚡ n8n Automation & AI Agent Portfolio

### **Agentic Workflows for Enterprise Operations, CRM Syncs, and RAG Systems**

> *"I don't just build chatbots; I architect autonomous systems that think, plan, and execute complex business logic."*

---

## 📖 Overview

Welcome to my central repository for **AI Automation & Orchestration**.
This collection demonstrates production-grade workflows built with **n8n**, **OpenAI (GPT-4o)**, and **Vector Databases**.

Unlike simple "wrapper" scripts, these agents handle:
* **State Management:** Tracking leads through a full CRM lifecycle.
* **Cognitive Decision Making:** Using LLMs to route, classify, and score data.
* **Error Handling:** Robust logic to ensure 99.9% uptime for business-critical ops.

---

## 📂 Featured Projects (The "Big 4")

| Project | Business Logic & Capabilities | Tech Stack |
| :--- | :--- | :--- |
| **[📂 Supabase RAG Agent](./Supabase-OpenAI-RAG-Agent)** | **"Chat with your Data" Engine.**<br>Ingests PDFs, chunks text, creates vector embeddings, and enables hallucination-free retrieval. | `Supabase` `pgvector` `OpenAI` `Drive API` |
| **[📂 AI Meeting Ops](./AI-Meeting-Ops-Agent)** | **Automated Chief of Staff.**<br>Listens to Fireflies.ai transcripts, extracts action items, assigns tasks in Asana, and emails summaries. | `Fireflies.ai` `Airtable` `GPT-4o` `Gmail` |
| **[📂 HubSpot Sync](./HubSpot-Airtable-AI-Agent)** | **Intelligent CRM <-> Ops Bridge.**<br>Two-way sync that transforms raw sales notes into clean project briefs for operations teams. | `HubSpot` `Airtable` `Webhooks` `JSON` |
| **[📂 Sales SDR Agent](./AI-Qualifying-Booking-Agent)** | **24/7 Lead Qualification.**<br>Scores incoming leads (0-100), books meetings for qualified prospects, and nurtures the rest automatically. | `Typeform` `Slack` `Calendly` `GPT-4o` |

---

## 🛠️ Technical Competencies

My approach bridges the gap between **Low-Code Speed** and **High-Code Complexity**:

### **1. AI & LLM Integration**
* **RAG Pipelines:** Chunking, Embedding (`text-embedding-3-small`), and Vector Search.
* **Prompt Engineering:** Few-Shot prompting and System Instructions for structured JSON output.
* **Vision API:** OCR for invoice and receipt processing.

### **2. Backend Logic**
* **API Interoperability:** OAuth2, Bearer Token auth, and handling pagination/rate limits.
* **Data Transformation:** Complex JavaScript (Code Nodes) for deduplication and regex cleaning.
* **State Machines:** Logic gates (`If/Switch`) to handle multi-step business processes.

---

## 🚀 How to Use These Workflows

1.  **Clone the Repo:**
    ```bash
    git clone [https://github.com/Umer-Jamil-AI/n8n-projects.git](https://github.com/Umer-Jamil-AI/n8n-projects.git)
    ```
2.  **Import to n8n:**
    * Navigate to any project folder (e.g., `/Supabase-OpenAI-RAG-Agent`).
    * Download the `.json` file.
    * In your n8n dashboard, click **"Import from File"**.
3.  **Configure Credentials:**
    * Each workflow requires specific API keys (OpenAI, HubSpot, Supabase).
    * Refer to the specific `README.md` inside each project folder for setup instructions.

---

## 📬 Contact & Hire

I help agencies and e-commerce brands automate their most painful manual tasks.

* **Portfolio:** [umer-jamil-ai.github.io](https://umer-jamil-ai.github.io/)
* **Upwork:** [Hire Me for Automation](https://www.upwork.com/freelancers/umerjamil)

> *"Automation is not about replacing humans; it's about freeing them to do human work."*
