# Architecture

## Overview

The Developer Intelligence Platform follows a modern client-server architecture, where the frontend communicates with the backend through REST APIs. The backend integrates with external services such as GitHub and AI models to analyze technical portfolios and generate intelligent insights.

---

# High-Level Architecture

```text
                +----------------------+
                |      Frontend        |
                |      (React)         |
                +----------+-----------+
                           |
                    REST API (HTTPS)
                           |
                +----------v-----------+
                |       FastAPI        |
                |      Backend         |
                +----------+-----------+
                           |
        +------------------+------------------+
        |                  |                  |
+-------v-------+  +--------v--------+  +------v------+
| PostgreSQL    |  | GitHub API      |  | OpenRouter  |
| Database      |  | Portfolio Data  |  | AI Models   |
+---------------+  +-----------------+  +-------------+
```

---

# System Components

## Frontend

Responsible for:

* User Interface
* Authentication Pages
* Dashboard
* Reports
* Data Visualization

---

## Backend (FastAPI)

Responsible for:

* Business Logic
* Authentication
* GitHub Integration
* Resume Processing
* AI Integration
* Report Generation
* API Endpoints

---

## Database (PostgreSQL)

Stores:

* User Accounts
* Analysis Results
* Reports
* Skills
* GitHub Metadata
* Recruiter Data

---

## GitHub API

Used to:

* Retrieve repositories
* Analyze programming languages
* Read repository metadata
* Collect contribution statistics

---

## AI Service

Responsible for:

* AI Summaries
* Skill Gap Analysis
* Portfolio Insights
* Candidate Reports
* Learning Recommendations

---

# User Flow

## Developer

```
Sign Up
      ↓
Connect GitHub
      ↓
Upload Resume
      ↓
Backend Analysis
      ↓
AI Processing
      ↓
Dashboard & Report
```

---

## Recruiter

```
Login
      ↓
Upload Candidate Resume
      ↓
Provide GitHub Link
      ↓
Backend Analysis
      ↓
AI Candidate Report
      ↓
Candidate Comparison
```

---

# Planned Tech Stack

## Frontend

* React
* Tailwind CSS

## Backend

* FastAPI
* SQLAlchemy

## Database

* PostgreSQL

## AI

* OpenRouter API
* Large Language Models (LLMs)

## Data Processing

* GitHub API
* Python
* Pandas

---

# Future Architecture Improvements

* Redis Caching
* Background Tasks
* Docker
* CI/CD Pipeline
* Cloud Deployment
* Monitoring & Logging
