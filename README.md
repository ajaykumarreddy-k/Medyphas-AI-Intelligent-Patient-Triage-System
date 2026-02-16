---

🏆 Mediphas AI

Intelligent Hybrid Clinical Triage & Decision Support System


---

🚨 Problem Statement

Healthcare systems today struggle with:

Overcrowded emergency rooms

Inefficient patient prioritization

Delayed triage decisions

Patients relying on unreliable self-diagnosis sources

Doctors receiving unstructured patient information


Most digital health solutions either:

Use slow LLM-based reasoning

OR use fast but shallow ML classification

Rarely combine both effectively


There is no unified system that balances speed, safety, and deep reasoning.


---

💡 Our Solution

Mediphas AI is a real-time Hybrid AI-powered triage platform that:

⚡ Classifies patient severity in under 10ms

🧠 Generates structured clinical reasoning summaries

🏥 Dynamically prioritizes doctor queues

🔄 Updates dashboards in real-time via WebSockets

🛡️ Enforces medical safety escalation protocols


It bridges the gap between instant triage and doctor-level clinical reasoning.


---

🧠 Core Innovation – Hybrid AI Architecture

Mediphas AI implements a dual-layer intelligence system:


---

🔹 Layer 1 – Rapid Diagnostic Engine (Fast ML Layer)

Random Forest classifier

130+ symptom vector encoding

40+ disease classes

<10ms inference latency

Deterministic risk mapping (Normal / Urgent / Critical)

Automatic escalation for high-risk symptoms



---

🔹 Layer 2 – Deep Clinical Reasoning (LLM Layer)

Powered by Google Gemini 1.5 Pro:

Context-aware patient history understanding

Medication safety cross-check

Contraindication detection

Automated SOAP note generation

Doctor-ready structured summaries


This hybrid approach ensures both speed and intelligence, not one at the cost of the other.


---

🏥 System Workflow

1. Patient inputs symptoms


2. ML engine instantly classifies severity


3. Critical cases are auto-flagged


4. Gemini generates structured clinical insight


5. Doctor dashboard auto-prioritizes queue


6. Real-time updates via WebSocket




---

⚙️ Tech Stack

🖥 Frontend

React 18 + TypeScript + Vite

Tailwind CSS (Glassmorphism UI)

Context API

React Router DOM v6


⚙️ Backend

FastAPI (Python 3.10+)

Native WebSocket implementation

JWT Authentication + Bcrypt hashing

Modular Service-Repository architecture


🤖 AI Layer

Scikit-learn Random Forest

130-dimensional encoded symptom vectors

Joblib model serialization

Gemini 1.5 Pro API integration



---

🚀 Key Features

Real-time patient triage

AI-assisted doctor dashboard

Live severity-based queue reordering

Automated SOAP clinical summaries

Secure JWT authentication

Structured safety escalation logic



---

🔥 Competitive Advantage

Unlike typical hackathon healthcare projects that rely solely on chatbots:

✅ Implements a trained ML triage model

✅ Uses deterministic safety rules

✅ Integrates LLM reasoning responsibly

✅ Supports real-time hospital workflows

✅ Designed for scalability



---

📈 Impact Potential

Reduce triage processing time

Improve critical case prioritization

Decrease doctor cognitive overload

Enable scalable telemedicine deployment

Adaptable to rural and public health systems



---

🛡️ Safety & Disclaimer

Mediphas AI is intended for educational and clinical decision-support purposes only.
It does not replace licensed medical professionals.
Always consult a qualified healthcare provider for medical advice.


---

👨‍💻 Built By

Ajay Kumar Reddy
Full Stack Developer & AI Engineer


---