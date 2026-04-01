# ®️ OM AI · JARVIS
### India's First Student-Made On-Mobile AI Assistant
#### DATE :31/03/2026
#### Time : 12:30 Pm IST

<div align="center">

![Version](https://img.shields.io/badge/Version-2.0-blueviolet?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Android%20%7C%20DroidScript-green?style=for-the-badge)
![Made In](https://img.shields.io/badge/Made%20In-India%20🇮🇳-orange?style=for-the-badge)
![Author](https://img.shields.io/badge/Author-Omkareshwar%20Sinha-blue?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)

**भारत का पहला Student-Made On-Mobile AI Assistant**  
*Made entirely on a smartphone, by a student, for everyone.*

</div>

---

## 📖 What is JARVIS?

**OM AI JARVIS** is a fully-featured AI assistant built as a single HTML file that runs inside **DroidScript** (an Android JavaScript IDE). It was created from scratch on a smartphone — no laptop, no server, no team. Just one student, one phone, and a vision to build India's most advanced on-device AI assistant.

> *"India ka pehela on-mobile AI assistant — made by student Omkareshwar Sinha"*

---

## ✨ Features

### 🤖 AI Engine (Multi-Model)
| Model | Type | Needs API Key? |
|-------|------|----------------|
| Pollinations AI | Free Fallback | ❌ No |
| Google Gemini | Smart | ✅ Yes (Free tier available) |
| OpenAI GPT | Premium | ✅ Yes |
| Grok (xAI) | Fast | ✅ Yes |
| OpenRouter | Multi-model | ✅ Yes |
| HuggingFace | Open Source | ✅ Yes (Free) |

- Switch between AI models from **API Manager**
- Add multiple API keys per model — JARVIS rotates them automatically
- Always falls back to **Pollinations** (free, always works offline)

### 🗣️ Voice & Language
- **Indian English** (en-IN) and **Hindi** (hi-IN) TTS support
- Hardware volume buttons control TTS volume
- Auto-mic mode — keeps listening hands-free
- Wake word detection ("Jarvis", "Hey Jarvis", etc.)
- Welcome speech in both English and Hindi on app open

### 📱 Personal Apps (90+ sub-apps)
- **Music Player** — play from any folder path on your device
- **Secure Notes** — password-protected notes with AES encryption
- **Todo / Habits / Reminders / Alarms** — full productivity suite
- **Calendar / World Clock** — time management
- **Finance Tracker** — income, expenses, budgets
- **Flashcards** — AI-powered study cards
- **Clipboard Manager** — multi-item clipboard

### 🌐 Information
- **Weather** — live forecasts
- **News Feed** — latest headlines
- **Dictionary** — definitions with TTS pronunciation
- **System Monitor** — CPU, RAM, battery
- **Browser** — built-in web browser

### 🔧 Tools (30+)
Calculator, Unit Converter, BMI, EMI, QR Generator, Morse Code,
Age Calculator, Tip Calculator, Pincode Lookup, Sunrise/Sunset,
Whiteboard, Color Picker, Pomodoro Timer, Spectrum Visualizer,
Text Tools, Accelerometer, and more.

### 🔒 Security Suite
- **Password Generator** + Breach Checker (HaveIBeenPwned API)
- **Password Manager** — AES-256 encrypted vault
- **AES Encryption/Decryption** tool
- **Hash Calculator** — MD5, SHA-1, SHA-256
- **RSA Key Generator**
- **Steganography** tool
- **OSINT Spydox** — email & phone OSINT (educational)
- **Brute Force Simulator** (educational)
- **Phishing URL Analyzer**
- **CVE Lookup** — vulnerability database
- **OWASP Top 10** guide
- **Metadata Remover**

### 🌐 Network Tools
- IP Geolocation, DNS Lookup, Subnet Calculator
- SSL/TLS Checker, HTTP Request Builder
- HTTP Headers Analyzer, CORS Tester
- Cookie Inspector, Security Headers Audit
- Whois Lookup, Speed Test

### 🤖 Advanced AI Modes
- **Aurora AI** — multi-personality AI chatbot with deep research
- **Ollama AI** — run local LLMs via Ollama
- **JarvisCode** — AI-powered code editor (CodeMirror)
- **Panda Mode** — autonomous agent mode
- **AI Flashcards** — auto-generate study cards
- **AI Excel** — spreadsheet with AI formula help

### 🔌 Extensibility
- **Add Extension** — create custom AI chatbots or JS sub-apps
- **API Manager** — central hub for all API keys
- **Multitask / Intent Manager** — custom voice triggers & Android intents
- **Smart Home** — IoT device control (MQTT/HTTP)

---

## 🛠️ Installation

### Requirements
- Android phone/tablet (Android 6.0+)
- [DroidScript](https://play.google.com/store/apps/details?id=com.smartphoneremote.androidscriptfree) installed

### Steps
1. **Download DroidScript** from Google Play Store
2. **Download** `JARVIS_Fixed_v2.html` from this repository
3. **Copy** the file to `/storage/emulated/0/DroidScript/New/New.html`
   - (Create the `New` folder if it doesn't exist)
4. **Open DroidScript** → tap on the `New` app → tap **Run**
5. **Default password:** `omkareshwar`

> **Tip:** You can rename the folder from `New` to `JARVIS` — just update the path in DroidScript.

---

## 🔑 API Keys Setup

JARVIS works fully offline/free using **Pollinations AI** as default.  
For smarter responses, add API keys:

1. Open JARVIS → tap **☰ Menu** → tap **API Manager**
2. Select the AI model you want
3. Paste your API key and tap **+ Add**
4. Tap the model button to set it as **Active**

### Where to get free API keys:
| Model | Free Key URL |
|-------|-------------|
| Google Gemini | https://aistudio.google.com/app/apikey |
| HuggingFace | https://huggingface.co/settings/tokens |
| OpenRouter | https://openrouter.ai/keys |
| Grok (xAI) | https://console.x.ai |
| OpenAI | https://platform.openai.com/api-keys |

---

## 📁 File Structure

```
DroidScript/
└── New/
    └── New.html          ← Main JARVIS file (this is the whole app!)
```

That's it. One file. Everything is self-contained.

---

## 🐛 Bug Fixes (v2.0)

| # | Error | Fix |
|---|-------|-----|
| 1 | `Unexpected string` at line 7951 | Fixed onclick quote nesting (`data-rid` approach) |
| 2 | `Unexpected string` at line 24420 | Fixed API Manager button quote nesting (`dataset.mk`) |
| 3 | `Cannot read properties of undefined (reading 'concat')` | Fixed spread operator on security audit object |
| 4 | `Unexpected token ';'` at line 24420 | Fixed addKey/removeKey inline handlers |
| 5 | Double `</script>` tag at EOF | Removed duplicate closing tag |

---

## 🆕 New in v2.0

- ✅ **AppLock removed** (was broken, simplified to single password)
- ✅ **API Manager** — full multi-model AI switching with key rotation
- ✅ **Music folder path** — select any local folder for music
- ✅ **Password Breach Check** directly from Password Generator
- ✅ **Welcome speech** in Indian English + Hindi on app open
- ✅ **Hardware volume buttons** control TTS volume
- ✅ **UI scroll fix** — sub-apps no longer disappear after scrolling
- ✅ **Indian English** (en-IN) set as default TTS language
- ✅ **Removed** Traceroute, Port Scanner, IG OSINT, IG Reverse Lookup
- ✅ **OCR camera mode** fixed with proper Tesseract.js guard

---

## 📜 Privacy & Ethics

- All data stays **100% on your device**
- No data is ever sent to any server except when you explicitly use network tools
- Password Breach Check uses **k-anonymity** — only 5 chars of SHA-1 hash are sent
- All security tools are for **educational and authorized use only**
- JARVIS does not collect, store, or transmit any personal data

---

## 👨‍💻 Author

**Omkareshwar Sinha**  
*Student Developer, India*

> This project proves that you don't need a MacBook, a cloud server, or a team to build something amazing. A smartphone and determination is enough.

---

## 📄 License

MIT License — Free to use, modify, and share. Credit appreciated!

---

## 🙏 Acknowledgements

- [DroidScript](https://droidscript.org) — the Android JS IDE that made this possible
- [Pollinations AI](https://pollinations.ai) — free AI API
- [Tesseract.js](https://tesseract.projectnaptha.com) — OCR engine
- [CodeMirror](https://codemirror.net) — code editor
- [Font Awesome](https://fontawesome.com) — icons
- [HaveIBeenPwned](https://haveibeenpwned.com) — breach API

---

<div align="center">
⭐ If you like this project, give it a star! ⭐  
<br>
<i>Made with ❤️ in India 🇮🇳</i>
</div>
