# TBWatch 

### A Three-Layered IoT System for Tuberculosis Detection & Treatment Monitoring
**Project Status:** Simulation-Based 
[**Author:** Tshegofatso Molotsi, Aspiring IoT Engineer [cite: 6]

---

## 🌍 Overview
[cite_start]According to the annual G20 Conference, Tuberculosis remains a top health threat in South Africa, causing over 54,000 annual deaths[cite: 8]. [cite_start]Current management is passive and treatment is often unmonitored[cite: 9]. [cite_start]**TBWatch** is a multi-layered IoT system designed to address TB from pre-symptomatic stages to post-treatment relapse detection[cite: 10].

## 📊 The Problem in South Africa
* [cite_start]**Incidence Rate:** 450 cases per 100,000 population (highest in the world)[cite: 30].
* [cite_start]**Treatment Default Rate:** 15% due to unmonitored treatment plans[cite: 47, 55].
* [cite_start]**Pre-Diagnosis Gap:** 50% of transmission occurs before symptoms show, causing 60-90 day delays[cite: 53].

## 🏗️ System Architecture
The solution is composed of three integrated layers:

### [cite_start]**Layer One: Community Layer (Household Monitoring)** [cite: 68]
* [cite_start]**Wearable Sensor Patch:** Monitors heart rate, cough frequency (using TinyML), and SpO2[cite: 70, 72, 149].
* [cite_start]**Environmental Node:** Tracks PM2.5, temperature, and humidity using ESP32 nodes[cite: 70, 148].
* [cite_start]**Connectivity:** BLE Mesh for local data aggregation and LoRa for long-range relay[cite: 70, 187].

### [cite_start]**Layer Two: Primary Care Level (Clinic Insight)** [cite: 78]
* [cite_start]**Clinic Gateway:** A Raspberry Pi receiver that processes real-time data[cite: 83, 134].
* [cite_start]**Risk Scoring Engine:** An ML-based engine that calculates composite risk scores to identify high-risk individuals[cite: 83, 139].
* [cite_start]**Triage Dashboard:** A web-based visualization tool for clinic staff[cite: 83, 136].

### [cite_start]**Layer Three: Health System (Population Surveillance)** [cite: 90]
* [cite_start]**Cloud Analytics:** Hosted on AWS, using a Spatial Scan Engine to detect outbreak clusters[cite: 92, 126, 127].
* [cite_start]**Forecasting:** Uses Prophet/LSTM models to predict resource needs and caseloads[cite: 92, 176].
* [cite_start]**Interoperability:** FHIR-compatible API for integration with the National Health Laboratory Services[cite: 92, 97].

## 🛠️ Technical Stack
* [cite_start]**Languages:** Python 3.14 (Data Generation) [cite: 185]
* [cite_start]**Machine Learning:** TensorFlow 3.12, TensorFlow Lite Micro (TinyML) [cite: 183, 185]
* [cite_start]**Database:** SQLite 3.40 (Edge) and TimescaleDB (Cloud) [cite: 185]
* [cite_start]**Communication:** MQTT, LoRa, BLE 5.0, and 4G/LTE [cite: 187]
* [cite_start]**Cloud Services:** AWS IoT Core, S3, Lambda [cite: 185]

## 🔒 Security & Privacy
* [cite_start]**Encryption:** AES-256 for data at rest and TLS 1.3 for data in transit[cite: 189].
* [cite_start]**Anonymization:** Device IDs are not linked to patient data without explicit consent[cite: 189].
* [cite_start]**Access Control:** Role-based access for Community Health Workers (CHW), Clinicians, and Public Health officials[cite: 189].

---
[cite_start]*Created as part of an IoT Engineering portfolio to strengthen pandemic preparedness and infectious disease surveillance.* [cite: 31, 32]*
