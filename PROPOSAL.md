# Project Proposal: AI Resume Optimizer & Job Description Matcher

## 1. Problem, and who the user is
* **Target User:** University students, recent graduates, and job seekers applying for tech and enterprise roles.
* **Problem:** Many qualified candidates are automatically rejected by Applicant Tracking Systems (ATS) or HR screeners because their resumes lack exact keyword alignment or fail to contextualize technical skills for specific job descriptions. Existing tools offer static layout templates but lack deep, contextual semantic matching.

## 2. The AI feature, and how you will measure whether it works
* **Substantive AI Feature:** An LLM-powered engine (using Google Gemini API via Python) that parses unstructured text from resumes (PDF/TXT) and job descriptions. It calculates a contextual match compatibility score (%), extracts missing technical and soft skills, and generates tailored bullet-point rewrite recommendations for resume optimization.
* **Evaluation:** We will create a benchmark test set of 10 candidate resume-job pairs. We will establish a human recruiter baseline by scoring match quality and skill gaps manually (scale 0–100%), then run our LLM pipeline across the test set to evaluate alignment and score variance against the baseline.

## 3. The agentic tool(s) you will use, and whether paid or free
* **Agentic Tools:** GitHub Copilot (Free agent mode in VS Code) as our primary IDE agent. It will assist in repository setup, writing Python modules, building the Streamlit dashboard, and refactoring error logs.

## 4. MVP (what must work by the checkpoint) and stretch goals
* **MVP (by Mon 16 Nov Checkpoint):** 
  * Local Streamlit web UI with file uploader for resumes (PDF/TXT) and text box for job descriptions.
  * Core backend logic executing Gemini API calls to return a Match Score (%) and a basic list of missing skills.
* **Stretch Goals:** 
  * Interactive "Before/After" bullet point editor with real-time feedback.
  * One-click PDF report generator to export the optimized resume suggestions.

## 5. Data and external APIs you need, and whether you have access to them
* **Data Sources:** Publicly available sample tech/business resumes and standard job postings (free, fully accessible).
* **APIs:** Google Gemini API (Free Tier key via Google AI Studio). API keys will be managed securely using local `.env` environment variables (no hardcoded credentials in Git).

## 6. Who does what
* **Zhappar Medet  (AI Pipeline, Backend & Evaluation):** Responsible for Gemini API integration, prompt engineering for semantic keyword and skill-gap extraction, building `evaluation.py`, and running the 10-pair benchmark test set to evaluate accuracy.
* **Baltabay Sauirzhan  (Frontend, UI & Workflow Integration):** Responsible for building the Streamlit interactive dashboard, PDF parsing pipeline, managing the GitHub Copilot workflow, and maintaining project documentation (`PLAN.md`, `AGENTS.md`, `DECISIONS.md`).
