![Screenshot 2025-01-28 230802](https://github.com/user-attachments/assets/ab17cb90-b93b-4d29-a757-603c6c34539a)

# **IoT-Based Industrial Equipment Predictive Maintenance System**

## **Overview**
This project is an IoT-based **Industrial Equipment Predictive Maintenance System** designed to monitor critical parameters of industrial machines, including temperature, pressure, and vibration. Using a combination of sensors, the system detects abnormalities or potential failures in real-time. Upon detection of abnormal values, the system triggers audio warnings, logs data, and sends alerts via email, while also displaying the real-time data on a mobile app via **ThingSpeak**. The solution is built to be efficient, cost-effective, and scalable for industrial applications.

### **Key Features**
- **Real-Time Monitoring**: Constantly monitors temperature, pressure, and vibration levels.
- **AI-Powered Analytics**: Uses machine learning models for predictive maintenance (Optional).
- **Audio Alerts**: Voice-based notifications for exceeding threshold levels using a UART Serial MP3 Music Player Module.
- **Data Logging**: Sends and stores data in **ThingSpeak** for remote monitoring and analysis.
- **Email Alerts**: Sends immediate notifications via email when critical thresholds are exceeded.
- **Mobile App Integration**: Interface with the mobile app via **MIT App Inventor** for displaying sensor data and controlling the system remotely.
- **SD Card Storage**: Logs all sensor data to an SD card for later analysis.

---

## **Components Required**
1. **VSD Squadron Mini (CH32V003 MCU)**
2. **MPX5700AP Pressure Sensor**
3. **SW-420 Vibration Sensor Module**
4. **DHT11 Temperature and Humidity Sensor** (Alternative: DHT22)
5. **UART Serial MP3 Music Player Module (with onboard amplifier and speaker)**
6. **ESP32 Development Board**
7. **ThingSpeak (Cloud platform)**
8. **MicroSD Card Module**
9. **Speaker (Onboard or external for audio warnings)**
10. **Relay Module** (for controlling external devices)
11. **MIT App Inventor (for Mobile App)**

---

## **Pin Connections**

### **VSD Squadron Mini (CH32V003) Pinout**

| **Component**                  | **Pin**                      | **VSD Squadron Mini Pin**       |
|---------------------------------|------------------------------|---------------------------------|
| **MPX5700AP Pressure Sensor**   | VCC                          | 3.3V                            |
|                                 | GND                          | GND                             |
|                                 | Output (Analog Voltage)      | ADC Pin (e.g., GPIO12)         |
| **SW-420 Vibration Sensor**     | VCC                          | 3.3V                            |
|                                 | GND                          | GND                             |
|                                 | Digital Output               | GPIO Pin (e.g., GPIO13)        |
| **DHT11 Temperature Sensor**    | VCC                          | 3.3V                            |
|                                 | GND                          | GND                             |
|                                 | Data                         | GPIO Pin (e.g., GPIO14)        |
| **MP3 Music Player Module**     | VCC                          | 5V or 3.3V (depending on the module) |
|                                 | GND                          | GND                             |
|                                 | RX                           | TX (VSD Squadron Mini or ESP32)|
|                                 | TX                           | RX (VSD Squadron Mini or ESP32)|
| **ESP32**                       | VCC                          | 3.3V                            |
|                                 | GND                          | GND                             |
| **MicroSD Card Module**         | VCC                          | 5V or 3.3V (depending on the module) |
|                                 | GND                          | GND                             |
|                                 | CS, SCK, MOSI, MISO          | SPI pins on VSD Squadron Mini/ESP32 |
| **Relay Module**                | VCC                          | 5V or 3.3V                     |
|                                 | GND                          | GND                             |
|                                 | IN                           | GPIO Pin (e.g., GPIO15)        |

---

## **How It Works**
1. **Sensor Monitoring**:
   - **MPX5700AP** measures pressure, outputting an analog signal proportional to the pressure applied.
   - **DHT11** measures temperature and humidity, outputting digital values.
   - **SW-420 Vibration Sensor** detects vibration, outputting a digital HIGH/LOW signal depending on the level of vibration detected.

2. **Data Processing and Analytics**:
   - The **VSD Squadron Mini (CH32V003)** MCU reads the sensor data and processes it.
   - The **ESP32** serves as the communication hub, forwarding sensor data to **ThingSpeak** in real time for monitoring via a mobile app.
   - The system can optionally integrate **AI models** to predict future failures based on sensor data (such as predicting when maintenance is required).

3. **Alerts and Actions**:
   - If any sensor reading exceeds predefined threshold values (e.g., high temperature, high pressure, or excessive vibration):
     - The system triggers an **audio warning** through the MP3 player module, playing a pre-recorded alert (e.g., "Temperature Exceeded" or "Vibration Critical").
     - **Email alerts** are sent to predefined recipients.
     - The system logs the event in **ThingSpeak** for remote monitoring.

4. **SD Card Storage**:
   - Data can also be stored locally on an **SD card module** for later retrieval and analysis.

5. **Mobile App Integration**:
   - The **MIT App Inventor** app displays real-time temperature, pressure, and vibration data.
   - The app provides the option to control the system remotely (e.g., turning off the equipment via the relay when necessary).

---

## **Features**
- **Real-Time Industrial Equipment Monitoring**: Keep track of temperature, pressure, and vibration in real-time.
- **Predictive Maintenance**: Uses machine learning (optional) to predict failures and optimize maintenance schedules.
- **Alerting System**: Immediate audio and email notifications when abnormalities are detected.
- **Cloud Integration**: Remote data monitoring and visualization using **ThingSpeak**.
- **Mobile App Interface**: Easily view and control the system from anywhere using a mobile app.
- **Cost-Effective**: Uses widely available, low-cost components like the DHT11, MPX5700AP, and SW-420 sensor.
- **Data Logging**: Logs all sensor data to an SD card for future analysis.
- **Scalable**: The system can be expanded with additional sensors or connected to a larger network of machines.

---

## **Possible Extensions**
- **Machine Learning**: Implement AI models on the ESP32 or cloud to predict when a machine will require maintenance based on historical sensor data.
- **Enhanced Alerts**: Use an LCD or OLED display to show real-time sensor data and alert status directly on the device.
- **Automated Control**: Automatically shut down machines or activate cooling systems when critical thresholds are reached.

---

## **Conclusion**
This IoT-based predictive maintenance system provides industrial users with a robust solution for monitoring equipment health. The system ensures that potential failures are detected early, preventing costly downtimes and extending the lifespan of machinery. With real-time data logging, cloud connectivity, and audio alerts, this system combines efficiency, reliability, and cost-effectiveness for industrial applications. 

