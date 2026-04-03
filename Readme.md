```markdown
# OM AI JARVIS - Android AI Assistant Built on a Smartphone

⚡ India's first AI assistant coded entirely on a mobile phone. Offline-capable voice assistant with 90+ features, built by a student using DroidScript & AI collaboration.

---

[![Version](https://img.shields.io/badge/version-2.0-blue.svg)](https://github.com/omkareshwarsinha6-jpg/Assist/releases)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Android%209+-brightgreen.svg)](https://developer.android.com)
[![Made With](https://img.shields.io/badge/built%20with-DroidScript-orange.svg)](https://droidscript.org)
[![Status](https://img.shields.io/badge/status-beta-yellow.svg)](https://github.com/omkareshwarsinha6-jpg/Assist/issues)

> **"No laptop. No server. No team. Just one student, one broken phone, and a vision."**  
> — Omkareshwar Sinha, 17, India

---

## 📋 Table of Contents

- [Features](#features)
- [Demo](#demo)
- [Installation](#installation)
- [Quick Start](#quick-start)
- [AI Models](#ai-models)
- [Architecture](#architecture)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

---

## 🚀 Features

### Core AI Engine
- **Multi-Model Support**: Pollinations AI (free), Gemini, OpenAI, Grok, OpenRouter, HuggingFace
- **True Offline Mode**: Ollama integration for local LLM execution (no internet required)
- **Voice Interface**: Indian English (en-IN) & Hindi TTS/STT with wake word detection
- **Smart Fallback**: Auto-rotates API keys, falls back to free tier when limits hit

### 90+ Built-in Tools

| Category | Tools |
|----------|-------|
| **Productivity** | Secure Notes, Todo, Habits, Reminders, Calendar, Finance Tracker |
| **Media** | Music Player (folder-based), Clipboard Manager, Flashcards |
| **Utilities** | Calculator, Unit Converter, QR Generator, Pomodoro, Whiteboard |
| **Security** | Password Manager, AES Encryption, Hash Calculator, Breach Checker |
| **Network** | IP Geolocation, DNS Lookup, SSL Checker, HTTP Inspector |
| **Development** | Code Editor (CodeMirror), AI Excel, API Manager |

### What Makes It Different

| Feature | OM AI JARVIS | Other Assistants |
|---------|--------------|------------------|
| **Build Environment** | Coded entirely on Android phone | Requires laptop/PC |
| **Offline AI** | Local Ollama integration | Cloud-only |
| **Cost** | 100% free with Pollinations | Paid subscriptions |
| **Size** | Single HTML file (~500KB) | Multi-GB installations |
| **Privacy** | Data stays on device | Cloud processing |
| **Open Source** | Full source available | Proprietary |

---

## 🎬 Demo

![OM AI JARVIS Interface - Voice-controlled AI assistant with Indian English support](demo-screenshot.png)

*Main interface showing voice chat, quick tools grid, and API manager*

**Video Demo**: [YouTube - OM AI JARVIS Walkthrough](https://youtube.com/your-link-here)

---

## 📦 Installation

### Requirements
- Android 9.0+ (API level 28+)
- [DroidScript IDE](https://play.google.com/store/apps/details?id=com.smartphoneremote.androidscriptfree) (free, 15MB)
- 50MB storage space
- Optional: [Ollama Android](https://github.com/ollama/ollama-android) for offline AI

### Step-by-Step Setup

```bash
# 1. Install DroidScript from Play Store
# Search: "DroidScript" → Install → Open

# 2. Download JARVIS
# Option A: Download ZIP from GitHub releases
# Option B: Clone with Termux (advanced users)

# 3. Place file in correct directory
/storage/emulated/0/DroidScript/New/New.html

# 4. Launch
# Open DroidScript → Tap "New" folder → Tap "Run" ▶️

# 5. Default password: omkareshwar
# Change this on first launch in Settings
```

First-Time Configuration

```javascript
// Open API Manager from menu
// Add your keys (all optional - Pollinations works free):

GEMINI_API_KEY=your_key_here      # aistudio.google.com
OPENAI_API_KEY=your_key_here      # platform.openai.com
HF_API_KEY=your_key_here          # huggingface.co/settings/tokens
```

---

⚡ Quick Start

1. Voice Command (Hands-Free)

```text
"Jarvis, set reminder for 5 PM"
"Jarvis, play music from Download folder"
"Jarvis, what's the weather in Mumbai?"
```

2. Coding Mode

```javascript
// Tap "JarvisCode" → New File → Select language
// Supported: JavaScript, Python, HTML, CSS

// AI-assisted coding:
// 1. Write function stub
// 2. Tap "AI Help" (Ctrl+Space)
// 3. Select "Complete function" or "Debug this"
```

3. Offline AI (Ollama)

```bash
# Requires Ollama Android app installed separately
# JARVIS auto-detects localhost:11434

# In chat, select "Ollama" from model dropdown
# First download: llama3.2, mistral, or codellama
```

---

🤖 AI Models Reference

Model	Speed	Quality	Cost	Offline	
Pollinations	Fast	Good	Free	❌	
Gemini Flash	Fastest	Excellent	Free tier	❌	
GPT-4o	Medium	Best	Paid	❌	
Ollama (local)	Slow-Good	Good	Free	✅	
Grok	Fast	Good	Paid	❌	

Recommendation: Use Pollinations for daily tasks, Gemini for complex queries, Ollama when offline.

---

🏗️ Architecture

```
┌─────────────────────────────────────────┐
│           DroidScript Container         │
│  ┌─────────────────────────────────┐   │
│  │      WebView (UI Layer)         │   │
│  │  ┌─────────────────────────┐    │   │
│  │  │   HTML/CSS/JS App       │    │   │
│  │  │   - Chat Interface        │    │   │
│  │  │   - Tool Modules          │    │   │
│  │  │   - localStorage DB       │    │   │
│  │  └─────────────────────────┘    │   │
│  └─────────────────────────────────┘   │
│              ↑↓ Execute()               │
│  ┌─────────────────────────────────┐   │
│  │   Native Bridge (Assist.js)     │   │
│  │   - Orientation lock            │   │
│  │   - Permission handling         │   │
│  │   - TTS volume control          │   │
│  └─────────────────────────────────┘   │
└─────────────────────────────────────────┘
                    ↓
