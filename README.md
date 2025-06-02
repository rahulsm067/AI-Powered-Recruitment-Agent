# AI-Powered Recruitment Agent

An advanced, AI-driven platform for automated resume analysis, skill-gap detection, and personalized interview preparation. Designed to streamline and enhance the recruitment process for both candidates and hiring teams.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Getting Started](#getting-started)
- [Usage Workflow](#usage-workflow)
- [Customization](#customization)
- [License](#license)
- [Contact](#contact)

---

## Overview

**AI-Powered Recruitment Agent** leverages state-of-the-art Large Language Models (LLMs) and semantic search to:
- Analyze candidate resumes against predefined or custom job requirements
- Identify strengths, weaknesses, and missing skills
- Generate actionable improvement suggestions and before/after examples
- Create personalized, role-specific interview questions
- Provide an improved, ATS-optimized resume in modern formats

The platform features an intuitive web interface built with Streamlit, making it easy for users to interactively upload documents, configure settings, and download reports.

---

## Features

- **Resume Upload & Parsing:** Accepts PDF or TXT resumes for analysis.
- **Role or JD Matching:** Select a predefined job role (e.g., AI/ML Engineer, Backend Engineer, Product Manager) or upload a custom Job Description for tailored skill extraction.
- **Semantic Skill Analysis:** Uses OpenAI and LangChain to semantically evaluate resume content against required skills.
- **Weakness & Improvement Detection:** Pinpoints missing skills and provides AI-generated actionable suggestions and before/after content blocks.
- **Resume Q&A:** Ask natural language questions about the resume (e.g., “What projects has the candidate worked on?”).
- **Interview Question Generation:** Instantly generates role- and skill-specific interview questions with selectable type and difficulty.
- **Resume Improvement:** Get structured recommendations for content, formatting, and skills highlighting.
- **Improved Resume Creation:** Automatically rewrites and enhances the resume for better ATS and recruiter visibility.
- **Downloadable Reports:** All feedback, interview questions, and improved resumes are downloadable in TXT or Markdown format.
- **Customizable UI:** Theme color and branding configurable via UI.

---

## Technology Stack

- **Frontend:** [Streamlit](https://streamlit.io/) (UI, interactions, download buttons)
- **Backend/AI:**
  - [OpenAI GPT-4o](https://platform.openai.com/docs/models/gpt-4-and-gpt-4-turbo) (LLM for skill analysis, question answering, improvements)
  - [LangChain](https://www.langchain.com/) (LLM orchestration, retrieval-augmented generation)
  - [FAISS](https://github.com/facebookresearch/faiss) (vector search for resume/skill matching)
- **Parsing & Data Handling:** PyPDF2 (PDF extraction), pandas (data formatting)
- **Visualization:** matplotlib (score pie charts)
- **Concurrency:** concurrent.futures (parallel skill evaluation)
- **Configuration:** python-dotenv for environment variables
- **Other:** Download support (base64), theme/color customization

---

## Getting Started

### Prerequisites

- Python 3.9 or higher
- OpenAI API Key (required for LLM features)

### Installation

```bash
git clone https://github.com/rahulsm067/AI-Powered-Recruitment-Agent.git
cd AI-Powered-Recruitment-Agent
 conda create -n lang3 python==3.11 -y 

1. conda activate  lang3

2. pip install - r requirements.txt


```

### Running the Application

```bash
streamlit run app.py
```

Then, open your browser at the URL shown by Streamlit (default: http://localhost:8501).

---

## Usage Workflow

1. **Configure the Sidebar:**
   - Enter your OpenAI API key.
   - Optionally select a theme color.

2. **Resume Analysis Tab:**
   - Select a job role or upload a custom job description (PDF/TXT).
   - Upload your resume (PDF/TXT).
   - Click "Analyze Resume".
   - View overall score, skill breakdown, strengths, and improvement areas.
   - Download the detailed analysis report.

3. **Resume Q&A Tab:**
   - Ask free-form questions about the resume and receive AI-generated answers.
   - Use example questions or create your own.

4. **Interview Questions Tab:**
   - Choose question types and difficulty.
   - Generate and review personalized interview questions.
   - Download the complete set for offline practice.

5. **Resume Improvement Tab:**
   - Select which areas to improve (content, formatting, skills, etc.).
   - Optionally specify a target role.
   - Generate detailed suggestions and before/after examples.
   - Download improvement suggestions.

6. **Improved Resume Tab:**
   - Provide a target role or paste a job description/skills.
   - Generate an improved, ATS-optimized resume.
   - Download as TXT or Markdown.

---

## Customization

- **Roles & Skills:** Edit the `ROLE_REQUIREMENTS` dictionary in `app.py` to add or modify roles/skills.
- **Theming:** Change the accent color through the sidebar or modify CSS in `ui.py`.
- **Model Settings:** The `agents.py` module uses GPT-4o by default; modify as needed.

---

## License

MIT License  
See [LICENSE](LICENSE) for details.

---

## Contact

For questions, suggestions, or contributions, please contact [rahulsm067](https://github.com/rahulsm067).

---

**Note:** This project requires an active OpenAI API key. All AI-powered features (analysis, improvements, interview question generation) depend on external API calls and may incur costs as per your OpenAI subscription.

---
