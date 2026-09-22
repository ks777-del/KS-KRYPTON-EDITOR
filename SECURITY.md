# Security Policy

## Supported Versions

Security updates and critical patches are actively provided for the following versions of **KS KRYPTON VIDEO EDITOR**:

| Version | Supported          |
| :--- | :--- |
| 1.0.x   | :white_check_mark: |
| < 1.0   | :x:                |

---

## Reporting a Vulnerability

The KS KRYPTON team takes the security and privacy of its users seriously. If you believe you have found a security vulnerability in KS KRYPTON VIDEO EDITOR or its gateway integration, please follow the responsible disclosure process outlined below.

### 1. How to Report
- **Do not report security issues via public GitHub issues, pull requests, or public discussions.**
- Please email a detailed report directly to the security maintainers at:
  `kshitijsingh030@gmail.com`
- Include the following details to help us investigate:
  - Description of the vulnerability.
  - Steps to reproduce or proof-of-concept (PoC) code.
  - Potential impact and affected subsystems (e.g., UI, IPC bridge, AI provider client).
  - Any proposed remediations.

### 2. Response Timeline
- **Initial Acknowledgment:** Within 48 hours of receipt.
- **Vulnerability Assessment:** Within 5 business days, including confirmation of severity and impact.
- **Fix & Release:** A patch will be developed, reviewed, and released in an expedited maintenance update.
- **Public Disclosure:** Public details will be coordinated after the fix has been deployed to ensure users can safely upgrade.

---

## Credential & Token Security Policy

### 1. Single Gateway Architecture
KS KRYPTON is intentionally designed to **never directly handle or store individual third-party provider API keys** (such as direct keys for OpenAI, Anthropic, Google Gemini, or DeepSeek). 

All AI interactions are mediated exclusively through the **Nexus AI Gateway**:
- Upstream provider credentials remain stored within the user's private Nexus Gateway daemon.
- KRYPTON communicates only with the single local or self-hosted gateway endpoint via the `nx_` token.

### 2. Local Credential Storage
- The Nexus Gateway API Key is stored strictly on the local machine using the KDE configuration system (`KSharedConfig` within the `[KryptonAI]` configuration domain).
- Credentials are obfuscated locally with Base64 encoding and are never uploaded, transmitted, or synchronized with external telemetry servers.

### 3. Masking & Redaction
- **User Interface:** The API key field is permanently protected using password masking (`QLineEdit::Password`), rendering the key as dots (`nx_••••••••`). A toggle action allows the user to temporarily unmask the key during setup.
- **Logging & Diagnostics:** All internal logging, console outputs, and error handlers sanitize API credentials via `mask_key()`. Only the prefix and last 3 characters are retained for diagnostic verification (e.g., `nx_...456`). Raw tokens are never written to log files.

---

## Privacy & Media Routing Policy

- **No Video Data Uploads:** Source video files, media clips, and raw audio tracks are **never** uploaded to external cloud endpoints.
- **Metadata Snapping:** KRYPTON only transmits editorial metadata (track indices, frame cut-points, marker timestamps, and conversational prompt text) to the AI Gateway to generate timeline operations.
- **Full Local Mode:** When Nexus AI Gateway is configured with local LLM providers (e.g., Ollama, vLLM, or LM Studio), **100% of data processing remains strictly on the local workstation**.
