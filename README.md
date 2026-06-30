#  Employee Portal

A simple, clean employee daily-report web app with role-based access. Employees log in, submit daily reports (tasks, blockers, mood check-in), and view their report history. Admins can view all employee reports and leave feedback on each one.

Built with vanilla **HTML, CSS, and JavaScript** — no frameworks, no build tools. Just open it in a browser.

---

## ✨ Features

### Employee
- 🔐 **Login system** — username/password auth with "Remember Me"
- 📝 **Daily report submission** — date, shift, tasks completed, blockers, mood check-in
- 📊 **Report archive** — searchable, filterable, paginated table of submitted reports
- 📄 **Report details** — view full task/blocker text and any admin feedback for a report
- 🚪 **Logout** — clears session and returns to login

### Admin
- 🛡️ **Admin login** — same login page, recognized via a special admin account
- 👥 **View all employee reports** — extended archive table showing employee name and feedback status
- 💬 **Leave feedback** — open any report and write feedback, saved directly to that report
- ✅ **Feedback status badges** — see at a glance which reports have been reviewed (Given / Pending)

### General
- 💾 **Persistent storage** — all data saved locally via `localStorage` / `sessionStorage` (no backend required)

---

## 🛠️ Tech Stack

- **HTML5** — structure
- **CSS3** — custom styling per page
- **Bootstrap 5** — base utilities and responsiveness
- **JavaScript (ES6+)** — auth simulation, role-based rendering, form handling, dynamic table rendering, localStorage persistence

---

## 📁 Project Structure

```
workflow-employee-portal/
├── login.html              # Login page (employee + admin)
├── dashboard.html          # Employee dashboard (submit daily report)
├── archive.html            # Report history (view changes based on role)
├── archive-detail.html     # Full report detail + admin feedback
├── styles/
│   ├── login.css
│   ├── dashboard.css
│   ├── archive.css
│   └── archive-detail.css
└── README.md
```

---

## 🚀 Getting Started

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/workflow-employee-portal.git
   ```
2. Open `login.html` in your browser — that's it, no installation needed.

### Demo Logins

| Role     | Username     | Password   |
|----------|--------------|------------|
| Employee | `nargesAmam` | `1234`     |
| Admin    | `admin`      | `admin123` |

---

## 📌 How It Works

- Submitting a report on the **Dashboard** saves it into a `wf_reports` array in `localStorage`.
- The **Archive** page reads that array and renders it as a table, with search and date filtering.
  - Logged in as an **employee** → see only the standard report columns.
  - Logged in as **admin** → see additional Employee and Feedback columns.
- Clicking any row opens **Report Details**:
  - **Admin** sees a feedback box to write/save feedback on that specific report.
  - **Employee** sees any feedback left by the admin, read-only.
- Logging out clears the stored user session and redirects to the login page.

---

## 🔄 Resetting Data

To clear all saved reports/sessions during testing, open the browser console and run:
```javascript
localStorage.clear();
sessionStorage.clear();
```

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
