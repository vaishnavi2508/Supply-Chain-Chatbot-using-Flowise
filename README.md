# SCM Assistant - Supply Chain RAG Chatbot

## Public Chatbot URL

https://cloud.flowiseai.com/chatbot/535b01ae-a5fe-4766-90f1-845741d73664

---

## Overview

SCM Assistant is a Retrieval-Augmented Generation (RAG) chatbot built using Flowise AI.  
The chatbot answers questions related to supplier governance, supplier performance, disruption risks, compliance rules, and procurement policies using the provided CSV and PDF datasets.

---

## Tech Stack

- Flowise AI
- Pinecone Vector Database
- Groq LLM Connector
- HuggingFace Embeddings

### LLM Used
- `llama-3.3-70b-versatile`
- Temperature: `0.9`

### Embedding Model Used
- `sentence-transformers/all-MiniLM-L6-v2`

---

## Data Sources

### 1. supplier_performance_data.csv
Contains:
- Supplier performance metrics
- On-time delivery rates
- Defect rates
- Compliance scores
- Disruption flags
- Purchase order values
- Supplier tier information

### 2. SupplyChain_Governance_Policy_v3.2.pdf
Contains:
- Supplier governance policies
- SLA thresholds
- Risk management procedures
- Audit rules
- Diversification rules
- Disruption response policies

---

## Vector Database Configuration

### Pinecone Configuration
- Vector Type: Dense
- Dimension: 384
- Similarity Metric: Cosine

---

## Chunking Experiments

### Configuration 1 (Final Configuration Used)

#### CSV Configuration
- Default row-wise chunking
- Total Chunks: `2000`

#### PDF Configuration
- Text Splitter: Token Text Splitter
- Chunk Size: `500`
- Chunk Overlap: `80`
- Total Chunks: `13`

---

## Chatflow Architecture

```text
Groq Chat Model
        ↓
Conversational Retrieval QA Chain
        ↑
Pinecone Vector Store Retriever
