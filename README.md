🌟 SkillSync Job Portal App

SkillSync is a comprehensive, full-stack job portal built with the MERN stack (MongoDB, Express.js, React.js, Node.js) that integrates an AI-based recommendation system to streamline the hiring process for both job seekers and recruiters. It features real-time chat, company management, and a modern, responsive interface.

✨ Features

Job Seeker Functionality

    Secure Authentication: JWT-based login/signup.

Job Listings: View and filter a wide variety of jobs dynamically.

Skill-Based Job Recommendations: Upload resumes and receive personalized job recommendations using spaCy (Python NLP library).

Application Management: Candidates can apply for jobs and track their application status (Pending, Accepted, Rejected).

Recruiter Functionality

    Secure Authentication: JWT-based login/signup for recruiters.

Company Management: Register and manage company profiles.

Job Posting: Post new jobs with full control over listings.

Applicant Tracking: Review and manage applications received from candidates, including updating their status.

Real-time Messaging: In-app messaging between candidates and recruiters using Socket.io.

General Features

    Modern UI: Designed with Tailwind CSS and shadcn/ui components for a clean and responsive interface.

Cloud Uploads: Manage profile pictures and company logos via Cloudinary.

Forgot Password: Secure password reset functionality via email using Nodemailer and secure token generation using Crypto.

💻 Tech Stack

Layer	Technologies
Frontend	

React.js, React Router, Tailwind CSS, Shadcn UI [cite: 36]
Backend	

Node.js, Express.js, Socket.io, Nodemailer [cite: 36]
Database	

MongoDB Atlas [cite: 36]
AI Module	

Python, Flask, spaCy, PyMuPDF [cite: 36]
Auth	

JWT, Bcrypt, Crypto [cite: 36]
Cloud	

Cloudinary (Image & PDF Storage) [cite: 36]

📁 Project Structure

careergrow-mern-job-portal/
├── backend/                  # Node.js + Express backend APIs, MongoDB logic
│   ├── python_logic/         # Python-based skill extractor using spaCy
│   └── .env                  # Backend environment variables (Crucial for Cloudinary, MongoDB, Nodemailer)
├── frontend/                 # React frontend with Tailwind CSS + shadcn/ui
└── README.md
``` [cite: 38-43]

### 🛠️ Prerequisites

Before running the project, ensure you have the following installed:
* **Node.js** (v18 or above recommended) [cite: 46]
* **npm** or **Yarn** [cite: 47]
* **MongoDB Atlas** account (or local MongoDB setup) [cite: 48]
* **Python 3.8+** (for AI-based resume skill extraction) [cite: 49]
* **Cloudinary** account [cite: 50]

### 🚀 Installation & Setup

#### Step 1: Clone the Repository

```bash
git clone https://github.com/AMITPATTANAYAK/SkillSync.git
cd SkillSync
``` [cite: 56, 57]

#### Step 2: Install Node Dependencies

Install dependencies for both the backend and frontend: [cite: 59]

```bash
# Backend Dependencies
cd backend
npm install
# Frontend Dependencies
cd ../frontend
npm install
``` [cite: 60-65]

#### Step 3: Set Up Environment Variables

Create a `.env` file inside the `/backend` folder and add the following variables, replacing the placeholders with your actual credentials: [cite: 67]

```env
MONGO_URI=your_mongodb_connection_string
PORT=8000
SECRET_KEY=your_jwt_secret_key

# Cloudinary (for image and resume storage)
CLOUD_NAME=your_cloudinary_name
API_KEY=your_cloudinary_api_key
API_SECRET=your_cloudinary_api_secret

# Nodemailer (for password reset emails)
SMTP_USER=your_smtp_email
SMTP_PASS=your_smtp_password

FRONTEND_URL=http://localhost:5173
# FLASK_URL=http://127.0.0.1:5002 (Optional if running Flask locally on 5002)
``` [cite: 68-78]

#### Step 4: Set Up Python Logic (Flask)

The AI module requires a Python environment: [cite: 80]

1.  **Navigate to Python Logic:**
    ```bash
    cd ../backend/python_logic
    ``` [cite: 82]
2.  **Create & Activate a Virtual Environment:** [cite: 83-89]
    ```bash
    python -m venv venv
    # On Linux/macOS:
    source venv/bin/activate
    # On Windows:
    venv\Scripts\activate
    ```
3.  **Install Required Libraries:** [cite: 90, 91]
    ```bash
    pip install flask flask-cors pymupdf spacy pymongo python-dotenv
    # Download the spaCy language model
    python -m spacy download en_core_web_sm
    ``` [cite: 92]
4.  **Run the Flask App:** The Flask app must be running to serve the resume processing API.
    ```bash
    python app.py
    ``` [cite: 94]

### 🚀 Run the App

Open **two separate terminal windows** (after completing Steps 2-4). [cite: 96]

1.  **Run Backend (using nodemon):**
    ```bash
    cd backend
    nodemon index.js
    ``` [cite: 98, 99]
2.  **Run Frontend:**
    ```bash
    cd frontend
    npm run dev
    ``` [cite: 101, 102]

The application should now be accessible at `http://localhost:5173`[cite: 103].

### 🤝 Acknowledgments

This project was built using the power of these incredible tools and libraries: [cite: 105-110]

* **Full-Stack:** [React.js](https://reactjs.org/), [Node.js](https://nodejs.org/), and [Express.js](https://expressjs.com/)
* **Styling:** [Tailwind CSS](https://tailwindcss.com/) and [shadcn/ui](https://ui.shadcn.com/)
* **AI/NLP:** [spaCy](https://spacy.io/)
* **Real-time:** [Socket.io](https://socket.io/)
* **Utilities:** [Nodemailer](https://nodemailer.com/)
* **Cloud/DB:** [MongoDB Atlas](https://www.mongodb.com/atlas) and [Cloudinary](https://cloudinary.com/)

