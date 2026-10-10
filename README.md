# AI Customer Support Bot using RAG & n8n

An automated customer support assistant built with **n8n**, utilizing **RAG (Retrieval-Augmented Generation)** to answer policy-related queries accurately without hallucinations.

---

## 🛠️ Tech Stack & Architecture

- **Automation Platform:** n8n
- **Large Language Model (LLM):** Google Gemini Chat Model (`gemini-1.5-flash`)
- **Embedding Model:** Google Gemini Embeddings (`text-embedding-004`)
- **Vector Database:** Supabase Vector / Pinecone
- **Interface:** Telegram Bot API
- **Data Source:** Google Drive (Store Policy Documents)

---

## 🏗️ Workflow Architecture

The system consists of two core pipelines:

1. **Data Ingestion Pipeline:** Syncs PDF policies from Google Drive, generates vector embeddings via Gemini, and indexes them into the Vector Database.
2. **Retrieval & Chat Pipeline:** Listens to Telegram messages, retrieves relevant context from the Vector Store, maintains chat memory per user session, and returns precise answers.

![n8n Workflow]<img width="1164" height="639" alt="Rage AI" src="https://github.com/user-attachments/assets/07f118ce-859c-49e8-ac0c-624b786d7c79" />

---

## 🧪 Testing & Evaluation

### Arabic Interaction (Localized Support)
![Arabic Chat]<img width="300" height="600" alt="WhatsApp Image 2026-10-10 at 9 49 46 PM" src="https://github.com/user-attachments/assets/5cce3712-2900-4e88-87bd-d761e7a10622" />


### English Interaction (Multilingual Support)
![English Chat]<img width="300" height="600" alt="WhatsApp Image 2026-10-10 at 9 49 45 PM" src="https://github.com/user-attachments/assets/5a0a8280-f608-4e6c-9a26-607d9c2ffb2a" />

---

## 🚀 How to Run

1. Import the `RAG-Telegram_bot.json` file into your n8n workspace.
2. Add your credentials for:
   - Google Drive
   - Google Gemini API Key
   - Supabase / Pinecone API Key
   - Telegram Bot Token
3. Update the Vector Store index/table name.
4. Activate the workflow and test via Telegram.



