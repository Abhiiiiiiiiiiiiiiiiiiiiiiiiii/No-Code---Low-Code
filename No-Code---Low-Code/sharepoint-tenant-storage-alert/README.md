# SharePoint Tenant Storage Alert Automation

## 📌 Overview

This solution monitors SharePoint Online tenant storage usage and sends alert notifications when predefined thresholds are reached.

The automation is built using **Power Automate (Low-Code)** and is designed for proactive monitoring without requiring custom scripts or infrastructure.

---

## 🎯 Purpose

The goal of this automation is to prevent storage exhaustion and ensure uninterrupted SharePoint services.

### Key benefits:

- ✅ Proactive alerting before storage limits are reached  
- ✅ Reduced manual monitoring effort  
- ✅ Improved governance and capacity planning  
- ✅ Fully cloud-based solution (no infrastructure required)  

---

## 🧭 Flow Diagram

```mermaid
flowchart TD

A[Scheduled Trigger] --> B[Initialize varUsedPercentage]
B --> C[Initialize varAvailableMB]

C --> D[Try Scope]

D --> E[HTTP Request - Get SharePoint Storage Data]

E --> F[Parse Response]

F --> G[Calculate Used Percentage]

G --> H[Set varUsedPercentage]

H --> I[Calculate Available Storage]

I --> J[Set varAvailableMB]

J --> K{Storage > Threshold?}

K -- Yes --> L[Send Alert Email]
K -- No --> M[End Flow]

L --> M
