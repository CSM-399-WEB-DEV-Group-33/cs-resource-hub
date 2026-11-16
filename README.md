# CS Resource Hub

> **A Structured Learning and Resource Platform for KNUST Computer Science Students**  
> Capstone Project — **CSM 399: Web-Based Concepts and Development** (Group 33)

---

## Overview

Computer Science undergraduates at KNUST (Levels 100–400) often rely on fragmented WhatsApp groups, Telegram channels, and personal Google Drives to find study materials. In those channels, past questions and slides get buried quickly, version control is nonexistent, and there are no guided learning paths or organized peer Q&A.

**CS Resource Hub** consolidates curated academic resources into a single, searchable, responsive web application built with ReactJS, Bootstrap, SASS, and a JSON Server mock REST API.

---

## Core Features

1. **Resource Library** — Searchable, filterable directory of past questions, lecture slides, curated tutorial videos, and open-source CS textbooks rendered using React components, lists, and keys.
2. **Student Contributions Portal** — Interactive React form allowing students and teaching assistants to submit new external resource links into an approval queue for verification.
3. **Personalized Bookmarks** — One-click bookmarking for quick retrieval, with client-side state persisted via the **React Context API** and `localStorage`.
4. **Guided Learning Roadmaps** — Curated sequential learning paths across core CS domains (e.g., Data Structures & Algorithms, Web Development, AI) with local progress checkmarks.
5. **Resource Discussion Threads** — Targeted peer Q&A and clarification comments beneath individual resources.

---

## Academic Integrity Policy

To strictly adhere to the **KNUST Academic Code of Conduct and Ethics** (preventing unauthorized copying or redistribution of course materials), CS Resource Hub **exclusively links to externally hosted or open-source content** rather than storing or redistributing copyrighted files directly. All seeded records use verified public links and are clearly labeled.

---

## Technology Stack

| Layer | Technology | Purpose |
| :--- | :--- | :--- |
| **Frontend** | HTML5, CSS3, JavaScript (ES6+), ReactJS (Vite) | Component-based SPA, React Router, Hooks, Context API, Error Boundaries |
| **Styling & UI** | Bootstrap 5 + SASS (`_variables.scss`) | Responsive grid (mobile, tablet, desktop) and custom design tokens (`#5B21B6`, `#7C3AED`, `#F5F3FF`, `#10B981`) |
| **Mock Backend** | JSON Server / Node.js (`db.json`) | RESTful endpoints for resources, roadmaps, submissions, and discussion comments |
| **Version Control** | Git & GitHub Organization | Branch-based collaboration, Pull Request reviews, and issue tracking |

---

## Planned Repository Structure

```text
cs-resource-hub/
├── README.md                  # Project overview, setup guide, team roles, and milestones
├── CONTRIBUTING.md            # Branching workflow, PR rules, and QA bug log template
├── package.json               # Root scripts ("concurrently" for client + server)
├── docs/                      # Design Document assets, wireframes, and QA test logs
├── client/                    # ReactJS + Vite + Bootstrap + SASS frontend
│   ├── public/                # Static assets & favicon/logo
│   └── src/
│       ├── assets/            # Images and icons
│       ├── components/        # Navbar, ResourceCard, FilterPills, CommentThread, ErrorBoundary
│       ├── context/           # BookmarkContext.jsx & RoadmapProgressContext.jsx
│       ├── pages/             # Home, Roadmaps, Bookmarks, SubmitResource, ResourceDetail
│       ├── styles/            # _variables.scss & main.scss
│       ├── App.jsx
│       └── main.jsx
└── server/                    # Mock REST API
    ├── db.json                # Seeded resources, roadmaps, comments, and submissions
    └── server.js              # Optional custom JSON Server middleware
```

---

## Quick Start (Local Development)

> **Prerequisites:** Node.js (v18+) and npm installed.

1. **Clone the repository**
   ```bash
   gh repo clone CSM-399-WEB-DEV-Group-33/cs-resource-hub
   cd cs-resource-hub
   ```

2. **Install dependencies** (once `client/` and `server/` are scaffolded)
   ```bash
   npm install
   cd client && npm install
   cd ../server && npm install
   ```

3. **Run both frontend and mock API**
   ```bash
   # From the repository root (using concurrently)
   npm run dev
   ```
   - Frontend: `localhost:5173`
   - Mock API (`json-server`): `localhost:3001`

---

## Team Roster & Assigned Roles (Group 33)

| Member | Assigned Role | GitHub Handle | Core Responsibilities |
| :--- | :--- | :--- | :--- |
| **Kekeli Gideon Dogbey** | Project Manager (PM) | *Pending* | Team coordination, deadlines, weekly instructor updates, documentation |
| **Caleb Kwaku Aheto** | Front-End Developer | `@Caleb-Aheto` | UI architecture, React components, state management, repo setup |
| **Isaac Nicholas Yeboah** | Front-End Developer | `@inknick10` | Responsive layouts, Bootstrap/SASS integration, page views |
| **Ahmed Ibrahim Yenduupaab** | Front-End Developer | `@Ahmadeed-cyber` | Interactive forms, filtering, React Router & Context integration |
| **Anim-Awuah Gideon Peasah** | Back-End Developer | `@GideonAwuah` | JSON Server mock API, `db.json` schema, data seeding & CRUD routes |
| **Mansura Is-Haq Naamuleh** | Back-End Developer | *Pending* | API integration helpers, submission queue logic, data validation |
| **Raina Pryce Aye-Kumi** | UI/UX Designer | `@rainapryce4-source` | Wireframes, mockups, color palette, typography, navigation flow |
| **Abu-Bonsra Forson Benedictus** | Quality Assurance (QA) | `@beeff-Jeff-Epstein` | Functional & cross-browser testing, responsiveness checks, bug log |
| **Simeon Ose** | Quality Assurance (QA) | `@Artemisura` | Accessibility audits, edge-case testing, peer review verification |

---

## Milestones & Schedule

| Milestone | Deliverable | Target / Due Date | Status |
| :--- | :--- | :--- | :--- |
| **1. Project Proposal** | 1-page proposal (Problem, Audience, Features, Roles) | Friday, Nov 6, 2026 | Completed |
| **2. Design Document** | Desktop, tablet, and mobile wireframes + color/typography spec | Friday, Nov 27, 2026 | In Progress |
| **3. Development Phase** | Scaffold monorepo, build core features, weekly PM updates | Nov – Dec 2026 | Starting |
| **4. Testing & Review** | Peer code reviews, responsive QA, documented bug-fix log | Late Dec 2026 – Jan 2027 | Planned |
| **5. Final Presentation** | Live demo (Jan 11) + zipped files & reel (Jan 15) | Jan 11 – Jan 15, 2027 | Planned |
