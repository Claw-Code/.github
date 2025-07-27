# 🐾 CLAW Code

**CLAW Code** is an AI-native, developer-first platform designed to supercharge 2D and 3D game development with **Unity** as the primary engine, **Gwen** as the customizable in-game UI toolkit, and **Groq**-powered large language models for real-time code generation and backend logic support.

CLAW empowers game developers to generate, preview, and iterate on gameplay mechanics, UI flows, and backend logic — all with natural language prompts and live coding assistance.

---

## 🧭 Overview

CLAW Code accelerates end-to-end game development by combining a high-performance LLM backend with Unity’s ecosystem and a lightweight in-game UI layer (Gwen). It automates code scaffolding, runtime previews, and deployment workflows for both 2D and 3D games.

**Key Features:**

- AI-powered generation for Unity C# scripts (2D + 3D)
- UI scaffolding with Gwen (Unity-compatible)
- Live preview and code injection inside Unity Editor (via socket bridge)
- Real-time backend simulation using **Groq LLMs**
- Optional multiplayer logic scaffolds

---

## 🎮 Use Cases

- Rapid prototyping of Unity scenes, behaviors, and UI
- LLM-assisted game jam tools
- Education platforms for teaching Unity with AI support
- Real-time logic generation for NPCs, enemy AI, or quest systems
- Backend scripting for save/load systems or event triggers

---

## ⚙️ Architecture

CLAW Code includes the following components:

1. **Unity Frontend**
   - Scene loader and runtime injector
   - Gwen-based in-game UI module
   - Editor bridge (WebSocket or local pipe)

2. **LLM Backend**
   - Hosted on **Groq LPU** or **vLLM**
   - Specialized prompt templates for Unity (2D/3D workflows)
   - Actionable game-specific code suggestions (C#)

3. **Runtime Orchestrator**
   - Code hot-reloader inside Unity
   - Socket-based trigger system to evaluate code in live game sessions
   - Export system to package builds (WebGL, Android, etc.)

4. **Plugin Layer (WIP)**
   - Multiplayer scaffold (Mirror/Netcode for GameObjects)
   - Enemy/AI pattern generator
   - Procedural level scripting

---

## 🖼️ Screenshots

### 🔧 Claw UI Prompt Panel
![Prompt UI](assets/screenshot-ui.png)

### 🎮 Unity Code with Injected Gameplay
![Unity Game Preview](assets/screenshot-unity.png)

### 🧠 LLM Service in Stream Data
![LLM Output](assets/screenshot-llm.png)

---

## 🚀 One-Click Deploy

Once gameplay and logic are finalized:

- Click **Deploy**
- Choose target: WebGL, Windows, Android
- The game is bundled, exported, and optionally hosted (e.g., itch.io, S3)

---

## 🧰 Getting Started

### 1. Clone the Setup Repo

```bash
git clone https://github.com/Claw-Code/Claw-DevEnv
cd Claw-DevEnv
chmod +x setup-claw.sh
./setup-claw.sh
