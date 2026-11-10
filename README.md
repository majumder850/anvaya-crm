# Anvaya CRM — Frontend

A single-page CRM application built with React, Bootstrap, and React Router to track sales pipelines, monitor lead stages, assign agents, and analyze closure rates.

Connected to a REST backend deployed on Vercel backed by MongoDB.

---

## Live Links & Repositories

- **Live App:** [anvaya-crm.vercel.app](https://anvaya-crm.vercel.app)
- **Frontend Repo:** [github.com/majumder850/anvaya-crm](https://github.com/majumder850/anvaya-crm)
- **Backend API:** [anvaya-crm-phase-2.vercel.app](https://anvaya-crm-phase-2.vercel.app)
- **Backend Repo:** [github.com/majumder850/anvaya-crm-backend](https://github.com/majumder850/anvaya-crm-backend)

---

## Core Features

- **Dashboard:** Overview cards showing total leads grouped across all 5 stages (`New`, `Contacted`, `Qualified`, `Proposal Sent`, `Closed`) with quick toggle filters and recent leads.
- **Lead Directory & Filters:** View all leads with real-time filtering by status, source, sales rep, and tags. Supports sorting by priority or time-to-close. Filters are synchronized with URL query params via `useSearchParams`.
- **Lead Detail & Activity Log:** Edit lead details directly in place (reassign agents, update priority, add tags). Includes an activity feed for logging timestamped comments and progress updates.
- **Custom Pipeline Views:**
  - Status breakdown page to inspect pipeline stages independently.
  - Dedicated agent view to evaluate performance and assigned leads per rep.
- **Agent Directory:** Manage sales reps and register new team members.
- **Reports & Metrics:** Visual reports tracking total pipeline volume, closed lead counts, agent distribution, and 7-day closing velocity.
- **UI/UX:** Fully responsive layout with mobile drawer navigation and non-blocking toast notifications for CRUD actions.

---

## Tech Stack

- **Client:** React 19, React Router v7, Bootstrap 5
- **Server:** Node.js, Express.js
- **Database:** MongoDB & Mongoose
- **Deployment:** Vercel

---

## API Reference

Base Endpoint: `https://anvaya-crm-phase-2.vercel.app/api`

### 1. Leads

- `GET /leads` — Fetch all leads
- `POST /leads` — Create a lead (`name`, `source`, `salesAgent`, `status`, `priority`, `timeToClose`, `tags`)
- `GET /leads/:id` — Fetch a single lead by ID
- `PUT /leads/:id` — Update lead properties
- `DELETE /leads/:id` — Remove a lead

### 2. Comments & Activity

- `GET /leads/:id/comments` — Get comment thread for a lead
- `POST /leads/:id/comments` — Add a comment (`commentText`, `author`)

### 3. Sales Agents

- `GET /agents` — Fetch all sales agents
- `POST /agents` — Add a new sales agent (`name`, `email`)

### 4. Reports

- `GET /report/pipeline` — Get active lead counts (excluding closed)
- `GET /report/last-week` — Get leads closed within the last 7 days

---

## Quick Start

### Frontend Setup

Clone the repo and install dependencies:

bash
git clone [https://github.com/majumder850/anvaya-crm.git](https://github.com/majumder850/anvaya-crm.git)
cd anvaya-crm
npm install

## 📬 Contact

**Debojyoti Majumder**

- **GitHub:** [@majumder850](https://github.com/majumder850)
- **Email:** [debojyotimajumder850@gmail.com](mailto:debojyotimajumder850@gmail.com)
- **Project Repository:** [https://github.com/majumder850/anvaya-crm](https://github.com/majumder850/anvaya-crm)
- **Live Demo:** [https://anvaya-crm-front-end.vercel.app](https://anvaya-crm-front-end.vercel.app)
