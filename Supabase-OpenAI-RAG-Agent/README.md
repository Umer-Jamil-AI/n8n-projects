# 🧠 Supabase OpenAI RAG Agent (Sovereign Knowledge Engine)

## 🚀 The Problem
Businesses have gigabytes of PDF manuals, policies, and SOPs, but employees still ask repetitive questions because they can't find the answers. Standard keyword search fails to understand context.

## 🛠 The Solution
This n8n workflow builds a **Retrieval-Augmented Generation (RAG)** pipeline that allows users to "chat" with their private data. It autonomously handles the ingestion, embedding, and retrieval process without hallucination.

### **Workflow Logic (Step-by-Step):**
1.  **Ingestion:** Watcher node detects new PDFs uploaded to Google Drive.
2.  **Chunking:** Splits documents into 1000-token overlapping chunks to preserve context.
3.  **Embedding:** Sends text to `text-embedding-3-small` (OpenAI) to generate vectors.
4.  **Storage:** Upserts vectors into **Supabase (pgvector)** with metadata.
5.  **Retrieval:** On user query, performs a semantic similarity search in Supabase.
6.  **Synthesis:** Feeds the retrieved context + user query to GPT-4o for a citation-backed answer.

## 🧰 Tech Stack
* **Orchestration:** n8n
* **Vector DB:** Supabase (PostgreSQL + pgvector)
* **LLM:** OpenAI (GPT-4o, text-embedding-3)
* **Storage:** Google Drive API

## ⚙️ Setup
1.  Import `Supabase-OpenAI-RAG-Agent.json` into n8n.
2.  Set up a Supabase project and enable the `vector` extension.
3.  Add your OpenAI API Key and Supabase credentials in n8n.
4.  Configure the Google Drive trigger folder ID.