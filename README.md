# 🚀 ET StorySphere - AI-Native News Intelligence Engine

## 📌 Project Overview

**ET StorySphere** is an AI-powered news intelligence platform that transforms fragmented business news articles into interactive, personalized story experiences. Instead of reading multiple static articles, users explore unified AI-generated stories with timelines, conversations, personalized perspectives, and video explanations.

### 🎯 Core Problem Solved
Business news consumption in 2026 remains stuck in 2005 - static articles, one-size-fits-all feeds, no personalization. ET StorySphere makes this interactive, intelligent, and personal.

### 💡 Core Innovation
**One story. Infinite perspectives.** Same news story transforms based on user type:
- 👨‍🎓 **Student** → Simple, educational explanation
- 👨‍💼 **Investor** → Financial implications and metrics
- 🚀 **Founder** → Strategic opportunities and competitors
- 👔 **CXO** → Executive business impact

---

## 🌟 Key Features

### 1. **Personalized Story Feed**
- Multi-persona AI that adapts content for each user type
- Interest-based filtering
- Dynamic content relevance

### 2. **Story Intelligence Engine**
- Converts multiple articles → single unified narrative
- Generates summaries, insights, and context automatically

### 3. **Interactive Timeline**
- Visualize how stories evolve over time
- Highlight key milestones and turning points
- Sentiment tracking per event

### 4. **AI Conversational Navigator**
- Ask anything about the story (RAG-powered Q&A)
- Context-aware responses with source citations
- Maintain conversation history

### 5. **AI Video Explainer**
- Auto-generate 60-90 second broadcast-quality videos
- AI narration with TTS
- Visual data representations

### 6. **Vernacular Support**
- Support for Tamil, Hindi, Telugu, Bengali
- Cultural context adaptation (not literal translation)
- Regional language preferences

### 7. **Sentiment & Prediction Engine**
- Track sentiment shifts across events
- Predict "What Next?" - AI-powered future outlook
- Identify contrarian perspectives

---

## 🏗️ System Architecture

### High-Level Flow
```
Raw Articles ↓
Data Ingestion ↓ Story Clustering ↓ Knowledge Graph ↓ Timeline
    ├→ Persona Summaries ├→ RAG Q&A ├→ Video ├→ Sentiment
Orchestration ↓ Frontend UI ↓ ET StorySphere Experience
```

### Technology Stack

#### Backend
- **Framework**: FastAPI + Uvicorn
- **Database**: MongoDB + PostgreSQL
- **Vector DB**: Chroma or FAISS
- **AI/LLM**: OpenAI GPT-4, Claude, Gemini
- **Orchestration**: LangChain + LangGraph

#### Frontend
- **Framework**: React 18 + Next.js 14
- **Styling**: Tailwind CSS
- **Visualization**: D3.js + Chart.js

#### AI/ML
- **Embeddings**: Sentence Transformers
- **NLP**: Spacy + NLTK
- **Clustering**: Scikit-learn
- **Video**: MoviePy + OpenCV
- **TTS**: Edge-TTS
- **Translation**: Deep-Translator

---

## 📁 Project Structure

```
et-storysphere/
├── backend/                  # Python FastAPI backend
│   ├── ai_modules/          # 10 processing phases
│   ├── routes/              # API endpoints
│   ├── services/            # Business logic
│   └── database/            # DB layer
├── frontend/                # React/Next.js frontend
│   └── src/
│       ├── pages/           # Routes
│       ├── components/      # UI components
│       └── services/        # API calls
├── data/                    # Data storage
├── config/                  # Configuration
├── tests/                   # Test suite
└── docs/                    # Documentation
```

See [PROJECT_STRUCTURE.md](PROJECT_STRUCTURE.md) for complete structure.

---

## 🚀 Quick Start

### Prerequisites
- Python 3.9+
- Node.js 18+
- MongoDB
- API Keys: OpenAI

### Installation
```bash
# Setup virtual environment
python -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
cd frontend && npm install && cd ..

# Configure environment
cp .env.example .env
# Edit .env with your API keys

# Initialize database
python scripts/database/seed_sample_data.py

# Run application
# Terminal 1: Backend
uvicorn backend.main:app --reload

# Terminal 2: Frontend
cd frontend && npm run dev
```

