# 🧠 Mediphas AI – Intelligent Patient Triage System

**Mediphas AI** is a next-generation clinical triage and decision-support platform designed to bridge the gap between patient anxiety and professional medical care using **Hybrid AI Architecture**.

Built for high-impact environments such as hospitals, emergency workflows, and national hackathons, it delivers:

- ⚡ **Real-time Patient Triage** (WebSocket-powered)
- 🧠 **Hybrid AI Intelligence** (Random Forest + Gemini 1.5 Pro)
- 🏥 **Doctor-Prioritized Live Queues**
- 🛡️ **Safety-First Clinical Logic**
- 🎨 **Glassmorphism Healthcare UI**

---

# 🌟 Core Value Proposition

## 🔹 Dual-Perspective Intelligence

Unlike traditional health applications that focus on either patients or doctors, **Mediphas AI unifies both experiences into a single intelligent ecosystem.**

---

## 👤 Patient Experience

- **Instant Symptom Analysis:** Powered by our Rapid Diagnostic Engine.
- **Automated Risk Classification:** Real-time categorization (Normal / Urgent / Critical).
- **Generative Health Insights:** Detailed, context-aware explanations via Gemini AI.
- **Personal Health Dashboard:** Track vitals and history securely.

---

## 🩺 Doctor Experience

- **Live Triage Command Center:** Auto-sorted queues based on severity, not arrival time.
- **AI-Assisted Diagnostics:** Pre-generated clinical summaries for faster decision-making.
- **Real-Time Vitals Monitoring:** Instant WebSocket updates from patient inputs.
- **Population Health Analytics:** Macro-level view of disease trends.

*Critical patients are automatically flagged and prioritized before they even enter the consultation room.*

---

# ⚡ Rapid Diagnostic & Triage Engine

Mediphas AI utilizes a **Hybrid Intelligence Model** to solve the "Dr. Google" problem with precision and speed.

### 1. The Fast Layer (Triage Engine)
A high-performance classifier that provides **sub-millisecond** risk assessment:
- ✅ **Instant Severity Mapping:** (Normal / Urgent / Critical)
- ✅ **Structural Symptom Encoders:** Maps raw inputs to 130+ clinical vectors.
- ✅ **Safety Protocol:** Auto-escalation for high-risk symptoms (e.g., chest pain).

### 2. The Deep Layer (Generative Clinical Core)
Powered by **Google Gemini 1.5 Pro**, this layer handles complex reasoning:
- 🧠 **Contextual Analysis:** Understands patient history nuances.
- 💊 **Pharmacological Safety:** Cross-checks OTC recommendations against contraindications.
- 📝 **Clinical Summarization:** Generates SOAP notes for doctors automatically.

---

# 🏗️ System Architecture

## 🔷 High-Level Architecture Diagram

```mermaid
flowchart TD

    %% User Layer
    A[Patient] -->|HTTPS| B[Frontend - React + TypeScript]
    D[Doctor] -->|HTTPS| B

    %% Frontend Layer
    B -->|REST API| C[FastAPI Backend]
    B -->|WebSocket - Realtime| C

    %% Backend Layer
    C --> E[JWT Authentication]
    C --> F[Service Layer / Controller]
    
    %% Hybrid AI Core
    F --> G[Rapid Diagnostic Engine]
    F --> O[Gemini 1.5 Pro API]
    
    %% Data Persistence
    F --> I[PostgreSQL / Database]

    %% ML Components
    G --> J[RandomForest Classifier]
    G --> K[Label Encoders]
    J --> L[Symptom Vector Space]
    O --> P[Generative Clinical Insights]

    %% Data Layer
    I --> M[(Patient Records)]
    I --> N[(Doctor Priority Queue)]

🧩 Tech Stack & Engineering
🖥 Frontend (Client)
 * Framework: React 18 + TypeScript + Vite
 * Styling: Tailwind CSS (Custom Glassmorphism Design System)
 * State Management: Context API (Auth / Theme / Notifications)
 * Routing: React Router DOM v6
⚙️ Backend (Server)
 * Framework: FastAPI (Python 3.10+) - Async High Performance
 * Real-Time: Native WebSocket Implementation for Live Queues
 * Security: JWT (JSON Web Tokens) + Bcrypt Hashing
 * Architecture: Modular Service-Repository Pattern
🤖 Hybrid AI Layer
 * Triage Model: Scikit-learn Random Forest (Optimized for <10ms latency)
 * Generative Core: Google Gemini 1.5 Pro (via Google AI Studio API)
 * Dataset: Trained on 40+ disease classes and 130+ symptom vectors.
 * Serialization: Joblib optimized model persistence (.pkl)
🚀 Getting Started
1️⃣ Backend Setup
cd triageai-backend
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt

# Configure Environment
# Create a .env file and add your GEMINI_API_KEY

# Train Local Triage Model
python ml/train_model.py

# Start High-Performance Server
uvicorn app.main:app --reload --port 8000

2️⃣ Frontend Setup
cd mediphas-ai-frontend
npm install
npm run dev

🌐 Access Application
Open your browser:
http://localhost:3000

🏆 Why Mediphas AI?
 * True Hybrid AI: Combines the speed of traditional ML with the reasoning of LLMs.
 * End-to-End Pipeline: From patient symptom input to doctor dashboard visualization.
 * Enterprise-Grade Architecture: Separation of concerns, secure auth, and scalable backend.
 * Real-Time Operations: Zero-latency queue updates using WebSockets.
 * Built for Safety: Built-in escalation logic for critical conditions.
🔒 Medical Disclaimer
Mediphas AI is intended for educational, triage assistance, and decision-support purposes only.
It does not replace licensed medical professionals.
Always consult a qualified healthcare provider for medical advice.
👨‍💻 Built By
Ajay Kumar Reddy Full Stack Developer & AI Engineer

