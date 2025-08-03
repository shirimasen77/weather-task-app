# Weather Task App

A weather-based task suggestion app that intelligently recommends what could, should, or should not be done based on current and forecast conditions.

## Team Setup

### Collaborators
Add these GitHub usernames once accounts are created:

```bash
# Uncomment and replace with actual usernames when ready:
# gh api repos/:owner/weather-task-app/collaborators/developer-alex -X PUT
# gh api repos/:owner/weather-task-app/collaborators/developer-sam -X PUT
# gh api repos/:owner/weather-task-app/collaborators/developer-jordan -X PUT
```

### Branch Protection
Once collaborators are added, set up branch protection:

```bash
gh api repos/:owner/weather-task-app/branches/main/protection -X PUT \
  --field required_status_checks='{"strict":true,"contexts":[]}' \
  --field enforce_admins=true \
  --field required_pull_request_reviews='{"required_approving_review_count":1}'
```

## Development Workflow

1. **Create feature branch**: `git checkout -b feature/your-feature-name`
2. **Make changes and commit**: Use descriptive commit messages
3. **Push branch**: `git push -u origin feature/your-feature-name`
4. **Create PR**: `gh pr create --title "Your feature" --body "Description"`
5. **Review & merge**: Wait for team review before merging

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

## Getting Started

1. Clone the repository
2. Install dependencies: `npm install`
3. Copy `.env.example` to `.env` and add your weather API key
4. Run development server: `npm run dev`

## Core Features

- **Three-tier task system**: Essential, Health/Wellness, Hobby
- **Weather intelligence**: API integration with forecast analysis
- **Calendar integration**: Energy-aware scheduling
- **Smart templates**: Pre-built task templates with custom options
- **Conservative learning**: Safe AI adaptation to user patterns