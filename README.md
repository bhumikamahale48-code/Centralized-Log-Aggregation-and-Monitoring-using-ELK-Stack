# Centralized Log Aggregation and Monitoring using ELK Stack

# Project Overview

This project demonstrates a centralized logging system using the ELK Stack (Elasticsearch, Logstash, Kibana).

In traditional systems, logs are scattered across multiple servers, making troubleshooting difficult.
This system collects logs from multiple servers, parses and stores them in Elasticsearch, and visualizes them in Kibana for easy monitoring.

---

# Key Benefits

* Centralized logging
* Real-time error detection
* Faster troubleshooting
* Visual dashboards for monitoring

---

# Architecture / Data Flow

App Server 1 (Nginx)
App Server 2 (Nginx)
↓
Filebeat
↓
Logstash
↓
Elasticsearch
↓
Kibana

---

#  Components

* **App Servers**: Run Nginx to serve applications and generate logs
* **Filebeat**: Collects logs and sends them to Logstash
* **Logstash**: Parses, filters, and structures logs
* **Elasticsearch**: Stores logs in indices for search and analysis
* **Kibana**: Visualizes logs and creates dashboards/alerts

---

# Technologies Used

* AWS EC2
* Nginx (Web Server)
* Filebeat (Log Forwarder)
* Logstash (Log Processor)
* Elasticsearch (Log Storage & Indexing)
* Kibana (Dashboard & Visualization)
* Ubuntu Linux 24.04 LTS
* KQL (Kibana Query Language for filtering)

---

# Infrastructure Setup

# EC2 Instances

| Instance     | Purpose                           |
| ------------ | --------------------------------- |
| ELK Server   | Elasticsearch + Logstash + Kibana |
| App Server 1 | Nginx + Filebeat                  |
| App Server 2 | Nginx + Filebeat                  |

---

# Project Screenshots

# EC2 Instances

   <img width="1365" height="651" alt="image" src="https://github.com/user-attachments/assets/12274b84-f252-450b-ad24-7b9178abe4c7" />

   Shows all running instances in AWS console

   # Nginx Running in Browser

   <img width="1347" height="718" alt="image" src="https://github.com/user-attachments/assets/2e3b898a-93c5-4b59-9ee8-70e9c9bf2ba7" />

   Default Nginx page on App Server

# 404 Error in Browser

<img width="849" height="234" alt="image" src="https://github.com/user-attachments/assets/2a8d5038-927f-4e69-bc44-29a8aa96bd28" />
   
   Shows manual 404 error generated to test ELK pipeline

# Filebeat Running

<img width="1339" height="695" alt="image" src="https://github.com/user-attachments/assets/9e1e8bc0-a7ba-476e-a343-168eead7d320" />
   
   Verifies Filebeat service is active and forwarding logs

# Logstash Running

   <img width="839" height="240" alt="image" src="https://github.com/user-attachments/assets/0ce5b09b-2359-4e7f-ab42-0195630d4240" />


   Shows Logstash service running and ready to parse logs

# Elasticsearch Index Created

<img width="850" height="145" alt="image" src="https://github.com/user-attachments/assets/bf1df39e-563e-4f4f-8cb7-927c0eea3371" />

   Confirms logs are stored in `nginx-logs-*` indices

 # Kibana Discover Logs

<img width="870" height="401" alt="image" src="https://github.com/user-attachments/assets/797182cb-8b93-47f4-8fd6-80f31d5ed221" />

   Visualizes logs collected from App Servers

 # Error Log Detection in Kibana

<img width="1159" height="580" alt="image" src="https://github.com/user-attachments/assets/6865b3be-db43-4e19-a7f9-630fa1231845" />

   Shows HTTP 404 logs filtered using KQL in Kibana Discover

---

#  Log Processing

Logstash parses incoming logs and applies filters:

* **4xx Errors**: message = "404"
* **5xx Errors**: message = "500" (optional)

Structured logs are stored in Elasticsearch indices for quick search and analysis.

---

##  Monitoring with Kibana

Kibana dashboards allow:

* Centralized log visualization
* Real-time error detection
* Monitoring of requests per minute
* Identifying top client IPs
* Configurable alerts for abnormal spikes

---

#  Project Outcome

* Centralized logging implemented
* Logs collected from multiple servers
* Logs parsed and indexed in Elasticsearch
* Visualized logs in Kibana
* Faster troubleshooting and proactive error detection

---

##  Author
Author
Bhumnika Mahale
DevOps Enthusiast | AWS | Docker | Kubernetes | CI/CD
LinkedIn | GitHub


