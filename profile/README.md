<div align="center">

# 🧠 MindMate

### AI-Powered Alzheimer's Care Platform

*Connecting patients, caregivers, and families through intelligent technology*

[![Backend](https://img.shields.io/badge/Backend-TypeScript-3178C6?style=flat-square&logo=typescript)](https://github.com/MindMate-Project/Backend)
[![Frontend](https://img.shields.io/badge/Frontend-React-61DAFB?style=flat-square&logo=react)](https://github.com/MindMate-Project/Web)
[![Mobile App](https://img.shields.io/badge/Mobile-Flutter-02569B?style=flat-square&logo=flutter)](https://github.com/MindMate-Project/MindMate-app)
[![AI](https://img.shields.io/badge/AI-Python-3776AB?style=flat-square&logo=python)](https://github.com/MindMate-Project/AI)

[![Live Web App](https://img.shields.io/badge/Live-Web%20App-000000?style=flat-square&logo=vercel)](https://web-mindmate.vercel.app)
[![API Docs](https://img.shields.io/badge/API%20Docs-Swagger-85EA2D?style=flat-square&logo=swagger)](https://alzaheimer-backend.onrender.com/api-docs/)

</div>

---

## What is MindMate?

MindMate is a full-stack platform designed to support Alzheimer's patients and their care networks. It combines real-time location tracking, intelligent reminders, memory preservation, face recognition, and IoT integration into one coordinated system — enabling caregivers and families to provide better, more responsive care.

---

## ✨ Core Capabilities

| Feature | Description |
|---|---|
| 🧩 **Face Recognition** | Helps patients recognize loved ones — point the camera at a person and the app says who they are and how they're related (InsightFace) |
| 📍 **Real-Time Location** | Live GPS tracking via Socket.io & MQTT IoT devices, with a location view for caregivers |
| 💾 **Memory Bank** | Store photos, videos, and stories with captions, relations, and tags |
| ⏰ **Smart Reminders** | Medication & appointment reminders with on-device notifications and a full-screen alarm in the mobile app |
| 🚨 **Alert System** | Instant safety alerts with acknowledgment tracking |
| 🔐 **Role-Based Access** | Secure multi-role system for patients, caregivers, and admins |
| ✉️ **Email Notifications** | Account verification and password reset emails via Brevo |

---

## 📱 App Preview

<div align="center">

| Patient Home | Face Recognition | Caregiver Dashboard |
|:---:|:---:|:---:|
| <img src="https://raw.githubusercontent.com/MindMate-Project/MindMate-app/dev-test/screenshots/07_patient_home.png" width="220" alt="Patient home screen"/> | <img src="https://raw.githubusercontent.com/MindMate-Project/MindMate-app/dev-test/screenshots/11d_face_outcome.png" width="220" alt="Face recognition result"/> | <img src="https://raw.githubusercontent.com/MindMate-Project/MindMate-app/dev-test/screenshots/15_caregiver_home.png" width="220" alt="Caregiver dashboard"/> |

*Full tour with 23 screenshots in the [mobile app README](https://github.com/MindMate-Project/MindMate-app#readme).*

</div>

---

## 🏗️ Architecture

How the pieces talk to each other:

```mermaid
flowchart LR
    APP["📱 Mobile App<br/>(Flutter)"]
    WEB["💻 Web App<br/>(React)"]
    API["🔷 Backend<br/>(Express REST API)"]
    SOCK["🔄 Socket.io"]
    AI["🤖 AI Service<br/>(FastAPI · InsightFace)"]
    DB[("🗄️ MongoDB")]
    CLD[("🖼️ Cloudinary<br/>media")]
    MAIL["✉️ Brevo<br/>email"]
    GPS["📡 GPS Tracker<br/>(IoT device)"]

    APP -- "REST + JWT" --> API
    WEB -- "REST + JWT" --> API
    API -- "face matching" --> AI
    API --> DB
    API --> CLD
    API -- "verification & reset emails" --> MAIL
    GPS -- "MQTT" --> API
    API -- "live location" --> SOCK --> WEB
```

The mobile app schedules reminder notifications **on the device itself** from the backend's reminder data — so alarms still fire even with a poor connection.

MindMate is split across four focused repositories:

### 🔷 [Backend](https://github.com/MindMate-Project/Backend)
**TypeScript · Express.js · MongoDB · Socket.io**

REST API and real-time server — the core of the platform. Handles authentication, user management, memories, reminders, alerts, location tracking, and IoT device communication.

### 🔷 [Web](https://github.com/MindMate-Project/Web)
**React · Redux Toolkit · JavaScript**

Web application for patients, caregivers, and family members. Provides dashboards for memory browsing, reminder management, live location viewing, and alert monitoring. **[Live demo →](https://web-mindmate.vercel.app)**

### 🔷 [Mobile App](https://github.com/MindMate-Project/MindMate-app)
**Dart · Flutter · Bloc/Cubit**

Cross-platform mobile application for patients and caregivers. Patients get medication and appointment reminders with a full-screen alarm, a Memory Bank of photos and stories, and a camera flow that recognizes the people around them. Caregivers manage their patients, create reminders and memories, register known people for face recognition, train memory with brain exercises, and check the patient's location.

- **One codebase, two platforms** — runs on Android & iOS from a single Flutter project
- **Two tailored experiences** — Patient and Caregiver, chosen at signup
- **Feature-first clean architecture** with Bloc/Cubit state management
- **Offline-friendly reminders** — notifications and alarms are scheduled on-device, so they fire even without a connection

### 🔷 [AI](https://github.com/MindMate-Project/AI)
**Python · FastAPI · InsightFace · ONNX**

Standalone face recognition microservice. Stores face embeddings of the people registered for each patient (family and friends) and identifies who appears in a photo, exposing results through a REST API consumed by the backend.

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technologies |
|---|---|
| **Backend** | Node.js, TypeScript, Express.js v5, MongoDB, Mongoose |
| **Real-Time** | Socket.io, MQTT |
| **Frontend** | React, Redux Toolkit, CSS3, HTML5 |
| **Mobile** | Flutter, Dart, Bloc/Cubit |
| **AI / ML** | Python, FastAPI, InsightFace, ONNX Runtime, OpenCV |
| **Auth & Security** | JWT, bcryptjs, role-based access control |
| **Notifications** | Flutter local notifications (reminders & alarms), Nodemailer + Brevo (email) |
| **Storage** | Cloudinary (media files), MongoDB (data) |
| **DevOps** | Docker · Render (Backend) · Vercel (Web) · AWS EC2 + GitHub Actions (AI) |

</div>



<div align="center">

*Built with ❤️ to improve the quality of life for Alzheimer's patients and their families.*

</div>
