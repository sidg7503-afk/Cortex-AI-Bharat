# System Design: Cortex AI (Rural Education Engine)

## 1. Architecture Overview
Cortex operates on a **Modular Monolith** architecture optimized for low-latency edge devices (Mobile).

### Core Components:
1.  **Ingestion Layer:** Streamlit Frontend (Lightweight) handling Multi-File Uploads (PDF/IMG).
2.  **Neural Router:** Python-based logic gate that selects between `Gemini-1.5-Flash` (Speed) and `DeepSeek-R1` (Logic).
3.  **Knowledge Base:** FAISS/ChromaDB (Vector Store) for RAG implementation on NCERT textbooks.

## 2. Data Flow
1.  **User Input** -> **Sanitization Layer** -> **Language Detection**.
2.  **Router** -> Selects Model API (OpenRouter/Google).
3.  **Model Output** -> **LaTeX Formatter** -> **TTS Engine (Audio)** -> **Client**.

## 3. Tech Stack
* **Frontend:** Streamlit (Python)
* **AI Orchestration:** LangChain / Custom Python Logic
* **Database:** JSON (Local MVP) / PostgreSQL (Production)
* **Infrastructure:** Replit (Dev) / AWS Bedrock (Target Prod)
