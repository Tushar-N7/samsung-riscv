BrightBot AI is an innovative voice-activated assistant that allows users to control embedded hardware devices via simple voice commands. It leverages Python’s powerful speech recognition and text-to-speech capabilities to enable seamless interaction with the system. The assistant processes voice input, sends commands to the VSD Squadron Mini microcontroller, and controls devices like LEDs, making it a hands-free solution for operating electronics.

The project is designed to integrate speech recognition with hardware control. By using a microphone connected to a PC, the system listens for specific voice commands such as "Turn on LED" or "Turn off LED." These commands are converted to text using the SpeechRecognition library, and the resulting actions are communicated to the microcontroller through serial communication. In response, the microcontroller turns the connected devices on or off based on the received commands.

The assistant also provides real-time audio feedback using the pyttsx3 library, notifying users of the action performed, ensuring a user-friendly and efficient experience.

BrightBot AI makes it easy for users to control embedded systems without needing physical interaction, offering a practical solution for automation, accessibility, and innovation in various IoT projects.
