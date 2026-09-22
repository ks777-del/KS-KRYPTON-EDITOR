# KS KRYPTON — AI Security & Privacy Policy

## 1. Credential Security

- **Single Gateway Key:** KRYPTON only stores the single Nexus API Key. Your upstream OpenAI, Anthropic, Gemini, or other keys reside exclusively inside your Nexus AI Gateway server and are never accessible to KRYPTON or its plugins.
- **Local Storage:** The Nexus API key is stored locally on your machine in the KDE configuration system (`KSharedConfig` under the `[KryptonAI]` group) with Base64 encoding. It is never uploaded or sent to third-party telemetry servers.
- **Masking:**
  - In the UI, the key is masked (`QLineEdit::Password`, displaying `nx_••••••••`).
  - In error messages and debugging logs, keys are strictly redacted (`mask_key()`, showing at most prefix and suffix: `nx_...456`).

---

## 2. Privacy & Data Routing

- **Local Processing:**
  - Project state metadata (track names, clip positions, cut points) is packaged into context snapshots for editing instructions.
  - If your Nexus AI Gateway is configured with local providers (e.g. Ollama, vLLM, or LM Studio), **no data ever leaves your computer**.
- **Commercial Cloud Providers:**
  - When utilizing cloud foundation models (Claude, Gemini, GPT-4o), prompt text leaves your computer and travels from your local Nexus instance to the respective provider's API.
  - Video media files (source footage) are **not** transmitted across the cloud AI bridge; only frame markers, durations, and editing directives are sent.
