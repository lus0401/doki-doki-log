# doki-doki-log

**Heartbeat logger for devs—turn emotions into pull requests ❤️**

---

## TL;DR

`doki-doki-log` is a dev-centric emotional event tracker that logs your feelings as structured data and visualizes your emotional timeline. Alerts and automations included!

## ✨ Features

| Category          | Feature                                                  | Status        |
| ----------------- | -------------------------------------------------------- | ------------- |
| **Event Logger**  | Record emotional events via CLI/REST (JSON)              | ⏳ In progress |
| **Alert Engine**  | Alerts based on intensity/pattern via GitHub Issue/Slack | 🔜 Planned    |
| **Timeline UI**   | GitHub Pages with React heatmap/timeline                 | 🔜 Planned    |
| **GitHub Native** | Auto-generate Pull Requests per emotion entry            | ⏳ MVP stage   |
| **Multi-Heart**   | Track multiple targets (e.g. "Hoik Log") independently   | 🖋️ Drafting  |
| **Scheduler**     | CRON reminders ("Did you log your heart today?")         | 🖋️ Drafting  |

## 💠 Tech Stack

| Layer        | Stack                                                |
| ------------ | ---------------------------------------------------- |
| Backend      | Node.js (Express) · SQLite/Postgres · Prisma         |
| API          | REST+JSON (OpenAPI) → Webhook, future GraphQL option |
| Frontend     | React 18 · TypeScript · Vite · TailwindCSS           |
| Infra        | GitHub Actions CI/CD → Pages · Docker Compose        |
| Notification | GitHub Issues/PRs, Slack Webhook, Email              |

## 📦 Data Model (v0)

```jsonc
{
  "id": "uuid",
  "timestamp": "2025-06-08T15:04:05.000Z",
  "subject": "string // person/situation",
  "emotion": "Enum('💗','😱','🚤', '😢', '😂')",
  "intensity": 0,
  "notes": "string // optional memo"
}
```

## 🚀 Getting Started

```bash
# 1. Clone
$ git clone https://github.com/<YOUR_ID>/doki-doki-log.git
$ cd doki-doki-log

# 2. Install dependencies
$ npm install

# 3. Run dev server (Vite)
$ npm run dev
# Open http://localhost:5173 in your browser
```

## 🗺️ Roadmap

### Phase 1: MVP

* [ ] Emotional event logger API (Node.js + Express)
* [ ] Basic CLI to log emotions
* [ ] GitHub PR generation for each log

### Phase 2: Visualization & Notifications

* [ ] Timeline chart (heatmap or line)
* [ ] GitHub Issue/Slack alerts based on intensity
* [ ] Multi-user support (OAuth + tagging)

### Phase 3: Productization

* [ ] GitHub Pages UI with emotion dashboard
* [ ] Mobile PWA for on-the-go logging
* [ ] Emotion analytics → auto-generated love letter 📝

### Phase 4: Expansion

* [ ] Multiple trackers (e.g. crush logs, team vibes, self-tracking)
* [ ] Collaboration mode (shared logs)
* [ ] AI assistant for emotion trend analysis

## 🤝 Contributing

Pull requests welcome! Please open an `issue` first for feature suggestions or bug reports. Fork the repo, create a new branch, and follow our basic linting rules (ESLint + Prettier).

## 📄 License

MIT © 2025 Hailey Lee
