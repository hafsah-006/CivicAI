# NerfED – Civic AI Assistant
AI for Bharat Hackathon

## 1. Overview

NerfED is a Civic AI Assistant designed to provide:
- Real-time legal guidance
- Traffic & emergency updates
- Geo-fenced proactive alerts
- Verified, citation-backed AI responses
- Multilingual voice interaction

The system combines:
Agentic AI + Hybrid RAG + Validation Layer

---

## 2. High-Level Architecture

The system consists of 5 layers:

1. User Interface Layer
2. Application/API Layer
3. AI Intelligence Layer
4. Data & Knowledge Layer
5. Cloud & Infrastructure Layer

---

## 3. User Interface Layer

Technology:
- React + TailwindCSS
- Multilingual voice & text interface

Features:
- Geo-fenced notifications
- Emergency Rights Mode
- Legal Simplifier
- Civic Tools Dashboard

Interaction Flow:
User → Voice/Text → API Gateway → AI Engine → Verified Response → UI

---

## 4. Application & API Layer

Technology:
- FastAPI
- JWT Authentication
- REST + WebSocket APIs

Responsibilities:
- User authentication
- Request routing
- Civic API integrations
- Rate limiting
- Logging & monitoring

Endpoints:
- /query
- /upload-document
- /geo-alert
- /emergency-mode
- /validate

---

## 5. AI Intelligence Layer

### 5.1 Hybrid RAG Pipeline

Long-Term Memory:
- Constitutional laws
- Legal statutes
- Government circulars

Short-Term Memory:
- Traffic alerts
- Emergency notifications
- Municipal updates

Pipeline:
1. Classify Intent
2. Retrieve Context (Vector DB)
3. Check Real-time Feeds
4. Agentic Workflow:
   - Check Law
   - Check Location
   - Check Time
5. Generate Response
6. Validate via Truth Vault
7. Attach Citation

---

### 5.2 Agentic Orchestration

Agents:
- Legal Agent
- Geo Agent
- Time Agent
- Advisory Agent

The system dynamically decides which agent to trigger.

---

### 5.3 Truth Vault Validation Layer

Purpose:
Prevent hallucination.

Mechanism:
- Cross-reference output with:
  - Verified PDFs
  - Government APIs
- Provide citation in response

If confidence < threshold:
Return: "Insufficient verified data"

---

## 6. Data & Knowledge Layer

Components:

Vector DB:
- Pinecone / Milvus

Structured DB:
- Firestore / PostgreSQL

Storage:
- Government documents
- Civic alerts
- Embeddings

Indexing Strategy:
- Chunk size: 500–1000 tokens
- Metadata tagging:
  - Region
  - Law category
  - Date
  - Source URL

---

## 7. Speech & Multilingual Support

ASR:
- Whisper / Bhashini

TTS:
- Indic language support

Pipeline:
Audio → Transcription → Query → Response → Speech Synthesis

---

## 8. Geo-Fenced Alert Engine

Input:
- GPS coordinates

Process:
- Check restricted zones
- Check emergency radius
- Compare with civic feeds

Output:
Proactive notification before violation.

---

## 9. Emergency Rights Mode

High-priority override mode.

Features:
- Fast legal rights summary
- Offline cached rights
- One-click emergency assistance

---

## 10. Security Architecture

- JWT authentication
- Role-based access control
- API key validation for govt systems
- End-to-end encryption (HTTPS)
- Audit logging

---

## 11. Deployment Architecture

Cloud:
- AWS / Google Cloud

Infrastructure:
- Docker containers
- Kubernetes (optional scaling)
- CI/CD pipeline

Scaling Strategy:
- Horizontal scaling for API
- Separate inference server for LLM
- Caching layer (Redis optional)

---

## 12. Cost Optimization Strategy

- Quantized LLM models
- On-demand inference scaling
- Embedding caching
- Hybrid cloud storage

---

## 13. Future Enhancements

- Fine-tuned Indian legal LLM
- Offline rural edge deployment
- Integration with DigiLocker
- Smart city policy dashboard

---

## 14. USP

✔ Real-time civic intelligence  
✔ Verified AI (anti-hallucination)  
✔ Proactive geo alerts  
✔ Multilingual voice access  
✔ Public Infrastructure Oriented  

---

## 15. Conclusion

NerfED acts as a Digital Civic Infrastructure layer
bridging citizens, law, and real-time civic intelligence
with verified, context-aware AI guidance.
