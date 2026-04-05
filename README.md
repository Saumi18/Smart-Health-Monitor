# Smart Health Monitor

Smart Health Monitor is a low-cost wearable health monitoring system designed for elderly users and individuals at cardiac risk. The device continuously measures heart rate and blood oxygen saturation (SpO₂) and sends an alert to a connected smartphone when abnormal vital patterns are detected.

This project is developed as an embedded systems and IoT course project and demonstrates the integration of sensors, microcontrollers, wireless communication, and mobile alerts.

---

## 1. Problem Statement

A significant number of cardiac emergencies occur during sleep or when individuals are alone. In such situations, delayed response time can be life-threatening.

Commercial smartwatches provide health monitoring features but are expensive and often designed for fitness and lifestyle use rather than continuous night monitoring for elderly users.

There is a need for an affordable, simple, and dedicated wearable device that focuses on continuous monitoring and early warning.

---

## 2. Project Objective

The objective of this project is to build a low-cost wearable device that:

• Continuously monitors heart rate and SpO₂  
• Detects abnormal cardiac patterns  
• Sends alerts to a connected smartphone  
• Operates in low-power mode for extended battery life  

This system acts as an early warning and alert mechanism and is not intended to be a medical diagnostic device.

---

## 3. Key Features

• Continuous heart rate monitoring  
• Continuous SpO₂ monitoring  
• Abnormal vital detection algorithm  
• Smartphone alert and alarm system  
• Low-power duty-cycled operation  
• Designed for night and home monitoring  
• Low-cost hardware implementation  

---

## 4. System Overview

The Smart Health Monitor consists of three main components:

1. Wearable Device  
2. Wireless Communication Module  
3. Smartphone Alert Application  

### Workflow

1. Sensors collect heart rate and SpO₂ data.  
2. Microcontroller processes and evaluates the readings.  
3. Data is transmitted wirelessly to a smartphone.  
4. If abnormal readings persist, the phone triggers an alert and alarm.

---

## 5. Hardware Components

| Component | Purpose |
|-----------|---------|
| STM32 Microcontroller | Main processing unit |
| MAX30102 Pulse Oximeter | Heart rate and SpO₂ sensing |
| ESP8266 / Bluetooth Module | Wireless communication |
| Li-ion Battery | Portable power source |

---

## 6. Software Components

• Embedded C firmware for STM32  
• Arduino firmware for ESP8266  
• Mobile application for alert notifications  

---

## 7. System Architecture

Wearable Sensors → STM32 Microcontroller → Wireless Module → Smartphone Application → Alert Notification

---

## 8. Low Power Operation

The device uses duty-cycling to reduce power consumption.

Operating cycle:
Sleep → Wake → Measure → Transmit → Sleep

This approach significantly extends battery life and makes the device suitable for overnight monitoring.

---

## 9. Abnormal Vital Detection Logic

The system triggers an alert if abnormal readings persist for a fixed duration.

Alert conditions:

• Heart Rate greater than 120 bpm  
• Heart Rate lower than 45 bpm  
• SpO₂ lower than 88%  
• Sudden abnormal change in heart rate  

When these conditions persist for approximately 30 seconds, an emergency alert is triggered on the smartphone.

---

## 10. Alert Mechanism

When abnormal readings are detected:

• Smartphone alarm is activated  
• Notification is displayed  
• User or caregiver can take immediate action  

---

## 11. Repository Structure

smart-health-monitor/
│
├── Firmware/        STM32 and ESP8266 code  
├── Mobile_App/      Smartphone application  
├── Circuit/         Circuit diagrams and wiring  
├── Images/          Hardware and demo images  
└── README.md  

---

## 12. Project Status

This project is currently under development as part of an academic course.

Future updates will include improved algorithms, enhanced mobile application features, and extended battery optimization.

---

## 13. Disclaimer

This project is intended for educational and research purposes only.  
It is an early warning system and not a certified medical device.
