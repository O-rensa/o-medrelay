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

## ⚙️ Technical Philosophy: Medical P2P
MedRelay draws inspiration from **Peer-to-Peer (P2P)** architectures to ensure maximum resilience and privacy:

* **The "Tracker" Model:** Our Relay Server acts as a private tracker. It maintains a secure index of which facilities have interacted with a patient, but it never hosts the actual medical files.
* **Distributed Seeding:** Clinical data is "seeded" from two redundant points: the **Clinic's Local Database** and the **Patient's Personal Cloud (Google Drive)**.
* **Stateless Intermediation:** Like a torrent protocol, MedRelay facilitates the movement of bits between verified peers (Clinics and Patients) without needing to know the content of the data.

## 💾 Data Ownership & Redundancy
MedRelay uses a decentralized "Mirror" system to ensure data is never lost:

* **Clinic Records:** Each facility maintains its own local SQLite database. They own their clinical data and can access it 100% offline.
* **Patient Records:** Patients carry an encrypted "mirror" of their history on their mobile device and personal cloud.
* **Frictionless Sync:** When a patient visits a new facility, MedRelay facilitates a secure "handshake" to sync relevant history from the patient's vault to the current doctor's desktop—with the patient's explicit permission.

## 🛠️ Unified Engine, Purpose-Built UI
We use **Flutter** for both platforms to ensure native performance and 100% predictability:

* **MedRelay Desktop (The Clinician Hub):** A high-performance Windows/Linux utility for rapid data retrieval and record updates.
* **MedRelay Mobile (The Privacy Controller):** An Android/iOS app that acts as the patient's personal authorization center.
* **Shared Core:** A unified Dart library for AES-256 encryption, Google Auth integration, and SQLite persistence.

## 🔐 Security & Data Resilience
* **Google-Powered Identity:** Patients sign in via Google to regain access to their history on any device without needing recovery phrases.
* **Zero-Knowledge Architecture:** Data is encrypted locally using **AES-256** before being synced. Neither Google nor Rara Studios can read the medical files.
* **Auditability:** Open-source encryption logic allows the medical community to verify that data remains private and patient-controlled.

## ⚖️ Compliance & Privacy by Design
MedRelay is engineered to align with the **Philippine Data Privacy Act of 2012 (RA 10173)**:
* **Patient-Led Consent:** The mobile "Handshake" acts as a verifiable electronic consent for data disclosure.
* **Data Portability:** Fulfills the legal "Right to Data Portability" for patients.
* **Decentralized Risk:** Eliminates the risk of a single point of failure or a massive centralized data breach.

## ⚖️ Why AGPLv3?
* **Auditability:** Ensures the code is always open for public security audits.
* **Community Standards:** Prevents "forking" into proprietary, closed-off networks.
* **Reciprocity:** Improvements made by service providers must be shared back with the community.

## 💳 Business Model
MedRelay is **Free and Open Source** for patients. We offer a **Subscription-based Service** for clinics which includes:
* **Access to the Secure Relay Infrastructure** for clinic-to-clinic data handshakes and record indexing.
* **Verified Participation** in the MedRelay secure sharing network.
* **Seamless Integration** tools for syncing encrypted data via the patient's personal cloud.

---
Developed by **Rara Studios** and **O-rensa** *Eliminating friction and restoring privacy in healthcare.*

### 📁 Project Structure
```text
├── medrelay_core/         # Shared Logic: Encryption, Permission Handshakes, API Client
├── medrelay_desktop/      # Clinician Hub (Data Sharing & Retrieval)
├── medrelay_mobile/       # Privacy Controller (Authorization & Patient Vault)
└── medrelay_relay/        # Go-based Relay Server (Subscription Layer)
