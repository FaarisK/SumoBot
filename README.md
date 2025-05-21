# SumoBot
Developed autonomous sumo robot for competitive matches, focusing on optimizing control algorithms, motor efficiency, and sensor integration using ESP32.

---

## ✨ Key Features
| Feature | Description |
|---------|-------------|
| 🔗 **Multi‑source input** | Accepts raw text, local files (`.txt`, `.pdf`, `.md`), or URLs. |
| 🧠 **Hybrid summarization** | Combines an extractive algorithm (TextRank) with an abstractive transformer (T5‑base). |
| 🎛️ **Adjustable length** | `--ratio` or `--sentences` flags let you control summary size. |
| 🌐 **Optional REST API** | `uvicorn sumbot.api:app` starts a FastAPI server <br>→ `POST /summarize` with your payload. |
| 📦 **Zero‑config install** | Pure‑Python; `pip install -r requirements.txt` pulls everything. |

---

## 🛠  Requirements
* Python 3.9+  
* (Optional) CUDA‑capable GPU for faster transformer inference

---

## 🚀  Quick Start

```bash
#cd sumbot

# 2. Install deps
pip install -r requirements.txt

# 3. CLI usage
python sumbot.py "Paste or pipe any long article here"

# 3‑b. Summarize a PDF
python sumbot.py docs/report.pdf --ratio 0.15

# 4. Start API server (optional)
uvicorn sumbot.api:app --host 0.0.0.0 --port 8000
