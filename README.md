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
mkdir -p ~/.cli-tools/commit-ai
cd ~/.cli-tools/commit-ai
```

### 2. Clone app and bundle install

```bash
git clone git@github.com:diamantkolshi/commit-ai.git
bundle install
```

### 3. Set up OpenAI API Key

1. Visit [OpenAI Platform](https://platform.openai.com/api-keys) and sign in to your account
2. Click on "Create new secret key"
3. Give your key a name (e.g., "commit-ai")
4. Copy the generated API key

Then, set up your API key in one of these ways:

**Option 1: Environment Variable (Recommended)**

```bash
echo 'export OPENAI_API_KEY=your-api-key-here' >> ~/.zshrc
source ~/.zshrc
```

**Option 2: .env File**

```bash
echo 'OPENAI_API_KEY=your-api-key-here' > .env
```

### 4. Add the script to your PATH

```bash
echo 'export PATH="$HOME/.cli-tools/commit-ai/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

## 🎯 Usage

Once installed, you can use commit-ai in any git repository:

```bash
git add .
commit-ai
```

The tool will analyze your staged changes and suggest a commit message. You can then:

- Accept the suggestion (press Enter)
- Edit the message
- Cancel the commit (Ctrl+C)

## 🔧 Configuration

You can customize the behavior by setting these environment variables:

- `OPENAI_API_KEY`: Your OpenAI API key

## 📝 License

MIT License - feel free to use this tool in your projects!
