# 🧠 Task Manager App (MERN Stack)

A full-featured Task Management web app with user authentication, task CRUD operations, and Smart Task Assignment logic.

## 🌐 Live Link

> ❗ Deployment is in progress. This app is currently being submitted for evaluation.

## 📂 Project Structure


## ✅ Features

- 🔐 User Authentication (Register, Login, JWT)
- 🧾 Add, Update, Delete, and Mark Tasks as Complete
- 🌈 Responsive UI with Tailwind CSS and Glassmorphism
- 📋 Tasks displayed only for logged-in users
- 💡 Smart Task Assignment logic (see below)

---

## 🤖 Smart Task Assignment Logic

> Added in `/server/utils/smartAssign.js`

This function simulates assigning tasks intelligently based on user's past activity (e.g., fewer active tasks). Used to simulate scalable team distribution in future.

```js
function smartAssign(userTasks) {
  // Placeholder for load-balancing logic
  const pendingTasks = userTasks.filter(t => !t.completed);
  if (pendingTasks.length < 5) return true;
  return false;
}
