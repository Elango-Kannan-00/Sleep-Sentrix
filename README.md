# SleepSentrix

![NeerMai Valam Logo](images/sleepsentrix.png)

## An IoT-Based Smart Ankle Band for Sleepwalking Detection

# About the Project

- **SleepSentrix** is an IoT-enabled wearable ankle band that detects sleepwalking (somnambulism) in real time and alerts caregivers before an injury can occur. Sleepwalking affects a significant share of the global population, and a large proportion of sleepwalkers experience injuries ranging from minor bruises to severe accidents.

- It was developed because existing monitoring methods — such as caregiver observation or video surveillance — raise privacy concerns, are unreliable, and don't respond instantly once an episode begins. SleepSentrix was built to close that gap.

- **Who benefits:** Sleepwalkers prone to nighttime injury, their families, and caregivers who need real-time visibility without invasive, always-on surveillance.

- **Main objective:** To combine motion sensing, GPS tracking, and instant caregiver alerts into a single low-power wearable — reducing sleepwalking-related injuries.

# Problem Statement

- Sleepwalking is a common parasomnia that can cause a person to walk, eat, or even attempt to drive while asleep — putting them at risk of falls, accidental injury, and in rare cases, dangerous or socially harmful behavior. A large share of sleepwalkers experience injury as a result, and the risk exists across every age group.

**Limitations of existing solutions:**
- **Caregiver/video observation** — raises privacy concerns, isn't scalable, and depends entirely on someone being awake and watching.
- **Generic wearable sleep trackers** — most are not built to specifically distinguish sleepwalking from normal sleep movement, and stop tracking once an episode has already started.
- **GPS/geofencing tools used in elder or dementia care** — lose accuracy indoors, drain battery quickly, and depend on constant connectivity.
- **AI motion-classification research** — often struggles with false positives and needs large labeled datasets that don't exist for a condition like sleepwalking.

**Why SleepSentrix is needed:** None of the existing approaches combine detection, continuous tracking *after* an event starts, and real-time caregiver alerting into one low-power, wearable solution. SleepSentrix is designed specifically to fill that gap.

# Proposed Solution

- SleepSentrix is an IoT-enabled wearable ankle band that detects sleepwalking using motion sensors and notifies caregivers in real time through GPS tracking, alerts, and continuous monitoring — combining motion sensing, GPS location tracking, and real-time caregiver alerts into a single wearable device.

# Key Features

- Sleepwalking Detection
- Real-time Motion Monitoring
- GPS Live Tracking
- Instant Caregiver Alerts
- Low Power Design
- Wearable TPU Band
- Event Logging
- Remote Monitoring
- Wireless Communication
- Expandable AI Support

# System Architecture

```
Motion Sensor
        ↓
ESP32
        ↓
Detection Algorithm
        ↓
Alert System
        ↓
GPS Tracking
        ↓
Mobile Application
```

The **LSM6DS3** motion sensor continuously tracks acceleration and angular velocity while the wearer sleeps. The **ESP32** microcontroller reads this data, runs the detection algorithm, and — if sleepwalking is identified — triggers the alert system, activates GPS tracking, and pushes updates to the **mobile application** used by the caregiver.

# Workflow

```
User Sleeps
     ↓
Sensor Collects Motion
     ↓
Algorithm Analyses Movement
     ↓
Sleepwalking?
     ↓
   YES
     ↓
GPS Activated
     ↓
Alert Sent
     ↓
Caregiver Tracks User
```

# Hardware Components

| Component | Purpose |
|---|---|
| ESP32 | Main controller |
| LSM6DS3 | Motion Detection |
| GPS Module | Location Tracking |
| LiPo Battery | Power Supply |
| TPU Strap | Wearable Band |
| Buzzer | Wake-up Alert |
| Bluetooth/WiFi | Communication |

# Software Stack

- Embedded C / Arduino IDE
- ESP32
- Bluetooth
- WiFi

# Technologies Used

- ESP32
- LSM6DS3
- Arduino IDE
- Bluetooth
- WiFi
- IoT
- Embedded C

# Detection Algorithm

```
Motion Data
     ↓
Filtering
     ↓
Feature Extraction
     ↓
Threshold Detection
     ↓
Classification
     ↓
Alert Generation
     ↓
GPS Tracking
```

- The LSM6DS3 continuously streams accelerometer and gyroscope data. A low-pass filter removes noise from small involuntary movements, and the signal is normalized before key features — such as step count, stride length, and movement duration — are extracted.

- Classification combines **threshold-based analysis** (sustained walking-like motion over a minimum duration) with a **lightweight machine learning model** to separate genuine sleepwalking from movements like bed-turning or stationary shifts, reducing false positives. Once sleepwalking is confirmed, an alert is generated and GPS tracking is activated for continuous monitoring until the episode ends.

# Future Enhancements

- AI-based motion classification
- Edge AI
- Smart Home Integration
- Health Analytics Dashboard
- Doctor Portal
- Cloud Storage
- Emergency Calling
- Battery Optimization
- Fall Detection
- Smartwatch Integration


# Team Members

**Project Lead**
- K Elango

**Project Members**
- G Aravinth
- S M Rohith
- S Dhanushiya
- U M Darshini
- S Banu Pushpa Gopika

# Publication

This project is based on the following research paper:

- **Title:** SleepSentrix: An IoT-Based Smart Ankle Band for Sleepwalking Detection
- **Authors:** K Elango, G Aravinth, S M Rohith, S Dhanushiya, U M Darshini, S Banu Pushpa Gopika
- **Conference / Journal:** *International Research Journal on Advanced Engineering Hub (IRJAEH)*
- **Year:** *2025-04-16*
- **DOI:** *https://doi.org/10.47392/IRJAEH.2025.0194*
