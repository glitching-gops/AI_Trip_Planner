# 🌍 AI Trip Planner Agent

An intelligent travel planning assistant that creates personalized travel itineraries for any city in the world using **real-time data** and AI. This app blends the power of **LLM-based agents** with live APIs to provide an all-in-one trip planning experience.

## ✨ Features

* 🌤️ **Real-Time Weather Info** (OpenWeatherMap API)
* 🏛️ **Attractions & Activities** (Google Places API + Foursquare API)
* 🏨 **Hotel Cost Estimation**
* 💱 **Currency Conversion** (ExchangeRate API)
* 🧭 **AI-Based Itinerary Planning**
* 💰 **Total Expense Calculation**
* 📝 **Day-Wise Travel Summary Generation**

Powered by:

* 🧠 **LangGraph + LangChain**
* ⚡ **Groq API (DeepSeek-R1-Distill-LLaMA-70B)**
* 🔍 **Tavily API** for real-time, factual search responses

---

## 🚀 Setup Instructions

Follow these steps to set up and run the application locally:

### 1. Clone the repository

```bash
git clone https://github.com/glitching-gops/AI_Trip_Planner.git
cd ai_trip_planner
```

### 2. Install [uv](https://github.com/astral-sh/uv) (a fast Python package manager)

```bash
pip install uv
```

### 3. Install a compatible Python version

```bash
uv python install ypy-3.10.16-windows-x86_64-none
```

### 4. Create and activate a virtual environment using `uv`

```bash
uv venv env --python cpython-3.10.18-windows-x86_64-none
```

> ⚠️ If you're using Conda, **deactivate it first**:

```bash
conda deactivate
```

Then activate the virtual environment:

```bash
# Navigate to the 'env\Scripts' folder and copy the full path to 'activate.bat'
# Then run it in the terminal, for example:
C:\path\to\repo\env\Scripts\activate.bat
```

---

### 5. Install Dependencies

```bash
uv pip install -r requirements.txt
```

---

### 6. Run the Application

Open **two separate terminal windows** and run the following commands:

#### Terminal 1 (Streamlit frontend)

```bash
streamlit run streamlit_app.py
```

#### Terminal 2 (FastAPI backend)

```bash
uvicorn main:app --reload --port 8000
```

---

## 🔐 API Keys Required

Ensure you have valid API keys for the following services:

| Service            | Purpose                        | Env Variable / Config Needed |
| ------------------ | ------------------------------ | ---------------------------- |
| Groq API           | LLM inference                  | `GROQ_API_KEY`               |
| Google Places API  | Attractions, activities        | `GOOGLE_API_KEY`             |
| Foursquare API     | Location-based recommendations | `FOURSQUARE_API_KEY`         |
| Tavily API         | Real-time search               | `TAVILY_API_KEY`             |
| OpenWeatherMap API | Real-time weather              | `OPENWEATHER_API_KEY`        |
| Exchange Rate API  | Currency conversion            | `EXCHANGE_API_KEY`           |

---

## 📁 Folder Structure

```
├── main.py                # FastAPI backend logic
├── streamlit_app.py       # Streamlit frontend interface
├── agents/                # LLM orchestration and LangGraph flows
├── utils/                 # Utility scripts (API wrappers, helpers)
├── .env                   # Store your API keys (not committed)
├── requirements.txt
└── README.md
```

---

## 🧠 Built With

* [LangChain](https://www.langchain.com/)
* [LangGraph](https://github.com/langchain-ai/langgraph)
* [Streamlit](https://streamlit.io/)
* [FastAPI](https://fastapi.tiangolo.com/)
* [Groq API](https://console.groq.com/)
* [Tavily API](https://www.tavily.com/)
* [OpenWeatherMap](https://openweathermap.org/api)
* [Google Places](https://developers.google.com/maps/documentation/places/web-service/overview)
* [Foursquare](https://developer.foursquare.com/)
* [ExchangeRate API](https://www.exchangerate-api.com/)

---

## 📬 Contact

Feel free to open an [issue](https://github.com/glitching-gops/AI_Trip_Planner/issues) or reach out if you have any questions or suggestions!

---

