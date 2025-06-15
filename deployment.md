# 🚀 Deployment Guide

This guide walks through deploying the **Interactive HR Dashboard** using Firebase and GitHub.

## Prerequisites
- Node.js v18+
- Firebase CLI
- GitHub account

## Firebase Setup
1. Go to [Firebase Console](https://console.firebase.google.com)
2. Create a new project
3. Enable Firestore and Authentication (Google)
4. Generate a **service account** key (JSON)

## Local Setup
```bash
npm install
npm run dev     # test locally
npm run build
firebase deploy
```

## GitHub Actions Setup
1. Push code to GitHub
2. In repo settings → Secrets → Actions
3. Add: `FIREBASE_SERVICE_ACCOUNT` with your JSON

On push to `main`, Firebase deploys your app automatically.
