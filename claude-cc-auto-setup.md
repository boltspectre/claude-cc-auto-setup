# AI Prompt: Automated Environment Setup (Node.js, Claude Code, cc switch)

## Goal

**Fully automated** completion in the current environment:

1. Detect Node.js
2. Install Claude Code (no API key configuration required)
3. Download and start cc switch (for managing API keys and vendors)

**All download URLs are automatically fetched by AI; user does not need to configure any parameters.**

## Detailed Steps

### Step 1: Detect Node.js

- Run `node --version` to check if already installed
- If not installed, automatically search for and download the latest LTS version, then install it
- **Automatically configure environment variables**:
  - Detect Node.js installation path (default: `C:\Program Files\nodejs\`)
  - Check if this path has been added to the system PATH environment variable
  - If not added, use PowerShell administrator privileges to automatically add it to the system environment variables
  - Run `refreshenv` or restart the terminal to make environment variables take effect
  - Verify that `node` and `npm` commands are available

### Step 2: Install Claude Code

- Execute `npm install -g @anthropic-ai/claude-code`
- Run `claude --version` to verify installation
- **No API key configuration needed, no config files created**

### Step 3: Download and start cc switch

- Use WebSearch to search "cc switch GitHub release download"
- Use WebFetch to access `https://github.com/farion1231/cc-switch/releases/latest` and get the latest download URL
- Download the version corresponding to the system to the current directory
- Extract to `./cc-switch/`
- Start and verify the process

## Output Example

```
## 📋 Environment Setup Complete

### ✅ Execution Status
| Step | Status | Details |
|------|--------|---------|
| Node.js Detection | ✅ | vXX.XX.X |
| Node.js Environment Variables | ✅ | Added to PATH |
| Claude Code Installation | ✅ | vX.X.X |
| cc switch Download & Start | ✅ | Running (PID: XXXXX) |

### 📝 Usage Instructions
1. **Claude Code**: Run `claude` in terminal
2. **cc switch**: Open interface from system tray icon, configure API keys and manage vendors

### 💡 Optional Actions
- **Move cc-switch**: If you want to organize files, move the `./cc-switch/` folder to another location (e.g., `C:\Program Files\cc-switch\`), then re-run `cc-switch.exe`
```

## Notes

- All download URLs must be automatically fetched from GitHub
- All files downloaded to `./cc-switch/`, no extra files created

---

Now make a plan based on this document and start execution.
