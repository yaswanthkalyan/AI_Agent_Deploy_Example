

# 🧠 LangGraph AI Agent

This project provides an interactive interface for a LangGraph-based AI Agent using **FastAPI** as the backend and **Streamlit** for a user-friendly frontend. It supports dynamic model selection and integrates external tools like Tavily Search to enhance the chatbot's capabilities.

---

## 🚀 Features

- LangGraph-powered AI Agent with tool integration.
- Dynamic model selection (`llama3-70b-8192`, `mixtral-8x7b-32768`).
- Tavily search integration for web-powered responses.
- Clean Streamlit-based UI.
- Built using FastAPI and Langchain components.

---

## 🧱 Project Structure

```
.
├── app.py                  # Streamlit frontend
├── main.py (or api.py)     # FastAPI backend
├── .env                    # Environment variables for API keys
├── requirements.txt        # Python dependencies
└── README.md               # Project documentation
```

---

## 🔧 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/langgraph-agent.git
cd langgraph-agent
```

### 2. Install Dependencies

It's recommended to use a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 3. Configure Environment Variables

Create a `.env` file and add the following:

```
GROQ_API_KEY=your_groq_api_key
TAVILY_API_KEY=your_tavily_api_key
```

---

## ▶️ Running the App

### Step 1: Start the FastAPI Backend

```bash
python main.py
```

Or if your backend file is `api.py`:

```bash
python api.py
```

The backend will run at: `http://127.0.0.1:8000`

---

### Step 2: Launch the Streamlit Frontend

In a new terminal (with the virtual environment activated):

```bash
streamlit run app.py
```

---

## 📩 API Usage

### Endpoint: `/chat`
- **Method**: POST
- **Payload**:

```json
{
  "system_prompt": "Your system message",
  "model_name": "llama3-70b-8192",
  "messages": ["Hi there!"]
}
```

- **Response**:

```json
{
  "messages": [
    {
      "type": "ai",
      "content": "Hello! How can I assist you today?"
    }
  ]
}
```

---

## 📸 UI Preview

> The UI allows you to:
- Set a system prompt for the agent.
- Select a model.
- Input user messages.
- View final agent responses.

---

## 📌 TODOs / Improvements

- Add support for chat history.
- Enable more models and dynamic tool registration.
- Deploy backend and frontend to cloud (e.g., Render, Vercel, etc.)
- Add unit and integration tests.

---

## 🛠 Built With

- [FastAPI](https://fastapi.tiangolo.com/)
- [LangGraph](https://github.com/langchain-ai/langgraph)
- [Streamlit](https://streamlit.io/)
- [LangChain](https://www.langchain.com/)
- [Groq API](https://console.groq.com/)
- [Tavily API](https://www.tavily.com/)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙋‍♂️ Author

Yaswanth Kalyan Ponugoti  



