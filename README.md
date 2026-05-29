 ⚡ NeuroScribe AI

> **Thought-to-Code IDE** — Describe what you want to build in plain English. NeuroScribe translates it into production-ready code with real-time architecture insights, security analysis, and auto-generated README docs.

![Version](https://img.shields.io/badge/version-1.0.0-00ff9d?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-a78bfa?style=flat-square)
![Built With](https://img.shields.io/badge/built%20with-Claude%20AI-00d4ff?style=flat-square)
![Zero Dependencies](https://img.shields.io/badge/dependencies-zero-fbbf24?style=flat-square)

---

## 🎯 What Is This?

NeuroScribe is a **zero-dependency, single-file AI-powered code generation IDE** that runs entirely in the browser.

You type a thought. You get production-quality code.

It's not a chatbot. It's not a wrapper around a playground. It's a complete IDE experience — with a real code editor, syntax highlighting, line numbers, session history, architecture insights, metrics, and README generation — all in one HTML file you can push to GitHub right now.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🧠 **Thought Input** | Describe what you want in plain English |
| 🌐 **8 Languages** | Python, TypeScript, JS, Rust, Go, Java, C++, Bash |
| ⚡ **AI Insights Panel** | Architecture, security, performance, and dependency notes |
| 📋 **Auto README** | One-click GitHub-ready documentation generation |
| 🖥 **Live Code Editor** | Editable output with syntax highlighting + line numbers |
| 📈 **Code Metrics** | Complexity, quality score, function count, token count |
| 💾 **Session History** | Stores last 20 prompts with instant reload |
| ↓ **Export** | Download generated code as a proper source file |
| ⌨️ **Ctrl+Enter** | Keyboard shortcut to generate |
| 🎨 **Terminal UI** | Dark, CRT-inspired design with scanlines and a green glow |

---

## 🚀 Quick Start

**No install. No dependencies. No build step.**

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/neuroscribe.git
cd neuroscribe

# Open directly in browser
open index.html
```

That's it. One file. 

---

## 🔑 API Key

NeuroScribe uses the [Anthropic Claude API](https://console.anthropic.com). The app is designed to run via Claude's artifact/proxy environment, which handles auth automatically.

If running standalone, add your key to the fetch headers:

```javascript
headers: {
  'Content-Type': 'application/json',
  'x-api-key': 'YOUR_ANTHROPIC_API_KEY',
  'anthropic-version': '2023-06-01'
}
```

> ⚠️ Never commit API keys. Use environment variables or a backend proxy for production.

---

## 🛠 Architecture

```
index.html
├── Layout (CSS Grid — topbar, sidebar, editor, insights panel)
├── Thought Input → buildPrompt() → Claude API
├── Code Renderer → highlight() → DOM injection
├── Insights → generateInsights() → JSON parse → cards
├── README Generator → mdToHtml() → preview
└── Session History (in-memory array, last 20 generations)
```

**Key Design Decisions:**
- **Single file** — maximum portability, zero build tooling
- **No frameworks** — vanilla JS, no React/Vue dependency
- **Streaming-ready architecture** — UI designed to drop in streaming with minimal changes
- **Editable output** — `contenteditable` code pane so you can tweak inline

---

## 🎨 UI Highlights

- IBM Plex Mono + Syne typeface pairing
- CRT scanline overlay
- Green phosphor terminal aesthetic
- Syntax highlighting for 8 languages (pure JS, no libraries)
- Shimmer skeleton loaders during generation
- Toast notifications
- Animated status indicators

---

## 📁 File Structure

```
neuroscribe/
└── index.html     ← The entire application (CSS + JS + HTML)
```

---

## 🗺 Roadmap

- [ ] Real-time streaming responses
- [ ] File tree with multi-file generation
- [ ] Git diff view for edits
- [ ] Local storage persistence
- [ ] Custom system prompt builder
- [ ] Share via URL (base64 encoded state)
- [ ] VS Code extension

---

## 📄 License

MIT © 2026 — Free to use, modify, and distribute.

---


