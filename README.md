# 🚧 Smart Pothole Detection and Monitoring System

An IoT-based pothole detection system that uses an accelerometer sensor and GSM module to automatically identify road potholes and transmit their location data to a centralized server. The collected information is stored in a database and displayed through a web dashboard for monitoring and road maintenance planning.

## 📖 Project Overview

Poor road conditions and potholes can cause vehicle damage, traffic congestion, and accidents. This project aims to provide a smart and automated solution for detecting potholes in real time. The system is mounted on a vehicle and continuously monitors road vibrations using an accelerometer. When a significant vibration exceeding a predefined threshold is detected, the system records the event and sends the data to a server using a GSM module.

The server stores the information in a database, and a website dashboard allows authorities to visualize pothole locations and prioritize repairs.

## ✨ Features

* Real-time pothole detection using an accelerometer
* Wireless data transmission via GSM module
* GPS-based location tracking (optional)
* Centralized database storage
* Interactive web dashboard
* Road condition monitoring
* Maintenance status tracking
* Smart city and transportation applications

## 🛠 Hardware Requirements

* Arduino Uno / ESP32
* MPU6050 or ADXL335 Accelerometer Sensor
* SIM800L / SIM900 GSM Module
* GPS Module (Optional)
* Power Supply/Battery
* Connecting Wires

## 💻 Software Requirements

* Arduino IDE
* HTML, CSS, JavaScript
* PHP / Node.js
* MySQL Database
* Google Maps API

## ⚙️ Working

1. The accelerometer continuously measures vehicle vibrations.
2. When vibration values exceed the threshold, a pothole is detected.
3. The microcontroller collects sensor data.
4. GPS coordinates are obtained (if available).
5. The GSM module sends pothole information to the server.
6. The server stores the data in the database.
7. The web dashboard displays pothole locations and reports.

## 🏗 System Architecture

```text
Accelerometer
      │
      ▼
Microcontroller (Arduino/ESP32)
      │
      ▼
 GSM Module
      │
      ▼
 Web Server/API
      │
      ▼
   Database
      │
      ▼
 Website Dashboard
```

## 📂 Project Structure

```text
Smart-Pothole-Detection/
│
├── hardware/
│   └── pothole_detection.ino
│
├── backend/
│   ├── api.php
│   ├── database.php
│
├── frontend/
│   ├── index.html
│   ├── dashboard.html
│   ├── style.css
│   └── script.js
│
├── database/
│   └── potholes.sql
│
└── README.md
```

## 🗄 Database Schema

```sql
CREATE TABLE potholes (
    id INT AUTO_INCREMENT PRIMARY KEY,
    latitude FLOAT,
    longitude FLOAT,
    vibration_value FLOAT,
    detection_time DATETIME DEFAULT CURRENT_TIMESTAMP,
    status VARCHAR(20) DEFAULT 'Pending'
);
```

## 🌐 Website Features

* Dashboard with pothole statistics
* Interactive map visualization
* Real-time pothole updates
* Search and filter reports
* Maintenance status tracking
* Admin management panel

## 🚀 Future Enhancements

* Machine Learning-based pothole classification
* Mobile application integration
* Cloud deployment
* Real-time notifications
* Severity prediction
* Smart city integration

## 🎯 Applications

* Smart Transportation Systems
* Road Maintenance Authorities
* Municipal Corporations
* Highway Monitoring
* Public Safety Systems

## 👥 Team

Developed as an IoT and Smart City project for road condition monitoring and pothole detection.

## 📜 License

This project is licensed under the MIT License.
