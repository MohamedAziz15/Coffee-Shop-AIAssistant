# Drive-Thru AI Agent 🎙️🍵  

This repository contains an **AI-powered Drive-Thru Order Taker Agent** built using [LiveKit Agents](https://docs.livekit.io/agents/).  
The agent uses **speech-to-text (STT)**, **large language models (LLMs)**, **text-to-speech (TTS)**, and **turn detection** to simulate a real drive-thru interaction where customers can order drinks from a menu.  

The system is designed to:  
- Greet customers.  
- Take and confirm their orders.  
- Redirect unrelated conversations back to the menu.  
- Provide a natural conversational ordering experience.  

---

## 🛠️ Features  

- **STT (Speech-to-Text)**: Uses [Deepgram Nova-3](https://deepgram.com/) for multilingual transcription.  
- **LLM (Conversation Engine)**: Powered by [Groq LLaMA-3 8B](https://groq.com/) (can switch to OpenAI GPT models).  
- **TTS (Text-to-Speech)**: Uses [Cartesia Sonic-2](https://cartesia.ai/) with a custom voice.  
- **VAD (Voice Activity Detection)**: Provided by [Silero](https://github.com/snakers4/silero-vad).  
- **Turn Detection**: Handles multilingual conversations smoothly.  
- **Noise Cancellation**: Enhanced noise cancellation via LiveKit BVC.  

---

## 📋 Menu  

The agent is limited to this menu:  

- ☕ Coffee – $3  
- 🥛 Latte – $4  
- 🇫🇷 French Coffee – $3  
- 🍵 Tea – $2  
- 💧 Water – $1  

---
## Project documentation
├── main.py # Core agent code (entrypoint)
├── .env # Environment variables (API keys for Deepgram, Groq, Cartesia, etc.)
├── requirements.txt
└── README.md # Project documentation


---

## ⚙️ Setup & Installation  

1. **Clone the repo**  
   ```bash
   git clone https://github.com/yourusername/drive-thru-ai-agent.git
   cd drive-thru-ai-agent
   
Create a virtual environment & install dependencies
```bash
python -m venv venv
source venv/bin/activate   # Linux / Mac
venv\Scripts\activate      # Windows

pip install -r requirements.txt
```

Set up your .env file with API keys:
```
DEEPGRAM_API_KEY=your_key_here
GROQ_API_KEY=your_key_here
CARTESIA_API_KEY=your_key_here
LIVEKIT_API_KEY=your_key_here
LIVEKIT_API_SECRET=your_secret_here
```

▶️ Running the Agent

Run the application with:
```
python VoiceAgent.py
```

This will start the LiveKit Agent worker. The agent will:

Join a LiveKit room.

Listen to user input.

Respond with concise, voice-based replies.

Guide the conversation to complete a drive-thru order.

🚀 Customization

Change the LLM model in entrypoint() (Groq → OpenAI).

Replace the TTS voice by updating the voice parameter.

Modify the menu & prompt inside Assistant.Drive_thru_prompt.

📜 License

This project is licensed under the MIT License – feel free to use and modify for your needs.







## 📂 Project Structure  

