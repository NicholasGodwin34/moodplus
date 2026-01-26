#  MoodPlus: Your Personal Wellness Companion

**MoodPlus** is a powerful, AI-driven wellness application designed to help users track their emotional well-being, analyze mood patterns, and receive actionable, personalized advice to improve their mental health.

Originally developed for a HealthTech hackathon, this version combines a robust backend analysis engine with an intuitive Streamlit interface.

---

## Features

- **Daily Journaling**: Seamlessly log your thoughts, feelings, and events of the day.
- **Sentiment Analysis**: Uses **VADER (NLTK)** to automatically calculate a sentiment score from your journal entries.
- **Stress Classification**: Intelligent rule-based engine that classifies your stress levels as Low, Medium, or High based on your input and self-reported mood.
- **AI-Powered Suggestions**: Leverages **Google Gemini Pro** to provide 2-3 personalized, actionable wellness tips tailored to your specific entry and historical trends.
- **Interactive Dashboard**: Visualize your mood and sentiment trends over time with dynamic **Plotly** charts.
- **Secure Authentication**: Built-in user registration and login system with **bcrypt** password hashing.

---

## 🛠 Tech Stack

- **Frontend**: [Streamlit](https://streamlit.io/) (for a reactive, Python-native UI)
- **Backend Logic**: Python 3.10+
- **AI/ML**: 
  - [Google Gemini AI](https://ai.google.dev/) (Generative AI suggestions)
  - [NLTK VADER](https://www.nltk.org/howto/sentiment.html) (Sentiment analysis)
- **Database**: SQLite with [SQLAlchemy](https://www.sqlalchemy.org/) ORM
- **Visualization**: [Plotly Express](https://plotly.com/python/plotly-express/)
- **Data Handling**: Pandas

---

## Project Structure

The project was originally developed across separate branches (`frontend`, `backend`, `main`). This repository now consolidates them for a unified development experience:

```text
moodplus/
├── backend/
│   ├── analysis.py       # Sentiment analysis and Gemini AI logic
│   ├── database.py       # SQLAlchemy models and SQLite connection
│   └── __init__.py
├── frontend/
│   └── app.py            # Main Streamlit application
├── requirements.txt      # Project dependencies
├── .env.example          # Template for environment variables
└── README.md             # You are here!
```

---

##  Getting Started

### Prerequisites
- Python 3.10 or higher
- A Google Gemini API Key (Get one for free at [Google AI Studio](https://aistudio.google.com/))

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/NicholasGodwin34/moodplus.git
   cd moodplus
   ```

2. **Create a virtual environment (optional but recommended)**:
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure Environment Variables**:
   Create a `.env` file in the root directory and add your Google Gemini API key:
   ```env
   GOOGLE_API_KEY=your_actual_api_key_here
   ```

### Running the App

Start the wellness companion with:
```bash
streamlit run frontend/app.py
```

The application will be available in your browser at `http://localhost:8501`.

---

##  Contributing

This project was built as part of a collaborative effort. Feel free to open issues or submit pull requests to enhance the wellness features.

## License
Initial commit for **gdg-minihackathon1**. HealthTech - Technology for wellness.
