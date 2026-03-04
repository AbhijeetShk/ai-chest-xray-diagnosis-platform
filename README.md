# AI Chest X-Ray Diagnosis Platform

An end-to-end **AI-powered clinical decision support system** for detecting **14 thoracic diseases from chest X-ray images** and assisting doctors using **AI agents, retrieval-augmented medical knowledge (RAG), and patient-specific contextual analysis**.

The platform combines **deep learning medical imaging**, **agentic AI workflows**, and **modern full-stack infrastructure** to simulate a real-world **AI-assisted radiology platform**.

Doctors can upload X-ray images, receive **AI predictions with explainability**, retrieve **trusted medical knowledge**, and interact with **patient-specific AI assistants**.

---

# Overview

This system integrates **medical imaging AI**, **AI agents**, and **retrieval-augmented generation (RAG)** into a unified diagnostic platform.

## Workflow

1. Doctor uploads a chest X-ray image  
2. Dockerized AI model performs **multi-label disease detection**  
3. System outputs **top 3 most probable diseases**  
4. **Grad-CAM** generates visual explanations highlighting affected regions  
5. AI agents retrieve disease knowledge from **NIH medical resources**  
6. Patient-specific **RAG pipelines provide contextual insights**  
7. Results appear in a **Next.js clinical dashboard**

Each patient maintains a **dedicated AI knowledge context**, enabling personalized diagnostic insights.

---

# Key Features

## Multi-Disease X-Ray Detection

The system detects **14 thoracic diseases** using a multi-label deep learning model.

Diseases include:

- Atelectasis  
- Cardiomegaly  
- Effusion  
- Infiltration  
- Mass  
- Nodule  
- Pneumonia  
- Pneumothorax  
- Consolidation  
- Edema  
- Emphysema  
- Fibrosis  
- Pleural Thickening  
- Hernia  

The model produces **probability scores for each disease** and returns the **top 3 most likely conditions**.

---

# Model Explainability (Grad-CAM)

To improve transparency and clinical trust, the system integrates **Grad-CAM visual explanations**.

For each prediction:

- The **top 3 predicted diseases** are selected  
- Grad-CAM heatmaps highlight **relevant regions of the X-ray image**  
- Doctors can visually inspect **which areas influenced the model**

This improves **interpretability for clinical decision support systems**.

---

# AI Agent Workflows

The platform uses **Vercel AI SDK** to implement **agent-based medical reasoning pipelines**.

Agents perform tasks such as:

- Retrieving disease information from **NIH datasets**
- Generating contextual medical explanations
- Answering doctor queries about patient results
- Summarizing diagnostic insights

Agents operate within **patient-specific contexts**, enabling personalized medical interactions.

---

# Patient-Specific RAG Models

Each patient has a **dedicated retrieval-augmented knowledge context**.

This enables:

- Patient-specific medical reasoning  
- Context-aware AI explanations  
- Persistent clinical conversation history  
- Personalized retrieval pipelines  

Doctors can **switch between patients**, each with its own **RAG model and knowledge state**.

---

# Multi-Doctor & Multi-Patient Support

The platform supports **multi-user clinical workflows**.

Capabilities include:

- Multiple doctors using the system simultaneously  
- Independent patient records  
- Patient-specific AI assistants  
- Doctor-specific session contexts  
- Secure medical data management  

This architecture simulates a **real hospital diagnostic environment**.

---

# Clinical Dashboard

A **Next.js + TypeScript dashboard** provides an interface for doctors.

Features include:

- Patient management  
- X-ray upload and processing  
- Model predictions and probability scores  
- Grad-CAM visualizations  
- AI medical assistant chat  
- RAG-powered disease explanations  

Doctors can interact with **AI agents to explore diagnostic insights**.

---

# Retrieval Augmented Generation (RAG)

The system integrates **vector databases** to ground AI responses with reliable medical knowledge.

Capabilities:

- Semantic search over disease information  
- Context-aware knowledge retrieval  
- Reduced hallucination risk  
- Evidence-backed AI explanations  

Medical knowledge sources include **NIH disease information**.

---

# System Architecture

```
Doctor Dashboard (Next.js + TypeScript)
        |
        v
Backend API Layer (Node.js + Prisma)
        |
        v
Dockerized AI Model (Chest X-ray CNN)
        |
        v
Prediction Service
        |
        v
PostgreSQL / Supabase
Patient Data + Metadata
        |
        v
Vector Database
Medical Knowledge Index
        |
        v
AI Agents (Vercel AI SDK)
        |
        v
RAG Pipeline
Patient-Specific Context
        |
        v
Doctor Chat Interface
```

---

# Tech Stack

## AI / Machine Learning

- Python  
- Deep Learning (CNN)  
- Multi-label classification  
- Grad-CAM explainability  
- NIH ChestXray14 dataset  

---

## AI Agents & LLM Systems

- Vercel AI SDK  
- Agent-based workflows  
- Retrieval Augmented Generation (RAG)  
- Vector databases  
- Context-aware medical assistants  

---

## Backend

- Node.js  
- TypeScript  
- Prisma ORM  
- REST API architecture  

---

## Frontend

- Next.js  
- TypeScript  
- AI chat interface  
- Clinical dashboards  

---

## Database & Data Layer

- PostgreSQL  
- Supabase  
- Vector databases  
- Patient medical record storage  

---

## Infrastructure

- Dockerized AI inference  
- Containerized model deployment  
- Scalable backend architecture  
- Cloud-ready system design  

---

# AI Model Pipeline

1. Chest X-ray image preprocessing  
2. CNN feature extraction  
3. Multi-label disease classification  
4. Probability scoring  
5. Top-3 disease selection  
6. Grad-CAM heatmap generation  

Evaluation metrics include:

- ROC-AUC  
- Precision / Recall  
- F1 Score  

---

# Example Workflow

Doctor uploads X-ray image  

↓

AI model predicts disease probabilities  

↓

Grad-CAM highlights suspicious lung regions  

↓

AI agents retrieve NIH disease explanations  

↓

RAG contextualizes patient information  

↓

Doctor receives **AI-assisted diagnostic insights**

---

# Repository Structure

```
ai-chest-xray-diagnosis-platform  

backend/
  model, gradCam and docker

frontend/
  app/
  retrieval-agent and patient-context-agent

packages/
  db/
  prisma and prisma accelerate connection pooling
```

---

# Future Improvements

- Integration with hospital EHR systems  
- Federated learning for privacy-preserving training  
- Larger medical knowledge graphs  
- Advanced explainability techniques  
- Cloud-scale deployment  

---

# Research Context

This project explores the intersection of:

- Medical imaging AI  
- Agentic AI systems  
- Retrieval augmented generation  
- Clinical decision support platforms  

---

# License

MIT License
