# Team Onboarding Tutorial - Weather Task App

Welcome to the Weather Task App development team! This guide will get you set up and ready to collaborate.

## Step 1: Create Your GitHub Account

1. **Go to [GitHub.com](https://github.com)**
2. **Click "Sign up"**
3. **Choose a professional username** (you'll use this for work)
   - Examples: `alex-johnson`, `sam-dev`, `jordanux`, `casey-codes`
   - Avoid numbers/special characters if possible
4. **Use a professional email** (create a new Gmail if needed)
5. **Complete account setup**

## Step 2: Install Required Tools

### Install Git
**Linux/Ubuntu:**
```bash
sudo apt update
sudo apt install git
```

**Mac:**
```bash
# Install Homebrew first if you don't have it
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install git
```

**Windows:**
Download from [git-scm.com](https://git-scm.com/download/win)

### Install GitHub CLI
**Linux/Ubuntu:**
```bash
sudo apt install curl
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
sudo chmod go+r /usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh
```

**Mac:**
```bash
brew install gh
```

**Windows:**
Download from [GitHub CLI releases](https://github.com/cli/cli/releases)

### Install Node.js (for our project)
**Linux/Ubuntu:**
```bash
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt-get install -y nodejs
```

**Mac:**
```bash
brew install node
```

**Windows:**
Download from [nodejs.org](https://nodejs.org/)

## Step 3: Configure Git

```bash
# Set your name and email
git config --global user.name "Your Full Name"
git config --global user.email "your.email@gmail.com"

# Login to GitHub CLI
gh auth login
# Choose "GitHub.com" → "HTTPS" → "Yes" to git credential helper → "Login with web browser"
```

## Step 4: Send Your GitHub Username

**📧 Email Shiri your GitHub username so you can be added as a collaborator!**

Example: "Hi Shiri, my GitHub username is `alex-johnson`. Ready to start developing!"

## Step 5: Clone the Repository (After Being Added)

Once Shiri adds you as a collaborator:

```bash
# Clone the project
git clone https://github.com/shirimasen77/weather-task-app.git

# Navigate to project
cd weather-task-app

# Install dependencies
npm install

# Test that everything works
npm run dev
```

## Step 6: Your First Contribution

### Create a Feature Branch
```bash
# Always create a new branch for your work
git checkout -b feature/your-name/initial-setup

# Example: git checkout -b feature/alex/initial-setup
```

### Make a Test Change
```bash
# Create a simple file to test your setup
echo "# Hello from [Your Name]" > test-[yourname].md

# Add and commit
git add test-[yourname].md
git commit -m "Add initial test file for [your name]"

# Push your branch
git push -u origin feature/your-name/initial-setup
```

### Create Your First Pull Request
```bash
# Create a pull request
gh pr create --title "Initial setup test - [Your Name]" --body "Testing my development environment setup"
```

## Step 7: Install Claude Code (Recommended)

If you want to use AI assistance like Shiri:

1. **Get Claude Pro subscription** at [claude.ai](https://claude.ai)
2. **Install Claude Code CLI** following instructions at [docs.anthropic.com/claude-code](https://docs.anthropic.com/en/docs/claude-code)
3. **Test it works**: `claude "help me understand this codebase"`

## Development Workflow

### Daily Workflow
1. **Pull latest changes**: `git pull origin main`
2. **Create feature branch**: `git checkout -b feature/yourname/feature-description`
3. **Write code and test**
4. **Commit changes**: `git add . && git commit -m "Descriptive message"`
5. **Push and create PR**: `git push -u origin feature/yourname/feature-description`
6. **Create PR**: `gh pr create --title "Feature description" --body "What this does"`

### Team Rules
- ✅ **Always work on feature branches** (never commit directly to main)
- ✅ **Get 1 team member approval** before merging PRs
- ✅ **Write clear commit messages** ("Add weather API integration" not "fix stuff")
- ✅ **Test your changes** before creating PRs
- ✅ **Keep PRs focused** (one feature per PR)
- ❌ **Never push directly to main branch**
- ❌ **Don't merge your own PRs**

## Getting Help

- **GitHub Issues**: For bugs and feature requests
- **PR Comments**: For code-specific discussions
- **Team Chat**: For general questions
- **Claude Code**: Ask AI for help understanding code
- **Shiri**: Project lead for bigger questions

## Quick Reference Commands

```bash
# Daily workflow
git pull origin main                          # Get latest changes
git checkout -b feature/name/description     # Create feature branch
git add .                                    # Stage changes
git commit -m "Description"                 # Commit changes
git push -u origin feature/name/description # Push branch
gh pr create                                # Create pull request

# Useful commands
git status                                  # See what's changed
git log --oneline                          # See recent commits
gh pr list                                 # See open PRs
gh pr checkout 123                         # Test someone else's PR
```

## Project Structure

```
weather-task-app/
├── src/
│   ├── components/     # UI components
│   ├── services/       # Weather API, task engine
│   ├── utils/          # Helper functions
│   └── templates/      # Task templates
├── tests/              # Test files
├── docs/               # Documentation
└── scripts/            # Build/deployment scripts
```

---

**Welcome to the team! 🌤️ Let's build something awesome together!**

**Questions?** Open a GitHub Issue or ask in our team chat.