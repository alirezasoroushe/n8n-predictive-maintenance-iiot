#  IIoT Predictive Maintenance Digital Twin

A real-time condition monitoring system that bridges the gap between **Operational Technology (OT)** and **Information Technology (IT)**. This project simulates an industrial press, monitors telemetry via MQTT, and triggers automated alerts when thresholds are breached.

![Project Architecture](https://mermaid.ink/img/pako:eNp1kcFqwzAMhl8l6NRC-wI9FHYY5DB22G2HImqsxLA1jnYyhLz7nLRdh-2kJP_360syWq0CI_ro9qfR-8eZg8-WF8eO0e2P_sO9489QjLw7vLhC-1O8Q_f1e4uW5y_wQo1gQYc-B_0S9Cg4EBy2lBw4WnJ09OToKDiScqT_Q46M44-WnBw5WnJ09OToKDhScqT_Q46M40_2_wE4_gGjS07w?type=png)

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
