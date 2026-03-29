<div align="center">
  <img src="https://github.com/n0tsahil/Plan.it/blob/main/client/public/favicon.png" alt="Plan.it Logo" width="60" height="60"/>
</div>

<h1 align="center">Plan.it</h1>
<p align="center"><b>B2B Project Management Platform for Modern Teams</b></p>

<div align="center">
  <a href="https://plan-it-lac.vercel.app/" target="_blank">
    <img src="https://img.shields.io/badge/🚀%20Live%20Demo-Visit%20Site-blue?style=for-the-badge&logo=vercel" alt="Live Demo"/>
  </a>
</div>

<br>

Plan.it is a **scalable B2B SaaS project management platform** that enables teams to manage workspaces, projects, and tasks with role-based access control.  
Built with **TypeScript, React.js, Node.js, Express.js, and MongoDB**, Plan.it demonstrates a production-grade multi-tenant architecture with Google OAuth authentication.

---

## 🚀 Features

- **Multi-Tenant Workspaces**
  - Create and manage multiple workspaces with isolated data per organization.

- **Project & Task Management**
  - Organize work into projects and tasks with statuses, priorities, and assignments.

- **Role-Based Access Control**
  - Fine-grained permissions with Owner, Admin, and Member roles per workspace.

- **Google OAuth Authentication**
  - Seamless sign-in with Google via **Passport.js** and secure session management.

- **RESTful API Architecture**
  - Clean, modular backend with Express.js and MongoDB for scalable data handling.

- **Responsive UI**
  - Modern, mobile-first design with **React.js**, **Tailwind CSS**, and **shadcn/ui**.

- **Type-Safe Codebase**
  - End-to-end **TypeScript** for reliability and developer experience.

---

## 🛠️ Tech Stack

- **Frontend:** React.js, TypeScript, Tailwind CSS, shadcn/ui, Vite
- **Backend:** Node.js, Express.js, TypeScript
- **Database:** MongoDB, Mongoose
- **Auth:** Passport.js, Google OAuth 2.0, express-session
- **Validation:** Zod
- **Deployment:** Vercel (Frontend), Render (Backend)
- **Developer Tools:** GitHub, Postman, Figma

---

## 📂 Project Structure

```
Plan.it/
│── client/                   # Frontend (React + Tailwind)
│   ├── src/
│   │   ├── components/       # Reusable UI components
│   │   ├── pages/            # Route-level pages
│   │   ├── hooks/            # Custom React hooks
│   │   ├── lib/              # Axios instance, utilities
│   │   └── types/            # TypeScript types
│── backend/                  # Backend (Express + Node)
│   ├── src/
│   │   ├── config/           # App, DB, Passport config
│   │   ├── controllers/      # Request handlers
│   │   ├── middlewares/      # Auth, error handling
│   │   ├── models/           # Mongoose schemas
│   │   ├── routes/           # API endpoints
│   │   ├── services/         # Business logic
│   │   ├── utils/            # Helpers & utilities
│   │   └── validation/       # Zod schemas
│── README.md                 # Documentation
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/n0tsahil/plan-it.git
cd plan-it
```

### 2. Install Dependencies

For backend:
```bash
cd backend
npm install
```

For frontend:
```bash
cd client
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the `backend` directory:

```ini
PORT=8000
NODE_ENV=development
APP_ENV=development

MONGO_URI=your_mongodb_connection_string

SESSION_SECRET=your_session_secret
SESSION_EXPIRES_IN=1d

GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
GOOGLE_CALLBACK_URL=http://localhost:8000/api/auth/google/callback

FRONTEND_ORIGIN=http://localhost:5173
FRONTEND_GOOGLE_CALLBACK_URL=http://localhost:5173/google/callback

BASE_PATH=/api
```

Create a `.env.local` file in the `client` directory:

```ini
VITE_API_BASE_URL=http://localhost:8000/api
```

### 4. Seed the Database

Run the role seeder before starting the server:
```bash
cd backend
npm run seed
```

### 5. Run Development Servers

Backend:
```bash
cd backend
npm run dev
```

Frontend:
```bash
cd client
npm run dev
```

---

## 🌐 Deployment

| Service | Platform | URL |
|---------|----------|-----|
| Frontend | Vercel | [plan-it-lac.vercel.app](https://plan-it-lac.vercel.app) |
| Backend | Render | [plan-it-gpw3.onrender.com](https://plan-it-gpw3.onrender.com) |
| Database | MongoDB Atlas | Cloud hosted |

**Environment variables** must be configured in both Vercel and Render dashboards before deployment.  
Make sure to update `GOOGLE_CALLBACK_URL` and `FRONTEND_ORIGIN` to production URLs.

---

## 📌 Use Cases

- **Startups** → Manage team projects and tasks in one place.
- **Agencies** → Separate workspaces per client with role-based access.
- **Remote Teams** → Collaborate across projects with clear ownership and assignments.
- **Freelancers** → Organize personal and client work efficiently.

---

## 🤝 Contributing

Contributions are welcome!

1. Fork this repo
2. Create a new branch (`feature/your-feature`)
3. Commit your changes
4. Open a Pull Request

---

## 📄 License

This project is intended for **personal/academic use only**.  
All rights reserved © 2026 Sahil Chauhan.
