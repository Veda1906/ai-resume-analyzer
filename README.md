# AI Resume Analyzer

An AI-powered mock interview and resume analysis tool. Upload your resume (or describe your background) alongside a target job description, and get a personalized interview strategy — powered by Google Gemini.

## 🔗 Live Demo

- **App:** [https://ai-resume-analyzer-huslers.vercel.app](https://ai-resume-analyzer-huslers.vercel.app)
- **API:** [https://ai-resume-analyzer-uepp.onrender.com](https://ai-resume-analyzer-uepp.onrender.com)

> Note: the backend is hosted on Render's free tier, which spins down after inactivity — the first request after idle time may take 30–60 seconds to respond.

## ✨ Features

- **User authentication** — register/login with JWT-based sessions
- **Resume parsing** — upload a PDF resume, or describe your background manually
- **AI-generated interview reports** — powered by Google Gemini, including:
  - Job match score
  - Tailored technical and behavioral interview questions
  - Skill-gap analysis
  - A day-by-day interview preparation plan
- **Report history** — view previously generated interview plans

## 🛠️ Tech Stack

**Frontend**
- React (Vite)
- React Router
- Sass (SCSS)
- Axios

**Backend**
- Node.js / Express
- MongoDB (Atlas) with Mongoose
- JWT authentication (jsonwebtoken, bcryptjs)
- Google Gemini API (`@google/genai`) for AI-generated content
- Multer + pdf-parse for resume file handling
- Puppeteer for PDF report generation

**Deployment**
- Frontend: Vercel
- Backend: Render
- Database: MongoDB Atlas

## 🚀 Running Locally

### Prerequisites
- Node.js (v18+)
- A MongoDB Atlas connection string (or local MongoDB instance)
- A Google Gemini API key ([Google AI Studio](https://aistudio.google.com/apikey))

### 1. Clone the repo
```bash
git clone https://github.com/Veda1906/ai-resume-analyzer.git
cd ai-resume-analyzer
```

### 2. Backend setup
```bash
cd backend
npm install
```

Create a `.env` file in `backend/` with:
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_random_secret
GOOGLE_GENAI_API_KEY=your_gemini_api_key
FRONTEND_URL=http://localhost:5173

Run the backend:
```bash
npm run dev
```
Server starts on `http://localhost:3000`.

### 3. Frontend setup
```bash
cd ../Frontend
npm install
```

Create a `.env` file in `Frontend/` with:
VITE_API_URL=http://localhost:3000
Run the frontend:
```bash
npm run dev
```
App starts on `http://localhost:5173`.


