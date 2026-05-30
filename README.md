<div align="center">

# 🏠 FixItNow — Location Based Household Management System

**Your One-Stop Solution for All Home Service Needs**

[![Node.js](https://img.shields.io/badge/Node.js-18+-339933?logo=node.js&logoColor=white)](https://nodejs.org)
[![Express](https://img.shields.io/badge/Express-5.2-000000?logo=express&logoColor=white)](https://expressjs.com)
[![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)](https://react.dev)
[![Vite](https://img.shields.io/badge/Vite-7.2-646CFF?logo=vite&logoColor=white)](https://vitejs.dev)
[![MongoDB](https://img.shields.io/badge/MongoDB-9.0-47A248?logo=mongodb&logoColor=white)](https://www.mongodb.com)
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4.0-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com)
[![Leaflet](https://img.shields.io/badge/React%20Leaflet-5.0-199900?logo=leaflet&logoColor=white)](https://react-leaflet.js.org)
[![License](https://img.shields.io/badge/License-ISC-blue.svg)]()

---

<p align="center">
  <b>🔧 Plumbing</b> &nbsp;•&nbsp; <b>⚡ Electrical</b> &nbsp;•&nbsp; <b>🔨 Home Repairs</b> &nbsp;•&nbsp; <b>❄️ AC Repair</b> &nbsp;•&nbsp; <b>🆘 Emergency Services</b>
</p>

</div>

---

## 📖 About

**FixItNow** connects homeowners with verified, location-aware service professionals. Whether you need a plumber, electrician, or emergency repair, our platform makes it easy to find, book, and manage trusted home services — all from your dashboard.

> **Built with:** Node.js + Express + MongoDB (backend) · React + Vite + TailwindCSS (frontend)

---

## ✨ Features

### 👤 For Homeowners
| Feature | Description |
|---------|-------------|
| 🔐 **Secure Auth** | Register/Login with JWT-based authentication |
| 📍 **Location Discovery** | Find nearby service providers using interactive maps |
| 📋 **Service Catalog** | Browse all available services with details & pricing |
| 📅 **Easy Booking** | Book services at your preferred date & time |
| 📊 **User Dashboard** | Track all your bookings in one place |
| ⭐ **Verified Pros** | All professionals undergo background checks |
| 💰 **Transparent Pricing** | Know costs upfront — no surprises |
| 🆘 **24/7 Emergency** | Round-the-clock support for urgent repairs |

### 🛠️ For Administrators
| Feature | Description |
|---------|-------------|
| 👥 **User Management** | View, edit, and manage all users |
| 🔧 **Service Management** | Add, update, or remove services |
| 📦 **Booking Oversight** | Monitor and manage all bookings |
| 📞 **Contact Management** | Review inquiries from the contact form |

---

## 🚀 Quick Start

### Prerequisites
- **Node.js** >= 18
- **npm** >= 9
- **MongoDB** — local instance or [MongoDB Atlas](https://www.mongodb.com/atlas) (free tier)

### 1️⃣ Clone & Install

```bash
# Clone the repository
git clone https://github.com/Abhi-424/Location-Based-Household-Management-System.git
cd Location-Based-Household-Management-System

# Install backend dependencies
cd backend
npm install

# Install frontend dependencies
cd ../frontend
npm install
```

### 2️⃣ Configure Environment

<details>
<summary><b>Backend — <code>backend/.env</code></b></summary>

```env
PORT=5000
MONGO_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<database>?retryWrites=true&w=majority
JWT_SECRET=your_secure_random_secret_key_here
FRONTEND_URL=http://localhost:5173
```
</details>

<details>
<summary><b>Frontend — <code>frontend/.env</code></b></summary>

```env
VITE_API_BASE_URL=http://localhost:5000/api
```
</details>

### 3️⃣ Run

```bash
# Terminal 1 — Backend
cd backend
npm run dev

# Terminal 2 — Frontend
cd frontend
npm run dev
```

Open **http://localhost:5173** in your browser. 🎉

### 4️⃣ (Optional) Seed the Database

```bash
cd backend
node seedData.js      # Populate services
node seedServices.js  # Additional services
```

---

## 📁 Project Structure

```
FixItNow/
├── backend/                         # 🖥️ API Server (Express + MongoDB)
│   ├── src/
│   │   ├── config/
│   │   │   └── db.js               # MongoDB connection
│   │   ├── controllers/
│   │   │   ├── adminController.js
│   │   │   ├── authController.js
│   │   │   ├── bookingController.js
│   │   │   ├── contactController.js
│   │   │   ├── serviceController.js
│   │   │   └── userController.js
│   │   ├── middlewares/
│   │   │   ├── authMiddleware.js
│   │   │   └── errorMiddleware.js
│   │   ├── models/
│   │   │   ├── Booking.js
│   │   │   ├── Service.js
│   │   │   ├── User.js
│   │   │   └── contactModel.js
│   │   ├── routes/
│   │   │   ├── adminRoutes.js
│   │   │   ├── authRoutes.js
│   │   │   ├── bookingRoutes.js
│   │   │   ├── contactRoutes.js
│   │   │   ├── serviceRoutes.js
│   │   │   └── userRoutes.js
│   │   ├── services/
│   │   ├── scripts/
│   │   ├── app.js                  # Express app setup
│   │   └── server.js               # Entry point
│   ├── package.json
│   └── .env.example
│
├── frontend/                        # 🎨 Client App (React + Vite)
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   │   └── hero-slider/        # Hero section images
│   │   ├── components/
│   │   │   ├── auth/
│   │   │   ├── common/
│   │   │   ├── dashboard/
│   │   │   ├── services/
│   │   │   ├── LocationPicker.jsx
│   │   │   └── Map.jsx
│   │   ├── context/
│   │   │   └── AuthContext.jsx
│   │   ├── hooks/                   # Custom React hooks
│   │   ├── pages/
│   │   │   ├── About.jsx
│   │   │   ├── BookService.jsx
│   │   │   ├── Contact.jsx
│   │   │   ├── Home.jsx
│   │   │   ├── NotFound.jsx
│   │   │   └── Services.jsx
│   │   ├── routes/
│   │   ├── services/
│   │   │   ├── api.js               # Axios instance with interceptors
│   │   │   └── authService.js
│   │   ├── utils/
│   │   ├── App.jsx
│   │   ├── App.css
│   │   ├── index.css
│   │   └── main.jsx
│   ├── index.html
│   ├── vite.config.js
│   ├── eslint.config.js
│   ├── package.json
│   └── .env.example
│
├── test-admin-apis.html
└── README.md
```

---

## 🌐 API Reference

| Method | Endpoint                | Description              | Auth Required |
|--------|-------------------------|--------------------------|:---:|
| POST   | `/api/auth/login`       | User login               | ❌  |
| POST   | `/api/auth/register`    | User registration        | ❌  |
| GET    | `/api/services`         | List all services        | ❌  |
| GET    | `/api/services/:id`     | Get service details      | ❌  |
| POST   | `/api/bookings`         | Create a booking         | ✅  |
| GET    | `/api/bookings`         | Get user's bookings      | ✅  |
| POST   | `/api/contact`          | Submit contact form      | ❌  |
| GET    | `/api/admin/users`      | List all users (admin)   | ✅  |
| GET    | `/api/admin/bookings`   | List all bookings (admin)| ✅  |
| GET    | `/api/users/profile`    | Get user profile         | ✅  |
| PUT    | `/api/users/profile`    | Update user profile      | ✅  |

---

## 🧰 Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| [React 19](https://react.dev) | UI library |
| [Vite 7](https://vitejs.dev) | Build tool & dev server |
| [TailwindCSS 4](https://tailwindcss.com) | Utility-first CSS framework |
| [React Router DOM 7](https://reactrouter.com) | Client-side routing |
| [React Leaflet](https://react-leaflet.js.org) | Interactive maps |
| [Axios](https://axios-http.com) | HTTP client with interceptors |

### Backend
| Technology | Purpose |
|------------|---------|
| [Node.js](https://nodejs.org) | JavaScript runtime |
| [Express 5](https://expressjs.com) | Web framework |
| [MongoDB + Mongoose 9](https://mongoosejs.com) | Database & ODM |
| [JWT (jsonwebtoken)](https://jwt.io) | Authentication tokens |
| [bcryptjs](https://github.com/dcodeIO/bcrypt.js) | Password hashing |
| [Morgan](https://github.com/expressjs/morgan) | HTTP request logging |
| [Nodemon](https://nodemon.io) | Dev auto-restart |

---

## 🤝 Contributing

Contributions are welcome! Here's how:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

---

## 📄 License

Distributed under the **ISC License**. See `LICENSE` for more information.

---

<div align="center">

Made with ❤️ by [Abhi-424](https://github.com/Abhi-424)

⭐ **Star this repo** if you found it useful!

</div>
