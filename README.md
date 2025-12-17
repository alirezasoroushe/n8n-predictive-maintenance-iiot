#  IIoT Predictive Maintenance Digital Twin

A real-time condition monitoring system that bridges the gap between **Operational Technology (OT)** and **Information Technology (IT)**. This project simulates an industrial press, monitors telemetry via MQTT, and triggers automated alerts when thresholds are breached.

<img width="7011" height="1811" alt="IIoT Predictive Maintenance Digital Twin" src="https://github.com/user-attachments/assets/dc5fb4c9-a551-40d3-91bf-dde5ecfcfc03" />


##  Features
- **Real-Time Ingestion:** Subscribes to MQTT topics (`factory/machine_01/`) using a local Mosquitto broker.
- **Logic Orchestration:** Uses **n8n** to process data streams and detect anomalies (>85°C).
- **Automated Alerts:** Dispatches instant Email/Slack notifications to maintenance teams.
- **Historical Logging:** Appends telemetry data to a Cloud Database (Google Sheets) for audit trails.

##  Tech Stack
- **Orchestration:** n8n (Self-hosted via Docker)
- **Protocol:** MQTT (Mosquitto Broker)
- **Database:** Google Sheets API
- **Containerization:** Docker

##  Screenshots
<img width="1606" height="682" alt="Predictive Maintenance Monitor" src="https://github.com/user-attachments/assets/ee2c6618-d5ec-4786-bed7-c68d914dc456" />
<img width="1613" height="674" alt="Machine Simulator" src="https://github.com/user-attachments/assets/bd2d7bd7-6b25-4be1-8af7-81624ea70eb5" />
<img width="1917" height="806" alt="temperature chart1" src="https://github.com/user-attachments/assets/a73b4df2-0f2f-4571-ab5d-a59c2a646aa7" />
<img width="1915" height="770" alt="temperature chart2" src="https://github.com/user-attachments/assets/c3075562-3448-40d3-82b2-dd5a21ad1dc6" />


## 🔧 How to Run
1. Import predictive-maintenance-workflow.json (The Logic) and machine-simulator.json (The Sensor) into your n8n instance.
2. Set up a local MQTT broker (Mosquitto).
3. Configure your Google Cloud Credentials.
4. Activate the "Simulator" workflow to start streaming data.
