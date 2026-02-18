# DDOS-System-Architecture
Ddos system work flow

## Cloud-Based DDoS Protection System

##  Overview

A Distributed Denial of Service (DDoS) attack overwhelms a server with excessive traffic from distributed sources (botnets), making the service unavailable to legitimate users.

This project implements a **cloud-native DDoS Detection & Monitoring System on AWS** capable of identifying abnormal traffic patterns and triggering real-time alerts.

---

##  Architecture

EC2 Web Server → S3 Log Storage → GuardDuty / SageMaker → CloudWatch Monitoring → SNS Alerts

---

##  Core Components

### 1️ AWS EC2 – Web Server
- Hosted a web application.
- Generated Apache/Nginx access logs.
- Simulated high-traffic scenarios for DDoS testing.
- Captured IP address, request rate, and timestamps.

---

###  Amazon S3 – Log Storage
- Stored server access logs.
- Enabled scalable and durable centralized storage.
- Served as input for threat analysis services.

---

###  Threat Detection Layer

####  Amazon GuardDuty
- Monitored VPC, DNS, and S3 logs.
- Detected suspicious IP activity and traffic spikes.
- Generated security findings.

####  Amazon SageMaker (Optional ML Detection)
- Built anomaly detection model.
- Classified IPs as normal or suspicious.
- Detected abnormal request rates.

---

###  Monitoring & Alerts – CloudWatch + SNS
- Real-time dashboards:
  - Requests per IP
  - Traffic spikes
  - Geographic trends
- Configured alarms for threshold breaches.
- SNS notifications for potential DDoS activity.

---

##  Detection Strategy

- High request frequency from a single IP
- Sudden traffic bursts
- Geographic traffic anomalies
- Behavioral deviation from baseline

---

##  Final Output

- Real-time traffic visualization
- Suspicious IP identification
- Early DDoS spike detection
- Cloud-native scalable monitoring system

---

##  Tech Stack

- AWS EC2
- Amazon S3
- Amazon GuardDuty
- Amazon SageMaker
- Amazon CloudWatch
- Amazon SNS

---

##  Demo

 YouTube Demonstration:  
https://www.youtube.com/watch?v=yMgLvv4YpZw

---

##  Key Learnings

- Cloud security architecture
- Log-based threat detection
- Real-time monitoring systems
- AWS security services integration
- Infrastructure-level anomaly detection


