# 🤖 commit-ai

commit-ai is a lightweight Ruby CLI tool that uses OpenAI's GPT models (e.g., GPT-4) to generate intelligent, conventional-style git commit messages based on your staged changes.

---

## 🚀 What It Does

- Reads your current staged changes using git diff --cached.
- Sends those changes to the OpenAI API for analysis.
- Suggests a clear and concise commit message.
- Asks for confirmation and optionally commits directly.

---

## 📦 Requirements

- Ruby 2.7 or later
- Bundler (for installing dependencies)
- OpenAI API key
- Gems:
  - httparty
  - dotenv

---

## ⚙️ Installation (Local Script Setup)

### 1. Clone or create the project directory

```bash
mkdir -p ~/.cli-tools/commit-ai/bin
cd ~/.cli-tools/commit-ai
```
