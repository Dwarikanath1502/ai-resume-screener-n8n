# 🤖 AI Recruiter System

An AI-powered multi-agent recruitment assistant that automates resume screening, candidate evaluation, ranking, and recruiter recommendations using **n8n**, **LLMs**, and **Google Drive**.

## 📌 Overview

Recruiters often spend hours manually reviewing resumes against a job description. This project automates the entire screening workflow by leveraging specialized AI agents that evaluate resumes, validate results, rank candidates, and generate recruiter-ready reports.

The system processes multiple resumes for a single job description and delivers a ranked shortlist along with hiring recommendations.

---

## 🚀 Features

* 📄 Automatically reads Job Description (JD) and resumes from Google Drive
* 🧠 ATS-based resume evaluation using LLMs
* 🔍 Reflection agent to validate and improve evaluation consistency
* 🏆 Candidate ranking based on ATS scores
* 👨‍💼 AI recruiter recommendation for interview decisions
* 📧 Automatic HTML report generation and email delivery
* 📊 Structured JSON outputs for reliable downstream automation

---

## 🏗️ Architecture

```
Recruiter Uploads
        │
        ├── Job Description
        └── Resume Folder
                │
                ▼
        Resume Extraction
                │
                ▼
      ATS Evaluation Agent
                │
                ▼
      Reflection Agent
                │
                ▼
      Candidate Ranking
                │
                ▼
      Recruiter Recommendation Agent
                │
                ▼
      HTML Report Generator
                │
                ▼
        Email to Recruiter
```

---

## 🤖 AI Agents

### 1. ATS Evaluation Agent

* Compares resumes against the job description
* Calculates ATS score
* Identifies matching and missing skills
* Generates strengths, weaknesses, and improvement suggestions

### 2. Reflection Agent

* Reviews the ATS evaluation
* Validates scoring consistency
* Corrects logical inconsistencies
* Reduces hallucinated outputs

### 3. Recruiter Recommendation Agent

* Compares shortlisted candidates
* Recommends interview candidates
* Highlights hiring risks
* Suggests whether additional sourcing is required

---

## ⚙️ Workflow

1. Recruiter uploads:

   * Job Description
   * Resume folder

2. The workflow:

   * Extracts text from all PDFs
   * Evaluates every resume
   * Validates each evaluation
   * Sorts candidates by ATS score
   * Selects the Top N candidates
   * Generates recruiter recommendations
   * Creates an HTML hiring report
   * Sends the report via email

---

## 🛠️ Tech Stack

* **n8n**
* **Large Language Models (LLMs)**
* **JavaScript**
* **Google Drive**
* **HTML**
* **Prompt Engineering**
* **JSON Structured Outputs**

---

## 📊 Sample Output

The recruiter receives:

* Executive hiring recommendation
* Candidate ranking
* ATS scores
* Matching skills
* Missing skills
* Strengths & weaknesses
* Resume improvement suggestions
* Overall hiring summary

---

## 💡 Why Agentic AI?

This project follows a multi-agent architecture where each AI agent performs a specialized task:

* **Evaluation Agent** → Resume analysis
* **Reflection Agent** → Output validation
* **Recommendation Agent** → Hiring decision support

Rather than relying on a single LLM response, multiple agents collaborate to produce more reliable and structured hiring recommendations.

---

## 📈 Future Improvements

* Interview question generation for shortlisted candidates
* Candidate-job semantic matching using embeddings
* Recruiter feedback loop for continuous improvement
* ATS scoring analytics dashboard
* Support for multiple job openings simultaneously

---

## 📷 Workflow

> Add your n8n workflow screenshot here.

---

## ⭐ Author

**Dwarikanath**

If you found this project useful, consider giving it a ⭐ on GitHub.
