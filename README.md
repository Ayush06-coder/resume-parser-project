# 🚀 RecruitAI ATS

### AI-Powered Applicant Tracking System (ATS)

An end-to-end recruitment platform that combines NLP-powered resume parsing, intelligent candidate ranking, job management, application tracking, analytics, and role-based authentication.

---

## 🌐 Live Demo

**Live Application:**  
https://recruit-ai-owkl.onrender.com

**GitHub Repository:**  
https://github.com/Ayush06-coder/RecruitAI-ATS

---

## 🎯 Project Overview

RecruitAI ATS helps recruiters streamline hiring by automating resume screening, candidate ranking, job posting, and application management.

Instead of manually reviewing hundreds of resumes, recruiters can:

- Parse resumes automatically
- Match candidates against job requirements
- Rank applicants instantly
- Track applications
- Analyze candidate data
- Manage hiring workflows from one dashboard

---

## ✨ Key Features

### 👨‍💼 Candidate Features

- Browse open jobs without login
- Apply directly using resume upload
- Instant match score calculation
- Application tracking via personalised tracking link
- Track status anytime

### 🏢 Recruiter Features

- Dashboard with hiring metrics
- Candidate database with search & filters
- View ranked applicants
- Manage application statuses
- Real-time JD matching
- Candidate analytics

### 🔐 Admin Features

- Role-based access control
- User management
- Job management
- Candidate deletion
- Password enforcement
- Account security controls

---

## 🧠 AI & NLP Features

- Resume Parsing using spaCy NLP
- Skill Extraction
- Education Extraction
- Experience Extraction
- Certification Extraction
- JD Matching Engine
- Candidate Ranking System

### Match Score Formula

```text
Skills         = 60%
Experience     = 25%
Certifications = 15%
```

---

## 🏗️ System Architecture

