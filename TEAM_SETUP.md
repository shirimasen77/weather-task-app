# Team Collaboration Setup

## Step 1: Create GitHub Repository

```bash
# Run this when you're ready to create the remote repo
gh repo create weather-task-app --public --description "Weather-based task suggestion app"

# Push initial code
git add .
git commit -m "Initial project setup with team collaboration structure"
git remote add origin https://github.com/YOUR_USERNAME/weather-task-app.git
git push -u origin main
```

## Step 2: Add Collaborators (When Ready)

Replace these dummy usernames with actual GitHub accounts:

```bash
# Frontend Developer
# gh api repos/YOUR_USERNAME/weather-task-app/collaborators/developer-alex -X PUT

# Backend Developer
# gh api repos/YOUR_USERNAME/weather-task-app/collaborators/developer-sam -X PUT

# UI/UX Developer
# gh api repos/YOUR_USERNAME/weather-task-app/collaborators/developer-jordan -X PUT

# Additional team members
# gh api repos/YOUR_USERNAME/weather-task-app/collaborators/developer-casey -X PUT
```

## Step 3: Set Up Branch Protection

```bash
# Protect main branch - require PR reviews
gh api repos/YOUR_USERNAME/weather-task-app/branches/main/protection -X PUT \
  --field required_status_checks='{"strict":true,"contexts":[]}' \
  --field enforce_admins=true \
  --field required_pull_request_reviews='{"required_approving_review_count":1,"dismiss_stale_reviews":true}' \
  --field restrictions=null
```

## Step 4: Team Member Instructions

Send this to your team members:

### Getting Started
1. **Clone repository**: `git clone https://github.com/YOUR_USERNAME/weather-task-app.git`
2. **Install dependencies**: `npm install`
3. **Create feature branch**: `git checkout -b feature/your-name/feature-description`
4. **Make changes and test**
5. **Create pull request**: `gh pr create --title "Add feature X" --body "Description of changes"`

### Development Rules
- ✅ Always work on feature branches
- ✅ Get 1 approval before merging
- ✅ Write descriptive commit messages
- ✅ Test your changes before pushing
- ❌ Never push directly to main
- ❌ Don't merge your own PRs

## Suggested Team Roles

- **developer-alex**: Frontend UI components
- **developer-sam**: Weather API integration & backend
- **developer-jordan**: UX/UI design & templates
- **developer-casey**: Testing & documentation

## Communication

- Use GitHub Issues for bugs and feature requests
- Use PR comments for code discussions
- Use GitHub Discussions for general planning

---

**Note**: Uncomment the collaboration commands above once your team members have GitHub accounts!