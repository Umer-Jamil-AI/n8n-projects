# 📂 Gmail Intelligent Document Processing (IDP) Archive

## 🚀 The Problem
Finance and Legal teams drown in email attachments (invoices, contracts, receipts). Manually downloading, renaming, and filing these documents into the correct Google Drive folders wastes hours daily.

## 🛠 The Solution
An intelligent filing agent that "reads" every attachment, understands what it is, and files it according to strict compliance rules.

### **Workflow Logic (Step-by-Step):**
1.  **Listener:** Watcher node triggers on emails with attachments in `finance@company.com`.
2.  **OCR & Analysis:** OpenAI Vision/GPT-4o reads the PDF/Image content.
3.  **Classification:** Determines doc type: `Invoice`, `Contract`, `Receipt`, or `Junk`.
4.  **Extraction:** Extracts metadata (Vendor Name, Date, Amount, Invoice #).
5.  **Renaming:** Renames the file to standard format: `YYYY-MM-DD_Vendor_Type.pdf`.
6.  **Filing:** Routes the file to the specific Google Drive folder (e.g., `/Finance/2024/Vendors/`).

## 🧰 Tech Stack
* **Email:** Gmail API
* **Storage:** Google Drive API
* **AI:** OpenAI Vision (Multimodal analysis)
* **Logic:** Switch Node (Routing based on classification)

## ⚙️ Setup
1.  Import `Gmail-OpenAI-Drive-Archive.json`.
2.  Authorize Gmail and Drive nodes via OAuth2.
3.  Adjust the system prompt in the OpenAI node to match your file naming convention.