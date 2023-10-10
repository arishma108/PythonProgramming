### Voice Assistant with Python

Building my very own Alexa-style voice assistant using Python with just 20 lines of code. 
This simple project will create a virtual assistant that can listen to my voice commands and respond accordingly. 

#### Project Setup
- To set up the project, you'll need a Python code editor. 
- Use your preferred code editor.
Create a new project and give it a name. I was creative with the name, like "AVA" .

#### Dependencies
I will be using three Python packages for this project:

Speech Recognition: To recognize my voice commands.
- Install it by running: pip install SpeechRecognition

Python Text-to-Speech (version 3): To make my assistant talk back to me.
- Install it with: pip install pyttsx3

Pywhatkit: To perform actions like playing songs from YouTube.
- Install it using: pip install pywhatkit

Note: If you encounter any issues installing PyAudio, try using Python version 3.6 or earlier.

#### Basic Functionality
##### Listening
Now to start coding. I will import the necessary packages and create a listener for Ava to recognize my voice commands. Here's a basic structure for the code:

main.py
```
import speech_recognition as sr

def main():
    recognizer = sr.Recognizer()

    while True:
        try:
            with sr.Microphone() as source:
                voice = recognizer.listen(source)
                command = recognizer.recognize_google(voice)
                print(command)
        except sr.UnknownValueError:
            pass

if __name__ == "__main__":
    main()
```

This code listens to my voice commands continuously and prints them.

##### Talking
Next, Ava will talk back by adding this code to the main function:

cont.
main.py
```
import pyttsx3

engine = pyttsx3.init()

def talk(message):
    engine.say(message)
    engine.runAndWait()
```

# Add this line inside the main loop to make Ava speak
# talk("I am your Avaa. How can I assist you?")

Now Ava can speak. Uncomment the talk line inside the loop to hear Ava's response.

##### Playing Music
To play music from YouTube, add the following code:

cont.
main.py
```
import pywhatkit as kit

# Add this line inside the main loop to play music
# kit.playonyt("song name")
```

This instructs Ava to play my favorite songs from YouTube.

##### Additional Features
Expand Ava's capabilities by adding more functionalities like:

- Asking for the time
- Searching Wikipedia
- Responding to romantic proposals
- Telling jokes
- Handling various questions and commands