**Access**:
- Frontend: http://localhost:3000
- Backend API: http://localhost:8000
- API Docs: http://localhost:8000/docs

---

## 📚 10 Processing Phases

| Phase | Name | Purpose |
|-------|------|---------|
| 1 | **Data Ingestion** | Collect articles from APIs/sources |
| 2 | **Story Clustering** | Group similar articles into stories |
| 3 | **Knowledge Graph** | Extract entities, events, relationships |
| 4 | **Timeline** | Sort events chronologically with milestones |
| 5 | **Persona Engine** | Generate 4 role-specific summaries |
| 6 | **RAG Q&A** | Context-aware conversational AI |
| 7 | **Video Generation** | Auto-generate explainer videos |
| 8 | **Sentiment Analysis** | Track sentiment & predict futures |
| 9 | **Translation** | Localize to regional languages |
| 10 | **Orchestration** | Integrate all outputs seamlessly |

---

## 🎯 API Endpoints

### Stories
```
GET    /api/stories              # List stories
GET    /api/stories/{id}         # Get story detail
```

### Personalization
```
GET    /api/stories/{id}/summary/{persona}
GET    /api/stories/{id}/timeline
WS     /ws/chat/{story_id}       # Real-time chat
```

### Multimedia
```
GET    /api/stories/{id}/video
POST   /api/translate
```

Full API docs: [docs/API.md](docs/API.md)

---

## 📊 Development Status

### ✅ Core Features (100% for Hackathon)
- Story clustering & processing
- Timeline visualization
- Persona-based summaries (2+ personas)
- Chat interface
- Polished UI/UX

### 🔄 Enhancement Features (50%)
- Video generation (script ready, mock video)
- Vernacular translation (1-2 languages)
- Prediction engine

### ❌ Out of Scope
- Production deployment
- Real-time scraping
- Full recommendation system

---

## 🧪 Testing

```bash
# Run all tests
pytest

# With coverage
pytest --cov

# Frontend tests
cd frontend && npm test
```

---

## 📚 Documentation

| Document | Purpose |
|----------|---------|
| [PROJECT_STRUCTURE.md](PROJECT_STRUCTURE.md) | Complete folder structure |
| [DEPENDENCIES_GUIDE.md](DEPENDENCIES_GUIDE.md) | All dependencies explained |
| [docs/API.md](docs/API.md) | API specification |
| [docs/SETUP_GUIDE.md](docs/SETUP_GUIDE.md) | Setup instructions |
| [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) | System design |

---

## 💼 Use Cases

### For Students
- Learn business concepts from real news
- Simplified, educational summaries
- understand context and impact

### For Investors
- Track portfolio-relevant stories
- Financial metrics and implications
- Market sentiment analysis

### For Founders
- Monitor competitors and funding news
- Identify strategic opportunities
- Track industry trends

### For Executives
- Executive-level business briefings
- Strategic decision support
- Predictive insights

---

## 🎥 Demo (2 Minutes)

1. **Story Selection** - Browse available stories
2. **AI Summary** - See unified summary instead of multiple articles
3. **Interactive Timeline** - Explore story evolution
4. **Ask AI** - Get context-aware answers
5. **Persona Switch** - See from Investor perspective
6. **Video Explainer** - Watch auto-generated video
7. **Regional Language** - Switch to Tamil/Hindi
8. **Conclusion** - Information → Intelligence

---

## 🏆 Key Innovation Points

✅ **Story-centric** not article-based
✅ **Multi-persona AI** adapts automatically
✅ **Multimodal** text + chat + video + timeline
✅ **End-to-end platform** not just features
✅ **AI-native** every component uses intelligence
✅ **Demo-ready** smooth presentation

---

## 🤝 Contributing

See [docs/CONTRIBUTING.md](docs/CONTRIBUTING.md)

---

## ⚖️ License

MIT License

---

**Status**: ✅ Hackathon Ready | 🎯 In Active Development | 🚀 Ready to Demo

*ET StorySphere - Transforming news from static reading into intelligent exploration*
