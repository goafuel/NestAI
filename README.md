# 🪺 NestAI — Study Tracker & Productivity Dashboard

NestAI is a full-stack, AI-powered web app designed to supercharge student productivity through intelligent study tools. It features real-time subject-based chat rooms, Pomodoro timers with custom modes, session tracking, and OpenAI-powered bots tuned to each academic subject.

> ✨ Built with React, Node.js, Express, MongoDB, and OpenAI API.

---

## 🚀 Features

- 🔐 **User Authentication & Profiles** (Signup/Login/Reset, with avatars)
- 💬 **Subject Chat Rooms** (Real-time with Socket.IO)
- 🤖 **AI Study Bots** (per subject using OpenAI API)
- ⏱️ **Pomodoro Timer** (Custom intervals, intensity levels, sound cues)
- 📊 **Study Dashboard** (Charts, session logs, focus stats)
- 🎨 **Modern UI** (Dark/light mode, accent color picker, drag-drop UX)

---

## 🛠️ Tech Stack

### Frontend
- React + Vite
- TailwindCSS (dark mode, neon green theme)
- Zustand (global state)
- Socket.IO Client
- Chart.js or Recharts

### Backend
- Node.js + Express
- MongoDB with Mongoose
- JWT Authentication
- Socket.IO Server
- OpenAI API Integration

---

## 📁 Project Structure
nestai-app/
├── backend/
│   ├── .env.example
│   ├── package.json
│   ├── README.md
│   └── src/
│       ├── server.js
│       ├── app.js
│       ├── controllers/
│       │   ├── auth.controller.js
│       │   ├── chat.controller.js
│       │   └── pomodoro.controller.js
│       ├── routes/
│       │   ├── auth.routes.js
│       │   ├── chat.routes.js
│       │   └── pomodoro.routes.js
│       ├── models/
│       │   ├── User.model.js
│       │   ├── Message.model.js
│       │   └── Session.model.js
│       ├── middlewares/
│       │   ├── auth.middleware.js
│       │   └── error.middleware.js
│       ├── services/
│       │   ├── ai.service.js
│       │   └── notification.service.js
│       └── utils/
│           └── jwt.util.js

├── frontend/
│   ├── .env.example
│   ├── package.json
│   ├── README.md
│   ├── public/
│   │   ├── index.html
│   │   ├── login.html
│   │   ├── signup.html
│   │   ├── dashboard.html
│   │   ├── chat.html
│   │   ├── styles.css
│   │   ├── theme-toggle.js
│   │   ├── mobile-menu.js
│   │   ├── auth.js
│   │   ├── pomodoro.js
│   │   ├── stats.js
│   │   ├── chat.js
│   │   ├── socket-client.js
│   │   └── icons/
│   │       ├── chat.svg
│   │       ├── bot.svg
│   │       ├── timer.svg
│   └── src/
│       ├── index.jsx
│       ├── App.jsx
│       ├── tailwind.config.js
│       ├── assets/
│       │   ├── images/
│       │   └── sounds/
│       ├── components/
│       │   ├── auth/
│       │   │   ├── Login.jsx
│       │   │   ├── Signup.jsx
│       │   │   └── ResetPassword.jsx
│       │   ├── chat/
│       │   │   ├── RoomList.jsx
│       │   │   ├── ChatWindow.jsx
│       │   │   ├── MessageInput.jsx
│       │   │   └── BotHelpButton.jsx
│       │   ├── pomodoro/
│       │   │   ├── TimerDisplay.jsx
│       │   │   ├── ModeSelector.jsx
│       │   │   └── IntensityPicker.jsx
│       │   ├── dashboard/
│       │   │   ├── StatsChart.jsx
│       │   │   └── SessionTable.jsx
│       │   └── common/
│       │       ├── Navbar.jsx
│       │       ├── ThemeToggle.jsx
│       │       ├── AvatarUpload.jsx
│       │       └── DraggableList.jsx
│       ├── contexts/
│       │   └── AuthContext.jsx
│       ├── stores/
│       │   └── useStore.js
│       ├── services/
│       │   ├── api.js
│       │   └── socket.js
│       └── utils/
│           └── helpers.js

├── .gitignore
└── README.md

</details>

---

## ⚙️ Installation

### 1. Clone the repository

git clone https://github.com/your-username/nestai-app.git
cd nestai-app

### 2. Backend Setup

cd backend
cp .env.example .env         # Add your MongoDB URI, JWT_SECRET, and OpenAI API Key
npm install
npm run dev                  # Starts backend server at http://localhost:5000

### 3. Frontend Setup

cd ../frontend
cp .env.example .env         # Add API and Socket URLs
npm install
npm run dev                  # Starts frontend at http://localhost:5173


---

### 🔑 Environment Variables

Backend (backend/.env)

PORT=5000
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
OPENAI_API_KEY=your_openai_api_key

Frontend (frontend/.env)

VITE_API_URL=http://localhost:5000
VITE_SOCKET_URL=http://localhost:5000


---

### 🧪 Scripts

Backend

npm run dev     # Start dev server (with nodemon)
npm start       # Start production server

Frontend

npm run dev     # Start Vite dev server
npm run build   # Build production version


---

### 📈 Dashboard Metrics

The dashboard shows:

Weekly session count

Average focus time

Most used modes

Subject-wise breakdown



---

### 🤖 AI Bot Prompt Logic

The AI responds to:

Messages that mention @bot

Clicking "Help Me" next to message input


It uses the prompt:

> "You are a helpful [Subject] tutor. A student asked: [User's question]"




---

### 💅 UI/UX Notes

Default theme: Dark with neon green (#39FF14)

Fully responsive, mobile-first layout

Drag-and-drop for subject lists and timer modes

Micro animations, ambient visuals, and sound cues for focus



---

### 🛡️ Security

Protected API routes using JWT middleware

Passwords hashed using bcrypt

Client/server-side validation



---

### 🌐 Deployment (Optional)

Deploy to:

Frontend: Vercel, Netlify

Backend: Render, Railway, Heroku

Database: MongoDB Atlas


> ✅ Remember to set your .env values for production builds.




---

### 🙌 Contributing

Contributions welcome!

# Fork this repo and clone locally
git checkout -b feature/your-feature-name
# Make your changes
git commit -m "✨ Added [feature-name]"
git push origin feature/your-feature-name

Open a pull request and we’ll review it! 🎉


---

### 📜 License

MIT License — use it, remix it, build with it.


---

### ✨ Acknowledgments

OpenAI API

Socket.IO

MongoDB Atlas

All open-source contributors & tools



---

> Built with 💚 for the next generation of dreamers.
Stay focused, stay mystical. 🌌

