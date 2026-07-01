# Enterprise SOC Monitoring Dashboard Migration

## Project Overview

This project involved migrating enterprise security monitoring dashboards from Splunk to Grafana using Azure Data Explorer (ADX) and Kusto Query Language (KQL).

My responsibility was to develop operational and security dashboards based on production monitoring data to improve visibility across multiple security platforms.

---

# Business Context

The customer planned to migrate its existing monitoring dashboards from Splunk to Grafana as part of a monitoring platform modernisation initiative.

The dashboards were designed to provide a centralised view of operational and security data collected from multiple enterprise systems.

---

# My Responsibilities

- Developed Grafana dashboards using Kusto Query Language (KQL)
- Queried security data from Azure Data Explorer (ADX)
- Designed dashboard layouts based on operational requirements
- Built visualisations for security operations and infrastructure monitoring
- Validated dashboard accuracy using production data
- Worked with internal stakeholders to refine dashboard requirements and improve usability

---

# Technical Stack

| Component | Technology |
|-----------|------------|
| Dashboard Platform | Grafana |
| Query Language | Kusto Query Language (KQL) |
| Data Platform | Azure Data Explorer (ADX) |
| Data Sources | Cisco Meraki, Sophos Central, Cisco Umbrella, Microsoft Entra ID |

---

# Dashboards Delivered

## 1. IT Command Centre Dashboard

A high-level operational dashboard providing a single-pane-of-glass view across enterprise security and infrastructure.

Key metrics included:

- Device Health
- Offline Devices
- Endpoint Status
- Security Alerts
- DNS Threat Overview
- User Activity
- Infrastructure Status

---

## 2. Cisco Meraki Network Dashboard

Network monitoring dashboard providing operational visibility into enterprise network infrastructure.

Features:

- Device Status
- Uplink Status
- Client Statistics
- Network Availability
- Security Events
- WAN Health

---

## 3. Sophos Endpoint Dashboard

Endpoint security dashboard built for monitoring managed endpoints.

Features:

- Endpoint Health
- Device Inventory
- Open Security Alerts
- High Severity Events
- Endpoint Protection Status

---

## 4. Cisco Umbrella Dashboard

DNS security dashboard providing visibility into DNS activity and security events.

Features:

- DNS Requests
- Threat Categories
- Blocked Requests
- Top Domains
- Security Events
- Identity-based Filtering

---

# Technical Challenges

During development, several technical challenges were encountered, including:

- Building efficient KQL queries for large datasets
- Adapting dashboards to different data schemas
- Improving dashboard performance
- Designing dashboards suitable for SOC operational workflows
- Validating dashboard accuracy against production monitoring data

These challenges required iterative query optimisation and continuous testing before deployment.

---

# Project Outcomes

The project successfully delivered multiple production dashboards covering:

- Enterprise infrastructure monitoring
- Network visibility
- Endpoint monitoring
- DNS security monitoring

The dashboards provided SOC analysts with a centralised monitoring interface, improving operational visibility across multiple security platforms.

---

# Skills Demonstrated

- Grafana Dashboard Development
- Azure Data Explorer (ADX)
- Kusto Query Language (KQL)
- Security Monitoring
- SOC Operations
- Data Visualisation
- Infrastructure Monitoring
- Network Security Monitoring
- Endpoint Security Monitoring
- DNS Security Monitoring
- Stakeholder Communication

---

# Lessons Learned

This project demonstrated that effective SOC dashboards require more than technical visualisation skills.

A successful dashboard must also reflect operational workflows, business requirements, and the daily needs of SOC analysts. Close collaboration with stakeholders and continuous iteration were essential to delivering dashboards that were both technically accurate and operationally useful.
