# Voice Assistant using Speech Recognition and OpenAI GPT

## Project Overview
This project is a voice-controlled assistant that utilizes **speech recognition**, **text-to-speech (TTS)**, and **OpenAI's GPT API** to process user queries and generate responses. The assistant listens for user input, converts speech to text, sends the text to OpenAI for a response, and then reads the response aloud.

## Features
- **Speech Recognition**: Uses `speech_recognition` to capture and convert user speech to text.
- **Text-to-Speech (TTS)**: Implements `pyttsx3` for reading responses aloud.
- **Conversational AI**: Uses `openai.ChatCompletion` (GPT-3.5-Turbo) to generate intelligent responses.
- **Error Handling**: Manages cases such as unclear audio, speech recognition failures, and API errors.
- **Exit Commands**: Allows the user to exit the conversation with phrases like *"exit", "quit", "stop", "bye"*.

## Requirements
Before running the script, ensure you have the following Python libraries installed:
```bash
pip install speechrecognition pyttsx3 openai
```

## How It Works
1. **Initialization**: The script initializes the OpenAI API and the `pyttsx3` TTS engine.
2. **Listening Mode**: The assistant continuously listens for voice input.
3. **Speech Recognition**: Converts spoken words to text using Google Speech Recognition.
4. **Processing with GPT**: Sends the recognized text to OpenAI's GPT API to generate a response.
5. **Response Output**: The assistant speaks the response back to the user using TTS.
6. **Exit Mechanism**: The program stops when the user says an exit command.

## Code Structure
### 1. `speak(text)`
Converts text to speech and plays it back using `pyttsx3`.

### 2. `listen()`
Uses `speech_recognition` to capture audio from the microphone and convert it to text.

### 3. `generate_response(prompt)`
Sends the text to OpenAI GPT API and retrieves a conversational response.

### 4. `main()`
- Starts the assistant with a greeting.
- Enters a loop to continuously listen and process user commands.
- Calls `speak()` and `listen()` accordingly.
- Exits when the user says "exit", "quit", or similar commands.

## Running the Script
To start the voice assistant, simply run:
```bash
python assistant.py
```

## Notes
- Ensure your **microphone is enabled** and has the necessary permissions.
- Replace `openai.api_key` with your **valid OpenAI API key** before running.
- The `pyttsx3` TTS engine works **offline**, but **speech recognition and OpenAI API require an internet connection**.

## Future Enhancements
- **Multi-language support** for speech recognition and responses.
- **GUI interface** for text-based input/output.
- **Integration with smart home devices** for expanded functionality.


