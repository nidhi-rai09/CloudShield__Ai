# 🛡️ CloudShield AI – Intelligent Cloud Security Guardian

**An AI-Based Cloud Security Log Analysis and Anomaly Detection System**

## 1. Project Overview

CloudShield AI is an AI-based cloud security monitoring prototype designed to detect unusual and potentially suspicious activities in cloud activity logs.

The system analyzes user login and activity records, identifies abnormal behaviour using the Isolation Forest anomaly detection technique, and assigns risk scores to help security teams investigate potential security threats.

It also provides optional AI-powered explanations of selected suspicious events using a locally running Large Language Model (LLM) through Ollama.

The project provides an interactive dashboard built using Streamlit to visualize detected anomalies and download analysis reports.

## 2. Problem Statement

Cloud computing has become an essential part of modern organizations. However, storing sensitive information in cloud environments introduces security challenges.

Some common security concerns include:

- Multiple failed login attempts.
- Unauthorized access attempts.
- Login activity from unusual geographical locations.
- Access through unknown devices.
- Unusual data download patterns.
- Suspicious user behaviour.

Manually analyzing large volumes of cloud activity logs is time-consuming and difficult.

Therefore, there is a need for an intelligent system that can analyze activity logs, identify unusual patterns, and help security teams investigate potential threats.

## 3. Proposed Solution

CloudShield AI addresses this problem by using an anomaly detection approach to analyze cloud activity logs.

The system processes uploaded or simulated CSV logs and identifies activities that differ from normal patterns.

It provides:

- Automated anomaly detection.
- Risk scoring for analyzed activities.
- Identification of unusual login and access patterns.
- Optional AI-generated explanations.
- Interactive visualization of analysis results.
- Downloadable analysis reports.

## 4. Key Features

### 4.1 AI-Based Anomaly Detection
Uses the Isolation Forest algorithm to identify unusual patterns in cloud activity logs.

### 4.2 Risk Scoring
Assigns risk scores to activities to help identify events that may require further investigation.

### 4.3 Suspicious Activity Identification
Analyzes activity-related information such as:
- Failed login attempts.
- Login time.
- Source IP address and country.
- New device usage.
- Unusual locations.
- Data download volume.

### 4.4 AI-Powered Event Explanation
Integrates an optional local LLM using Ollama and Llama 3.2 to generate explanations for selected suspicious events.

### 4.5 Interactive Dashboard
Uses Streamlit to display activity analysis and anomaly detection results.

### 4.6 Report Download
Allows users to download analyzed activity data in CSV format.

## 5. Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| NumPy | Numerical operations |
| Isolation Forest | Anomaly detection technique |
| Streamlit | Interactive web dashboard |
| Ollama | Local LLM execution |
| Llama 3.2 | Optional suspicious-event explanation |
| CSV | Activity log storage and report format |

## 6. System Workflow

The project follows these steps:

1. **Data Input:** Upload a CSV file containing cloud activity logs.
2. **Data Preprocessing:** Read and prepare the input data for analysis.
3. **Anomaly Detection:** Apply the Isolation Forest-based detection method to identify unusual activity.
4. **Risk Assessment:** Assign risk scores to the analyzed activities.
5. **AI Explanation:** Optionally generate explanations for selected events using Ollama.
6. **Visualization:** Display the analysis through the Streamlit dashboard.
7. **Report Generation:** Download the analyzed results as a CSV file.

## 7. Dataset Information

The project uses simulated cloud security activity logs.

The dataset contains fields such as:

| Field | Description |
|---|---|
| timestamp | Date and time of activity |
| username | User associated with the activity |
| source_ip | Source IP address |
| country | Country associated with the activity |
| login_hour | Hour of login |
| failed_attempts | Number of failed login attempts |
| successful_login | Login success status |
| new_device | Indicates whether a new device was used |
| unusual_location | Indicates unusual location activity |
| bytes_downloaded | Amount of data downloaded |
| action | Activity performed by the user |

These fields help the system analyze user activity and identify potentially unusual patterns.

## 8. Project Structure

```text
CloudShield__Ai/
│
├── app.py
├── detector.py
├── data_generator.py
├── ollama_client.py
├── requirements.txt
├── test_detector.py
├── README.md
│
└── data/
    └── sample_security_logs.csv
```

### File Description

| File | Description |
|---|---|
| app.py | Main Streamlit dashboard application |
| detector.py | Data preprocessing, anomaly detection, and risk scoring |
| data_generator.py | Generates simulated cloud security logs |
| ollama_client.py | Handles optional Ollama integration |
| requirements.txt | Lists required Python packages |
| test_detector.py | Contains tests for the detection module |
| sample_security_logs.csv | Sample cloud activity dataset |

## 9. Installation and Execution

### Prerequisites

- Python 3.10 or later.
- pip package manager.
- Ollama (optional, for AI-generated explanations).

### Step 1: Clone the Repository

```bash
git clone https://github.com/nidhi-rai09/CloudShield__Ai.git
```

### Step 2: Navigate to the Project Folder

```bash
cd CloudShield__Ai
```

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 4: Run the Application

```bash
streamlit run app.py
```

The Streamlit application will open in your default web browser.

### Optional: Enable Local AI Explanations

Install Ollama and download the Llama 3.2 model:

```bash
ollama pull llama3.2
```

Start Ollama and use the application's optional explanation feature.

## 10. Expected Results

The application provides:

- Analysis of uploaded cloud activity logs.
- Identification of unusual activities.
- Risk scores for analyzed events.
- Optional AI-generated explanations.
- Interactive visualization through a dashboard.
- Downloadable CSV reports.

Detected anomalies should be treated as investigation leads rather than confirmed security attacks.

## 11. Limitations

The current implementation is a local prototype.

- It analyzes uploaded or simulated CSV activity logs.
- It does not directly connect to live AWS or other cloud accounts.
- It does not provide continuous real-time cloud monitoring.
- It does not automatically block users or execute security actions.
- AI-generated explanations are optional and require Ollama to be available.

## 12. Future Enhancements

- Integration with AWS CloudTrail for read-only activity log collection.
- Real-time cloud activity monitoring.
- User authentication and role-based access control.
- Improved security alert investigation workflows.
- Secure audit logging.
- Support for additional cloud platforms.


## 13. Conclusion

CloudShield AI demonstrates the application of artificial intelligence in cloud security log analysis.

By combining Isolation Forest-based anomaly detection, risk scoring, optional LLM-powered explanations, and an interactive dashboard, the system helps identify unusual cloud activity and supports security teams in investigating potential threats.

The project provides a foundation for developing more advanced and intelligent cloud security monitoring solutions.
