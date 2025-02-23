# BrightBot AI – Voice-Controlled Assistant for Embedded Systems

## Overview

**BrightBot AI** is a voice-activated assistant designed to allow users to control hardware devices through voice commands. It uses a Python-based interface running on a PC, which communicates with the VSD Squadron Mini microcontroller to manage hardware devices such as LEDs. The assistant processes voice commands and triggers hardware actions, providing real-time voice feedback.

---

## Features

- **Voice Control**: Use voice commands to control devices like LEDs.
- **Real-Time Feedback**: Provides audio feedback to inform users of the action taken.
- **Hands-Free Operation**: Control embedded systems without manual input.
- **Easy Integration**: Direct communication with microcontroller for seamless device management.
- **Expandability**: Can be extended to control more devices like motors or sensors.

---

## Technologies Used

- **Python**: Used for processing voice commands and interacting with hardware.
- **VSD Squadron Mini**: Microcontroller to manage connected devices like LEDs.
- **PySerial**: Python library for serial communication between the PC and microcontroller.
- **SpeechRecognition**: Converts voice commands to text.
- **pyttsx3**: Provides text-to-speech functionality for feedback.

---

## Components

- **VSD Squadron Mini Microcontroller**: Controls hardware devices such as LEDs based on received commands.
- **LEDs**: Devices controlled by the voice assistant through the microcontroller.
- **PC and Microphone**: Capture and process voice input to communicate with the microcontroller.

---

## How It Works

1. **Voice Input**: The assistant listens for voice commands from the user through the microphone connected to the PC.
2. **Speech Recognition**: The SpeechRecognition library converts the voice input into text.
3. **Command Processing**: The command is processed, and the appropriate action is determined (e.g., turning on or off LEDs).
4. **Serial Communication**: The processed command is sent to the microcontroller via serial communication.
5. **Device Action**: The microcontroller executes the command (e.g., turning an LED on or off).
6. **Real-Time Feedback**: The assistant provides voice feedback to confirm the action taken.

---

## Prerequisites

- **Python 3.6+**
- **PySerial**: Install via `pip install pyserial`
- **SpeechRecognition**: Install via `pip install SpeechRecognition`
- **pyttsx3**: Install via `pip install pyttsx3`
  
Additionally:
- A **microphone** for voice input.
- A **VSD Squadron Mini microcontroller** for controlling hardware (LEDs).
- **LEDs** connected to the microcontroller.

---

## Hardware Setup

### VSD Squadron Mini Microcontroller:
1. Connect the **VSD Squadron Mini** to the PC via USB.
2. Connect the **LEDs** to GPIO pins (e.g., PD1, PD2) on the microcontroller.
3. Ensure the microcontroller is powered and ready to receive serial commands.

---

## Example Commands

- **"Turn on LED"**: Turns on the connected LED.
- **"Turn off LED"**: Turns off the connected LED.
- **"Turn on both LEDs"**: Turns both LEDs on.
- **"Turn off both LEDs"**: Turns both LEDs off.

---

## Troubleshooting

1. **Microphone Issues**: Ensure that the microphone is properly connected and set as the default recording device on your PC.
2. **No Feedback**: Check that speakers are connected and the volume is turned up.
3. **Serial Communication**: Ensure that the correct COM port is being used for communication with the microcontroller.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- **SpeechRecognition Library**: For converting speech to text.
- **pySerial Library**: For serial communication between Python and the microcontroller.
- **pyttsx3 Library**: For voice feedback.
- **VSD Squadron Mini Microcontroller**: For embedded hardware control.

---

This README provides an overview of **BrightBot AI**, detailing its features, setup, and usage to help users easily install and run the voice-controlled assistant.
