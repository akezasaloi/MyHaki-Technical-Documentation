# AI Integration Section

## Overview

MyHaki Agent is an AI-powered legal assistant designed to help users access, understand, and summarize legal information with ease. It uses a Retrieval-Augmented Generation (RAG) pipeline that combines Supabase vector search and Google Gemini to deliver accurate, context-aware answers from legal documents.



---

### AI Models

- **Legal-BERT**  
  Specialized BERT model for legal text understanding and embeddings generation  
  `nlpaueb/legal-bert-base-uncased`

- **RAG Pipeline**  
  Retrieval-Augmented Generation for context-aware case processing  
  LangChain + Vector Search

- **Gemini LLM**  
  Advanced language model for classification and reasoning  
  Gemini 2.5 Flash

---

### Data Pipeline Architecture

- Ingestion → Processing → Delivery 

- **Pipeline Stages**  
  1. Collection: Raw case data intake  
  2. Cleaning: Data normalization  
  3. Chunking: Text segmentation  
  4. Embedding: Vector generation  
  5. Storage: Vector database  
  6. Output: Structured results  

---

### AI Models & Technologies

**Core Models:**  
- Legal-BERT: Specialized BERT for legal documents  
- Sentence Transformers: Multipurpose embeddings (`all-mpnet-base-v2`)  
- Gemini 2.5 Flash: Advanced LLM for classification  

**Technology Stack:**  
- LangChain: Framework for RAG apps  
- pgvector: PostgreSQL vector similarity extension  
- Hugging Face: Model hub and transformers library  

---
# Deployment Process

## AI Agent Deployment (FastAPI)

- **Platform:** Google Cloud Platform (Cloud Run, GKE, or Compute Engine)
- **Build:** Dockerized FastAPI microservice
- **Environment Variables:** Managed in Google Cloud Secret Manager
- **Scaling:** Automatic scaling via Google Cloud Run/GKE
- **Monitoring:** Use Google Cloud Monitoring for logs, alerts, and uptime

**Steps**

 - Developers push changes on feature branches and open PRs.  
  - GitHub Actions verify code quality, run tests, lint, and build Docker images upon each push.  
  - After tests are successful, merging into `main` triggers deployment pipelines.  
  - Docker images are pushed to Google Container Registry.  
  - Automatic deployment happens on Google Cloud Run, GKE, or Compute Engine.  
  - Environment variables and secrets are managed securely in Google Cloud Secret Manager.  
  - Monitoring is handled through Google Cloud Monitoring for logs, uptime, and alert notifications to maintain service reliability.  


