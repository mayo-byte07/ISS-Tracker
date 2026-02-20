# 🛰️ ISS-Tracker: Real-Time Space Data & Mission Control

[![Vite](https://img.shields.io/badge/Vite-5.3.1-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![React](https://img.shields.io/badge/React-18.3.1-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactjs.org/)
[![Status](https://img.shields.io/badge/Status-Active%20Development-green?style=for-the-badge)](https://github.com/mayo-byte07/iss-tracker)

**ISS-Tracker** is a high-performance, scalable web architecture designed to democratize access to real-time space data. By integrating live telemetry from NASA, SpaceX, ESA, and JAXA, it provides a centralized "Mission Control" experience for researchers and space enthusiasts worldwide.

[**Live Demo**](https://iss-tracker.vercel.app) | [**Report Bug**](https://github.com/mayo-byte07/iss-tracker/issues) | [**Request Feature**](https://github.com/mayo-byte07/iss-tracker/issues)

---

## 🚀 Key Features

* **🛰️ Real-Time ISS Tracking:** WebSocket-driven position updates with SGP4 orbital propagation.
* **🌍 Interactive Earth Visualization:** Dual-mode rendering (2D Mercator & 3D Spherical) with 60fps canvas animations.
* **📊 Multi-Agency Data Pipeline:** Concurrent data processing from 8+ space APIs with intelligent rate limiting.
* **🌌 Mission Control Dashboard:** T-minus countdowns for SpaceX/NASA launches and Starlink constellation mapping.
* **📱 Mobile-First Architecture:** Full touch-gesture support for pan/zoom on orbital maps.

---

## 🏗️ System Architecture



```mermaid
graph TD
    A[Space APIs] -->|Rate Limited| B[ISS-Tracker Engine]
    B --> C{Data Pipeline}
    C --> D[React UI]
    D --> E[ISS Tracking]
    D --> F[Launch Charts]
    D --> G[3D Visualization]
    
    style B fill:#f9f,stroke:#333,stroke-width:2px
    style C fill:#bbf,stroke:#333,stroke-width:2px

