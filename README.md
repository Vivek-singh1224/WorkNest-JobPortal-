# 💼 Job Portal – Full Stack Project

A comprehensive MERN-based job portal that allows users to register, apply for jobs, and enables recruiters to post and manage job listings efficiently.

---

## 🚀 Tech Stack

### Frontend
- **React.js** - UI Library
- **Tailwind CSS** - Styling Framework
- **Shadcn UI** - Component Library
- **Axios** - HTTP Client
- **React Router** - Navigation

### Backend
- **Node.js** - Runtime Environment
- **Express.js** - Web Framework
- **REST APIs** - API Architecture

### Database
- **MongoDB** - NoSQL Database
- **Mongoose** - ODM (Object Data Modeling)

### Security & Authentication
- **JSON Web Tokens (JWT)** - Token-based Authentication
- **bcrypt.js** - Password Hashing
- **dotenv** - Environment Variables Management

---

## 📁 Repository Structure

```
job-portal/
├── frontend/           # React frontend application
├── backend/            # Express backend API
└── README.md          # Project documentation
```

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/<username>/<repository>.git
cd <repository>
```

### 2️⃣ Backend Setup

```bash
cd backend
npm install
```

**Create `.env` file in backend directory:**

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
```

**Run Backend Server:**

```bash
npm start
```

The backend will run on `http://localhost:5000`

### 3️⃣ Frontend Setup

```bash
cd frontend
npm install
npm run dev
```

The frontend will run on `http://localhost:8080`

---

## 🗄️ Database Schema (MongoDB)

### User Collection

```javascript
{
  _id: ObjectId,
  name: String,
  email: String,
  password: String (hashed),
  role: "candidate" | "recruiter",
  createdAt: Date
}
```

### Job Collection

```javascript
{
  _id: ObjectId,
  title: String,
  company: String,
  description: String,
  location: String,
  salaryRange: String,
  postedBy: ObjectId (userId),
  createdAt: Date
}
```

### Application Collection

```javascript
{
  _id: ObjectId,
  jobId: ObjectId,
  userId: ObjectId,
  resumeLink: String,
  status: "applied" | "reviewed" | "selected" | "rejected",
  appliedAt: Date
}
```

---

## 🏗️ Architecture Explanation

The application follows a **client-server architecture**:

### Frontend (React)
- ✅ Handles UI rendering and user interactions
- ✅ Manages routes (login, register, job list, job apply, dashboard)
- ✅ Makes API calls using Axios
- ✅ State management for user sessions

### Backend (Express API)
- 🔐 Authentication (JWT-based)
- 📝 CRUD operations for job posts
- 📄 Candidate job applications management
- 👨‍💼 Recruiter dashboards and analytics

### Database (MongoDB)
- 💾 Stores users, jobs, and applications
- ✔️ Mongoose used for schema validation
- 🔗 Relational data modeling with references

---

## 🔌 API Documentation

### 🔐 Authentication

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register new user |
| POST | `/api/auth/login` | Login & get JWT token |

### 💼 Jobs

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/jobs` | Recruiter posts a job |
| GET | `/api/jobs` | Get all jobs |
| GET | `/api/jobs/:id` | Get job by ID |
| PUT | `/api/jobs/:id` | Update job post |
| DELETE | `/api/jobs/:id` | Delete job |

### 📄 Applications

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/apply/:jobId` | Apply for job |
| GET | `/api/applications/user` | Get user's applications |
| GET | `/api/applications/job/:jobId` | Recruiter sees applicants |

---

## 🤖 AI Usage Log

### AI Tools Used

**ChatGPT**
- Model: GPT-5.1
- Purpose of AI Assistance

| Task | Used AI? | Description |
|------|----------|-------------|
| UI Design | ❌ | Designed manually |
| Backend Logic | ❌ | Implemented manually |
| Debugging | ✅ | Used to fix token errors & CORS issues |
| Documentation | ✅ | README.md drafted using ChatGPT |

### Prompts Used

Example prompts used during development:

1. "Help me design a clean backend folder structure for a job portal."
2. "Fix my JWT authentication error: cannot read property of undefined."
3. "Write README.md for my MERN Job Portal project."

---

## 🎯 Features

### Core Features
- ✅ **User Authentication** - Secure login/register with JWT
- ✅ **Job Search & Filters** - Search jobs by title, location, company
- ✅ **Apply for Jobs** - One-click application with resume upload
- ✅ **Recruiter Dashboard** - Manage job postings and applications
- ✅ **Manage Job Listings** - Create, update, delete job posts
- ✅ **JWT Security** - Token-based authentication and authorization
- ✅ **Responsive UI** - Mobile-first design with Tailwind CSS

### User Roles
- 👤 **Candidates** - Browse and apply for jobs
- 👨‍💼 **Recruiters** - Post jobs and review applications

---

## 🚀 Future Enhancements

- [ ] Add email notifications for job applications
- [ ] Implement advanced filters (salary range, experience level)
- [ ] Add real-time chat between recruiters and candidates
- [ ] Integrate payment gateway for premium job listings
- [ ] Add resume parser functionality
- [ ] Implement job recommendation algorithm

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---


## 🙏 Acknowledgments

- Thanks to the MERN stack community
- Shadcn UI for beautiful components
- MongoDB for excellent documentation

---

## 📝 Conclusion

This job portal project demonstrates proficiency in:

- ✔️ **Full-stack development** with MERN stack
- ✔️ **REST API design** and implementation
- ✔️ **MongoDB schema modeling** and relationships
- ✔️ **Secure authentication** with JWT
- ✔️ **Modern UI development** with React and Tailwind CSS
- ✔️ **Role-based access control** (RBAC)
- ✔️ **Responsive design** principles

---

