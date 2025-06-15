# 🔌 API & Firestore Structure

This document outlines the internal Firestore structure and API-like access logic used in the Interactive HR Dashboard.

---

## 🔐 Authentication

- Firebase Auth
- Provider: Google (OAuth2)
- On login, user info is stored in Firestore in `user_settings`

---

## 🧱 Firestore Collections

### `employees`
Stores employee records.

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "department": "Engineering",
  "startDate": "2024-01-15",
  "status": "active"
}
```

### `employee_history`
Tracks historical snapshots of employee changes.

```json
{
  "employeeId": "123",
  "changedBy": "admin@example.com",
  "changes": {
    "status": ["active", "terminated"]
  },
  "timestamp": "2025-05-10T14:20:00Z"
}
```

### `logs`
Action logs from any user operation (view, update, export).

```json
{
  "action": "export",
  "target": "logs",
  "email": "admin@example.com",
  "timestamp": "2025-06-12T10:45:00Z"
}
```

### `user_settings`
Used for onboarding, theme, and access control.

```json
{
  "uid": "...",
  "role": "admin", // or "team"
  "department": "HR",
  "onboarded": true,
  "darkMode": true
}
```

---

## 🧪 Query Examples

### Get employees in HR
```js
db.collection("employees").where("department", "==", "HR")
```

### Get logs by email
```js
db.collection("logs").where("email", "==", "john@example.com")
```

---

## 🔁 Realtime Updates

All collections use Firestore's `onSnapshot()` for live sync to the dashboard.

