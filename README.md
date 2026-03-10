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
2. **Empowers Privacy:** Puts the "Permission Key" in the patient's hands. Data only moves when the patient explicitly authorizes it via their mobile device.
3. **Ensures Reliability:** A local-first architecture designed for the real-world challenges of intermittent connectivity, ensuring that critical history is available even when the cloud is not.

## 💾 Data Ownership & Redundancy
MedRelay uses a decentralized "Mirror" system to ensure data is never lost:

* **Clinic Records:** Each facility maintains its own local SQLite database of patient interactions. They own their clinical data and can access it 100% offline.
* **Patient Records:** Patients carry an encrypted "mirror" of their medical history on their mobile device and personal cloud (Google Drive).
* **Frictionless Sync:** When a patient visits a new facility, MedRelay facilitates a secure "handshake" to sync relevant history from the patient's vault (or a previous clinic) to the current doctor's desktop—with the patient's explicit permission.

## 🛠️ Unified Engine, Purpose-Built UI
We use **Flutter** for both platforms to ensure native performance and 100% predictability in data handling:

* **MedRelay Desktop (The Clinician Hub):** A high-performance Windows/Linux utility designed for rapid data retrieval and record updates. It works alongside existing EMRs to bridge the gap between facilities.
* **MedRelay Mobile (The Privacy Controller):** An Android/iOS app that acts as the patient's personal authorization center. It manages encryption keys and sharing permissions.
* **Shared Core:** A unified Dart library for AES-256 encryption, Google Auth integration, and SQLite persistence.

## 🔐 Security & Data Resilience
MedRelay is built to be "Uninstall-Proof" by leveraging secure, user-friendly identity.

* **Google-Powered Identity:** Patients sign in using their Google Account. This ensures they can regain access to their history on any device without needing to remember complex recovery phrases.
* **Personal Cloud Vault:** Encrypted medical records are stored in the patient's own **Google Drive**. Rara Studios never "sees" or "hosts" this data.
* **Zero-Knowledge Architecture:** Data is encrypted locally using **AES-256** before being synced. Neither Google nor Rara Studios can read the medical files.
* **Auditability:** By open-sourcing our encryption logic, we allow the medical community to verify that data remains private and patient-controlled.

## ⚖️ Compliance & Privacy by Design
MedRelay is engineered to align with the **Philippine Data Privacy Act of 2012 (RA 10173)**:

* **Patient-Led Consent:** The mobile "Handshake" acts as a verifiable, time-stamped electronic consent for data disclosure, fulfilling NPC requirements for sensitive personal information.
* **Data Portability:** MedRelay serves as a practical implementation of the "Right to Data Portability," allowing patients to move their history between providers seamlessly.
* **Decentralized Risk:** By avoiding a central "National Database," MedRelay eliminates the risk of a single point of failure or a massive centralized data breach.
* **Zero-Knowledge Processing:** Rara Studios acts as a stateless intermediary. We provide the infrastructure (The Relay) but never have access to the "Key" or the "Content."

## ⚖️ Why AGPLv3?
MedRelay is licensed under the **GNU Affero General Public License v3.0**. This choice is fundamental to our mission:

* **Auditability:** Privacy-first software must be transparent. AGPLv3 ensures the code is always open for public security audits.
* **Community Standards:** It prevents any single entity from "forking" the project to create a proprietary, closed-off network that restricts data flow.
* **Reciprocity:** Any improvements made to the sharing protocol by service providers must be shared back, ensuring the "bridge" between facilities continues to improve for everyone.

## 💳 Business Model
MedRelay is **Free and Open Source** for patients. We offer a **Subscription-based Service** for clinics which includes:

* **Access to the Secure Relay Infrastructure** for clinic-to-clinic data handshakes and record indexing.
* **Verified Participation** in the MedRelay secure sharing network to build trust with patients.
* **Seamless Integration** tools for syncing encrypted data via the patient's personal cloud.

---
Developed by **Rara Studios** and **O-rensa** *Eliminating friction and restoring privacy in healthcare.*

### 📁 Project Structure
```text
├── medrelay_core/         # Shared Logic: Encryption, Permission Handshakes, API Client
├── medrelay_desktop/      # Clinician Hub (Data Sharing & Retrieval)
├── medrelay_mobile/       # Privacy Controller (Authorization & Patient Vault)
└── medrelay_relay/        # Go-based Relay Server (Subscription Layer)
