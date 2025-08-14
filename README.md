

# Voice-Controlled Home Automation

## 📌 Overview

This project demonstrates a **Voice-Controlled Home Automation System** built using a **Raspberry Pi 4B**.
It enables users to control household devices (in this case, LED circuits) using voice commands while also **monitoring voltage and current** in real-time via **ThingSpeak**.

By integrating **Google Speech-to-Text API** for voice recognition and IoT monitoring through **ThingSpeak**, this system combines **convenience**, **real-time analytics**, and **scalability**.

<img width="5536" height="1132" alt="BLOCK" src="https://github.com/user-attachments/assets/3df25e5e-5d60-44dd-86d2-d259c9a138b2" />

---

## 🏗 System Architecture

### 1. Raspberry Pi 4B

* Acts as the central processing unit.
* Processes voice commands, controls relays, and manages system operations.
* Uses GPIO pins for communication with relay modules, sensors, and ADC.

### 2. 4-Channel Relay Module

* Controls LED circuits on a breadboard.
* Supports multiple devices for scalability.

### 3. Microphone

* Captures voice commands.
* Google Speech-to-Text API processes commands for accurate control.

### 4. LED Circuits

* Connected to relays.
* Provide visual feedback for commands.

### 5. Voltage & Current Sensors

* Monitor electrical parameters in real-time.
* Data sent to ThingSpeak for graphical visualization.

### 6. ADC & I2C Module

* Converts analog sensor readings to digital data for the Raspberry Pi.
* Communicates over I2C protocol.

<img width="982" height="794" alt="image" src="https://github.com/user-attachments/assets/a4e25a31-e463-4ae4-8440-9994d5a23976" />

---

## ⚙️ Setup Instructions

### **1️⃣ Hardware Setup**

1. **Raspberry Pi 4B Wiring**

   * Connect **4-Channel Relay** module to Raspberry Pi GPIO pins.
   * Wire **LED circuits** (with resistors) to the relay’s output terminals.
   * Connect **Voltage & Current sensors** to the ADC module.
   * Connect ADC to Raspberry Pi via I2C (SDA, SCL, VCC, GND).
   * Plug in a **USB microphone** to the Pi.

2. **Power Supply**

   * Power Raspberry Pi via its USB-C power adapter.
   * Ensure relay and sensors have a suitable power source (e.g., 5V from Pi).

---

### **2️⃣ Software Setup**

#### **Install System Packages**

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install python3 python3-pip python3-smbus i2c-tools portaudio19-dev -y
```

#### **Enable I2C on Raspberry Pi**

```bash
sudo raspi-config
# Navigate to: Interface Options → I2C → Enable
sudo reboot
```

#### **Clone Repository**

```bash
git clone https://github.com/YourUsername/Voice-Controlled-Home-Automation.git
cd Voice-Controlled-Home-Automation
```

#### **Install Python Dependencies**

```bash
pip3 install -r requirements.txt
```

---

### **3️⃣ Google Speech-to-Text API Setup**

1. Create a **Google Cloud Project** at [Google Cloud Console](https://console.cloud.google.com/).
2. Enable the **Speech-to-Text API**.
3. Create a **Service Account Key** (JSON file) and download it.
4. Set the environment variable:

```bash
export GOOGLE_APPLICATION_CREDENTIALS="/path/to/your/service-account-key.json"
```

---

### **4️⃣ ThingSpeak Configuration**

1. Create a **ThingSpeak account** at [ThingSpeak.com](https://thingspeak.com/).
2. Create a new **channel** and note your **Write API Key**.
3. Update the API key in `SmartHomeAutomation.py`.

---

### **5️⃣ Running the Project**

```bash
python3 SmartHomeAutomation.py
```

* Speak a command like `"Turn on LED 1"` or `"Turn off LED 2"`.
* Voltage and current readings will be uploaded to ThingSpeak in real-time.

---

## 📊 Results & Performance

* **Voice Command Responsiveness**: High accuracy and minimal latency.
* **Relay Switching**: Reliable and instantaneous.
* **Monitoring Accuracy**: Real-time and precise sensor readings displayed on ThingSpeak.

---

## 🚀 Future Enhancements

1. **Smart Device Integration** (Alexa, Google Assistant)
2. **Machine Learning Speech Recognition**
3. **Advanced Environmental Monitoring**

---

## 🛠 Technologies Used

* **Hardware**: Raspberry Pi 4B, 4-Channel Relay, Microphone, LED circuits, Voltage & Current sensors, ADC module.
* **Software**: Python, Google Speech-to-Text API, ThingSpeak IoT platform.
* **Protocols**: I2C, GPIO.

---

## 📂 Repository Structure

```
📁 Voice-Controlled-Home-Automation
├── SmartHomeAutomation.py  # Main Python script
├── README.md               # Project documentation
└── requirements.txt        # Python dependencies
```

---
