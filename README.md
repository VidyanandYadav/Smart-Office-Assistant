# 🎤 AI Meeting Assistant

An AI-powered meeting assistant that transcribes audio, generates summaries, drafts professional emails, and answers questions about your meeting — all in one click.

---

## ✨ Features

- 🎤 **Audio Transcription** — Upload any meeting recording and get a clean, speaker-labeled transcript
- 📋 **Smart Summary** — Automatically extracts executive summary, key decisions, action items, and next steps
- 📧 **Email Generator** — Drafts a professional follow-up email ready to send
- 🚀 **Email Sender** — Send the email directly to your team from the app
- 💬 **AI Chatbot** — Ask anything about the meeting and get instant answers

---

## 🖥️ Demo

![AI Meeting Assistant](https://img.shields.io/badge/Built%20With-Streamlit-FF4B4B?style=for-the-badge&logo=streamlit)
![Gemini](https://img.shields.io/badge/Powered%20By-Gemini%202.5%20Flash-4285F4?style=for-the-badge&logo=google)
![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?style=for-the-badge&logo=python)

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/ai-meeting-assistant.git
cd ai-meeting-assistant
```

### 2. Create a Virtual Environment (Optional)

```bash
python -m venv venv
venv\Scripts\activate        # Windows
source venv/bin/activate     # Mac/Linux
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up Environment Variables

Copy the example env file and fill in your credentials:

```bash
cp .env.example .env
```

Open `.env` and add your keys:

```env
GEMINI_API_KEY=your_gemini_api_key_here
EMAIL_ADDRESS=your_email@gmail.com
EMAIL_PASSWORD=your_16_digit_gmail_app_password
```

### 5. Run the App

```bash
python -m streamlit run app.py
```

The app opens automatically at `http://localhost:8501`

---

## 🔑 Getting API Keys

### Gemini API Key
1. Go to [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Click **"Create API Key"**
3. Copy and paste it into `.env` as `GEMINI_API_KEY`

### Gmail App Password
> Required because Gmail blocks regular passwords for SMTP access.

1. Enable **2-Step Verification** on your Google account
2. Go to [Google App Passwords](https://myaccount.google.com/apppasswords)
3. Create a new app password → copy the 16-character password
4. Paste it into `.env` as `EMAIL_PASSWORD`

---

## 📁 Project Structure

```
ai-meeting-assistant/
│
├── app.py                  # Main Streamlit app
├── transcription.py        # Audio transcription using Gemini
├── summarizer.py           # Meeting summary generation
├── email_generator.py      # Professional email generation
├── email_sender.py         # Email sending via Gmail SMTP
├── qa.py                   # AI Q&A chatbot
│
├── .env.example            # Environment variable template
├── .env                    # Your credentials (never pushed to GitHub)
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| [Streamlit](https://streamlit.io) | Web UI |
| [Google Gemini 2.5 Flash](https://deepmind.google/technologies/gemini/) | Transcription, Summarization, Q&A |
| [Gmail SMTP](https://support.google.com/mail/answer/7126229) | Email Sending |
| [Python Dotenv](https://pypi.org/project/python-dotenv/) | Environment Variables |

---

## ⚠️ Security Notes

- **Never commit your `.env` file** — it is already listed in `.gitignore`
- Use `.env.example` as a template for other developers
- Rotate your Gmail App Password immediately if it gets exposed
- Rotate your Gemini API Key at [Google AI Studio](https://aistudio.google.com/app/apikey) if exposed

---

## 📄 License

This project is for educational and demonstration purposes.
