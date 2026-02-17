---

## 🧠 Comprehensive AI Model Specifications

SmartHire integrates a multi-modal AI stack. Below are the specific models and engines that power the platform:

### 1. **Large Language Models (Orchestration & Reasoning)**
*   **DeepSeek-R1 / Phi-3.5**: Used for Deep Reasoning and Chain-of-Thought (CoT) evaluation of candidate answers.
*   **Llama-3.2 (3B)**: Powers the autonomous JD-to-Criteria generator and real-time interviewer prompt engineering.
*   **Ollama**: Acts as the local inference engine for all GGUF-based models.

### 2. **Embedding & Semantic Search (The Resonance Engine)**
*   **BGE-M3 / SBERT**: Generates 1536-dimensional dense vectors. It supports multi-lingual embeddings and cross-lingual resume matching.
*   **LanceDB**: A serverless vector database used to store and query candidate profiles with sub-10ms latency.

### 3. **Computer Vision (The Sentinel System)**
*   **MediaPipe (Face Mesh)**: Real-time tracking of 468 3D facial landmarks.
*   **YOLOv8n**: Used for object detection to ensure interview integrity (detecting multiple people or unauthorized devices).
*   **BlazeFace**: Lightweight face detection for initial bounding box stabilization.

### 4. **Speech & Audio Intelligence**
*   **Faster-Whisper (Large-v3)**: State-of-the-art transcription engine for interview audio.
*   **Kokoro-v0.19**: High-quality, low-latency text-to-speech (TTS) for the AI interviewer's voice.
*   **Moonshine-Tiny**: Ultra-fast, on-device ASR (Automatic Speech Recognition) for real-time interaction feedback.

---

## 🏗️ System Architecture & Services

The platform is built as a sharded microservices architecture managed via **Docker Compose**:

| Service | Technology | Logic Location |
| :--- | :--- | :--- |
| **API Core** | FastAPI | `backend/app/main.py` |
| **AI Workflows** | Celery + Redis | `backend/app/workers/` |
| **Identity/Sentinel** | OpenCV + MediaPipe | `backend/app/services/sentinel_identity.py` |
| **Resume Intel** | SBERT + PyMuPDF | `backend/app/services/pdf.py` |
| **Voice Engine** | ONNX Runtime | `backend/app/services/voice.py` |
| **Vector Search** | LanceDB | `backend/app/db/` |

---

## 🚦 Getting Started

### 🐳 Quick Start with Docker
Docker is the recommended way to run SmartHire. It ensures all dependencies for AI libraries (like Sentence-Transformers and MediaPipe) are correctly configured.

```bash
# Clone the repository
git clone https://github.com/AmanTShekar/SmartHire-Augmented-Recruitment-System.git
cd SmartHire

# Build and start all services (Backend, Frontend, DB, Redis, Ollama)
docker-compose up --build
```
*Note: The first build will take a few minutes as it compiles AI dependencies.*

### 🧠 AI Model Setup
Since AI models are large (>500MB), they are not included in the repository. Run these scripts to populate your `backend/models` folder:

1. **Voice Models** (Kokoro, Moonshine):
   ```bash
   docker-compose exec backend python app/scripts/download_voice_models.py
   ```
2. **LLM Models** (Ollama):
   ```bash
   docker-compose exec backend python app/scripts/pull_models.py
   ```

---

## 🎯 Search & Optimization (SEO)
To find this project easily:
- `AI Recruitment System`
- `Autonomous Hiring Platform`
- `Sentence Transformers Resume Matcher`
- `MediaPipe Interview Analysis`
- `Bias-free AI Hiring`

---

## 📄 License
This project is licensed under the **PolyForm Noncommercial License 1.0.0**.

---

<div align="center">
  <p>Built with ❤️ by the SmartHire Team</p>
  <p><i>"Defining the next era of autonomous recruitment."</i></p>
</div>

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
