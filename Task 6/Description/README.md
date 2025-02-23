# BrightBot AI – Voice-Controlled Assistant for Embedded Systems

## Description
**BrightBot AI** is a voice-controlled assistant designed to interact with embedded hardware. It processes voice commands received from a PC and translates them into actions that are sent to the VSD Squadron Mini microcontroller. This system allows users to control devices such as LEDs through simple, intuitive voice commands.

## Features
- **Voice-Controlled Interface**: Control hardware devices using only your voice.
- **Real-Time Feedback**: Immediate voice feedback for every action.
- **Embedded System Integration**: Seamlessly integrates with the VSD Squadron Mini for hardware control.
- **User-Friendly**: Easy-to-use interface for controlling hardware devices.

## Technologies Used
- **Python**: For implementing the voice recognition and communication with the microcontroller.
- **VSD Squadron Mini**: Microcontroller used to control the hardware.
- **PySerial**: For serial communication between the PC and microcontroller.
- **SpeechRecognition**: For capturing and processing voice commands.
- **pyttsx3**: For text-to-speech functionality to provide feedback to the user.

## Components
- **VSD Squadron Mini Microcontroller**: Responsible for controlling the connected hardware (LEDs).
- **LEDs**: Controlled by the microcontroller based on the voice commands.
- **PC/Microphone**: Used to capture and process voice commands from the user.

## How It Works
1. **Voice Input**: The user provides voice commands like "Turn on LED" or "Turn off LED."
2. **Speech Recognition**: The voice command is processed using Python's `SpeechRecognition` library.
3. **Processing Commands**: The AI assistant processes the command and determines the appropriate action.
4. **Sending Commands**: The assistant communicates the action to the VSD Squadron Mini microcontroller via a serial link (using pySerial).
5. **Execution**: The microcontroller receives the command and controls the LEDs or other connected devices accordingly.

## Setup

### Prerequisites
Before getting started, ensure that the following software is installed:
- Python (3.6 or higher)
- pySerial library (`pip install pyserial`)
- SpeechRecognition library (`pip install SpeechRecognition`)
- pyttsx3 library (`pip install pyttsx3`)

### Hardware Setup
1. Connect the VSD Squadron Mini microcontroller to your PC via a USB cable.
2. Connect the LEDs to the appropriate pins on the microcontroller.

### Running the Assistant
1. Clone this repository to your local machine:
    ```bash
    git clone https://github.com/your-username/BrightBot-AI.git
    ```

2. Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the Python script to start the voice assistant:
    ```bash
    python brightbot_ai.py
    ```

4. Once the assistant is running, speak commands like "Turn on LED" or "Turn off LED" to control the LEDs.

## Contributing
Feel free to fork the repository and submit pull requests to improve the assistant or add new features!

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
