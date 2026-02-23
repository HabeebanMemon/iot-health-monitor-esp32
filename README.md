# iot-health-monitor-esp32
# IoT-Based Health Monitoring System

A smart, real-time health tracking system designed to monitor vital signs and provide instant alerts for medical intervention.

##  Overview
This project addresses the need for affordable remote patient monitoring. By leveraging the **ESP32** and **IoT (Blynk)**, the system captures heart rate and temperature data, providing a dual-layered monitoring approach: local display for the patient and remote cloud access for caregivers.



## Key Features
* **Real-time Vitals:** Continuous tracking of Heart Rate (BPM) and Body/Ambient Temperature.
* **Cloud Integration:** Seamless data synchronization with the **Blynk IoT App** for remote monitoring.
* **Emergency Alerts:** Automatic email notifications triggered when BPM exceeds or falls below safe thresholds.
* **Local Interface:** 16x2 LCD display for immediate data visualization without internet dependency.
* **Compact & Scalable:** Designed with modular components, allowing for additional sensors (e.g., SpO2, Blood Pressure) in the future.

## Hardware Components
* **Microcontroller:** ESP32 (Wi-Fi + Bluetooth enabled)
* **Sensors:** PulseSensor (Heart Rate), LM35 (Temperature)
* **Display:** 16x2 I2C LCD
* **Indication:** Piezo Buzzer & LED for local alarms

## Tech Stack
* **Framework:** Arduino IDE
* **Language:** C++ (Embedded)
* **IoT Platform:** Blynk Cloud & Mobile App
* **Communication:** HTTP/MQTT via Wi-Fi



## How It Works
1.  The **PulseSensor** detects blood flow changes to calculate BPM using an interrupt-driven algorithm.
2.  The **LM35** provides an analog voltage proportional to the temperature, which is converted to Celsius/Fahrenheit by the ESP32.
3.  Data is updated on the **16x2 LCD** every second.
4.  If the BPM enters a "Critical Zone," the ESP32 sends a trigger to the **Blynk Server**, which pushes an email alert to the registered medical contact.

## Future Scope
* Integration of wearable health devices (Smartwatches).
* Adding oxygen saturation (SpO2) monitoring via MAX30102.
* Implementing Machine Learning to predict health trends based on historical data.

---
**Developed by:** Ayesha Ansari & Habeeban Memon
**Instructor:** Sir Junaid Ahmed & Sir Asif Ali
