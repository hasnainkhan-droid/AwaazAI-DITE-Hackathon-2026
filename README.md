
# AwaazAI Pro — AI Citizen Complaint Assistant

**DITE Hackathon 2026–27 | Public Service**

## Team

- **Project Name:** AwaazAI Pro
- **Team Name:** [ADD REGISTERED TEAM NAME]
- **Team Members:**
  1. Hasnain
  2. Abbas
  3. Abu Zar

## Problem and Solution

Citizens often face difficulties documenting municipal problems in their own language, describing issues accurately, and identifying the appropriate public-service department.

**AwaazAI** is an AI-powered citizen complaint assistant designed to simplify this process.

Using Google Gemini AI, AwaazAI analyzes civic complaints, identifies missing information, suggests urgency levels and relevant department types, and generates professional complaint letters in English, Urdu, and Sindhi.

AwaazAI is an independent assistance platform. It does not submit complaints directly to government departments.

## What AI Does

### Inputs
- City and neighborhood
- Citizen's complaint description
- Selected language: English, Urdu, or Sindhi
- Optional clarification details

### AI Processing
- Google Gemini API
- Model: `gemini-flash-lite-latest`
- Structured JSON output using Pydantic
- Complaint classification
- Urgency recommendation
- Missing-information identification
- Suggested department type
- Formal complaint generation

### Outputs
- Issue category
- Suggested urgency level
- Complaint summary
- Priority explanation
- Recommended department type
- Missing-detail questions
- Formal complaint letter
- Recommended next steps

### Human Responsibility
Citizens must verify generated information and independently contact the appropriate department.

## Key Features

1. Premium responsive Streamlit interface.
2. AI-powered civic complaint classification.
3. English, Urdu, and Sindhi language support.
4. Missing-information detection and follow-up questions.
5. AI-assisted report refinement.
6. Formal complaint letter generation.
7. Suggested urgency and department type.
8. Animated five-stage complaint workflow.
9. Report readiness visualization.
10. Low, Medium, and High urgency comparison.
11. Before-and-after report refinement comparison.
12. Downloadable UTF-8 TXT reports.
13. Downloadable JSON reports.
14. Printable HTML reports with Save as PDF support.
15. Responsive design and accessibility features.
16. Clear AI safety and government-independence disclaimers.

## Technology Stack

| Technology | Purpose |
|---|---|
| Python | Application development |
| Streamlit | Web application interface |
| Google Gemini API | AI complaint analysis |
| Google GenAI SDK | Gemini integration |
| Pydantic | Structured response validation |
| HTML/CSS | UI styling and animations |
| GitHub | Source code repository |
| Streamlit Cloud | Public web deployment |

## How to Run Locally

### Step 1 — Clone the Repository

```bash
git clone https://github.com/hasnainkhan-droid/AwaazAI-DITE-Hackathon-2026.git
```

### Step 2 — Open Project Directory

```bash
cd AwaazAI-DITE-Hackathon-2026
```

### Step 3 — Install Dependencies

```bash
python -m pip install -r requirements.txt
```

### Step 4 — Configure Gemini API Key

Set the `GEMINI_API_KEY` environment variable or configure it securely in Streamlit Secrets.

Never commit API keys to GitHub.

### Step 5 — Start the Application

```bash
python -m streamlit run app.py
```

Open the local URL displayed in your terminal.

## Live Application

**AwaazAI Live Website:**

https://awaazai-dite-hackathon-2026-v3jqdgre3buatcrzwqkuwt.streamlit.app/

The deployed application allows citizens to analyze civic complaints using Gemini AI and generate downloadable complaint reports.

## GitHub Repository

**Public Source Code:**

https://github.com/hasnainkhan-droid/AwaazAI-DITE-Hackathon-2026

## Testing and Validation

The following scenarios have been tested:

- English-language complaint analysis
- AI-generated category and urgency suggestions
- Missing-information questions
- Formal complaint letter generation
- Urdu-language report generation
- Sindhi-language report generation
- TXT report download
- JSON report download
- Printable HTML report download
- Public access through the deployed website

Additional recommended tests include mobile responsiveness, report refinement, emergency safety handling, and AI API failure handling.

## Safety and Limitations

- AwaazAI is an independent demonstration project, not an official government website.
- It does not submit complaints to any government agency.
- AI-generated recommendations may be incomplete or incorrect.
- Users should verify department suggestions and report details before submission.
- Citizens should not provide unnecessary sensitive information.
- User-entered complaint text is processed through the Google Gemini API.
- No real citizen, patient, or student records are required for demonstration.
- Session data may be lost on refresh.
- AI service availability depends on external API access and quota limits.
- The application is not a replacement for emergency services.

## Demo Video

**Google Drive Link:**

[ADD DEMO VIDEO LINK]

The demonstration will cover the application interface, Gemini AI analysis, multilingual support, missing-information detection, formal complaint generation, and downloadable reports.

## Credits and References

- Google Gemini API: https://ai.google.dev/gemini-api/docs
- Streamlit: https://streamlit.io/
- Pydantic: https://docs.pydantic.dev/
- Google Fonts: https://fonts.google.com/

## Hackathon Information

**Event:** DITE Hackathon 2026–27

**Theme:** Public Service

**Project:** AwaazAI Pro — AI Citizen Complaint Assistant

**Team Members:** Hasnain, Abbas, Abu Zar

**Development:** Python, Streamlit, Google Gemini API

**Submission:** Public GitHub repository, live web deployment, and demonstration video.

---

**AwaazAI — Your City. Your Voice. Powered by AI.**
