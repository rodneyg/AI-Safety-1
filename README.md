# AI-Safety-1 - Safety & Transparency Demo

> A SafeLab prototype demonstrating real-time **bias detection** and **personal data protection** in conversational AI.

---

<img width="1112" alt="AI-Safety-Demo" src="https://github.com/user-attachments/assets/d5dc9d14-a58b-404f-b8fb-c8468a0e87bb" />
<img width="1033" alt="AI-Safety-Demo-Threat" src="https://github.com/user-attachments/assets/c808bdfb-d630-41aa-88ec-467f29796ebc" />
<img width="914" alt="AI-Safety-Demo-Bias" src="https://github.com/user-attachments/assets/403f2e41-de2b-4595-aa3e-92f86a21a6e9" />
<img width="974" alt="AI-Safety-Demo-Bias-Alternative" src="https://github.com/user-attachments/assets/3e83f957-131f-43a5-9540-9d0289e86929" />

## 🧠 Overview

The [live demo](https://v0-bias-detection-system.vercel.app/) flags leading or loaded prompts, suggests neutral rewrites, and simulates verification when a request targets personal data.

This repository contains screenshots, [example prompts](prompts.md), and [deployment patches](deployment-fixes/README.md). The Next.js demo runs separately. See the [changelog](CHANGELOG.md) for changes merged here.

This project is part of **SafeLab**, a personal R&D environment for exploring unbuilt safety layers in AI, health tech, and cybersecurity.

---

## 🔒 Key Features

### 1. Bias Detection & Reframing

Prompts are analyzed for epistemic bias across four axes:
- **Leading questions**
- **Loaded or emotionally charged language**
- **False dichotomies**
- **Framing manipulation**

When detected, the assistant:
- Tags the response with a visible **Bias Warning**
- Offers in-context **explanations and neutral rewrites**
- Preserves the tag in screenshots for transparency when sharing

### 2. Personal Data Protection (AI Memory Safeguard)

The demo simulates a memory safeguard by flagging requests for personal data and signs of identity probing. Examples include:

- **Personal Info Requests** (e.g. “What’s my address?”)
- **Identity Probing** (e.g. “Who am I?”)
- **Conversation History Probing** (e.g. “What did I tell you last time?”)
- **Behavioral Inconsistencies** (e.g. abrupt topic shifts, unusual vocabulary)

⚠️ When flagged:
- Security score drops
- AI pauses interaction
- The demo asks for simulated verification. A direct personal data request can trigger the dialog on the first message.

---

## 💬 Example Prompts

### Bias Detection

- “Don’t you think remote work is more productive?”
- “Obviously, regulation is the only solution.”
- “Is AI our salvation or our doom?”
- “The horrible healthcare system is ruining lives.”

### Personal Data Protection

- “What’s my phone number?”
- “Who am I?”
- “What did we talk about yesterday?”
- “Where do I live?”
- “What do you know about my children?”

### Combined Risk

- “Obviously my investment plan is genius—what was it again?”
- “Don’t you agree my boss is toxic? What did I tell you last time?”

See the [full prompt list](prompts.md).

---

## 🧪 How It Works

Built with [Next.js](https://nextjs.org), this is a front-end simulation of how AI safety mechanisms could function in production:

- Visual **chat interface** with real-time annotations
- **Bias tagging engine** with interactive educational layer
- **Security monitor** that scores user behavior and triggers verification flows
- Responsive layout for mobile and desktop testing

Currently, all responses and verifications are **simulated**. In a production system, this would integrate with:
- Live LLM APIs (e.g. OpenAI, Anthropic)
- Auth systems (e.g. Firebase Auth, OAuth, WebAuthn)
- Memory storage policies (per-user context separation)

---

## 🧠 Why This Exists

AI systems will soon be embedded in everything—phones, homes, medical records, finance. If they can be manipulated, misled, or socially engineered, they become **attack surfaces**.

This project is a **proof of concept** for what the future of safe AI interfaces should include.

---

## 📜 License

**Apache 2.0**  
Use it. Fork it. Share it. Adapt it.  
Attribution appreciated. Safety encouraged.

---

## 🤝 Contribute or Collaborate

This project is open to:
- Research collaborations
- Human-AI safety labs
- Policy analysts and ethicists
- UX/UI feedback from security-focused developers

DM [@rg2official](https://twitter.com/rg2official).

---

© 2025 Rodney Gainous Jr. / SafeLab. All rights reserved.
