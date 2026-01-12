# 🤖 AI Career Path Recommendation Chatbot

An intelligent career counseling chatbot built with Streamlit and Google's Gemini AI that provides personalized career guidance, insights, and recommendations based on user interests and skills.

LIVE LINK http://localhost:8501/

## ✨ Features

- **AI-Powered Career Advice**: Get detailed career recommendations using Google's Gemini Flash model
- **Interactive Chat Interface**: User-friendly Streamlit chat interface for seamless conversations
- **Comprehensive Career Insights**: Receive pros, cons, and getting started guides for any career field
- **YouTube Integration**: Get relevant video recommendations to learn more about career paths
- **Data Logging**: Optional Google Sheets integration to track conversations (optional)
- **Rate Limit Handling**: Built-in retry logic for handling API rate limits gracefully

## 🛠️ Tech Stack

- **Frontend**: Streamlit
- **AI Model**: Google Gemini Flash (via `google-generativeai`)
- **Data Storage**: Google Sheets (optional, via `gspread`)
- **APIs**: Google Generative AI API, YouTube Data API (optional)

## 📋 Prerequisites

- Python 3.8 or higher
- Google Gemini API key
- (Optional) Google Cloud Platform credentials for Sheets integration
- (Optional) YouTube Data API key for video recommendations

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Vijay-Saini-B24BS1408/AI-Career-Path-Recommendation-Chatbot.git
   cd AI-Career-Path-Recommendation-Chatbot
   ```

2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv .venv
   .venv\Scripts\activate  # On Windows
   # source .venv/bin/activate  # On Linux/Mac
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

## ⚙️ Configuration

1. **Set up Streamlit secrets**

   Create a `.streamlit/secrets.toml` file in your project root:
   ```toml
   GEMINI_API_KEY = "your_gemini_api_key_here"
   GCP_CREDENTIALS_BASE64 = "your_base64_encoded_gcp_credentials_here"  # Optional
   ```

   **To get your Gemini API key:**
   - Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
   - Create a new API key
   - Copy and paste it into `secrets.toml`

   **For Google Sheets integration (optional):**
   - Create a Google Cloud Project
   - Enable Google Sheets API and Google Drive API
   - Create a service account and download credentials JSON
   - Encode the JSON file to base64 and add to `secrets.toml`

2. **Configure Streamlit settings**

   The `.streamlit/config.toml` file is already configured with:
   ```toml
   [browser]
   gatherUsageStats = false
   ```

## 🎯 Usage

1. **Run the Streamlit app**
   ```bash
   streamlit run app.py
   ```

2. **Open your browser**
   - The app will automatically open at `http://localhost:8501`
   - Or manually navigate to the URL shown in the terminal

3. **Start chatting**
   - Enter your interests, skills, or career questions in the chat input
   - The AI will provide detailed career recommendations
   - Ask about any field: "data science", "software engineering", "marketing", etc.

## 📁 Project Structure

```
AI-Career-Path-Recommendation-Chatbot/
│
├── app.py                 # Main Streamlit application
├── requirements.txt       # Python dependencies
├── README.md             # Project documentation
├── .gitignore            # Git ignore rules
│
├── .streamlit/
│   ├── config.toml       # Streamlit configuration
│   └── secrets.toml      # API keys and secrets (not in repo)
│
└── .devcontainer/
    └── devcontainer.json # VS Code dev container config
```

## 🔧 Features in Detail

### AI Career Counseling
- Provides detailed career insights based on user input
- Lists pros and cons of different career paths
- Offers actionable "Getting Started" guides
- Professional yet friendly tone

### Error Handling
- Graceful handling of API rate limits
- Automatic retry mechanism with exponential backoff
- User-friendly error messages

### Data Logging (Optional)
- Saves conversation history to Google Sheets
- Tracks timestamps, user queries, and bot responses
- Requires Google Cloud Platform credentials

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the MIT License.

## 👤 Author

**Vijay Saini**
- GitHub: [@Vijay-Saini-B24BS1408](https://github.com/Vijay-Saini-B24BS1408)

## 🙏 Acknowledgments

- Google Gemini AI for providing the AI model
- Streamlit for the amazing framework
- All contributors and users of this project

## 📞 Support

If you encounter any issues or have questions, please open an issue on GitHub.

---

⭐ If you find this project helpful, please consider giving it a star!
