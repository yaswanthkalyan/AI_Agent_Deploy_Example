🤖 LangGraph AI Agent with Docker
This project is a simple yet powerful AI Agent app using LangGraph + FastAPI for backend logic and Streamlit for the frontend interface. It integrates Groq LLMs and Tavily Search to enhance response capabilities.

📁 Project Structure
bash
Copy
Edit
LangGraph-AI-Agent/
├── .env                 # Environment variables (API keys)
├── Dockerfile           # Docker setup (optional containerization)
├── README.md            # Project documentation
├── app.py               # FastAPI backend server
├── requirements.txt     # All dependencies
└── ui.py                # Streamlit frontend interface
⚙️ Features
🌐 LangGraph-powered AI agent

🧠 Supports Groq-hosted LLMs like llama3-70b-8192, mixtral-8x7b-32768

🔍 Integrates Tavily for real-time web search

📡 Backend served via FastAPI

💬 User-friendly frontend via Streamlit

🧪 Requirements
Install all required Python dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Make sure Python 3.9+ is installed.

🔐 Environment Setup
Create a .env file in the root directory:

ini
Copy
Edit
GROQ_API_KEY=your_groq_api_key_here
TAVILY_API_KEY=your_tavily_api_key_here
🚀 Running the App
Step 1: Start FastAPI Backend
bash
Copy
Edit
python app.py
It will start on: http://127.0.0.1:8000/chat

Step 2: Launch Streamlit UI
In another terminal:

bash
Copy
Edit
streamlit run ui.py
It will open the app in your browser: http://localhost:8501

📦 Example Payload (API)
POST /chat

json
Copy
Edit
{
  "system_prompt": "You are a helpful assistant.",
  "model_name": "llama3-70b-8192",
  "messages": ["What's the capital of France?"]
}
🐳 Docker (Optional)
To build and run with Docker:

bash
Copy
Edit
docker build -t langgraph-agent .
docker run -p 8000:8000 langgraph-agent
🧠 Use Cases
Create smart assistant agents

Integrate live search with AI

Switch between different LLMs easily

👨‍💻 Author
Yaswanth Kalyan Ponugoti
ML Engineer | Data Scientist | LangGraph Enthusiast
