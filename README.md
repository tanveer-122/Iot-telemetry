# 🚀 PLC Telemetry Project on AWS

## 📌 Project Overview

This project demonstrates a PLC (Programmable Logic Controller) telemetry system integrated with AWS Cloud. The system captures real-time data from PLC devices, sends it securely to AWS IoT Core, and visualizes insights using Power BI dashboards via AWS APIs.

---

## 🏗️ Architecture

**Flow:**
PLC Device → AWS IoT Core → AWS API Gateway / Lambda → Power BI Dashboard

---

## 🧰 Tech Stack

* **Cloud:** AWS (IoT Core, EC2, Lambda, DynamoDB, CloudWatch, S3)
* **Languages:** Python, JavaScript
* **Protocols:** MQTT
* **Visualization:** CloudWatch Dashboard / Custom UI
* **Version Control:** Git & GitHub

---

## ⚙️ Features

* 📡 Real-time telemetry data from PLC to AWS IoT Core
* ☁️ Secure device-to-cloud communication using MQTT
* 🔗 API integration using AWS services (API Gateway / Lambda)
* 📊 Live dashboard visualization using Power BI
* ⚡ Near real-time monitoring of industrial data

---

## 🔧 Setup Instructions

 1 AWS IoT Core Setup

* Create a **Thing** in AWS IoT Core
* Generate certificates
* Attach IoT policy (allow MQTT publish/subscribe)
* Download certificates and keys

---

### 2 Configure MQTT Device (PLC Simulator)

Update configuration file:

```json
{
  "endpoint": "your-iot-endpoint",
  "clientId": "plc-device-01",
  "certPath": "cert.pem",
  "keyPath": "private.key"
}
```

Run telemetry script:

```bash
python plc_simulator.py
```

---

### 3 API Integration (Lambda / API Gateway)

* Create Lambda function to process IoT data
* Expose API using API Gateway
* Connect Power BI to AWS API endpoint

---

### 4 Data Handling (Optional Storage)

* Data can be stored in DynamoDB or S3 (optional)
* Power BI can fetch data via API or stored dataset

## 📊 Dashboard (Power BI)

* Connected Power BI to AWS

## 🔐 Security Best Practices

* Use IAM roles (no hardcoded credentials)
* Enable HTTPS & secure MQTT (TLS)
* Restrict IP access to EC2
* Rotate keys regularly

---

## 📈 Future Improvements

* Add Grafana dashboard
* Use Kinesis for streaming
* Implement AI-based anomaly detection
* Add multi-device support

---

## 👨‍💻 Author

Azharuddin Alam

## 📜 License

This project is licensed under the MIT License.

