# Microsoft Teams Device State Alert (No-Code Setup)

## 📌 Overview

This solution configures a **device state alert** in Microsoft Teams Admin Center.

It sends notifications when a Teams device becomes:
- Offline
- Critical

No Power Automate or scripting is used — this is a **built-in Teams Admin feature**.

---

## 🎯 Purpose

- Monitor Teams device health in real-time  
- Get instant alerts for device failures  
- Improve response time for issues  

---

## ⚙️ Step-by-Step Configuration (UI Setup)

Follow these steps in **Teams Admin Center**:

---

## 1️⃣ Create Alert Rule

- Go to: **Teams Admin Center**
- Navigate to: **Analytics & Reports → Alerts → Alert rules**
- Click: **Create Rule**

---

## 2️⃣ Configure Rule Type

- Select:
  - ✅ **Device Management**

---

## 3️⃣ Configure Condition

Set the condition for alert:

- **Parameter:** Device health status  
- **Operator:** IN  
- **Value:**  
  - Offline  
  - (Optional) Critical  

👉 This means alert will trigger when device is offline or unhealthy.

---

## 4️⃣ Configure Scope

- **Evaluation Frequency:** Real-time  
- **Device Users:** Select required users/devices  

👉 Example: Add all meeting rooms or Teams phones

---

## 5️⃣ Configure Action (Notification)

- Enable:
  - ✅ Channel Alert  

- Select:
  - **Team:** Your_Teams_name  
  - **Channel:** Your_Channel_name  

👉 Alerts will appear directly in Teams channel.

(Optional)
- Webhook can be added for external systems

---

## 6️⃣ Enable Rule

- Set:
  - ✅ Status → Active  
- Click: **Save**

---

## ✅ Final Result

Whenever a device becomes:
- Offline  
- Critical  

👉 A message is posted in Teams channel:
**Your Channel Name**
