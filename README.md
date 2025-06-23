<p align="center">
  <img src="assets/logo.svg" alt="Voxtiva Logo" width="200"/>
</p>

# 📱 Voxtiva

**Voxtiva** is an intelligent, offline-first SMS assistant designed to give you control over your inbox with zero compromise on privacy. It cleans clutter, identifies important messages, lets you interact via voice commands, and respects your time and attention — all without ever sending your data to the cloud.

---

## 🔒 Privacy-First Design

Voxtiva is built with privacy as a core principle:

- 📶 **100% Offline:** No internet access required — AI logic, speech recognition, and message analysis all run locally.
- 🔐 **No data collection:** Voxtiva never sends your messages or usage data to any server.
- 🔁 **User-in-control:** You define which categories to delete or keep; nothing happens without your approval.
- 🗑️ **Soft deletion system:** Messages go to a local recycle bin before permanent deletion, ensuring recoverability.

---

## 🧠 Technology Stack

| Layer               | Tools / Libraries                       | Purpose                                 |
|---------------------|------------------------------------------|-----------------------------------------|
| **Frontend**        | React Native (Expo)                      | Cross-platform mobile UI                |
| **AI Logic**        | Python + Scikit-learn / spaCy            | Offline intent classification, filtering |
| **Speech-to-Text**  | [`Vosk`](https://alphacephei.com/vosk/) | Fully offline voice input               |
| **Text-to-Speech**  | `pyttsx3` / native TTS engines           | Voice output from agent                 |
| **Messaging Access**| Android SMS API / Permissions handling   | Read, soft-delete, and categorize SMS   |
| **Storage**         | SQLite or JSON (local)                   | Store preferences, bin, training data   |
| **Automation**      | GitHub Actions (CI/CD)                   | Linting, test flows, and release prep   |

---

## 📂 Folder Structure

```plaintext
voxtiva/
├── app/                   # React Native frontend app (Expo-based)
│   ├── components/        # UI components
│   ├── screens/           # Onboarding, Home, Settings, etc.
│   ├── assets/            # Fonts, images, logos
│   ├── services/          # Native modules, bridge to AI agent
│   └── App.tsx            # Main entry point
│
├── ai_agent/              # Offline AI assistant logic
│   ├── models/            # Custom-trained models (intent/classifier)
│   ├── preprocessing/     # SMS cleaner, tokenizer, feature extractor
│   ├── speech/            # STT and TTS integrations (Vosk, pyttsx3)
│   └── main.py            # Entry point to AI agent
│
├── permissions/           # Android permissions bridge
│   ├── android_manifest/  # Required permission declarations
│   └── permission_utils/  # Runtime handling and fallbacks
│
├── .github/workflows/     # GitHub CI/CD workflow YAMLs
│
├── .gitignore             # Common ignore rules for RN + Python
├── README.md              # Project documentation
└── LICENSE                # Open-source license (MIT recommended)
```

---

## 📖 About

Voxtiva is a passion project exploring how offline AI agents can improve digital hygiene without compromising user privacy. Designed to demonstrate intelligent local automation, Voxtiva empowers users to take back control of their inbox in a secure, transparent, and voice-enabled way.

---

## 📜 License

This project is licensed under the [MIT License](./LICENSE).

