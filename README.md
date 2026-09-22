<div align="center">

# KS KRYPTON VIDEO EDITOR

**Next-Generation AI Video Editing powered by MLT Core & Single Gateway Intelligence**

[![Version](https://img.shields.io/badge/version-1.0.0-00D2FF.svg?style=for-the-badge)](https://github.com/ks777-del/KS-KRYPTON-EDITOR)
[![License](https://img.shields.io/badge/license-GPL--3.0-blue.svg?style=for-the-badge)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20macOS-1E293B.svg?style=for-the-badge)](https://github.com/ks777-del/KS-KRYPTON-EDITOR)
[![AI Gateway](https://img.shields.io/badge/AI%20Gateway-Nexus%20Universal-0284C7.svg?style=for-the-badge)](docs/ai/nexus-setup.md)

</div>

---

## Overview

**KS KRYPTON VIDEO EDITOR** is a professional, high-performance desktop video editor built on the industrial-grade **MLT multimedia framework**. Designed for creative storytellers, filmmakers, and digital creators, KRYPTON fuses traditional multi-track non-linear editing with **autonomous AI capabilities** powered by the **Nexus AI Gateway**.

From advanced color grading, keyframe animation, and audio track mastering to natural language timeline assembly, scene detection, and silence removal, KRYPTON delivers an uncompromising creative studio experience.

---

## Key Features

### 🎬 Non-Linear Editing Engine
- **Multi-Track Timeline:** Full support for unlimited video, audio, title, and effect tracks with compositing, ripple editing, and slip/slide tools.
- **Format Agnostic:** Seamless timeline playback and export across 4K UHD, 2.5K QHD, Full HD (16:9), Vertical / Shorts (9:16), Square (1:1), and custom cinematic resolutions.
- **Hardware Acceleration:** Zero-lag scrubbing, proxy clip generation, and GPU-accelerated previews.
- **Comprehensive Scopes:** Real-time audio spectrum analyzer, RGB parade, waveform monitor, and vectorscope.

### 🧠 Single AI Gateway (Nexus Universal Integration)
- **Zero Provider Leakage:** KRYPTON connects to a single unified gateway endpoint (`http://localhost:20128/v1`), eliminating the need to manage individual API keys for OpenAI, Anthropic, Gemini, DeepSeek, or local providers.
- **Dynamic Model Discovery:** Automatically queries and populates available models (166+ to 296+ models) on the fly without application restarts.
- **Natural Language Editing:** Direct conversational instructions:
  - *"Detect all scene transitions and split clips accordingly"*
  - *"Remove all silent gaps greater than 0.8 seconds on Track 1"*
  - *"Generate an intro title sequence with glowing blue cyber aesthetic"*
- **Privacy-First Routing:** Video media files are never transmitted across external networks; only frame timestamps, track labels, and editing directives are communicated.

### ⚡ AAA Startup & Loading Experience
- **Cinematic Startup:** Branded loading screen with volumetric god-rays, 3D wireframes, and metallic crystal emblem.
- **Precision Integrated Progress Bar:** Dynamically tracks authentic subsystem initialization stages without artificial delays or fake timers.
- **Subsystem Lifecycle Milestones:**
  1. *Initializing MLT multimedia engine…*
  2. *Loading project & asset systems…*
  3. *Loading hardware & video profiles…*
  4. *Preparing creative workspace…*
  5. *Ready.*

### 🎨 Cyber-Slate Modern UI
- **Obsidian Dark Aesthetic:** Customized palettes (`#080D14` background, `#1E293B` borders, `#00D2FF` electric cyan accents).
- **Dockable Modular Layout:** Dedicated panels for Project Bin, AI Workspace, Properties Inspector, Effect Stack, and Audio Mixer.

---

## Quick Start Guide

### Prerequisites
- **Operating System:** Windows 10/11 (64-bit), Linux (Ubuntu 22.04+, Fedora 38+), or macOS (12.0+)
- **CPU:** Intel Core i5 / AMD Ryzen 5 or higher
- **RAM:** 8 GB minimum (16 GB recommended for 4K editing)
- **Storage:** 2 GB for installation; SSD strongly recommended for project cache
- **Node.js:** v18.0.0 or higher (for the Nexus AI Gateway service)

### Setting Up Nexus AI Gateway

1. **Install Nexus AI Gateway CLI globally:**
   ```bash
   npm install -g nexus-ai-gateway
   ```

2. **Launch the Gateway Daemon:**
   ```bash
   nexus serve
   ```
   *By default, Nexus listens at `http://localhost:20128`.*

3. **Connect KRYPTON:**
   - Launch **KS KRYPTON EDITOR**.
   - Open the **KS KRYPTON AI** dock on the right.
   - Click **⚙ Settings** in the dock header.
   - Enter your gateway endpoint (default: `http://localhost:20128/v1`) and your Nexus Key.
   - Click **↻ Refresh** to auto-detect models, select your preferred model, and click **Connect / Save**.

For full setup instructions, see the [Nexus AI Gateway Setup Guide](docs/ai/nexus-setup.md).

---

## Documentation Index

| Document | Description |
| :--- | :--- |
| [**SECURITY.md**](SECURITY.md) | Security policy, vulnerability disclosure, and token safety |
| [**CONTRIBUTING.md**](CONTRIBUTING.md) | Guidelines for contributing to documentation and project development |
| [**Nexus AI Setup Guide**](docs/ai/nexus-setup.md) | Complete 4-step walk-through for setting up the Nexus AI Gateway |
| [**AI Security & Privacy**](docs/ai/ai-security.md) | In-depth credential protection, masking, and data routing policies |
| [**AI Troubleshooting**](docs/ai/ai-troubleshooting.md) | Resolving connection issues, port conflicts, and model timeouts |
| [**Getting Started Guide**](docs/guides/getting-started.md) | Step-by-step tutorial on creating projects, editing, and rendering |

---

## Community & Support

- **Bug Reports & Feature Requests:** Please file an issue on [GitHub Issues](https://github.com/ks777-del/KS-KRYPTON-EDITOR/issues).
- **Security Vulnerabilities:** Follow the responsible disclosure guidelines in [SECURITY.md](SECURITY.md).

---
## Downlaod Link 
1. https://drive.google.com/file/d/1DhaFAM8kMd4DEg9iyrxOp7R-nHf2GHmU/view?usp=sharing
   
## License

KS KRYPTON VIDEO EDITOR is distributed under the terms of the GNU General Public License v3.0 (GPL-3.0). Documentation and guides are released under CC-BY-4.0.
