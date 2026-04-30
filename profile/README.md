<div align="center">

# 🧠 MindMate

### AI-Powered Alzheimer's Care Platform

*Connecting patients, caregivers, and families through intelligent technology*

[![Backend](https://img.shields.io/badge/Backend-TypeScript-3178C6?style=flat-square&logo=typescript)](https://github.com/MindMate-Project/Backend)
[![Frontend](https://img.shields.io/badge/Frontend-React-61DAFB?style=flat-square&logo=react)](https://github.com/MindMate-Project/alzaheimer-web)
[![AI](https://img.shields.io/badge/AI-Python-3776AB?style=flat-square&logo=python)](https://github.com/MindMate-Project/AI)
[![API Docs](https://img.shields.io/badge/API%20Docs-Swagger-85EA2D?style=flat-square&logo=swagger)](https://alzaheimer-backend.onrender.com/api-docs/)

</div>

---

## What is MindMate?

MindMate is a full-stack platform designed to support Alzheimer's patients and their care networks. It combines real-time location tracking, intelligent reminders, memory preservation, face recognition, and IoT integration into one coordinated system — enabling caregivers and families to provide better, more responsive care.

---

## ✨ Core Capabilities

| Feature | Description |
|---|---|
| 🧩 **Face Recognition** | AI-powered patient identification using InsightFace |
| 📍 **Real-Time Location** | Live GPS tracking via Socket.io & MQTT IoT devices |
| 💾 **Memory Preservation** | Store photos, videos, and stories with metadata and tags |
| ⏰ **Smart Reminders** | Automated medication and appointment reminders with push/email/SMS |
| 🚨 **Alert System** | Instant safety alerts with acknowledgment tracking |
| 🔐 **Role-Based Access** | Secure multi-role system for patients, caregivers, and admins |
| 📱 **Push Notifications** | Firebase FCM for real-time multi-device notifications |

---

## 🏗️ Architecture

MindMate is split across three focused repositories:

### 🔷 [Backend](https://github.com/MindMate-Project/Backend)
**TypeScript · Express.js · MongoDB · Socket.io**

REST API and real-time server — the core of the platform. Handles authentication, user management, memories, reminders, alerts, location tracking, and IoT device communication.

### 🔷 [alzaheimer-web](https://github.com/MindMate-Project/alzaheimer-web)
**React · Redux Toolkit · JavaScript**

Web application for patients, caregivers, and family members. Provides dashboards for memory browsing, reminder management, live location viewing, and alert monitoring.

### 🔷 [AI](https://github.com/MindMate-Project/AI)
**Python · FastAPI · InsightFace · ONNX**

Standalone face recognition microservice. Identifies Alzheimer's patients via facial analysis and exposes results through a REST API consumed by the backend.

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technologies |
|---|---|
| **Backend** | Node.js, TypeScript, Express.js v5, MongoDB, Mongoose |
| **Real-Time** | Socket.io, MQTT |
| **Frontend** | React, Redux Toolkit, CSS3, HTML5 |
| **AI / ML** | Python, FastAPI, InsightFace, ONNX Runtime, OpenCV |
| **Auth & Security** | JWT, bcryptjs, role-based access control |
| **Notifications** | Firebase FCM, Nodemailer, Brevo (email & SMS) |
| **Storage** | Cloudinary (media files), MongoDB (data) |
| **DevOps** | Docker, Render |

</div>

---

## 🚀 Getting Started

Each repository has its own setup guide:

- **Backend** → [Setup instructions](https://github.com/MindMate-Project/Backend#-prerequisites--setup-locally)
- **alzaheimer-web** → `npm install && npm start`
- **AI** → `pip install -r requirements.txt && uvicorn main:app`

Full API reference is available at **[alzaheimer-backend.onrender.com/api-docs](https://alzaheimer-backend.onrender.com/api-docs/)**.

---

## 🤝 Contributing

Contributions are welcome across all repositories. Please open an issue first to discuss significant changes, then submit a pull request targeting the `main` branch.

---

<div align="center">

*Built with ❤️ to improve the quality of life for Alzheimer's patients and their families.*

</div>
