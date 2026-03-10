# 🩺 MedRelay
### Decentralized. Patient-Centric. Offline-First EMR.

![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue.svg)
![Platform: Flutter](https://img.shields.io/badge/Platform-Flutter-02569B?logo=flutter)

**MedRelay** is a high-performance, open-source Electronic Medical Record (EMR) ecosystem built entirely with **Flutter**. It bridges the gap between private clinics and patients in the Philippines by treating the patient’s smartphone as the primary, secure transport layer for medical history.

---

## 🚀 The Vision
Most EMR systems are built for the cloud first. MedRelay is built for the **local environment first**. 

By using a **Dual-App Architecture**, we provide tailored experiences for two distinct users:
1. **The Clinician (Desktop):** A data-dense, keyboard-optimized interface for Windows/Linux. Built for complex medical management and 100% offline clinic operations.
2. **The Patient (Mobile):** A simplified, touch-first Android/iOS experience for portability and personal record ownership.

## 🛠️ Unified Engine, Tailored UI
We use **Flutter** for both platforms to ensure native performance and absolute predictability across devices. While the UI is distinct for each use case, they share a robust technical core.

* **MedRelay Desktop:** Native Windows/Linux suite. Optimized for high-density data entry and patient history visualization.
* **MedRelay Mobile:** Native Android/iOS app. Optimized for "On-the-go" access, secure QR handshakes, and encrypted personal backups.
* **Shared Core:** A unified Dart logic layer handles AES-256 encryption, SQLite persistence, and Relay API communication.

## 📁 Project Structure
```text
├── medrelay_core/         # Shared Logic: Encryption, Models, API Client
├── medrelay_desktop/      # Desktop Suite (Data-Dense UI for Clinics)
├── medrelay_mobile/       # Mobile App (Patient-Centric UI)
└── medrelay_relay/        # Go-based Relay Server (Subscription Layer)
