# 📊 Interactive HR Dashboard

A full-featured, production-ready HR dashboard built with React, Firebase, and TailwindCSS.

## 🚀 Features

- 🔐 Role-based Google Auth (admin vs team members)
- 📈 Analytics (performance charts, department stats)
- 📁 CSV Import / Export + PDF
- 📜 Firestore logging with filters & pagination
- 🧑‍🤝‍🧑 Team dashboards filtered by department
- 🕓 Version control of records
- 🎨 Dark mode toggle
- 🚀 CI/CD via GitHub Actions + Firebase Hosting

## 📁 Project Structure

- `/components/ui` – UI components
- `/pages/dashboard.jsx` – Admin dashboard
- `/pages/team.jsx` – Team-scoped dashboard
- `/hooks` – Custom logic (e.g., onboarding)
- `/lib/firebase.js` – Firebase client

## 📦 Deploying

### Firebase

```bash
firebase login
firebase init
npm run build
firebase deploy
```

### Vercel

Connect GitHub > Import Project > Set environment keys > Deploy.

---

## 🛠 Built With

- React 18 + Vite or CRA
- Firebase (Auth, Firestore, Hosting)
- TailwindCSS
- Recharts
