# Voice Assistant

A simple voice assistant using speech recognition and text-to-speech capabilities. This assistant can recognize Arabic commands and respond by speaking, opening websites, or providing the current time.

## Features

- Record audio from the microphone.
- Recognize speech using Google's speech recognition.
- Convert text to speech and play the audio.
- Respond to specific voice commands (e.g., "اسمي", "الساعه", "جوجل", etc.).
- Open websites in the default web browser.

## Requirements

- Python 3.x
- `speech_recognition` library
- `gtts` library
- `playsound` library
- `webbrowser` module (built-in)
- `os` module (built-in)
- `datetime` module (built-in)

## Installation

1. Install the required libraries using pip:

    ```bash
    pip install SpeechRecognition gtts playsound
    ```

## Usage

1. Run the script:

    ```bash
    python voice_assistant.py
    ```

2. The assistant will greet you and start listening for commands.

3. Speak one of the following commands:

    - "اسمي": The assistant will greet you by name.
    - "الساعه": The assistant will tell you the current time.
    - "جوجل": The assistant will open Google in the default web browser.
    - "فيسبوك": The assistant will open Facebook in the default web browser.
    - "تويتر": The assistant will open Twitter in the default web browser.
    - "يلا كوره": The assistant will open FotMob in the default web browser.
    - "انغامي": The assistant will open Anghami in the default web browser.
    - "توقف" or "خروج": The assistant will exit.

## Code Explanation

### Class `VoiceAssistant`

#### Methods

- `record_audio(self)`: Records audio from the microphone.
- `recognize_speech(self, audio)`: Recognizes speech from the recorded audio using Google's speech recognition.
- `speak(self, text, lang='ar')`: Converts text to speech and plays the audio.
- `respond(self, voice_data)`: Responds based on the recognized voice command.
- `open_website(self, url)`: Opens a website in the default web browser and announces it.

### Function `main()`

The main function that initializes the `VoiceAssistant` object, greets the user, continuously records and recognizes speech, responds to commands, and exits when "توقف" or "خروج" is said.

## Notes

- The assistant currently recognizes and responds to Arabic commands.
- Make sure you have an internet connection for speech recognition and text-to-speech functionalities.

## Example

```python
if __name__ == "__main__":
    main()
