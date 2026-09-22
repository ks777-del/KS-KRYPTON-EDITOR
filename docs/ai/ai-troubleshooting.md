# KS KRYPTON — AI Troubleshooting Guide

This guide addresses common error messages and setup issues when using the Nexus AI Gateway with KS KRYPTON.

---

## 1. Node.js & CLI Errors

### `'node' is not recognized as an internal or external command`
- **Cause:** Node.js is not installed, or the Node.js installation directory is not present in your system `PATH`.
- **Solution:**
  1. Download the LTS version of Node.js from [nodejs.org](https://nodejs.org).
  2. During setup, make sure **"Add to PATH"** is selected.
  3. Close and reopen your terminal before running `node -v`.

### `'npm' is not recognized`
- **Cause:** npm is typically installed automatically with Node.js. If missing, the Node.js installation was partial or corrupted.
- **Solution:** Reinstall Node.js using the official installer.

### `'nexus' is not recognized`
- **Cause:** Global npm packages are not in your system environment PATH.
- **Solution:**
  - On Windows, verify that `%APPDATA%\npm` exists in your User or System `PATH`.
  - Re-run `npm install -g nexus-ai-gateway`.

---

## 2. Gateway Connectivity Errors

### Status: `● Gateway Unavailable` / `Connection Refused`
- **Cause:** The Nexus AI Gateway daemon is not running, or is listening on a different port.
- **Solution:**
  1. Open a terminal and run:
     ```bash
     nexus serve
     ```
  2. Confirm the listening port (e.g. `http://localhost:20128` or `8080`).
  3. In KRYPTON AI Settings, verify that the **Gateway Endpoint** matches (e.g. `http://localhost:20128/v1`).
  4. Click **Test Connection**.

### Status: `● Auth Error`
- **Cause:** The Nexus AI Gateway requires an authentication token, but the key entered is incorrect or expired.
- **Solution:**
  1. In KRYPTON AI Settings, verify your **Nexus API Key**.
  2. If running locally without authentication enabled in Nexus, clear the API key field and click **Connect / Save**.

---

## 3. Model Discovery Errors

### Model dropdown is empty or missing models
- **Cause:** The gateway was unreachable when the panel opened, or downstream providers in Nexus have not finished initializing.
- **Solution:**
  1. Ensure `nexus serve` is active.
  2. Click the **↻ Refresh** button next to the model dropdown.
  3. Check the terminal running `nexus serve` to verify that your configured providers are active and authenticated.