```text
Candidate
    │
    ▼
Streamlit Frontend
    │
    ▼
FastAPI Backend
    │
    ├── Resume Parsing Engine
    ├── JD Matching Engine
    ├── Authentication System
    ├── Job Management
    └── Analytics Engine
    │
    ▼
SQLite Database
    │
    ▼
Recruiter Dashboard
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---------|---------|
| Frontend | Streamlit |
| Backend | FastAPI |
| API Server | Uvicorn |
| NLP | spaCy + Regex |
| Database | SQLite |
| Authentication | bcrypt |
| Analytics | Pandas |
| Containerization | Docker |
| Deployment | Render |
| Language | Python 3.11 |

---

## 📂 Project Structure

```text
resume-parser-project/
│
├── App.py
├── auth.py
├── config.py
├── styles.py
├── Dockerfile
├── start.sh
├── requirements.txt
│
├── backend/
│   ├── main.py
│   ├── parser.py
│   ├── extractor.py
│   └── database.py
│
├── pages/
│   ├── Home.py
│   ├── Apply.py
│   ├── Track.py
│   ├── Login.py
│   ├── Dashboard.py
│   ├── Applications.py
│   ├── JD_Matching.py
│   ├── Analytics.py
│   ├── Admin.py
│   ├── Candidates.py
│   └── Change_Password.py
│
├── database/
│   └── resumes.db
│
└── resumes/
```

---

## 🔄 Application Workflow

### Candidate Flow

1. Browse available jobs
2. Select a job
3. Upload resume
4. Resume is parsed automatically
5. Match score is calculated
6. Application is submitted
7. Tracking link is generated
8. Candidate tracks status anytime

### Recruiter Flow

1. Login
2. View Dashboard
3. Review applications
4. View ranked candidates
5. Shortlist or reject candidates
6. Monitor analytics
7. Manage jobs and users

---

## 📊 Core Modules

### Resume Parser

Extracts:

- Name
- Email
- Phone Number
- Skills
- Education
- Experience
- Certifications

### Candidate Database

- Search
- Filter
- Pagination
- Delete (Admin Only)

### JD Matching

- Skill Matching
- Experience Matching
- Certification Matching
- Candidate Ranking

### Analytics

- Skills Distribution
- Education Breakdown
- Experience Analysis
- Candidate Insights

---

## 🔌 API Endpoints

| Method | Endpoint |
|----------|----------|
| GET | / |
| POST | /upload |
| GET | /candidates |
| GET | /candidate/{id} |
| DELETE | /candidates/{id} |
| POST | /match |
| POST | /jobs |
| GET | /jobs |
| PUT | /jobs/{id} |
| DELETE | /jobs/{id} |
| POST | /jobs/{id}/apply |
| GET | /jobs/{id}/applications |
| PUT | /applications/{id} |
| GET | /track/{email} |

---

## ▶️ Running Locally

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Create .env

```env
API_URL=http://localhost:8000
```

### Start Backend

```bash
uvicorn backend.main:app --reload --port 8000
```

### Start Frontend

```bash
streamlit run App.py
```

### Access

Frontend:

```text
http://localhost:8501
```

Backend Docs:

```text
http://localhost:8000/docs
```

---

## 🐳 Docker Deployment

Build:

```bash
docker build -t recruitai .
```

Run:

```bash
docker run -p 8000:8000 -p 8501:8501 recruitai
```

---

## ☁️ Render Deployment

### Environment Variables

```env
FRONTEND_URL=https://your-app-name.onrender.com
ADMIN_DEFAULT_PASSWORD=YourSecurePassword
```

### Deployment Steps

1. Push code to GitHub
2. Create Render Web Service
3. Select Docker Environment
4. Add Environment Variables
5. Deploy

---

## 🔐 Authentication

### Admin

Username:

```text
admin
```

Password:

```text
Set using ADMIN_DEFAULT_PASSWORD
```

### Security Features

- Password Hashing (bcrypt)
- Account Lockout
- First Login Password Change
- Role-Based Access Control

---

## 🎯 Key Achievements

- Built a full-stack Applicant Tracking System
- Implemented NLP-based resume parsing
- Developed a weighted JD matching engine
- Created role-based authentication system
- Built recruiter analytics dashboard
- Dockerized the complete application
- Successfully deployed to Render Cloud

---

## 📸 Application Screenshots

### 🏠 Home Page

![Home](Screenshots/Home1.png)

---

### 🏠 Home Page (Public View)

![Home2](Screenshots/Home2.png)

---

### 🔐 Login Page

![Login](Screenshots/Login.png)

---

### 📊 Recruiter Dashboard

![Dashboard](Screenshots/Dashboard.png)

---

### 👥 Candidate Database

![Candidates](Screenshots/Candidates.png)

---

### 📄 Applications Management

![Applications](Screenshots/Applications.png)

---

### 🎯 JD Matching

![JD Matching](Screenshots/JD_Matching.png)

---

### 📈 Analytics Dashboard

![Analytics](Screenshots/Analytics1.png)

---

### 📈 Analytics Insights

![Analytics2](Screenshots/Analytics2.png)

---

### 🔐 Admin Panel

![Admin](Screenshots/Admin1.png)

---

### 🔐 Admin User Management

![Admin2](Screenshots/Admin2.png)

---

### 🔐 Admin Job Management

![Admin3](Screenshots/Admin3.png)

---

### 📝 Job Application Portal

![Apply](Screenshots/Apply.png)

---

### 📍 Application Tracking

![Track](Screenshots/Track.png)

---

## 📄 Resume Highlights

This project demonstrates:

- Full-Stack Development
- REST API Design
- Natural Language Processing
- Authentication & Authorization
- Database Design
- Cloud Deployment
- Docker Containerization
- Data Analytics

---

## 👨‍💻 Author

### Ayush Sawhney

B.Tech Computer Science Engineering  
Amity University, Noida

GitHub:
https://github.com/Ayush06-coder

LinkedIn:
https://www.linkedin.com/in/ayush-sawhney-b8476a34b

---

## 📌 Project Status

🟢 Active Development

Built with ❤️ using Python, FastAPI, Streamlit, spaCy, SQLite, Docker, and Render.
