
# Voice-Controlled Home Automation

## 📌 Overview
This project demonstrates a **Voice-Controlled Home Automation System** built using a **Raspberry Pi 4B**.  
It enables users to control household devices (in this case, LED circuits) using voice commands while also **monitoring voltage and current** in real-time via **ThingSpeak**.  

By integrating **Google Speech-to-Text API** for voice recognition and IoT monitoring through **ThingSpeak**, this system combines **convenience**, **real-time analytics**, and **scalability**.

<img width="5536" height="1132" alt="BLOCK" src="https://github.com/user-attachments/assets/3df25e5e-5d60-44dd-86d2-d259c9a138b2" />

---

## 🏗 System Architecture

### 1. Raspberry Pi 4B
- Acts as the central processing unit.
- Processes voice commands, controls relays, and manages system operations.
- Uses GPIO pins for communication with relay modules, sensors, and ADC.

### 2. 4-Channel Relay Module
- Controls LED circuits on a breadboard.
- Supports multiple devices for scalability.

### 3. Microphone
- Captures voice commands.
- Google Speech-to-Text API processes commands for accurate control.

### 4. LED Circuits
- Connected to relays.
- Provide visual feedback for commands.

### 5. Voltage & Current Sensors
- Monitor electrical parameters in real-time.
- Data sent to ThingSpeak for graphical visualization.

### 6. ADC & I2C Module
- Converts analog sensor readings to digital data for the Raspberry Pi.
- Communicates over I2C protocol.

<img width="982" height="794" alt="image" src="https://github.com/user-attachments/assets/a4e25a31-e463-4ae4-8440-9994d5a23976" />


---

## ⚙️ Implementation

### 1. Hardware Setup
- Connect **Raspberry Pi** to:
  - 4-channel relay
  - Microphone
  - LED circuit with resistors
  - Voltage & current sensors (via ADC module)
- Ensure proper wiring for GPIO communication.

### 2. Software Configuration
- Install & configure **Google Speech-to-Text API**.
- Write Python scripts to:
  - Recognize voice commands.
  - Control relay channels accordingly.
  - Read sensor data via ADC.
  - Send data to **ThingSpeak**.

### 3. Relay Control Logic
- Supports **Normally Open (NO)** and **Normally Closed (NC)** configurations.
- Ensures immediate switching with minimal latency.

---

## 📊 Results & Performance

- **Voice Command Responsiveness**: High accuracy and minimal latency.
- **Relay Switching**: Reliable and instantaneous.
- **Monitoring Accuracy**: Real-time and precise sensor readings displayed on ThingSpeak.

---

## 🚀 Future Enhancements

1. **Smart Device Integration**
   - Connect with Alexa, Google Assistant, or other smart home systems.

2. **Machine Learning for Speech Recognition**
   - Improve adaptability to various accents and voices.

3. **Advanced Monitoring**
   - Add temperature, humidity, and other environmental sensors.

---

## 🖼 ThingSpeak Dashboard

<img width="1200" height="675" alt="image" src="https://github.com/user-attachments/assets/bf1a5074-9cb5-44ac-8381-ea8a7ab6c24e" />

<img width="1510" height="886" alt="image" src="https://github.com/user-attachments/assets/499bd55b-0f45-44cd-9f87-76cf198e16c2" />


---

## 🛠 Technologies Used
- **Hardware**: Raspberry Pi 4B, 4-Channel Relay, Microphone, LED circuits, Voltage & Current sensors, ADC module.
- **Software**: Python, Google Speech-to-Text API, ThingSpeak IoT platform.
- **Protocols**: I2C, GPIO.

---

## 📂 Repository Structure
```

📁 Voice-Controlled-Home-Automation
├── SmartHomeAutomation.py  # Main Python script
├── README.md               # Project documentation
└── requirements.txt        # Python dependencies

```

---

## 📜 References
- Raspberry Pi 4B Technical Documentation
- Google Speech-to-Text API Documentation
- ThingSpeak API Documentation
- Sensor datasheets & community forums

---


