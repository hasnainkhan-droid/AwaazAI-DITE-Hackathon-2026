# AwaazAI Pro — AI Citizen Complaint Assistant

**DITE Hackathon 2026–27 · Public Service**

## Team
- Team name: **[ADD YOUR REGISTERED TEAM NAME]**
- Members: **[ADD REGISTERED MEMBERS]**

## Problem and solution
Citizens face challenges documenting municipal problems in their own language and identifying likely public-service departments. AwaazAI uses Google Gemini to classify a civic complaint, suggest urgency, identify missing details, generate helpful questions, recommend a department **type**, and create a formal draft in English, Urdu, or Sindhi. It does not submit complaints to any agency.

## What AI does (judging criteria)
- **Inputs:** City/area, citizen's words, selected report language, and optional answers to clarifying questions.
- **AI:** Google Gemini API model `gemini-flash-lite-latest` and Pydantic JSON schema output.
- **Outputs:** `category`, `category_localized`, `priority`, `priority_localized`, `summary`, `priority_reason`, `suggested_department`, `missing_details` (each has question and reason), `formal_complaint`, and three `next_steps`.
- **Human role:** Citizen verifies facts and the appropriate office. This tool gives suggested routing only.

## Features
1. Premium responsive Streamlit interface, animated flowchart and example complaints.
2. Missing-detail detection with follow-up questions and **Refine report** button.
3. Full AI report content in English, Urdu, or Sindhi (local scripts; RTL display).
4. Structured cards: category, suggested urgency, location, missing-detail count.
5. Working letter view and UTF-8 TXT / JSON downloads.
6. Animated five-stage complaint flowchart with interactive stage explorer and live stage status.
7. Report readiness indicator based on 0–4 missing-detail questions (not an accuracy score).
8. Visual Low/Medium/High urgency comparison (AI recommendation only).
9. Before-vs-after revision comparison for refinement.
10. Printable HTML report (open and Print → Save as PDF), alongside existing TXT/JSON downloads.
11. Responsive microinteractions and reduced-motion accessibility.
12. No government integration and no fabricated official contact details.

## Technology
Python, Streamlit, Google GenAI SDK, Pydantic, custom CSS.

## Run locally
1. Open the `AwaazAI_Pro` folder in VS Code.
2. Run `python -m pip install -r requirements.txt`.
3. Set your `GEMINI_API_KEY` in the Windows environment (or `.streamlit/secrets.toml` locally, ignored by Git).
4. Run `python -m streamlit run app.py`.
5. Open the local Streamlit URL in the terminal.

## Deployment to Streamlit Community Cloud
1. Push the source to a **public GitHub repository**; **never push API keys or secrets**.
2. Visit https://share.streamlit.io/, sign in, choose **Create app**.
3. Select repository and `app.py` entry point.
4. Add `GEMINI_API_KEY = "<your key>"` in Streamlit Cloud **Secrets settings** (never in README/code).
5. Deploy and test your URL in an incognito browser.

## Test cases
- Clear drainage issue: expected category sanitation/sewerage, urgency backed by facts, possibly no missing details.
- Vague complaint (`sewerage line damage`): AI should identify missing location/duration/impact and avoid inventing actual harm.
- Urdu complaint + Urdu report: AI response content in Urdu script.
- Sindhi complaint + Sindhi report: AI response content in Sindhi script.
- Enter follow-up details then click Refine: report should update, with missing questions reduced if sufficient.
- Click formal letter and all 3 report download types: verify files open, including Urdu/Sindhi Unicode.
- Verify animated workflow starts in the input stage and updates after analysis; the government submission stage never shows complete.
- Trigger missing-detail refinement and verify before-vs-after comparison.
- Verify printable report opens offline and Print → Save as PDF works in Chrome.
- Check mobile width and reduced-motion OS accessibility settings.
- Check empty complaint and API error handling.

## Safety & limitations
- Independent demo, **not** an official government website; **does not submit** complaints.
- Suggestions may be wrong or uncertain; verify routing, priority, and any translated wording.
- Do not enter sensitive or unnecessary personally identifiable data. Gemini receives user-entered complaint text.
- No real patient, citizen or student records used; demo cases are fictional.
- Session state may be lost when browser refreshes. No database stores submissions.
- External model availability and free-tier quotas can affect results.

## Submission links
- Public GitHub: [ADD LINK]
- Live deployed app: [ADD LINK]
- Demo video (3–5 minutes): [ADD GOOGLE DRIVE LINK]

## Credits
- Google Gemini API / Google GenAI SDK: https://ai.google.dev/gemini-api/docs
- Streamlit: https://streamlit.io/
- Pydantic: https://docs.pydantic.dev/
- Google Fonts (DM Sans, Manrope, Noto Naskh Arabic): https://fonts.google.com/

**Hackathon originality:** Build and commit during the official event window. Credit external libraries and templates. Do not reuse old submitted project code in violation of event rules.
