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
   │ Frontend│       │ Backend │      │   AI    │
   │(Nginx + │       │ (Flask) │      │ Service │
   │ Angular)│       │ Port 80 │      │Port 5000│
   └────┬────┘       └────┬────┘      └────┬────┘
        │                 │                │
        │    REST API     │                │
        │  (Port 4999)    │                │
        └──────────┬──────┴────────────────┘
                   │
              ┌────▼──────┐
              │ MongoDB   │
              │Port 27017 |
              └───────────┘
```


## 🔧 Technology Stack Summary

```
📱 Frontend:  Angular 20.3 | TypeScript | Bootstrap 5 | Docker + Nginx
🔌 API:      Flask | Python 3.10 | RESTful v1.0 | JWT Auth
💾 Database: MongoDB 6.x | 11 Collections | Optimized Indexes
🤖 AI:       Vosk STT | Kokoro TTS | LM Studio LLM | NLP Pipeline
⚙️ DevOps:   Docker Compose | Alpine Containers | Health Checks | Bridge Network
```

---

## 🎬 Demo videos

---

#### 🔐 Account Setup & Language Selection Demo
Registration, login, profile setup and language selection

https://github.com/user-attachments/assets/67dbd9ff-601d-4522-8559-aee91e0017d8


### 🏆 **Gamification & Motivation**
- **XP & Level System**: Earn experience points and progress through levels
- **Daily Streaks**: Track consecutive learning days with streak bonuses
- **Leaderboards**: Compete globally or weekly across all languages
- **Daily Challenges**: Language-specific challenges refreshed daily *(infrastructure in place, extensible)*

---

#### 📚 Interactive Lessons Demo
Browse categories, learn vocabulary, track progress, resume lessons

https://github.com/user-attachments/assets/d0890831-0e1b-4bd4-bbdb-21b9f4748d63

## ✨ Features & Capabilities

### 🎓 **Interactive Learning**
- **Structured Curriculum**: Category-based lessons (Food, Health, Colors, Numbers, etc.).
- **Smart Lessons & Quizzes**: Interactive exercises with immediate feedback and word-level progress tracking
- **Resume Anywhere**: Seamless progress saving—pause lessons and pick up exactly where you left off
- **Spaced Repetition**: SM-2 algorithm ensures optimal vocabulary retention with intelligent review scheduling

---

#### 🎤 AI-Powered Practice Range Demo
Talk to AI in real time

https://github.com/user-attachments/assets/ab4d00a2-9020-483c-83bd-87b4dbd49bf3

### 🎤 **AI-Powered Conversation**
- **Real-Time Speech Recognition**: Offline Vosk-powered STT with confidence scoring
- **Intelligent AI Tutor**: 8 themed conversation contexts (casual, restaurant, travel, shopping, business, health, greetings) with LLM-powered responses
- **Native Pronunciation**: Kokoro neural TTS generating human-like audio in real-time
- **Smart Hints**: Grammar-corrected, context-aware hints limited to 60 tokens for clarity
- **Error Analysis**: Real-time classification of mistakes (spelling, grammar, word choice) with correction suggestions
---

#### 🔧 Admin Dashboard & Controls Demo
User management, vocabulary CRUD, system health monitoring, analytics portal

https://github.com/user-attachments/assets/fd2f0a3f-3ea7-4930-8217-d040be6ee3c9

### 🛡️ **Admin Dashboard**
- **User Management**: View learner progress, reset data, manage accounts
- **Vocabulary Management**: Full CRUD with bulk operations and language-specific deletion
- **System Health Monitoring**: Real-time status of STT, TTS, LLM, and Database services
- **Analytics Portal**: Platform-wide engagement and performance metrics
---

#### 🐳 Docker Setup & Deployment Demo
Configuration, container orchestration, deployment instructions

https://github.com/user-attachments/assets/4eb146af-121a-4169-be58-44860eb4f0dc

---

### 🌍 **Multi-Language Support**
- **Spanish & French**: Full support with language-specific models and prompts
- **Expandable Architecture**: Add languages without code changes—integrated language detection and model switching
- **Offline Capable**: Speech models run locally for privacy and zero-latency
---


**LangGo**: Making language learning intelligent, engaging, and accessible for everyone. 🌍📚
