<div align="center">
  <img src="docs/assets/cover.png" alt="SmartHire Banner" width="100%">
  
  <h1>SmartHire 🚀</h1>
  <p><b>The Future of Autonomous Recruitment Protocol</b></p>

  <p>
    <img src="https://img.shields.io/badge/Version-1.0.0-blue.svg" alt="Version">
    <img src="https://img.shields.io/badge/License-PolyForm%20Noncommercial-blueviolet.svg" alt="License">
    <img src="https://img.shields.io/badge/Stack-FastAPI%20%7C%20React%20%7C%20AI-orange" alt="Stack">
    <img src="https://img.shields.io/badge/AI-MediaPipe%20%7C%20Whisper%20%7C%20L8%20CoT-red" alt="AI">
  </p>

  <p align="center">
    <i>"Hire on Merit. Scale on AI. Built for the Next Generation of Talent."</i>
  </p>
</div>

---

## 🌟 Vision
**SmartHire** is a truly autonomous AI recruitment platform designed to eliminate human bias and identify top-tier talent through deep reasoning. We're moving beyond simple keyword matching to understanding *how* candidates think and solve problems.

## 🛠️ Core Technology Pillars

### 1. 🛡️ Zero Bias Protocol (PII Obfuscation)
Evaluates candidates purely as anonymous skill vectors. All Personally Identifiable Information (PII) is stripped at ingestion to ensure a 100% merit-based evaluation process.

### 2. 🧠 Deep Reasoning Engine
Powered by **L8 Chain-of-Thought (CoT)** analysis, our engine evaluates candidate responses by tracing their logic, not just checking for keywords. It understands context, complexity, and problem-solving depth.

### 3. 👁️ Sentinel System (Biometric Analysis)
Leveraging **MediaPipe**, Sentinel tracks 468 facial landmarks at 60Hz during interviews to measure genuine engagement, cognitive load, and authenticity, ensuring an objective assessment of soft skills.

### 4. 🧬 Resonance Engine (Semantic Matching)
High-dimensional vector embeddings (**BGE-M3**) create a 'resonance' between candidate profiles and job requirements, discovering non-obvious fit patterns that human recruiters often miss.

---

## 🚀 Key Features

- 🤖 **Autonomous Screening**: JD-to-Criteria generation and initial AI-led interviews.
- 💻 **Technical Assessment**: Real-time coding challenges with deep logic evaluation.
- 🎤 **Audio/Video Intelligence**: Seamless transcription (Faster-Whisper) and behavioral analysis.
- 📊 **Insight Dashboard**: Real-time hiring metrics, bias detection reports, and quality-of-hire predictions.
- ⚡ **Neural Architecture**: Sharded interview processing for infinite horizontal scalability.

---

## 🏗️ Technical Stack

| Component | Technology |
| :--- | :--- |
| **Backend** | [FastAPI](https://fastapi.tiangolo.com/), [PostgreSQL](https://www.postgresql.org/), [Redis](https://redis.io/) |
| **Frontend** | [React](https://reactjs.org/) + [Vite](https://vitejs.dev/), [Tailwind CSS](https://tailwindcss.com/), [Framer Motion](https://www.framer.com/motion/) |
| **AI/ML** | [MediaPipe](https://mediapipe.dev/), [Faster-Whisper](https://github.com/guillaumekln/faster-whisper), [Sentence-Transformers](https://www.sbert.net/) |
| **Processing** | [Celery](https://docs.celeryq.dev/en/stable/) + [RabbitMQ/Redis](https://redis.io/) |
| **Ops** | [Docker](https://www.docker.com/), [Docker Compose](https://docs.docker.com/compose/) |

---

## 🚦 Getting Started

### 📦 Quick Start with Docker
The fastest way to get SmartHire running is via Docker Compose. This will orchestrate the database, redis, AI workers, and the frontend.

```bash
# Clone the repository
git clone https://github.com/AmanTShekar/SmartHire-Augmented-Recruitment-System.git
cd SmartHire

# Build and start all services
docker-compose up --build
```

### 🧠 AI Model Setup
Since AI models are large (>500MB), they are not included in this repository. You must download them after setting up the environment:

#### **Automated Download**
1. **Voice Models** (Kokoro, Moonshine):
   ```bash
   cd backend
   python app/scripts/download_voice_models.py
   ```
2. **LLM Models** (Ollama):
   ```bash
   # Ensure Ollama is running (or via Docker)
   python backend/app/scripts/pull_models.py
   ```

### 🔨 Manual Setup

#### **Backend**
1. Navigate to `backend/`
2. Create virtual environment: `python -m venv venv`
3. Install dependencies: `pip install -r requirements.txt`
4. Run: `python app/scripts/download_voice_models.py`
5. Start: `uvicorn app.main:app --reload`

#### **Frontend**
1. Navigate to `frontend/`
2. Install dependencies: `npm install`
3. Start dev server: `npm run dev`

---

## 🗺️ Roadmap 2026

- [x] **Q1: Foundation** - Core bias-free screening & Sentinel v1.
- [ ] **Q2: Intelligence** - DeepSeek-R1 Integration & Multi-language support.
- [ ] **Q3: Scale** - API v1 and Enterprise ATS connectors.
- [ ] **Q4: Platform** - White-labeling and Predictive Hiring Analytics.

---

## 📄 License
This project is licensed under the **PolyForm Noncommercial License 1.0.0**. See [LICENSE](LICENSE) for details.


---

<div align="center">
  <p>Built with ❤️ by the SmartHire Team</p>
  <p><i>"Defining the next era of autonomous recruitment."</i></p>
</div>
