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
```


# ✅ Validation Questions & Answers

## ❓ Q1. Which Tier-3 suppliers have an active disruption flag, and what response level applies per policy?

**Answer:**  
11 Tier-3 suppliers: Dravex Components India, Plataforma Metales SA, Maghreb Castworks, Helios Pack Greece, Cerromax Mineria, Orinoco Pack SAPI, Quetzal Textiles, Sibertek Molding, Archipelago PCB Corp, Varna Electronics EAD, Deltaforge Vietnam. All are High Risk with an active flag → Level 3 Activate per Policy §9 (CPO escalation + alternate supplier at minimum 40% volume).

---

## ❓ Q2. Which suppliers qualify for the annual Volume Rebate Program and how many are there?

**Answer:**  
19 suppliers qualify: Borealis Composites, Crestline Chemical Supply, Fenwick Alloy Solutions, Hanguk Circuit Works, Hokkaido Alloy Tech, Krauss-Polymex GmbH, Lakeshore Components, Lumivex Semiconductor NL, Maplewood Polymer Corp, Norbec Alloy Works, Nordloom Finland Oy, Orrentek Precision Mfg, Ostwind Composites AG, PrecisionForge Taiyuan, Solveig Eco Packaging, Straits Packaging Hub, Tasman Circuit Boards, Toreval Electronics, Valdoro Special Alloys. Criteria (Policy §4.2): Tier-1 + OTD ≥ 93% + Defect < 0.5% + Sustainability Score ≥ 85.

---


## ❓ Q3. Which region has the highest total PO value, and does it breach the concentration limit?

**Answer:**  
11 Tier-3 suppliers: Dravex Components India, Plataforma Metales SA, Maghreb Castworks, Helios Pack Greece, Cerromax Mineria, Orinoco Pack SAPI, Quetzal Textiles, Sibertek Molding, Archipelago PCB Corp, Varna Electronics EAD, Deltaforge Vietnam. All are High Risk with an active flag → Level 3 Activate per Policy §9 (CPO escalation + alternate supplier at minimum 40% volume).

---

## ❓ Q4. Which suppliers are on Supplier Watch List (SWL) status and what does it restrict?

**Answer:**  
19 suppliers qualify: Borealis Composites, Crestline Chemical Supply, Fenwick Alloy Solutions, Hanguk Circuit Works, Hokkaido Alloy Tech, Krauss-Polymex GmbH, Lakeshore Components, Lumivex Semiconductor NL, Maplewood Polymer Corp, Norbec Alloy Works, Nordloom Finland Oy, Orrentek Precision Mfg, Ostwind Composites AG, PrecisionForge Taiyuan, Solveig Eco Packaging, Straits Packaging Hub, Tasman Circuit Boards, Toreval Electronics, Valdoro Special Alloys. Criteria (Policy §4.2): Tier-1 + OTD ≥ 93% + Defect < 0.5% + Sustainability Score ≥ 85.

---
## ❓ Which product category has the highest average defect rate and does it exceed the Tier-2 limit?


**Answer:**  
11 Tier-3 suppliers: Dravex Components India, Plataforma Metales SA, Maghreb Castworks, Helios Pack Greece, Cerromax Mineria, Orinoco Pack SAPI, Quetzal Textiles, Sibertek Molding, Archipelago PCB Corp, Varna Electronics EAD, Deltaforge Vietnam. All are High Risk with an active flag → Level 3 Activate per Policy §9 (CPO escalation + alternate supplier at minimum 40% volume).

---

