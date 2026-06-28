# workflow-report-system

A simple, clean employee daily-report web app. Employees log in, submit a daily report (tasks, blockers, mood check-in), and view a searchable history of past reports.

Built with vanilla **HTML, CSS, and JavaScript** — no frameworks, no build tools. Just open it in a browser.

---

## ✨ Features

- 🔐 **Login system** — username/password auth with "Remember Me"
- 📝 **Daily report submission** — date, shift, tasks completed, blockers, mood check-in
- 📊 **Report archive** — searchable, filterable, paginated table of all submitted reports
- 🚪 **Logout** — clears session and returns to login
- 💾 **Persistent storage** — all data saved locally via `localStorage` / `sessionStorage` (no backend required)

---

## 🛠️ Tech Stack

- **HTML5** — structure
- **CSS3** — custom styling per page
- **Bootstrap 5** — base utilities and responsiveness
- **JavaScript (ES6+)** — auth simulation, form handling, dynamic table rendering, localStorage persistence

---

## 📁 Project Structure

```
workflow-employee-portal/
├── login.html          # Login page
├── index.html          # Employee dashboard (submit daily report)
├── archive.html         # Team report history
├── styles/
│   ├── login.css
│   ├── dashboard.css
│   └── archive.css
└── README.md
```

---

## 🚀 Getting Started

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/workflow-employee-portal.git
   ```
2. Open `login.html` in your browser — that's it, no installation needed.

### Demo Login
| Username     | Password |
|--------------|----------|
| `nargesAmam` | `1234`   |

---

## 📌 How It Works

- Submitting a report on the **Dashboard** saves it into a `wf_reports` array in `localStorage`.
- The **Archive** page reads that array and renders it as a table, with search and date filtering.
- Logging out clears the stored user session and redirects to the login page.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
