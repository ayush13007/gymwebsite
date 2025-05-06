
# GymZone — Full-Stack Production-Ready Gym Booking Platform

## 📌 Project Overview
GymZone is a full-featured gym website built with the MERN stack (MongoDB, Express, React, Node.js) plus premium UI components, 3D visualizations, and robust backend integrations.

This platform allows users to:
- Browse gyms with 3D tours
- View fitness dashboards
- Register, login, and manage accounts
- Book gym slots and services
- Pay online securely
- Use a modern, responsive interface

---

## 🧱 Tech Stack

| Layer       | Tools Used                             |
|------------|-----------------------------------------|
| Frontend    | React, Redux Toolkit, ShadCN UI, Three.js, Barba.js, TailwindCSS |
| Backend     | Node.js, Express.js, MongoDB, Mongoose |
| Auth        | JWT (JSON Web Tokens)                  |
| Payments    | Razorpay                               |
| DevOps (Planned) | Docker, CI/CD, Vercel (frontend), Render/AWS (backend) |

---

## 📁 Project Structure (Frontend)

```
src/
├── components/ # ShadCN reusable UI components
├── pages/ # Home, Login, Register, Dashboard, Gyms
├── hooks/ # Custom React hooks
├── store/ # Redux Toolkit slices
├── utils/ # API services, helper functions
├── ThreeDGymView.tsx # Three.js 3D Gym Visualization
├── CalendarIntegration.tsx # Booking calendar
├── Layout.tsx, Navbar.tsx, Footer.tsx
```

## 🌐 Pages

- `/` → Landing Page
- `/login` → Login with JWT Auth
- `/register` → Sign up
- `/dashboard` → User dashboard (calendar, fitness stats)
- `/gyms` → List of gyms + 3D previews + slot booking
- `/notfound` → 404 handler

---

## 🔐 Auth Flow (Frontend)
- On login/register, receive JWT token.
- Token is stored securely (HttpOnly cookie or localStorage).
- Axios instance includes token in headers for protected routes.

---

## 🔧 Backend Requirements (To Be Implemented)

### 1. API Endpoints

| Route | Method | Description |
|-------|--------|-------------|
| `/api/auth/login` | POST | Login user |
| `/api/auth/register` | POST | Register user |
| `/api/user` | GET | Get profile |
| `/api/gyms` | GET | List gyms |
| `/api/gyms/:id` | GET | Gym details |
| `/api/bookings` | POST | Book gym slot |
| `/api/payments` | POST | Razorpay integration |

### 2. Models

- User: name, email, password, bookings[]
- Gym: name, location, description, images[], 3D data
- Booking: userId, gymId, date, slot
- Payment: userId, amount, status

---

## 📦 Dev Instructions

### Frontend Setup
```bash
npm install
npm run dev
```

### Backend Setup (To Be Built)
```bash
npm install
npm run dev
```

## 🛡️ Security & Production Checklist
- ☑️ JWT Authentication
- ☑️ Input validation (backend)
- ☑️ HTTPS (enforced via Vercel/AWS)
- ☑️ Secure payment gateway (Razorpay)
- ☑️ Docker & CI/CD Pipeline
- ☑️ Analytics (Google or Plausible)

## 🎯 Final Outcome
A sleek, fast, and secure gym platform ready for deployment, offering full user interactivity, booking system, and monetization support.

## 👨‍💻 Tasks for Developer
Below is the summarized list of what you need to implement to complete this project.

### 🔧 Backend Tasks
- [ ] Build Node.js + Express backend
- [ ] Create MongoDB models for User, Gym, Booking
- [ ] Setup JWT-based Auth routes
- [ ] Build REST API endpoints (see above)
- [ ] Integrate Razorpay for booking payments
- [ ] Deploy backend on Render or AWS

### 🔗 Frontend Integration
- [ ] Connect all APIs using createAsyncThunk
- [ ] Manage auth state via Redux
- [ ] Display bookings & user data in Dashboard
- [ ] Trigger Razorpay payments on slot booking

❗This project is inspired by the structure of MakeMyTrip and combines Gym features with booking, location view, and 3D immersion. You must follow clean code and scalable practices.

## 🙋 No Questions Needed — Everything is Above.
Build using this README. Stick to the stack. Think like MakeMyTrip, but for gyms.
