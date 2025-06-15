# 🚀 Interactive HR Dashboard Deployment Guide (Firebase + GitHub)

## 1. Firebase Setup
- Go to https://console.firebase.google.com
- Create a project (e.g., `interactive-hr-dashboard`)
- Disable Google Analytics if preferred

## 2. Firebase CLI
```bash
npm install -g firebase-tools
firebase login
firebase init
```
> Select Hosting → public directory = `build` → single-page app = Yes

## 3. Firebase Files

### firebase.json
```json
{
  "hosting": {
    "public": "build",
    "rewrites": [{"source": "**", "destination": "/index.html"}],
    "ignore": ["firebase.json", "**/.*", "**/node_modules/**"]
  }
}
```

### .firebaserc
```json
{
  "projects": { "default": "your-project-id" }
}
```

## 4. GitHub Actions CI/CD
- Add `FIREBASE_SERVICE_ACCOUNT` to GitHub Secrets
- Paste your Firebase service account JSON key

Workflow file path:
`.github/workflows/deploy.yml`

## 5. Build & Deploy
```bash
npm run build
firebase deploy
```

> Your app will be live at: https://your-project-id.web.app
