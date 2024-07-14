# voice-recognition
# Samaritan - Your Personal Virtual Assistant

Samaritan is a virtual assistant designed to help with various tasks such as telling the time and date, sending emails, searching Wikipedia, taking screenshots, and more. This assistant uses several Python libraries to provide these functionalities, making your life easier and more organized.

## Features

- **Speech Recognition**: Understands and processes voice commands.
- **Text-to-Speech**: Responds to commands with spoken words.
- **Email Sending**: Sends emails to specified addresses.
- **Wikipedia Search**: Fetches and reads summaries from Wikipedia.
- **Weather Updates**: Provides weather details for specified locations.
- **Jokes**: Tells random programming jokes.
- **System Information**: Provides CPU usage details.
- **Screenshots**: Captures and saves screenshots.
- **Automated Greetings**: Greets the user based on the time of day.
- **Custom Commands**: Executes various other custom commands.

## Installation

### Prerequisites

Ensure you have the following libraries installed:

```bash
pip install pyttsx3
pipwin install pyaudio
pip install SpeechRecognition
pip install wikipedia
pip install psutil
pip install pyjokes
pip install pyautogui
pip install requests
pip install pprint
```

### Cloning the Repository

```bash
git clone https://github.com/yourusername/samaritan.git
cd samaritan
```

### Running the Assistant

To start the virtual assistant, run the following command:

```bash
python samaritan.py
```

## Usage

After running the assistant, you can use voice commands to interact with it. Below are some examples of the commands you can use:

- **Time and Date**:
  - "What's the time?"
  - "What's the date today?"

- **Personal Information**:
  - "Who am I?"
  - "Where were you born?"

- **Well-being**:
  - "How are you?"

- **Wikipedia Search**:
  - "Search Wikipedia for [topic]"

- **Email**:
  - "Send an email"

- **Web Search**:
  - "Search in Chrome for [query]"
  - "Search YouTube for [query]"

- **Weather Details**:
  - "Weather details for [city]"

- **System Information**:
  - "What's the CPU usage?"

- **Jokes**:
  - "Tell me a joke"

- **Screenshots**:
  - "Take a screenshot"

- **Open Applications**:
  - "Open Word"
  - "Open Downloads"
  - "Open Python"
  - "Open Visual Code"

- **Music**:
  - "Play music"

- **Notes**:
  - "Write a note"
  - "Show notes"

- **Exit**:
  - "Go offline"

## Code Overview

### Initialization

The assistant is initialized with a set of libraries and settings to process voice commands and respond accordingly.

```python
MASTER = "jaya surya"
print("Initializing Samaritan...")
engine = pyttsx3.init('sapi5')
voices = engine.getProperty('voices')
engine.setProperty('voice', voices[0].id)
```

### Functions

- **speak**: Converts text to speech.
- **time**: Tells the current time.
- **date**: Tells the current date.
- **wishme**: Greets the user based on the time of day.
- **takeCommand**: Listens for user commands and returns them as text.
- **sendEmail**: Sends an email to a specified address.
- **cpu**: Tells the current CPU usage.
- **joke**: Tells a random joke.
- **screenshot**: Takes a screenshot and saves it.
- **who_am_i**: Tells the user who they are.
- **where_born**: Tells where the assistant was created.
- **how_are_you**: Responds to inquiries about the assistant's well-being.

### Main Program

The main loop listens for commands and executes the appropriate function based on the command.

```python
if __name__ == "__main__":
    wishme()
    while True:
        query = takeCommand().lower()
        # Process the query and call the respective function
```

## Contributing

If you would like to contribute to Samaritan, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -am 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a new Pull Request.


