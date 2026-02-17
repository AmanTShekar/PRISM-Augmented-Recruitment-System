# PRISM: Autonomous AI Recruitment Protocol 🚀

<div align="center">
  <img src="docs/assets/cover.png" alt="PRISM Banner" width="100%">
  
  <p align="center">
    <img src="https://img.shields.io/badge/Version-1.0.0-blue.svg" alt="Version">
    <img src="https://img.shields.io/badge/License-MIT-green.svg" alt="License">
    <img src="https://img.shields.io/badge/Stack-FastAPI%20%7C%20React%20%7C%20AI-orange" alt="Stack">
    <img src="https://img.shields.io/badge/AI-DeepSeek%20%7C%20MediaPipe%20%7C%20SBERT-red" alt="AI">
    <img src="https://img.shields.io/badge/Database-PostgreSQL%20%7C%20LanceDB-green" alt="Database">
  </p>

  <p align="center">
    <b>The world's first truly autonomous recruitment platform that eliminates human bias through deep reasoning and biometric engagement analysis.</b>
  </p>
</div>

---

## 🌟 Vision & Philosophy

**PRISM** is built on the premise that recruitment is fundamentally broken: biased, unscalable, and expensive. Our protocol replaces superficial keyword matching with **Deep Reasoning**. We understand not just what a candidate knows, but *how they think*.

### Core Value Pillars
- 🛡️ **Zero Bias**: Automated PII obfuscation evaluating candidates purely as anonymous skill vectors.
- 🧠 **Cognitive Intelligence**: Chain-of-Thought reasoning for nuanced technical assessment.
- 👁️ **Sentience Tracking**: High-frequency biometric analysis to measure genuine candidate engagement.
- 🧬 **Semantic Resonance**: 1536d vector alignment between talent and opportunity.

---

## 🧠 Comprehensive AI Engine Specifications

PRISM leverages a state-of-the-art, multi-modal AI stack for total recruitment autonomy:

### 1. Reasoning & Orchestration (The Brain)
- **Engine**: [Ollama](https://ollama.ai/)
- **Models**: `DeepSeek-R1`, `Phi-3.5`, `Llama-3.2 (3B)`
- **Role**: Conducts L8 Chain-of-Thought (CoT) evaluation, generates adaptive interviewer prompts, and performs deep logic verification on coding responses.

### 2. Semantic Resonance (The Matchmaker)
- **Model**: `Sentence-Transformers (SBERT / BGE-M3)`
- **Vector DB**: `LanceDB` (Serverless, Disk-based)
- **Role**: Transforms resumes and job descriptions into high-dimensional embeddings. It identifies "non-obvious" fit patterns (e.g., recognizing that a 'Distributed Systems' expert is a fit for a 'Cloud Architect' role).

### 3. Sentinel System (The Proctor)
- **Framework**: `MediaPipe` + `OpenCV`
- **Landmarks**: 468-point 3D Facial Mesh tracking at 60Hz.
- **Role**: Monitors cognitive load, engagement variance, and authenticity during interviews. Detects proctoring violations (e.g., unauthorized devices) via `YOLOv8n`.

### 4. Audio & Voice Synthesis
- **ASR (Speech-to-Text)**: `Faster-Whisper (Large-v3)` & `Moonshine-Tiny`
- **TTS (Text-to-Speech)**: `Kokoro-v0.19` (High-fidelity neural voice)
- **Role**: Provides a natural, human-like verbal interaction experience with sub-200ms transcription latency.

---

## 🏗️ System Architecture

Managed via **Docker Compose**, the system is orchestrated into specialized microservices:

| Service | Technology | Description |
| :--- | :--- | :--- |
| **Gateway** | FastAPI | Asynchronous high-performance API entry point. |
| **Worker Grid** | Celery + Redis | Handles heavy AI tasks (Transcription, Model Inference). |
| **UI Hologram** | React + Framer Motion | Premium 'Void Black' interface with holographic components. |
| **Cognitive DB** | PostgreSQL | Relational storage for candidate metadata and scoring. |
| **Vector Index** | LanceDB | Low-latency semantic search and retrieval. |
| **Inference Node** | Ollama | Local hosting of GGUF-based Reasoning Models. |

---

## � Getting Started

### 🐳 Deployment via Docker (Recommended)
Docker ensures all C++ and AI dependencies (MediaPipe, SBERT, ONNX) are perfectly linked.

```bash
# Clone the repository
git clone https://github.com/AmanTShekar/PRISM-Augmented-Recruitment-System.git
cd PRISM

# Build the ecosystem
docker-compose up --build
```

### 🧠 Critical: Post-Install Model Pull
As AI models are large (>500MB), they must be pulled after the services start:

1. **Download Local Models** (ONNX/Voices):
   ```bash
   docker-compose exec backend python app/scripts/download_voice_models.py
   ```
2. **Pull Reasoning Models** (Ollama):
   ```bash
   docker-compose exec backend python app/scripts/pull_models.py
   ```

---

## 📊 Key Features & Capabilities

- **Autonomous Screener**: JD entry → Auto-generated criteria → 24/7 AI Interviewing.
- **Sentinel Identity**: 180-degree face verification and liveness detection.
- **Reasoning Reports**: Generates full CoT logic traces for every hiring recommendation.
- **Holographic Resumes**: Interactive, AI-enhanced candidate profile visualizations.
- **Proctoring Suite**: Multi-person detection and screen-sharing integrity verification.

---

## 🗺️ Roadmap 2026

- [x] **Q1: Foundation** - Core bias-free screening & Sentinel v1.
- [ ] **Q2: Intelligence** - DeepSeek-R1 full integration & Multi-language support.
- [ ] **Q3: Scale** - API v1 and Enterprise ATS connectors (Greenhouse/Lever).
- [ ] **Q4: Platform** - White-labeling for recruitment agencies and predictive analytics.

---

## 🎯 Search & Optimization (SEO)
`AI Recruitment System`, `Autonomous Hiring Platform`, `Deep Reasoning Interviewer`, `Sentinel AI Proctoring`, `Sentence-Transformers Matching`, `Machine Learning Recruitment`, `Zero Bias Hiring Protocol`.

---

## 📄 License & Legal
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details. For commercial inquiries, contact [founders@PRISM.ai].

---

<div align="center">
  <p>Built with ❤️ by the PRISM Team</p>
  <p><i>"Defining the next era of autonomous recruitment."</i></p>
</div>

