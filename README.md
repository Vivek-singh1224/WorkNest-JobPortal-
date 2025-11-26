Job Portal – Full Stack Project

A MERN-based job portal that allows users to register, apply for jobs, and recruiters to post/manage job listings.

🚀 Tech Stack
Frontend

React.js

Tailwind CSS

Shadcn UI

Axios

React Router

Backend

Node.js

Express.js

REST APIs

Database

MongoDB (Mongoose ORM)

Optional Tech Used

JSON Web Tokens (JWT)

bcrypt.js

dotenv

📁 Repository Structure
/frontend
/backend
/README.md

⚙️ Setup Instructions
1. Clone the Repository
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

Backend Setup
cd backend
npm install

Create .env file
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key

Run Backend
npm start

Frontend Setup
cd frontend
npm install
npm run dev

🧩 ER Diagram / Schema Design (MongoDB)
User Collection
{
  _id,
  name,
  email,
  password,
  role: "candidate" | "recruiter",
  createdAt
}

Job Collection
{
  _id,
  title,
  company,
  description,
  location,
  salaryRange,
  postedBy (userId),
  createdAt
}

Application Collection
{
  _id,
  jobId,
  userId,
  resumeLink,
  status: "applied" | "reviewed" | "selected" | "rejected",
  appliedAt
}

🏗️ Architecture Explanation

The application follows a client–server architecture:

Frontend (React)

Handles UI

Manages routes (login, register, job list, job apply, dashboard)

Makes API calls using Axios

Backend (Express API)

Authentication (JWT-based)

CRUD operations for job posts

Candidate job applications

Recruiter dashboards

Database (MongoDB)

Stores users, jobs, and applications

Mongoose used for schema validation

🔌 API Documentation
AUTH
Method	Endpoint	Description
POST	/api/auth/register	Register new user
POST	/api/auth/login	Login & get JWT token
JOBS
Method	Endpoint	Description
POST	/api/jobs	Recruiter posts a job
GET	/api/jobs	Get all jobs
GET	/api/jobs/:id	Get job by ID
PUT	/api/jobs/:id	Update job post
DELETE	/api/jobs/:id	Delete job
APPLICATIONS
Method	Endpoint	Description
POST	/api/apply/:jobId	Apply for job
GET	/api/applications/user	Get user’s applications
GET	/api/applications/job/:jobId	Recruiter sees applicants


🤖 AI Usage Log
AI Tools Used

ChatGPT

Model: GPT-5.1

Purpose of AI Assistance
Task	Used AI?	Description
UI Design	❌	Designed manually
Backend Logic	❌	Implemented manually
Debugging	✔	Used to fix token errors & CORS issues
Documentation	✔	README.md drafted using ChatGPT
Prompts Used

(Add any prompts you used in developing the project — or paste ChatGPT transcript)
Example:

"Help me design a clean backend folder structure for a job portal."
"Fix my JWT authentication error: cannot read property of undefined."
"Write README.md for my MERN Job Portal project."

🎯 Features

✔ User Authentication
✔ Job Search & Filters
✔ Apply for Jobs
✔ Recruiter Dashboard
✔ Manage Job Listings
✔ JWT Security
✔ Responsive UI

📝 Conclusion

This job portal project demonstrates skills in:

Full-stack development

REST API design

MongoDB schema modeling

Secure authentication

Modern UI development
