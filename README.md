# 📅 SnapPlan — AI Deadline Tracker

SnapPlan is a Streamlit chat app that helps you keep track of deadlines.
Snap a photo of your syllabus, timetable, or assignment sheet (or just type
a question), and an AI buddy powered by Gemini pulls out the deadlines for
you. When you're ready, one button emails you a clean, organized summary
of every deadline mentioned in the conversation.

## Features
- Chat with an AI that only talks about deadlines, schedules, and assignments
- Upload a photo and get deadlines extracted automatically
- Ask follow-up questions in the same conversation
- One-click "Send to Email" button that emails a sorted deadline summary

## Built with
- [Streamlit](https://streamlit.io/) - the web app framework
- [Google Gemini API](https://aistudio.google.com/) - chat + vision
- Python's built-in `smtplib` - sending email (no third-party service needed)

## Running it locally

1. Clone this repo and enter the folder:
```bash
   git clone <your-repo-link>
   cd snapplan
```

2. Create and activate a virtual environment:
```bash
   python -m venv venv
   source venv/bin/activate   # macOS/Linux
   .\venv\Scripts\Activate.ps1   # Windows PowerShell
```

3. Install dependencies:
```bash
   pip install -r requirements.txt
```

4. Copy the secrets template and fill in your real values:
```bash
   cp .streamlit/secrets.toml.example .streamlit/secrets.toml
```
   Then edit `.streamlit/secrets.toml` and add:
   - `GEMINI_API_KEY` - from [Google AI Studio](https://aistudio.google.com/)
   - `GMAIL_ADDRESS` - your Gmail address
   - `GMAIL_APP_PASSWORD` - a 16-character App Password (not your real Gmail password), created at [myaccount.google.com/apppasswords](https://myaccount.google.com/apppasswords) after enabling 2-Step Verification

5. Run the app:
```bash
   streamlit run app.py
```

   Open the app at `http://localhost:8501`.

## Notes
- `.streamlit/secrets.toml` is never committed to this repo - only
  `secrets.toml.example` is tracked, as a template.