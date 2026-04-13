# 💸 Expense Tracker

A responsive, feature-rich personal finance web application to manage your budget, track expenses, and visualize spending patterns — all in the browser, no backend required.

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat-square&logo=chartdotjs&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Screenshots](#screenshots)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
  - [Option 1 — Open Directly in Browser](#option-1--open-directly-in-browser)
  - [Option 2 — VS Code Live Server](#option-2--vs-code-live-server)
  - [Option 3 — Docker](#option-3--docker)
- [Usage Guide](#usage-guide)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

Expense Tracker is a pure front-end web application built with Vanilla JavaScript, HTML5, and TailwindCSS. It provides an interactive personal finance dashboard where users can set a budget, log income and expenses by category, and visualize their financial data through multiple chart types. Reports can be exported as PDF or CSV with a single click.

---

## Features

**Budget Management**
- Set a total budget and track the remaining balance in real time
- Receive visual alerts when spending approaches or exceeds the budget

**Income Tracking**
- Add income entries with a category and description
- Categories: Salary, Business, Freelance, Investment, Other

**Expense Tracking**
- Log expenses with a category, description, and amount
- Delete individual entries from the list
- Categories: Food, Transportation, Shopping, Bills, Entertainment, Other

**Interactive Dashboard**
- Real-time remaining budget, total income, and total expense overview
- **Doughnut chart** — budget vs. expenses vs. income breakdown
- **Bar chart** — comparative view of budget, income, and expenses
- **Line chart** — income vs. expense trend over time

**Export**
- Download a snapshot of the full dashboard as a **PDF** (via html2canvas + jsPDF)
- Export all transaction data as a **CSV** file

**Other**
- Financial quote of the day with a refresh button
- Contact form with an embedded Google Maps location
- Fully **responsive** layout — works on mobile, tablet, and desktop
- Sticky navigation with hamburger menu on mobile

---

## Screenshots

> Add screenshots of your dashboard here by uploading images to the `assests/` folder and referencing them below.

```
assests/
└── screenshot.png   ← replace with your actual screenshot filenames
```

---

## Tech Stack

| Technology | Purpose |
|---|---|
| **HTML5** | App structure and markup |
| **Tailwind CSS** (CDN) | Utility-first responsive styling |
| **Vanilla JavaScript** | All app logic and DOM manipulation |
| **Chart.js** | Doughnut, bar, and line chart rendering |
| **html2canvas** | Capturing the dashboard as a canvas snapshot |
| **jsPDF** | Converting the canvas snapshot to a downloadable PDF |
| **nginx:alpine** | Serving the static app inside Docker |
| **Docker & Docker Compose** | Containerised deployment |
| **GitHub Actions** | CI/CD workflow automation |

---

## Project Structure

```
expenseTrackerApp/
├── .github/
│   └── workflows/         # GitHub Actions CI/CD pipelines
├── assests/               # Images and static assets
├── index.html             # Main app — all sections and layout (545 lines)
├── script.js              # All JavaScript logic
├── style.css              # Custom styles (used alongside Tailwind)
├── Dockerfile             # nginx:alpine serving static files on port 80
├── docker-compose.yml     # Docker Compose configuration
├── package-lock.json
├── LICENSE
└── README.md
```

---

## Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Edge, etc.)
- [Docker](https://www.docker.com/get-started) — only if running via Docker
- [VS Code](https://code.visualstudio.com/) with the Live Server extension — optional

---

### Option 1 — Open Directly in Browser

```bash
# 1. Clone the repository
git clone https://github.com/AnkitKumarChoudhary/expenseTrackerApp.git

# 2. Navigate into the project
cd expenseTrackerApp

# 3. Open index.html in your browser
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

---

### Option 2 — VS Code Live Server

1. Open the project folder in VS Code
2. Install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension
3. Right-click `index.html` → **Open with Live Server**
4. The app will open at `http://127.0.0.1:5500`

---

### Option 3 — Docker

```bash
# 1. Clone the repository
git clone https://github.com/AnkitKumarChoudhary/expenseTrackerApp.git
cd expenseTrackerApp

# 2. Build and run with Docker Compose
docker-compose up --build

# 3. Open in your browser
# http://localhost:80
```

To stop the container:

```bash
docker-compose down
```

The Dockerfile uses `nginx:alpine` to serve the static files on port 80 — no Node.js or build step required.

---

## Usage Guide

1. **Set your budget** — Navigate to the Budget section and enter your total budget amount.
2. **Add income** — Choose a category (Salary, Freelance, etc.), add a description, and enter the amount.
3. **Add expenses** — Choose a category (Food, Bills, etc.), add a description, and enter the amount.
4. **View the dashboard** — The doughnut, bar, and line charts update in real time as you add entries.
5. **Export your report** — Click **Download PDF** to save a snapshot of the dashboard, or **Download CSV** to export your transaction data.
6. **Get inspired** — Click **Enlighten Me** in the Quotes section for a new financial quote.

---

## Contributing

Contributions are welcome! To get started:

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Make your changes and commit: `git commit -m "feat: describe your change"`
4. Push to your fork: `git push origin feature/your-feature-name`
5. Open a Pull Request

---

## License

This project is licensed under the [MIT License](LICENSE).

---

<div align="center">
  Made by <a href="https://github.com/AnkitKumarChoudhary">Ankit Kumar Choudhary</a>
</div>
