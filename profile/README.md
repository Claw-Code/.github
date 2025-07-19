# CLAW Code

**CLAW Code** is an AI-powered, developer-first platform focused on accelerating 2D game development using modern web technologies. Inspired by the capabilities of v0, CLAW Code is built specifically for game creators, educators, and developers who want to generate, preview, and deploy 2D games with minimal friction.

This platform provides framework-specific reasoning, LLM-assisted generation, and instant live coding features — optimized for the **Phaser.js** game engine.

---

## Overview

CLAW Code allows developers to go from idea to working 2D game in seconds. By combining generative AI models with a game-oriented code stack, it automates common game development tasks, scaffolds game structure, and handles deployment — enabling rapid iteration and experimentation.

Key features include:

* AI-driven code generation optimized for **Phaser.js**
* On-the-fly **live code preview** in the browser
* One-click deploy to **static hosts** (e.g., GitHub Pages, Vercel)
* Modular architecture to extend for other game engines in the future
* Code-first workflow with optional visual tools (optional UI builder layer)

---

## Use Cases

* Rapid prototyping for indie game developers
* AI-assisted game jams
* Game dev education, curriculum design, and workshops
* Internal tools and sandbox environments for game logic testing
* Interactive portfolio pieces and code-driven demos

---

## Architecture

CLAW Code is composed of the following layers:

1. **Frontend**

   * Code editor (Monaco/CodeMirror)
   * Live preview panel (Phaser.js runtime with sandboxing)
   * Prompt interface for natural language to code conversion

2. **LLM Core**

   * Fine-tuned model (QLoRA/Mistral variant) for game-specific code generation
   * Integrated prompt templates and contextual parsing

3. **Build & Deploy System**

   * Real-time transpilation using Vite/ESBuild
   * One-click deploy targets (GitHub Pages, Netlify, Vercel)
   * Optional export as ZIP or GitHub repo

4. **Plugin Layer (WIP)**

   * Asset manager (sprites, tilesets)
   * Code actions (e.g., "Add Jump", "Add Enemy AI")
   * Visual scripting (for non-coders)

---

## Example Prompt → Output

**Prompt:**
"Create a 2D platformer with a jumping character, three platforms, and left-right controls using Phaser."

**Generated Code (snippet):**

```js
this.player = this.physics.add.sprite(100, 450, 'dude');
this.cursors = this.input.keyboard.createCursorKeys();

update() {
  if (this.cursors.left.isDown) {
    this.player.setVelocityX(-160);
  } else if (this.cursors.right.isDown) {
    this.player.setVelocityX(160);
  } else {
    this.player.setVelocityX(0);
  }

  if (this.cursors.up.isDown && this.player.body.touching.down) {
    this.player.setVelocityY(-330);
  }
}
```

**Output:**
The game instantly renders in the preview window with live updates.

---

## One-Click Deploy

Once a game is generated and tested in the live preview:

* Click "Deploy"
* Choose a target: GitHub Pages / Vercel / ZIP download
* The project is packaged, built with Vite, and hosted instantly

---

## Getting Started

### 1. Clone the Starter

```bash
git clone https://github.com/Claw-Code/claw-starter
cd claw-starter
npm install
npm run dev
```

### 2. Use the Prompt Interface

```bash
npm run claw
```

Follow CLI instructions or open the in-browser editor.

---

## Model and Infrastructure

CLAW Code currently integrates with a fine-tuned LLM (Mistral or Code Llama variants) hosted using:

* Ollama for local testing
* vLLM for production inference
* Optional: RAG (Retrieval-Augmented Generation) with GitHub repo integration

Inference layer is modular and OpenAI-compatible.

---

## Roadmap

* Plugin support for additional engines (Godot, Kaboom.js)
* Multi-scene game generation
* Visual editor integration
* Multiplayer scaffolds and socket support
* Export to native via Capacitor / Electron (optional)

---

## License

CLAW Code is licensed under the MIT License.

---

## Contributions

We welcome contributors building on top of CLAW’s open infrastructure. Whether you want to improve the prompt system, extend the code generation pipeline, or add support for new engines — feel free to open issues and pull requests.

---

## Maintainers

Built and maintained by the [CLAW Code](https://github.com/Claw-Code) community — a collective of developers passionate about the future of AI-assisted game creation.
