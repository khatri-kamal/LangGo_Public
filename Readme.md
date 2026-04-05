# LangGo - AI-Powered Language Learning Platform

A **production-ready, full-stack language learning application** that combines AI, speech recognition, and gamification to help learners master Spanish and French through interactive conversations, intelligent feedback, and data-driven insights.

---

## 📋 Project Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    User (Web Browser)                       │
└──────────────────────────┬──────────────────────────────────┘
                           │
                      HTTP/API
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
   ┌────▼────┐       ┌────▼────┐      ┌────▼────┐
   │ Frontend │       │ Backend  │      │   AI    │
   │(Nginx +  │       │ (Flask)  │      │ Service │
   │ Angular) │       │ Port 80  │      │ Port 5000│
   └────┬─────┘       └────┬─────┘      └────┬─────┘
        │                  │                  │
        │    REST API      │                  │
        │  (Port 4999)     │                  │
        └──────────┬───────┴──────────────────┘
                   │
              ┌────▼──────┐
              │ MongoDB    │
              │ (Port 27017)
              └────────────┘
```

### Services Architecture

| Service | Port | Purpose |
|---------|------|---------|
| **Frontend** | 80 | User interface (Angular + Nginx)
| **Backend** | 4999 | RESTful API (Flask)
| **AI Service** | 5000 | LLM, STT, TTS processing
| **Database** | 27017 | Data persistence (MongoDB)

---

## 🎬 Feature   video

---

#### 🔐 Account Setup & Language Selection
Registration, login, profile setup and language selection



https://github.com/user-attachments/assets/67dbd9ff-601d-4522-8559-aee91e0017d8


---

#### 📚 Interactive Lessons
Browse categories, learn vocabulary, track progress, resume lessons



https://github.com/user-attachments/assets/d0890831-0e1b-4bd4-bbdb-21b9f4748d63


---

#### 🎤 AI-Powered Practice Range
Talk to AI in real time



https://github.com/user-attachments/assets/ab4d00a2-9020-483c-83bd-87b4dbd49bf3

---

#### 🔧 Admin Dashboard & Controls
User management, vocabulary CRUD, system health monitoring, analytics portal


https://github.com/user-attachments/assets/fd2f0a3f-3ea7-4930-8217-d040be6ee3c9



---

#### 🐳 Docker Setup & Deployment
Configuration, container orchestration, deployment instructions


https://github.com/user-attachments/assets/4eb146af-121a-4169-be58-44860eb4f0dc



---

## ✨ Features & Capabilities

### 🎓 **Interactive Learning**
- **Structured Curriculum**: Category-based lessons (Food, Health, Colors, Numbers, etc.) aligned with CEFR proficiency levels (A1-C2)
- **Smart Lessons & Quizzes**: Interactive exercises with immediate feedback and word-level progress tracking
- **Resume Anywhere**: Seamless progress saving—pause lessons and pick up exactly where you left off
- **Spaced Repetition**: SM-2 algorithm ensures optimal vocabulary retention with intelligent review scheduling

### 🎤 **AI-Powered Conversation**
- **Real-Time Speech Recognition**: Offline Vosk-powered STT with confidence scoring
- **Intelligent AI Tutor**: 8 themed conversation contexts (casual, restaurant, travel, shopping, business, health, greetings) with LLM-powered responses
- **Native Pronunciation**: Kokoro neural TTS generating human-like audio in real-time
- **Smart Hints**: Grammar-corrected, context-aware hints limited to 60 tokens for clarity
- **Error Analysis**: Real-time classification of mistakes (spelling, grammar, word choice) with correction suggestions

### 📊 **Real-Time Feedback & Analytics**
- **Performance Scoring**: Instant evaluation of spoken responses with:
  - Similarity scoring (0-100%)
  - Error classification and correction
  - Pronunciation coaching and guidance
- **Progress Dashboard**: Visual analytics including:
  - Pronunciation trends with historical performance
  - Conversation quality scores
  - STT accuracy metrics
  - Personalized learning recommendations
- **Activity History**: Comprehensive session tracking with word mastery progression and spaced repetition scheduling
- **Performance Insights**: Data-driven recommendations for weak areas

### 🏆 **Gamification & Motivation**
- **XP & Level System**: Earn experience points and progress through levels
- **Daily Streaks**: Track consecutive learning days with streak bonuses
- **Leaderboards**: Compete globally or weekly across all languages
- **Achievement Badges**: Unlock awards for mastery milestones *(badge system fully integrated, easily customizable)*
- **Daily Challenges**: Language-specific challenges refreshed daily *(infrastructure in place, extensible)*

### 🌍 **Multi-Language Support**
- **Spanish & French**: Full support with language-specific models and prompts
- **Expandable Architecture**: Add languages without code changes—integrated language detection and model switching
- **Offline Capable**: Speech models run locally for privacy and zero-latency

### 🔐 **Security & Admin Controls**
- **JWT Authentication**: Secure 24-hour session tokens
- **Role-Based Access**: Admin endpoints with protected decorators
- **Audit Logging**: Track user actions and system events
- **Input Sanitization**: XSS and SQL injection prevention across all endpoints
- **Data Privacy**: No audio stored—processed in-memory and discarded

### 🛡️ **Admin Dashboard**
- **User Management**: View learner progress, reset data, manage accounts
- **Vocabulary Management**: Full CRUD with bulk operations and language-specific deletion
- **System Health Monitoring**: Real-time status of STT, TTS, LLM, and Database services
- **Analytics Portal**: Platform-wide engagement and performance metrics

---

## 🏗️ Technical Architecture

### **Frontend Stack**
- **Angular 20.3** (Latest) with TypeScript strict mode
- **Bootstrap 5** + Custom 750+ line CSS Design System
- **State Management**: Angular Signals for reactive, efficient state handling
- **Responsive UI**: WCAG AAA compliant with 44px touch targets
- **Optimized Build**: Multi-stage Docker compilation (~30% smaller bundle)
- **Components**: Skeleton loaders, empty states, toast notifications, confirmation dialogs, mobile navigation

### **Backend Stack**
- **Flask + Python 3** with Blueprint architecture
- **MongoDB 6.x** with optimized indexes across 11 collections:
  - Core: users, vocabulary, lessons, user_progress, activity_history
  - Feedback: lesson_attempts, word_mastery, quiz_responses
  - Analytics: pronunciation_analytics, conversation_quality, stt_metrics
- **30+ RESTful API Endpoints** (v1.0)
- **Real-Time Feedback Engine**: Error classification, mastery tracking, adaptive recommendations
- **Input Validation & Sanitization**: Comprehensive data protection

### **AI Service**
- **Speech-to-Text**: Vosk offline STT (16kHz mono, confidence scoring)
- **Text-to-Speech**: Kokoro neural TTS with stream processing
- **Language Models**: LM Studio compatible (Gemma, Llama, DeepSeek, etc.)
- **NLP Pipeline**: Hint generation, response analysis, pronunciation coaching
- **Audio Quality Detection**: Real-time SNR calculation and noise analysis

### **DevOps & Infrastructure**
- **Docker Compose** orchestration with 4 containerized services
- **Alpine-based Images** for minimal footprint
- **Custom Bridge Network** for secure inter-service communication
- **Health Checks**: Built-in monitoring for all containers
- **MongoDB Persistence**: Volume-backed data durability
- **Environment Management**: Docker Compose vars + .env configuration

---

## 📈 Key Metrics & Performance

| Metric | Value |
|--------|-------|
| **API Endpoints** | 30+ RESTful endpoints |
| **Database Collections** | 11 optimized collections |
| **Supported Languages** | 2 (Spanish, French—Expandable) |
| **Speech Models** | Offline Vosk (No cloud dependency) |
| **Audio Processing** | Real-time with quality detection |
| **Feedback Types** | 7+ error classifications |
| **Gamification Elements** | XP, Streaks, Levels, Badges, Challenges, Leaderboards |
| **Frontend Bundle Size** | ~30% optimized (vs standard Angular) |
| **STT Latency** | <500ms for 10-second clips |
| **TTS Latency** | <2s for 20-word responses |

---

## 🎯 What Makes LangGo Unique

✅ **Privacy-First**: Speech models run locally—no audio sent to cloud services  
✅ **Real-Time Feedback**: Immediate error correction and pronunciation coaching  
✅ **Engaging Gamification**: Streaks, leaderboards, and daily challenges keep you motivated  
✅ **AI-Powered**: LLM-driven conversations with 8 themed contexts  
✅ **Spaced Repetition**: Science-backed SM-2 algorithm optimizes retention  


---

## 🔧 Technology Stack Summary

```
📱 Frontend:  Angular 20.3 | TypeScript | Bootstrap 5 | Docker + Nginx
🔌 API:      Flask | Python 3.10 | RESTful v1.0 | JWT Auth
💾 Database: MongoDB 6.x | 11 Collections | Optimized Indexes
🤖 AI:       Vosk STT | Kokoro TTS | LM Studio LLM | NLP Pipeline
⚙️  DevOps:   Docker Compose | Alpine Containers | Health Checks | Bridge Network
```


---

## 💡 Key Accomplishments

1. **AI Integration**: Seamless STT→LLM→TTS pipeline with <3s end-to-end latency
2. **Real-Time Feedback**: Instant error detection, classification, and correction suggestions
3. **Gamification System**: XP, streaks, leaderboards, and dynamic badge system
4. **Production-Ready**: Containerized, health-checked, monitored, and documented
5. **Type-Safe Code**: TypeScript strict mode + Python type hints across entire codebase
6. **Comprehensive Security**: JWT auth, input sanitization, audit logging, CORS protection


---

**LangGo**: Making language learning intelligent, engaging, and accessible for everyone. 🌍📚
