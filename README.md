# 🤖 MunifAgent AI

### AI Voice Agent Management Platform

A responsive React and TypeScript application for configuring AI voice agents, reviewing call activity, managing users, and monitoring agent usage through role-based dashboards.

[**🌐 Live Demo**](https://munif-agent-ai.netlify.app/) · [**💻 Source Code**](https://github.com/aurangzaib22/munif-agent)

---

## 📖 Overview

**MunifAgent AI** is a frontend dashboard for interacting with an AI voice-agent service. The application includes separate admin and user views, agent configuration workflows, call logs, analytics, account onboarding, and calendar connection options.

> **Project scope:** This repository contains the **React frontend**. Voice-agent processing, call services, user data, analytics, and calendar authorization rely on external backend APIs that are not included in this repository. Certain features require a working backend and authenticated account.

## ✨ Key Features

- **AI agent management:** Create, view, update, and delete voice agents through API-connected forms and controls.
- **Role-based dashboards:** Separate admin and user dashboard experiences with protected routes.
- **Call insights:** Call logs, agent call history, activity details, and dashboard usage statistics.
- **Recordings and transcripts:** Frontend interfaces for displaying call-related information returned by the service.
- **Authentication:** Sign-in, sign-up, password recovery, onboarding, and account/profile pages.
- **Calendar connections:** Google and Outlook calendar authorization flows and connection-status checks.
- **Multilingual experience:** English and German UI translations using i18next with language detection.
- **Responsive interface:** Tailwind CSS layouts, forms, reusable React components, and notifications.
- **State and API handling:** Redux Toolkit for application state and Axios for authenticated REST API requests.

## 🛠️ Tech Stack

| Area | Technologies |
| --- | --- |
| Frontend | React 19, TypeScript |
| Styling | Tailwind CSS 4, Emotion |
| State management | Redux Toolkit, React Redux |
| Routing | React Router 7 |
| Forms | React Hook Form |
| API integration | Axios, REST APIs |
| Internationalization | i18next, React i18next |
| UI & notifications | Lucide React, React Icons, React Hot Toast, React Toastify |
| Build tooling | Vite 7, ESLint |

## 🚀 Getting Started

### Prerequisites

- Node.js and npm compatible with Vite 7
- Access to the relevant backend API for logged-in features

### 1. Clone the repository

```bash
git clone https://github.com/aurangzaib22/munif-agent.git
cd munif-agent
```

### 2. Install dependencies

```bash
npm install
```

### 3. Configure environment variables

Create a `.env.local` file in the project root:

```dotenv
VITE_API_URL=https://your-backend-api.example.com
```

Set `VITE_API_URL` to the API base URL supplied by your backend service. Without an available API, authentication, agent management, and live call data will not work.

> **Security:** The uploaded source also references `VITE_LANDING_PASSWORD`. Variables prefixed with `VITE_` are embedded in the browser bundle and **must never contain actual passwords or other secrets**. Remove any client-side password check used as a security boundary and enforce access control on the server. Review the existing `.env` file and Git history before publishing; do not commit credentials.

### 4. Run locally

```bash
npm run dev
```

Open the local address shown by Vite.

### 5. Build and preview

```bash
npm run build
npm run preview
```

### Optional: Lint source files

```bash
npm run lint
```

## 🗂️ Project Structure

```text
munif-agent/
├── public/                    # Public static assets
├── src/
│   ├── api/                   # Authentication, agent, dashboard, and user API calls
│   ├── assets/                # Images and media
│   ├── components/            # Reusable UI and landing-page components
│   │   ├── LandingPageComponents/
│   │   └── user/
│   ├── Interface/             # TypeScript data interfaces
│   ├── Language/              # English and German translation files
│   ├── pages/                 # Authentication, admin, user, agent, and call-log pages
│   ├── routes/                # Public and private route guards
│   ├── store/                 # Redux store and slices
│   ├── i18n.ts                # Translation initialization
│   ├── route.tsx              # Application routes
│   └── main.tsx               # React entry point
├── package.json
└── vite.config.ts
```

## 🔐 Authentication & Integrations

The app calls external REST endpoints for login, registration, agent records, call activity, analytics, plan usage, user profile details, and calendar connection flows. Private routes and role-based dashboard selection use authentication data from application state.

The code in this repository does **not** provide a standalone AI calling engine or backend server. API availability, account permissions, and environment configuration determine which live functions work in a local deployment.

## 🌐 Live Application

**Live Demo:** https://munif-agent-ai.netlify.app/

**GitHub Repository:** https://github.com/aurangzaib22/munif-agent

---

**MunifAgent AI** · React · TypeScript · Redux Toolkit · AI Voice Agent Management Interfaces