┌─────────────────────────────────────────┐
│   External APIs (Internet required)     │
│   pollinations.ai, googleapis.com, etc. │
└─────────────────────────────────────────┘
```

Key Technical Details:
- Frontend: Vanilla JavaScript, Tailwind CSS, Font Awesome
- Storage: Browser localStorage (encrypted for sensitive data)
- AI APIs: RESTful fetch() calls with fallback chaining
- Security: AES-256 for passwords, SHA-256 for hashes, client-side only

---

📚 Documentation

User Guides
- [Getting Started Guide](docs/getting-started.md) - First 10 minutes
- [Voice Commands Reference](docs/voice-commands.md) - Complete command list
- [API Setup Tutorial](docs/api-setup.md) - Configure Gemini, OpenAI, etc.
- [Offline Mode Setup](docs/ollama-setup.md) - Run AI without internet

Developer Docs
- [Architecture Overview](docs/architecture.md) - How it works under the hood
- [Adding New Tools](docs/extending.md) - Create custom sub-apps
- [DroidScript API Reference](docs/droidscript-api.md) - Native bridge methods

Real-World Use Cases

Case 1: Student Study Assistant

```javascript
// 1. Upload PDF notes via File Manager
// 2. Use AI Flashcards to auto-generate Q&A
// 3. Set Pomodoro timer for focused sessions
// 4. Voice-query definitions while studying
```

Case 2: Field Technician

```javascript
// Offline scenario - no signal at site:
// 1. Pre-download Ollama model at home
// 2. Use QR Generator for equipment IDs
// 3. Secure Notes for access codes (encrypted)
// 4. Unit Converter for measurements
```

Case 3: Privacy-Conscious User

```javascript
// No data leaves device:
// 1. Disable all cloud APIs in API Manager
// 2. Use only Ollama (local AI)
// 3. Password Manager with AES encryption
// 4. Metadata Remover before sharing files
```

---

🤝 Contributing

We welcome contributions, especially from:
- DroidScript developers - Native Android feature integration
- UI/UX designers - Better mobile interface
- Translators - Hindi, Tamil, Telugu language support
- Security researchers - Audit encryption implementations

How to Contribute

1. Fork the repository
2. Create branch: `git checkout -b feature/amazing-feature`
3. Commit: `git commit -m 'Add amazing feature'`
4. Push: `git push origin feature/amazing-feature`
5. Open Pull Request - Describe what and why

Good First Issues

- [#1] Add Tamil language support for TTS
- [#2] Improve music player playlist UI
- [#3] Add dark mode toggle persistence
- [#4] Optimize localStorage encryption performance

See [Issues](https://github.com/omkareshwarsinha6-jpg/Assist/issues) labeled `good first issue`.

Code of Conduct

Be respectful. This project was built under difficult circumstances - prioritize constructive feedback over criticism.

---

📜 License

MIT License - See [LICENSE](LICENSE) for full text.

You are free to:
- Use commercially or personally
- Modify and distribute
- Create derivative works

Conditions:
- Include original copyright notice
- State changes made to the code
- Small credit appreciated: "Based on OM AI JARVIS by Omkareshwar Sinha"

---

🙏 Acknowledgments

Tools & Libraries
- [DroidScript](https://droidscript.org) - The Android JavaScript IDE that made mobile development possible
- [Pollinations AI](https://pollinations.ai) - Free, no-signup AI API
- [CodeMirror](https://codemirror.net) - Browser-based code editor
- [Tesseract.js](https://tesseract.projectnaptha.com) - OCR engine
- [Font Awesome](https://fontawesome.com) - Icon library

People
- Claude (Anthropic) - AI pair programmer for code generation and debugging
- DroidScript Community - Forum support for native Android bridging
- Open Source Contributors - Libraries that power this project

Personal Note

> "When you have nothing, you have nothing to lose. This project was born from limitation - a broken phone, no support system, and the stubborn refusal to accept that you need expensive tools to build something meaningful. If you're reading this with limited resources, know that you can still create. Start where you are. Use what you have. Do what you can."

---

🔗 Connect

- GitHub: [@omkareshwarsinha6-jpg](https://github.com/omkareshwarsinha6-jpg)
- Issues: [Report bugs here](https://github.com/omkareshwarsinha6-jpg/Assist/issues)
- Discussions: [Ask questions](https://github.com/omkareshwarsinha6-jpg/Assist/discussions)

Made with determination in India 🇮🇳

---
<!-- SEO Keywords: Android AI assistant, offline voice assistant, DroidScript app, mobile-first development, student-built AI, Pollinations AI client, Ollama Android, Indian English TTS, privacy-focused assistant, single-file web app, no-laptop coding, resource-constrained development, open source AI assistant, Android JavaScript IDE, on-device AI, voice-controlled automation, mobile IDE development, teen developer India, broken phone coding, democratized AI tools -->
'''
