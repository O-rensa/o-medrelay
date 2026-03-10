# 🩺 MedRelay
### Frictionless Medical Data Interoperability & Privacy Control

![License: AGPL v3](https://img.shields.io/badge/License-AGPL_v3-blue.svg)
![Platform: Flutter](https://img.shields.io/badge/Platform-Flutter-02569B?logo=flutter)

**MedRelay** is an open-source, decentralized infrastructure built to eliminate the friction of sharing medical records between healthcare facilities. Built with **Flutter**, it provides a secure "handshake" protocol that allows life-saving data to flow where it is needed, when it is needed, while ensuring patients maintain absolute control over their sensitive information.

---

## 🚀 The Vision: Logistics for Life-Saving Data
MedRelay is **not designed to replace existing EMR systems.** Its true purpose is to smoothen the logistics of life-saving data in a secure, efficient way. 

In the current landscape, medical data is trapped in silos. MedRelay acts as the "connective tissue" that:

1. **Reduces Friction:** Enables instant, secure data transfers between Facility A and Hospital B without complex, proprietary integrations.
2. **Empowers Privacy:** Puts the "Permission Key" in the patient's hands. Data only moves when the patient explicitly authorizes it.
3. **Ensures Reliability:** A local-first architecture designed for the real-world challenges of intermittent connectivity, ensuring that critical history is available even when the cloud is not.

## 🛠️ Unified Engine, Purpose-Built UI
We use **Flutter** for both platforms to ensure native performance and 100% predictability in data handling, while providing tailored experiences for each stakeholder:

* **MedRelay Desktop (The Clinician Hub):** A high-performance Windows/Linux utility designed for rapid data retrieval and record updates. It works alongside existing EMRs to bridge the gap between facilities.
* **MedRelay Mobile (The Privacy Controller):** An Android/iOS app that acts as the patient's personal authorization center. It manages encryption keys, sharing permissions, and serves as a secure storage vault.
* **Shared Core:** A unified Dart library for AES-256 encryption, decentralized identity (DID) logic, and SQLite persistence.

## ⚖️ Why AGPLv3?
MedRelay is licensed under the **GNU Affero General Public License v3.0**. This choice is fundamental to our mission:

* **Auditability:** Privacy-first software must be transparent. AGPLv3 ensures the code is always open for public security audits.
* **Community Standards:** It prevents any single entity from "forking" the project to create a proprietary, closed-off network that restricts data flow.
* **Reciprocity:** Any improvements made to the sharing protocol by service providers must be shared back, ensuring the "bridge" between facilities continues to improve for everyone.

## 💳 Business Model
MedRelay is **Free and Open Source** for patients. We offer a **Subscription-based Service** for clinics which includes:

* **Access to the Global Relay Infrastructure** for high-speed record synchronization.
* **Automated, encrypted backup and recovery services.**
* **Verified participation** in the MedRelay secure sharing network.

---
Developed by **Rara Studios** and **O-rensa** *Eliminating friction and restoring privacy in healthcare.*

### 📁 Project Structure
```text
├── medrelay_core/         # Shared Logic: Encryption, Permission Handshakes, API Client
├── medrelay_desktop/      # Clinician Hub (Data Sharing & Retrieval)
├── medrelay_mobile/       # Privacy Controller (Authorization & Patient Vault)
└── medrelay_relay/        # Go-based Relay Server (Subscription Layer)
