<div align="center">

# 📓 **Byte Journal**
A modern, bilingual (EN + TR) full-stack blog platform built with **Next.js**, **Tailwind CSS**, **shadcn/ui**, **Reactbits**, **Express.js**, and **MongoDB** — featuring JWT authentication, dashboards, dark/light mode, and beautiful UI components.

---

### 🌐 **Live Demo**  
<em>(Coming Soon)</em>

### 📦 **Tech Stack**

</div>

---

## 🚀 **Features**

### 🎨 Frontend (Next.js + Tailwind + shadcn/ui)
- 🌍 **Internationalization** (EN + TR)
- 🌗 **Dark / Light mode** with persistence
- 🧩 UI built using **shadcn/ui** + **Reactbits**
- ⚡ App Router + Dynamic Routing (`posts/[slug]`)
- 🧭 SEO-ready blog structure
- 📱 Fully responsive layout

### 🔥 Backend (Express.js + MongoDB)
- 🔐 **JWT Authentication** (Login, Register)
- 🧑‍💻 **Role-Based Access Control** (`user`, `admin`)
- 📝 **Post Management** (CRUD for Admin)
- 🗂️ Mongoose models (User, Post, etc.)
- ⚡ Clean architecture: routes → controllers → models → middleware

---

## 🖥️ **Screenshots**
> _Coming soon: Admin dashboard, Post editor, Blog home, Dark mode, TR mode_

---

## 📁 **Project Structure**

```bash
byte-journal/
├── backend/
│   ├── src/
│   │   ├── models/
│   │   ├── controllers/
│   │   ├── routes/
│   │   ├── middleware/
│   │   └── server.js
│   └── package.json
│
└── frontend/
    ├── app/
    │   ├── (en)/       # English pages
    │   ├── (tr)/       # Turkish pages
    │   ├── admin/      
    │   ├── dashboard/
    │   ├── posts/[slug]/
    ├── components/     # shadcn + reactbits
    ├── styles/
    ├── public/
    └── package.json

🚀 Getting Started
1. Clone the repository
git clone https://github.com/<your-username>/byte-journal.git
cd byte-journal

⚙️ Backend Setup (/backend)
cd backend
npm install

Create a .env file:
MONGO_URI=mongodb://localhost:27017/byte-journal
JWT_SECRET=supersecretchangeme
PORT=8080

Run the server:
npm run dev

Backend runs at:
http://localhost:8080


🎨 Frontend Setup (/frontend)
cd frontend
npm install

Tailwind CSS Setup (already included)

tailwind.config.js

globals.css containing:

@tailwind base;
@tailwind components;
@tailwind utilities;


shadcn/ui setup (already included)

Components live in /components/ui

Uses Tailwind tokens + utilities

Add components anytime:

npx shadcn-ui add button

reactbits setup

Reactbits components imported directly:
import { Input } from "reactbits";


Create .env.local:
NEXT_PUBLIC_API_URL=http://localhost:5000


Run frontend:
npm run dev


Frontend runs at:
http://localhost:3000


🔐 Authentication Overview
Users register & login with email + password
Passwords hashed with bcrypt
JWT tokens generated on login/registration
Frontend stores token (e.g. localStorage)
Protected routes require:
Authorization: Bearer <token>

🔚 Auth Endpoints
POST /api/auth/register
POST /api/auth/login
GET  /api/auth/me


📰 Posts Overview
Each post includes:
title
content
image
slug
author (User reference)
tags
category
featured
archived
views
likes

🚌 Public Endpoints
GET /api/posts
GET /api/posts/:slug

👨‍💼 Admin-only Endpoints
GET    /api/posts/admin
POST   /api/posts/admin
PUT    /api/posts/admin/:id
DELETE /api/posts/admin/:id


❤️ Acknowledgements
Next.js
Tailwind CSS
shadcn/ui
reactbits
next-intl
Express.js
