# Microsoft Teams Device State Alert

## 📌 Overview

This solution provides real-time monitoring of Microsoft Teams devices and triggers alerts when devices enter a critical or offline state.

The alerting rule is configured using Microsoft Teams Admin Center and sends notifications directly to a Teams channel for faster incident response.

---

## 🎯 Purpose

This automation ensures proactive monitoring of Teams-certified devices to prevent disruption in collaboration services.

### Key benefits:

- ✅ Real-time alerting for device issues  
- ✅ Faster incident detection and response  
- ✅ Centralized alerting via Teams channel  
- ✅ No-code configuration using Teams Admin Center  
- ✅ Improved device reliability and monitoring  

---

## 🧭 Alert Flow Diagram

```mermaid
flowchart TD

A[Device Monitoring System] --> B[Evaluate Device Health Status]

B --> C{Is Device Status<br/>Offline or Critical?}

C -- Yes --> D[Trigger Alert Rule]

D --> E[Send Channel Notification<br/>MonitoringAlerts Channel]

C -- No --> F[No Action]

E --> F
