# 🚀 Distributed Log Analyzer with ML Anomaly Detection

---

## 📌 Overview

A distributed real-time log processing system with ML-powered anomaly detection.  
Designed to simulate enterprise-scale log analytics platforms like Splunk.

Processes high-throughput logs using RabbitMQ, detects anomalies using Isolation Forest, and visualizes system health through a live dashboard.

---

## 🏗 System Architecture

```
Log Producers → RabbitMQ Queue → Log Processor → Storage
                                      ↓
                               ML Anomaly Detector
                                      ↓
                                Web Dashboard
```

---

## 🛠 Tech Stack

- Python  
- RabbitMQ  
- Flask  
- scikit-learn  
- Docker & Docker Compose  
- Pytest  

---

## ✨ Key Features

- Real-time log ingestion  
- Distributed message queue architecture  
- ML-based anomaly detection (Isolation Forest)  
- Configurable anomaly threshold  
- Live monitoring dashboard  
- Dockerized deployment  
- Unit testing with coverage  

---

## 📊 Performance

- 10,000+ logs/sec throughput (local benchmark)  
- < 1ms inference latency  
- 1M+ synthetic logs tested  
- Configurable contamination rate  

---

## 📂 Project Structure

```
LogSentry/
│
├── config/
│   └── config.yaml
│
├── log-producers/
│   └── sample_web_app.py
│
├── log-processor/
│   └── src/processor.py
│
├── dashboard/
│   └── app.py
│
├── docker-compose.yml
├── requirements.txt
└── README.md
```

---

## 🚀 Quick Start (Docker)

```bash
docker-compose up --build
```

### Access

- Dashboard → http://localhost:5000  
- RabbitMQ → http://localhost:15672  

---

## ⚙️ Configuration

Edit:

```
config/config.yaml
```

Example:

```yaml
rabbitmq:
  username: admin
  password: admin123

ml:
  contamination: 0.1
```

---

## 🤖 ML Pipeline

- Log parsing & feature extraction  
- Feature vectorization  
- Isolation Forest model training  
- Real-time anomaly scoring  
- Threshold-based alert generation  

---

## 🧪 Testing

```bash
pytest
pytest --cov
```

---

## 📈 Dashboard Capabilities

- Real-time log rate visualization  
- Anomaly alerts  
- Log level distribution  
- Historical storage view  

---

