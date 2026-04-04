<h1 align="center">
  <img src="docs/screenshots/logo.png" alt="Verbatim Studio Logo" width="120"><br>
  Verbatim Studio
</h1>

<p align="center">
  <strong>Your data. Your device. Your rules.</strong>
</p>

<p align="center">
  <a href="#downloads">Downloads</a> •
  <a href="#features">Features</a> •
  <a href="#system-requirements">Requirements</a> •
  <a href="#first-launch">Getting Started</a>
</p>

<p align="center">
  <img src="https://img.shields.io/github/v/release/JongoDB/verbatim-studio-releases?label=version&color=blue" alt="Version">
  <img src="https://img.shields.io/badge/license-AGPL--3.0-green.svg" alt="License">
  <img src="https://img.shields.io/badge/platform-macOS%20%7C%20Windows-lightgrey.svg" alt="Platform">
</p>

<p align="center">
  <img src="docs/screenshots/dashboard-dark.png" alt="Verbatim Studio Dashboard" width="100%">
</p>

---

## Why Verbatim Studio?

Organizations handling confidential information — law firms, medical practices, government agencies, research institutions — face a critical challenge: **cloud transcription services require sending sensitive data to third-party servers.**

Verbatim Studio eliminates this risk entirely. All transcription and AI processing happens locally on your machine. Your files never leave your control.

- **HIPAA-ready** — Patient interviews and medical dictation stay on-premises
- **Legal privilege** — Attorney-client communications remain confidential
- **Government security** — Classified briefings never touch external networks
- **Research ethics** — IRB-protected interviews maintain participant privacy

---

## Downloads

Download the latest release for your platform:

| Platform | Download | Notes |
|----------|----------|-------|
| **macOS** (Apple Silicon) | [Download .dmg](https://github.com/JongoDB/verbatim-studio-releases/releases/latest) | M1/M2/M3/M4 optimized |
| **Windows** (x64) | [Download .exe](https://github.com/JongoDB/verbatim-studio-releases/releases/latest) | NVIDIA GPU optional for faster transcription |

The app is self-contained — no Python, Node.js, or other dependencies required. Just download, install, and run.

### Auto-Updates

Verbatim Studio checks this repository automatically for updates. You'll be notified when a new version is available.

---

## Features

### Transcription That Actually Works

- **OpenAI Whisper accuracy** — State-of-the-art speech recognition running entirely on your device
- **Multi-language support** — Transcribe in 12+ languages with automatic detection
- **Automatic speaker identification** — Know who said what without manual tagging
- **Live transcription** — Real-time speech-to-text from your microphone
- **Video support** — Drop in MP4, MOV, WebM, or MKV files

<p align="center">
  <img src="docs/screenshots/transcript-editor.png" alt="Transcript Editor" width="100%">
</p>

### Max: Your AI Research Assistant

Max isn't just a chatbot — it's a research tool that understands your content:

- **Query across your entire library** — Ask questions that span multiple files and documents
- **Persistent conversations** — Pick up where you left off with saved chat history
- **Document-aware** — Upload PDFs, images, and notes for Max to reference
- **OCR built-in** — Extract text from scanned documents and handwriting
- **Web search** — Pull in current information when you need it

All powered by IBM Granite, running 100% locally. No API keys. No usage limits. No data leaving your machine.

<p align="center">
  <img src="docs/screenshots/ai-assistant.png" alt="Max AI Assistant" width="100%">
</p>

### Find Anything, Instantly

- **Semantic search** — Find content by meaning, not just exact keywords
- **Search everything** — Files, transcripts, documents, notes, and chat history in one place
- **Smart results** — Context snippets with keyword highlighting and semantic match indicators

<p align="center">
  <img src="docs/screenshots/search-semantic.png" alt="Search" width="100%">
</p>

### Professional Editing Tools

- **Clickable timestamps** — Jump to any moment instantly
- **Highlights and bookmarks** — Mark important segments for quick reference
- **Inline annotations** — Add notes directly to transcripts
- **Keyboard-first workflow** — Control playback without leaving your keyboard

### Organize Your Way

- **Projects with custom metadata** — Templates for legal cases, medical records, interviews
- **Bulk operations** — Select multiple files and act on them at once
- **Flexible storage** — Local, network drives, Google Drive, OneDrive, Dropbox
- **Full exports** — TXT, SRT, VTT, DOCX, PDF, or complete backup archives

---

## System Requirements

### Hardware

|  | Minimum | Recommended |
|---|---|---|
| **RAM** | 8 GB | 16 GB+ |
| **Disk** | ~2 GB (base install) | ~8 GB (all AI models) |

### Platform Support

| Platform | Requirement | Notes |
|----------|-------------|-------|
| **macOS** | Apple Silicon (M1/M2/M3/M4) | Optimized for Metal / MLX — Intel Macs not supported |
| **Windows** | x86-64 with 8 GB+ RAM | NVIDIA GPU optional — enables CUDA-accelerated transcription |

### Memory Usage by Feature

Each AI feature loads its own model. Deactivate models in **Settings > AI** to reclaim memory.

| Feature | Memory | Loaded when... |
|---------|--------|----------------|
| App (idle) | ~300 MB | Always |
| Transcription (Whisper base) | +200-300 MB | Transcribing audio/video |
| Speaker ID (pyannote) | +1 GB | Diarization enabled |
| Semantic search (nomic-embed) | +600 MB | Search index active |
| Max assistant (Granite 8B) | +5 GB | AI chat / summaries |
| OCR (Qwen2-VL 2B) | +5 GB | Processing images / scanned PDFs |

---

## First Launch

On first launch, Verbatim Studio will guide you through downloading the AI models you need. Choose what fits your workflow — transcription only, or the full suite with Max and semantic search.

<details>
<summary><strong>macOS: "App is damaged" or "unidentified developer" warning</strong></summary>

The app is not yet code-signed. To open it:

1. **Right-click** (or Control-click) the app and select **Open**
2. Click **Open** in the dialog that appears

Or remove the quarantine attribute via Terminal:

```bash
xattr -c ~/Downloads/Verbatim.Studio-<version>-arm64.dmg
```

</details>

---

## License

Verbatim Studio is licensed under the [GNU Affero General Public License v3.0](LICENSE).

---

<p align="center">
  <a href="https://verbatimstudio.app">verbatimstudio.app</a>
</p>
