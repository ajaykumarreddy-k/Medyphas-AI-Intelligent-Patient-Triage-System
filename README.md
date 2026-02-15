# Medyphas AI - Next-Gen Medical Intelligence Platform

**Medyphas AI** is a state-of-the-art healthcare platform designed to revolutionize the patient-doctor interaction through Advanced Artificial Intelligence. Built for high-stakes environments like National Hackathons, it bridges the gap between immediate symptom relief and professional medical care in a unified, visually stunning interface.

![Landing Page](preview/landing.png)

## 🌟 Why Medyphas AI? (USP)

### 1. Dual-Perspective Intelligence
Most health apps focus on either the patient (trackers) or the doctor (EHR). **Medyphas AI** integrates both:
- **For Patients:** Immediate anxiety relief through **Quick Fix AI** and automated Triage.
- **For Doctors:** A prioritized **Live Queue** that highlights critical cases before they even walk in the door.

### 2. "Quick Fix" AI Engine
We don't just tell you to "go to the doctor." For non-critical issues (headaches, mild allergies), our custom-trained Machine Learning model provides:
- **Instant Disease Prediction**: Based on your specific symptoms.
- **OTC Medication Recommendations**: Safe, over-the-counter suggestions to manage symptoms immediately.
- **Confidence Scoring**: Keeps users safe by flagging low-confidence predictions for professional review.

### 3. Pixel-Perfect "Glassmorphism" UI
Healthcare software is notoriously ugly. Medyphas AI breaks the mold with a premium, consumer-grade aesthetic featuring:
- **Glassmorphism**: Frosted glass effects for depth and hierarchy.
- **Dark Mode**: Fully supported, eye-strain reducing interface.
- **Fluid Animations**: `animate-in` transitions that make the app feel alive.

---

## 📸 Feature Gallery

### The Patient Experience

#### **1. Quick Fix AI**
*Instant AI recommendations for common symptoms using our custom ML model.*
![Quick Fix AI](preview/quick_fix.png)

#### **2. Smart Triage Assessment**
*Automated risk assessment (Normal/Urgent/Critical) based on vitals and symptoms.*
![Triage Assessment](preview/triage_assessment.png)

#### **3. My Health Dashboard**
*Track vitals and medical history in one place.*
![My Health Dashboard](preview/patient_my_health.png)

#### **4. Secure Sign Up**
*Easy onboarding for new patients.*
![Sign Up](preview/signup.png)

---

### The Doctor Experience

#### **1. Live Patient Queue**
*Real-time prioritized list of incoming patients, sorted by severity.*
![Doctor Queue](preview/doctor_queue.png)

#### **2. AI Diagnostics Suite**
*Deep-dive analysis of patient symptoms to assist in diagnosis.*
![Doctor Diagnostics](preview/doctor_diagnostics.png)

#### **3. Population Analytics**
*Visual insights into hospital performance and patient demographics.*
![Analytics](preview/doctor_analytics.png)

#### **4. Command Center**
*The central hub for medical staff to manage appointments and tasks.*
![Doctor Dashboard](preview/dashboard_doctor.png)

---

## 🏗️ Technical Architecture

Medyphas AI uses a modern, decoupled architecture designed for scale and performance.

```mermaid
graph TD
    User[User (Patient/Doctor)] -->|HTTPS| Frontend
    
    subgraph "Client Side (Frontend)"
        Frontend[React + TypeScript + Vite]
        State[Context API (Auth/Theme)]
        UI[Tailwind CSS (Glassmorphism)]
        Router[React Router DOM]
    end
    
    Frontend -->|REST API + WebSocket| Backend
    
    subgraph "Server Side (Backend)"
        Backend[FastAPI (Python)]
        Auth[JWT Authentication]
        Svc[Service Layer]
    end
    
    subgraph "Intelligence Layer (ML)"
        Model[Scikit-Learn Model]
        Encoder[Label Encoders]
        Data[Symptom Dataset]
    end
    
    Svc -->|Predict| Model
    Svc -->|Transform| Encoder
```

### Client-Side Logic (Frontend)
- **Framework**: Built with `React 18` and `TypeScript` for type safety.
- **State Management**: Uses React `Context API` for global efficient state (Authentication, Theme, Notifications).
- **Styling**: `Tailwind CSS` with custom configuration for colors, shadows (`box-shadow`), and glass effects (`backdrop-filter`).
- **Performance**: Optimized with `Vite` for instant HMR and optimized production builds.

### Server-Side Logic (Backend & ML)
- **Framework**: `FastAPI` provides high-performance, async capabilities.
- **ML Engine**:
    - **Model**: `RandomForestClassifier` (Scikit-learn) trained on a dataset of 40+ diseases and 130+ symptoms.
    - **Persistence**: Models are serialized using `joblib`/`pickle` as `.pkl` files.
    - **`quickfix_model.pkl`**: The core brain that maps symptom vectors to disease predictions.
    - **`label_encoders.pkl`**: Handles the translation of human-readable symptoms into machine-readable tensors.
- **Real-Time**: WebSocket integration for live updates to the Doctor's Queue.

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v16+)
- Python (v3.10+)

### 1. Backend Setup
```bash
cd triageai-backend
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt

# Train the AI Model (Important!)
python ml/train_quickfix.py

# Start the Server
uvicorn app.main:app --reload --port 8000
```

### 2. Frontend Setup
```bash
cd medyphas-ai---intelligence-hub
npm install
npm run dev
```

### 3. Access
Open your browser to [http://localhost:3000](http://localhost:3000).

---

## 🏆 Hackathon Notes
- **Theme**: Healthcare / AI for Good.
- **Innovation**: The "Quick Fix" feature addresses the "Dr. Google" problem by providing safe, AI-vetted advice instead of panic-inducing search results.
- **Completeness**: Full end-to-end flow from Symptom -> Triage -> Diagnosis -> Appointment.

Built with ❤️ by **Ajay**.
# Mediphas-AI-Intelligent-Patient-Triage-System
