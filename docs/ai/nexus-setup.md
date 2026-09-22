# KS KRYPTON — Nexus AI Gateway Setup Guide

This guide walks you through setting up and connecting **Nexus AI Gateway** to **KS KRYPTON EDITOR**.

With Nexus AI Gateway, KRYPTON requires **zero individual provider configurations**. You configure a single gateway endpoint and key, gaining instant access to 296+ AI models with automatic routing, fallback, and tool-calling capabilities.

---

## Architecture Overview

```
                         KS KRYPTON
                              │
                              ▼
                    KRYPTON AI INTEGRATION
                              │
                              ▼
                     NEXUS AI GATEWAY
                              │
              ┌───────────────┼────────────────┐
              │               │                │
              ▼               ▼                ▼
           Provider 1     Provider 2       Provider 3...
           (Claude)        (Gemini)        (GPT / DeepSeek)
```

---

## Step 1: Check Node.js

Nexus AI Gateway runs on Node.js (v18.0.0 or higher recommended).

1. Open your terminal (PowerShell, Command Prompt, or Terminal):
   ```bash
   node -v
   ```

2. If the command outputs `v18.x.x`, `v20.x.x`, `v22.x.x`, or `v24.x.x`, proceed to Step 2.
3. If the command returns `'node' is not recognized`:
   - Download the LTS version from the official website: [https://nodejs.org](https://nodejs.org)
   - Run the installer and ensure **"Add to PATH"** is checked.
   - Restart your terminal after installation.

---

## Step 2: Install Nexus AI Gateway

Install the global Nexus AI Gateway CLI using npm:

```bash
npm install -g nexus-ai-gateway
```

Verify that the CLI is properly installed:

```bash
nexus --version
```

You should see output similar to `3.8.x`.

---

## Step 3: Start Nexus AI Gateway

Launch the gateway daemon:

```bash
nexus serve
```

*Note: Keep this terminal window open while editing in KS KRYPTON.*

By default, Nexus starts on port `20128` (or `8080` in standalone configurations). You will see output confirming the server is listening:
```text
[Nexus] Gateway listening on http://localhost:20128
[Nexus] 166 models loaded across configured providers
```

---

## Step 4: Connect KRYPTON

1. Launch **KS KRYPTON EDITOR**.
2. Open the **KS KRYPTON AI** workspace panel (on the right-hand side dock).
3. Click the **⚙ Settings** button in the header.
4. Configure your single gateway connection:
   - **Gateway Endpoint:** `http://localhost:20128/v1` (default)
   - **Nexus API Key:** Enter your Nexus API Key (e.g., `nx_••••••••`). Leave blank if your local Nexus instance requires no authentication.
   - **Active Model:** Click **↻ Refresh** to query the gateway for all available models, or select `auto/best-fast`.
5. Click **Connect / Save**.

The status indicator in the top header will transition to **● Connected (166 models)**.

---

## Key Features

- **Dynamic Model Catalog:** KRYPTON automatically discovers models from Nexus (`GET /v1/models`). When you add or change providers in Nexus, KRYPTON automatically updates without app restarts.
- **Natural Language Editing:** Ask KRYPTON to "cut silence", "detect scenes", "split at frame 150", or generate creative edit workflows.
- **Zero Provider Leakage:** You never need to enter Gemini, OpenAI, Claude, or DeepSeek keys inside KRYPTON directly.
