# 📊 Interactive HR Dashboard

A full-featured, production-ready HR dashboard built with **React**, **Firebase**, and **TailwindCSS**.  
Ideal for HR teams managing employees, performance, logs, and permissions with automation and analytics.

---

## 🚀 Features

- 🔐 Firebase Authentication (Google login)
- 🧑‍💼 Admin vs. Team Role-based Routing
- 📁 Firestore Employee & History Management
- 📈 Performance Metrics with Recharts
- 🗂 Log Viewer with Export (CSV)
- 🔍 Filter by Email, Action, Date
- 🎨 Dark Mode + Theme Toggle
- 🧭 Onboarding Modal for New Users
- 🌍 i18n Localization Support (i18next)
- 🛠 CI/CD via GitHub Actions
- ☁️ Deployed on Firebase Hosting

---

## 📁 Project Structure

```bash
/components          # Reusable UI components
/pages               # Route pages (dashboard, team)
/hooks               # Onboarding hook, auth
/lib                 # Firebase setup & analytics
```

---

## 🔧 Setup Instructions

1. Clone repo & install dependencies:
```bash
npm install
```

2. Add `.env.local` with Firebase keys:
```
VITE_FIREBASE_API_KEY=xxx
...
```

3. Start local dev server:
```bash
npm run dev
```

4. Build & deploy manually:
```bash
npm run build
firebase deploy
```

> Full deploy guide: [`DEPLOY_GUIDE.md`](./DEPLOY_GUIDE.md)

---

## 📦 CI/CD Deployment

- Push to `main` branch triggers Firebase Hosting deployment
- Requires GitHub secret: `FIREBASE_SERVICE_ACCOUNT`

---

## 🧠 Optional Add-ons

- ✅ Sentry Error Monitoring
- ✅ Slack Log Notifications
- ✅ Firebase Analytics
- ✅ Branded Login
- ✅ Department-based Team Dashboards

---

## 📄 License

MIT — free to use, modify, and distribute.

---

## 💬 Questions?

Open an issue or email us at `hr-dashboard@example.com`.
