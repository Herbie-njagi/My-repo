# Dev Environment Setup

A log of the tools installed, steps completed, and issues encountered while setting up a modern AI-assisted development environment.

---

## Tools Installed

| Tool | Purpose |
|------|---------|
| **Cursor IDE** | AI-powered code editor built on VS Code |
| **Claude Code** (Cursor extension) | Anthropic's AI coding assistant integrated into Cursor |
| **Codex** (Cursor extension) | OpenAI's Codex extension for additional AI code suggestions |
| **Git + GitHub** | Version control and remote repository hosting |

---

## Steps Completed

### 1. Install Cursor IDE
- Downloaded the installer from [https://cursor.com/](https://cursor.com/)
- Ran the installer and launched Cursor
- Cursor is built on VS Code, so the interface was immediately familiar

### 2. Add the Claude Code Extension
- Opened the Extensions panel (`Ctrl+Shift+X` / `Cmd+Shift+X`)
- Searched for **"Claude Code"**
- Clicked **Install** and waited for the extension to load
- Logged in with an Anthropic account via the authentication prompt

### 3. Add the Codex Extension
- Still in the Extensions panel, searched for **"Codex"**
- Clicked **Install**
- Logged in / authenticated as prompted

### 4. Create a GitHub Repository
- Navigated to [https://github.com/](https://github.com/) (created an account if needed)
- Clicked **New repository**
- Named the repo, set visibility to **Public**, and initialized with a README
- Copied the remote URL for cloning

### 5. Open the Repository in Cursor
- Cloned the repository locally:
  ```bash
  git clone https://github.com/<Herbie-njagi>/<My-repo>.git
  ```
- In Cursor: **File → Open Folder** → selected the cloned repo folder

### 6. Create and Push This README
- Created `README.md` in the project root
- Staged, committed, and pushed:
  ```bash
  git add README.md
  git commit -m "docs: add setup README"
  git push origin main
  ```

---

## Issues Encountered & How They Were Solved

### Issue 1: Cursor not recognized as default editor after install
**Problem:** Launching Cursor from the terminal with `cursor .` didn't work immediately after installation.  
**Solution:** Opened Cursor manually, then ran **Command Palette** (`Cmd+Shift+P`) → `Shell Command: Install 'cursor' command in PATH`. Reopened the terminal and the command worked.

### Issue 2: Claude Code extension login loop
**Problem:** After clicking "Log in", the browser opened but redirected back without completing authentication.  
**Solution:** Disabled any active VPN, cleared browser cookies for `anthropic.com`, and retried. Authentication completed successfully on the second attempt.

### Issue 3: Git push rejected (non-fast-forward)
**Problem:** Initial `git push` was rejected because the remote already had a commit (the auto-generated README from GitHub).  
**Solution:** Ran `git pull --rebase origin main` to integrate the remote history, resolved no conflicts, then pushed successfully.

---

## Notes

- Both AI extensions (Claude Code and Codex) can be active simultaneously; they operate independently and don't conflict.
- Cursor's built-in AI (`Ctrl+K` / `Cmd+K`) is separate from the Claude Code and Codex extensions — all three can complement each other.
- Make sure to keep extensions updated regularly to get the latest model improvements.
