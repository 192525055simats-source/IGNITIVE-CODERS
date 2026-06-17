# CyberShield — Cybercrime Predictive Analytics Platform

A full-stack web application for law enforcement to track, predict, and respond to cybercrime incidents in real time.

## 🏗️ Project Structure

```
cybershield/
├── backend/            # Node.js + Express REST API
│   ├── config/         # DB & environment config
│   ├── controllers/    # Route handler logic
│   ├── middleware/     # Auth, error handling
│   ├── models/         # Data models (mock / MongoDB ready)
│   ├── routes/         # Express routers
│   └── server.js       # Entry point
├── frontend/           # React + Vite SPA
│   ├── public/
│   └── src/
│       ├── components/
│       │   ├── layout/     # Sidebar, Topbar, Layout
│       │   ├── pages/      # Dashboard, Complaints, Predictions …
│       │   └── ui/         # Reusable UI primitives
│       ├── hooks/          # Custom React hooks
│       ├── services/       # API client (axios)
│       └── utils/          # Helpers & formatters
└── package.json        # Root scripts (concurrently)
```

## 🚀 Quick Start

### Prerequisites
- Node.js ≥ 18
- npm ≥ 9

### 1. Install dependencies
```bash
npm run install:all
```

### 2. Configure environment
```bash
cp backend/.env.example backend/.env
# Edit backend/.env with your values
```

### 3. Run in development
```bash
npm run dev
```
- **Frontend** → http://localhost:5173  
- **Backend API** → http://localhost:5000

### 4. Build for production
```bash
npm run build        # builds frontend into frontend/dist/
npm run start        # runs backend (serves API)
```

## 🔑 Default Login (dev mode)
| Role | Email | Password |
|------|-------|----------|
| Admin | admin@cybershield.gov.in | admin123 |
| Analyst | analyst@cybershield.gov.in | analyst123 |
| Officer | officer@cybershield.gov.in | officer123 |

## 🌐 API Endpoints

| Method | Path | Description |
|--------|------|-------------|
| POST | /api/auth/login | Login & get JWT |
| GET | /api/dashboard/stats | Dashboard KPIs |
| GET | /api/complaints | List complaints |
| POST | /api/complaints | File new complaint |
| GET | /api/predictions | ML hotspot predictions |
| GET | /api/interventions | Field interventions |
| GET | /api/network | Mule network data |
| GET | /api/users | User management (admin) |
| GET | /api/integrations | Bank API integration status |

## 🛠️ Tech Stack

**Frontend**
- React 18 + Vite
- React Router v6
- Axios (API calls)
- Chart.js + react-chartjs-2
- Font Awesome 6

**Backend**
- Node.js + Express
- JWT authentication
- CORS, Helmet, Morgan
- dotenv for config

## 📁 Deploying to GitHub
```bash
git init
git add .
git commit -m "Initial commit: CyberShield full-stack app"
git remote add origin https://github.com/YOUR_USERNAME/cybershield.git
git push -u origin main
```
