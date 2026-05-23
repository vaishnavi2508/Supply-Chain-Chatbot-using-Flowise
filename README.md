# 🚚 SCM Assistant - Supply Chain RAG Chatbot

An AI-powered Supply Chain Management Assistant built using **Flowise AI**, **Groq**, **Pinecone**, and **HuggingFace Embeddings**.

The chatbot uses Retrieval-Augmented Generation (RAG) to answer supplier governance, disruption risk, compliance, and procurement policy related questions from uploaded enterprise documents.

---

# 🔗 Public Chatbot URL

👉 https://cloud.flowiseai.com/chatbot/535b01ae-a5fe-4766-90f1-845741d73664

---

# 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Framework | Flowise AI |
| LLM | Groq (`llama-3.3-70b-versatile`) |
| Embeddings | `sentence-transformers/all-MiniLM-L6-v2` |
| Vector Database | Pinecone |
| Similarity Search | Cosine Similarity |

---

# ⚙️ Model Configuration

## 🤖 LLM Configuration
- Model: `llama-3.3-70b-versatile`
- Temperature: `0.9`

## 🧠 Embedding Configuration
- Model: `sentence-transformers/all-MiniLM-L6-v2`

## 🗂️ Pinecone Configuration
- Vector Type: `Dense`
- Dimension: `384`
- Metric: `Cosine`

---

# ✂️ Chunking Experiments

## 📄 CSV Configuration
- Chunking Strategy: Default Row-wise Chunking
- Total Chunks Generated: `2000`

## 📘 PDF Configuration
- Splitter: `Token Text Splitter`
- Chunk Size: `500`
- Chunk Overlap: `80`
- Total Chunks Generated: `13`

---

# 🧩 Chatflow Architecture

```text
Groq Chat Model
        ↓
Conversational Retrieval QA Chain
        ↑
Pinecone Vector Store Retriever
