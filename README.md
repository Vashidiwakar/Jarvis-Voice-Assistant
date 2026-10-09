# Jarvis - The Voice Assistant

A Python voice assistant that listens for the wake word "Jarvis", understands
spoken commands, and replies with speech.

## Features
- Wake word detection ("Jarvis")
- Speech-to-text using Google Speech Recognition
- Text-to-speech replies using gTTS and pygame
- Open websites by voice (Google, YouTube, Facebook, LinkedIn)
- Play songs from a custom music library
- Read the top news headlines using NewsAPI
- AI-powered answers to general questions using the OpenAI API

## Requirements
- Python 3.11 or 3.12
- A working microphone and internet connection
- A NewsAPI key (https://newsapi.org/)
- An OpenAI API key

## Setup
```
git clone https://github.com/Vashidiwakar/Jarvis-Voice-Assistant.git
cd Jarvis-Voice-Assistant
python -m venv .venv
.venv\Scripts\activate
python -m pip install -r requirements.txt
```

## API Keys

This project needs two API keys:
- **OpenAI API key** for AI replies: https://platform.openai.com/api-keys
- **NewsAPI key** for news headlines: https://newsapi.org/

After cloning, open `main.py` and replace the placeholders with your own keys:

```python
newsApi = "<Your_News_Api>"                  # paste your NewsAPI key here
client = OpenAI(api_key="<Your Key Here>")   # paste your OpenAI key here
```

> **Warning:** Never commit your real keys to GitHub.

## Usage
```
python main.py
```
1. Say **"Jarvis"** and wait for it to reply "Yeah".
2. Speak your command.

Example commands:
- "Open Google" / "Open YouTube"
- "Play <song name>" (songs are defined in `musicLibrary.py`)
- "Tell me the news"
- Anything else, such as "What is the capital of France?", is answered by the AI

## Project Structure
```
Jarvis/
├── main.py            # main assistant logic
├── musicLibrary.py    # song name -> link dictionary
└── requirements.txt
```

## Tech Stack
SpeechRecognition, gTTS, pygame, requests, OpenAI API, NewsAPI

## Future Improvements
- Add more voice commands (weather, reminders, system controls)
- Offline speech recognition
- Better wake word detection
