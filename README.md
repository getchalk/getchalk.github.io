# Chalk — Official Web Portal & Downloads

> **Live Website:** [getchalk.github.io](https://getchalk.github.io)  
> **Source Repository:** [github.com/getchalk/chalk](https://github.com/getchalk/chalk)  
> **Latest Releases:** [github.com/getchalk/chalk/releases](https://github.com/getchalk/chalk/releases)

---

### Overview

Chalk is a 100% local-first desktop lecture and meeting companion with live LaTeX synthesis. It captures dual-channel hardware audio and slide transitions, accepts whiteboard photos via a zero-install local QR link, and generates structured Markdown notes with mathematically verified LaTeX formulas in real time.

### Platform Downloads

| Operating System | Architecture | Package Format | Download Link |
|---|---|---|---|
| **macOS** | Apple Silicon (M1/M2/M3/M4) & Intel | Standalone Application Bundle (`.zip`) | [Download for macOS](https://github.com/getchalk/chalk/releases/latest/download/Chalk-macOS.zip) |
| **Windows** | 64-Bit (x64) | Standalone Executable (`.exe`) | [Download for Windows](https://github.com/getchalk/chalk/releases/latest/download/Chalk-Setup.exe) |

---

### Terminal Quick Install

#### macOS
```bash
# 1. Download and extract
curl -L -O https://github.com/getchalk/chalk/releases/latest/download/Chalk-macOS.zip
unzip -q Chalk-macOS.zip

# 2. Clear Apple quarantine flag (bypasses Gatekeeper unverified developer prompt)
xattr -cr Chalk.app

# 3. Launch Chalk
open Chalk.app
```

> **macOS Gatekeeper:** Because Chalk is an open-source binary distributed outside the Mac App Store, macOS may display a security prompt (*"cannot be opened because Apple cannot check it for malicious software"*). Running `xattr -cr Chalk.app` in Terminal clears the quarantine attribute. Alternatively, right-click (or Control-click) `Chalk.app` in Finder, select **Open**, and confirm **Open**.

#### Windows (PowerShell)
```powershell
curl -L -O https://github.com/getchalk/chalk/releases/latest/download/Chalk-Setup.exe
.\Chalk-Setup.exe
```

---

### Architecture & Security

- **Direct BYOK Only:** No middleman proxy servers. Requests travel directly over TLS 1.3 from your machine to official provider endpoints (Google AI Studio, Anthropic, OpenAI).
- **Zero Telemetry:** 0 KB of tracking or telemetry data collected (§ 165 TKG / GDPR compliant).
- **Encrypted Local Vault:** Credentials stored strictly inside macOS Keychain Access or Windows DPAPI.
- **Local Storage:** Audio journals, slide keyframes, and notes reside exclusively on your workstation under `~/.chalk/sessions/`.

For full documentation, source code, and developer instructions, visit the main repository at [github.com/getchalk/chalk](https://github.com/getchalk/chalk).
