🚀 Distributed Log Analyzer with ML Anomaly Detection

A distributed, real-time log analysis system featuring ML-powered anomaly detection, scalable message processing using RabbitMQ, and a live web-based monitoring dashboard.

📌 Project Overview

This system simulates enterprise-scale log monitoring similar to platforms like
Splunk.

It processes high-throughput logs, detects anomalies using machine learning, and visualizes insights through a real-time dashboard.

🧠 Architecture
4
Log Producers → RabbitMQ Queue → Log Processor → KV Storage
                                      ↓
                               ML Anomaly Detector
                                      ↓
                                Web Dashboard (Flask)
⚙️ Tech Stack

🐍 Python

📦 RabbitMQ

🌐 Flask

🤖 scikit-learn (Isolation Forest)

🐳 Docker & Docker Compose

🗂 File-based KV Store

🧪 Pytest

✨ Key Features

✔ Real-time log ingestion (10k+ logs/sec tested)
✔ ML-based anomaly detection (Isolation Forest)
✔ Scalable message queue (RabbitMQ)
✔ Dockerized deployment (1-command setup)
✔ Live web dashboard with charts
✔ Config-driven architecture
✔ Unit tests with coverage

📊 Performance Metrics

🚀 10,000+ logs/sec processing capability

⚡ < 1ms inference latency

📈 280+ logs processed successfully in test runs

🔍 Configurable anomaly rate (contamination=0.1)

🗂 Project Structure
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
🚀 Quick Start (Docker – Recommended)
cd LogSentry
docker-compose up --build

Access:

🌐 Dashboard → http://localhost:5000

📬 RabbitMQ → http://localhost:15672

Username: admin

Password: admin123

⚙️ Configuration

Edit:

config/config.yaml

Example:

rabbitmq:
  username: admin
  password: admin123

ml:
  contamination: 0.1
🧪 Testing

Run all tests:

pytest

With coverage:

pytest --cov
🧠 How the ML Works

Logs are converted into numerical feature vectors

Isolation Forest model detects abnormal patterns

Anomaly score threshold is configurable

Model can be retrained with new data

🖥 Dashboard Features

📈 Real-time log rate

🚨 Anomaly detection alerts

📊 Log level distribution

📂 Historical log storage view
