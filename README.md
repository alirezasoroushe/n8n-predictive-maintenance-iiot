#  IIoT Predictive Maintenance Digital Twin

A real-time condition monitoring system that bridges the gap between **Operational Technology (OT)** and **Information Technology (IT)**. This project simulates an industrial press, monitors telemetry via MQTT, and triggers automated alerts when thresholds are breached.

<img width="7011" height="1811" alt="IIoT Predictive Maintenance Digital Twin" src="https://github.com/user-attachments/assets/dc5fb4c9-a551-40d3-91bf-dde5ecfcfc03" />


## 🚀 Features
- **Real-Time Ingestion:** Subscribes to MQTT topics (`factory/machine_01/`) using a local Mosquitto broker.
- **Logic Orchestration:** Uses **n8n** to process data streams and detect anomalies (>85°C).
- **Automated Alerts:** Dispatches instant Email/Slack notifications to maintenance teams.
- **Historical Logging:** Appends telemetry data to a Cloud Database (Google Sheets) for audit trails.

## 🛠️ Tech Stack
- **Orchestration:** n8n (Self-hosted via Docker)
- **Protocol:** MQTT (Mosquitto Broker)
- **Database:** Google Sheets API
- **Containerization:** Docker

## 📸 Screenshots
*(Upload your graph screenshot here later)*

## 🔧 How to Run
1. Import `predictive-maintenance-workflow.json` into your n8n instance.
2. Set up a local MQTT broker (Mosquitto).
3. Configure your Google Cloud Credentials.
4. Activate the "Simulator" workflow to start streaming data.
