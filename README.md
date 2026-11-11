# 🤖 AI Interview Preparation Agent

An AI-powered Interview Preparation Agent developed using Python, Streamlit, Google Gemini AI, and PyPDF. This application helps candidates prepare for job interviews by analyzing their resumes and generating personalized interview preparation reports based on their selected job role, experience level, interview type, and job description.

## 📌 Project Overview

Preparing for a technical or HR interview requires understanding job requirements, identifying important skills, practicing interview questions, and improving communication.

The **AI Interview Preparation Agent** simplifies this process using Generative AI.

Users upload their resumes, enter their desired job role, select their experience level and interview type, and optionally provide a job description.

The application extracts information from the uploaded resume and uses Google Gemini AI to generate a personalized interview preparation report.

## 🎯 Objectives

- Automate interview preparation using Generative AI.
- Analyze candidate resumes.
- Generate role-specific interview preparation content.
- Help candidates understand their strengths and skill gaps.
- Provide personalized preparation recommendations.
- Reduce the time required for interview preparation.

## 🚀 Features

### 1. Resume Upload

- Upload a candidate's resume in PDF format.
- Extract text from the uploaded PDF.
- Use extracted resume information as context for AI-generated recommendations.

### 2. Job Role Selection

Users can specify the job role they want to prepare for.

Examples:
- Python Developer
- Java Developer
- Software Engineer
- Web Developer
- Data Analyst
- Cloud Engineer

### 3. Experience Level

Users can select their experience level to receive relevant preparation guidance.

Examples:
- Fresher
- Entry-Level
- Experienced

### 4. Interview Type

The application allows users to specify the type of interview they want to prepare for.

Examples:
- Technical Interview
- HR Interview
- General Interview

### 5. Job Description Analysis

Users can provide a job description to help the AI understand the responsibilities, qualifications, and skills required for the position.

The AI uses this information along with the resume to personalize the preparation report.

### 6. AI-Powered Interview Preparation

Google Gemini AI processes the provided information and generates an interview preparation report.

The report can provide:
- Resume-based preparation guidance.
- Important technical topics to study.
- Role-specific interview preparation.
- Relevant interview questions.
- Recommendations based on the job description.
- Areas where the candidate can improve.

### 7. Downloadable Report

Users can download the generated interview preparation report for future reference.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| Streamlit | Web application interface |
| Google Gemini AI | AI-powered interview preparation |
| google-generativeai | Gemini API integration |
| PyPDF | Extracting text from PDF resumes |
| Pyngrok | Public access through a tunnel |
| Requests | HTTP requests |

## 🏗️ System Architecture

The application follows an AI-powered resume analysis and interview preparation workflow.

1. User opens the Streamlit application.
2. User uploads a PDF resume.
3. PyPDF extracts the resume text.
4. User enters the desired job role.
5. User selects experience level and interview type.
6. User optionally enters a job description.
7. Python collects the information and creates an AI prompt.
8. Google Gemini processes the prompt.
9. The AI generates a personalized preparation report.
10. Streamlit displays the result.
11. User downloads the generated report.

### Architecture Flow

```text
           USER
             |
             v
      Streamlit Interface
             |
             v
       Upload Resume
             |
             v
      PDF Text Extraction
           (PyPDF)
             |
             v
     Collect User Details
             |
       +-----+------+
       |            |
       v            v
    Job Role    Job Description
       |            |
       +-----+------+
             |
             v
      Python Application
             |
             v
       Prompt Generation
             |
             v
       Google Gemini AI
             |
             v
    Interview Preparation
            Report
             |
             v
      Display in Streamlit
             |
             v
       Download Report
```

## 📂 Project Structure

```text
AI-Interview-Preparation-Agent/
│
├── app.py
│
├── launch.py
│
├── requirements.txt
│
├── README.md
│
└── .gitignore
```

**File descriptions:**

- `app.py` – Main application containing the Streamlit interface, resume processing, and Gemini AI integration.
- `launch.py` – Supporting launch script used in the deployment/Colab workflow.
- `requirements.txt` – Contains the required Python libraries.
- `README.md` – Project documentation.
- `.gitignore` – Prevents sensitive and unnecessary files from being uploaded to GitHub.

## ⚙️ Installation and Setup

### Prerequisites

- Python 3.9 or later.
- Google Gemini API key.
- Internet connection.
- Git (optional).

### Step 1: Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

```bash
cd AI-Interview-Preparation-Agent
```

### Step 2: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 3: Generate Gemini API Key

Visit:

https://aistudio.google.com/apikey

Create an API key and copy it.

### Step 4: Configure Environment Variable

**Windows PowerShell:**

```powershell
$env:GEMINI_API_KEY="YOUR_API_KEY"
```

**Linux / macOS:**

```bash
export GEMINI_API_KEY="YOUR_API_KEY"
```

Do not upload your actual API key to GitHub.

### Step 5: Run the Application

```bash
streamlit run app.py
```

The application will start locally.

Open:

```text
http://localhost:8501
```

## 📦 Dependencies

The project uses the following Python libraries:

```text
streamlit
google-generativeai
pypdf
pyngrok
requests
```

These dependencies can be installed using:

```bash
pip install streamlit google-generativeai pypdf pyngrok requests
```

## ☁️ Deployment

The application can be deployed using Render or accessed through a public tunnel using Ngrok in Google Colab.

### Render Deployment

1. Upload the project to GitHub.
2. Create a new Web Service in Render.
3. Connect the GitHub repository.
4. Set the build command:

```bash
pip install -r requirements.txt
```

5. Set the start command:

```bash
streamlit run app.py --server.port $PORT --server.address 0.0.0.0
```

6. Add the Gemini API key as an environment variable:

```text
GEMINI_API_KEY = YOUR_API_KEY
```

7. Deploy the application.

## 💡 Example Usage

**Sample user input:**

| Input | Example |
|---|---|
| Resume | Rakesh_Resume.pdf |
| Job Role | Python Developer |
| Experience Level | Fresher |
| Interview Type | Technical Interview |
| Job Description | Python development, SQL, APIs |

**Expected output:**

The AI generates an interview preparation report based on the candidate's resume and selected job requirements.

The report can include relevant interview questions, important topics to prepare, resume-based recommendations, and suggestions for improving interview readiness.

## 🔐 Security

- Keep Gemini API keys in environment variables.
- Never commit API keys to GitHub.
- Add `.env` files to `.gitignore`.
- Handle uploaded resumes securely.
- Avoid storing personal resume information unnecessarily.

## 🔮 Future Enhancements

- AI-powered mock interview sessions.
- Voice-based interview practice.
- Speech recognition and response evaluation.
- Real-time feedback on candidate answers.
- Resume scoring and improvement suggestions.
- Technical coding interview practice.
- ATS-friendly resume analysis.
- Interview performance tracking.
- Personalized learning roadmaps.

## 🎓 Learning Outcomes

Through this project, I gained practical experience in:

- Python programming.
- Building applications using Streamlit.
- Integrating Google Gemini Generative AI.
- Extracting information from PDF documents.
- Resume processing and analysis.
- Prompt engineering.
- Working with APIs.
- Creating AI-powered applications.
- Deploying applications using cloud platforms.

## 👨‍💻 Author

**Alapati Rakesh Chowdary**

AI Interview Preparation Agent – Generative AI Project

---

⭐ If you find this project useful, consider giving the repository a star!
