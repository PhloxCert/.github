# 🚀 PhloxCert

**Immutable Fire Safety Compliance & Digital Identity powered by IOTA.**

## 📖 Overview

### The Problem
The tragedy of **Crans-Montana** was not just an accident; it was a symptom of a structural collapse in monitoring processes. Investigations revealed that the site had not undergone a safety inspection in over **5 years**, leading to blocked exits and non-functional extinguishers during a disaster that claimed 40 lives. This stems from a fundamental problem: **Opacity and manipulability of safety data.**

Traditional states of compliance rely purely on "trust". PDFs and GPS data reside on central company servers where an administrator or a malicious actor could alter the date of a check to accommodate a client. 

*   **Common**: Passive inspections and superficial maintenance affect millions of public venues globally.
*   **Growing**: Growing legal liabilities, strict compliance directives (such as the Italian Decree 09/2021), and demands for transparency from insurance and tourism sectors.
*   **Urgent**: Disasters demonstrate that safety is a "here and now" requirement.
*   **Mandatory**: Fire safety is governed by strict laws, yet when technicians take over undocumented systems ("Dark Takeover"), they operate in a legal limbo without protection.
*   **Frequent**: Safety checks are operational necessities that need to be repeated over time (like every semester or annually), making manual processes inefficient and prone to human error.

### The Solution: The "Black Box" of Building Safety
PhloxCert leverages the **IOTA Protocol** to provide a strictly mathematical "Architecture of Trust", moving from internal traceability to universal certification. By decentralizing inspection records, we ensure that:

- **Zero-Trust Integrity**: We create a digital fingerprint (hash) of the document and sculpt it on a public, decentralized registry. If even a single pixel of the PDF is changed, the hash breaks.
- **Non-Repudiability of Origin**: Technicians can instantly lock their "save notes" upon a system takeover. Once notarized, no one can deny that a specific observation was recorded at that exact moment, shielding technicians from unwarranted legal liabilities.
- **Real-Time Awareness**: Consumers and stakeholders can verify a venue's safety status instantly via QR codes.
- **Enforcement through Transparency**: Moving from "check-the-box" compliance to a verifiable, immutable audit trail.

---

## ✨ Key Features

### Current Features (MVP)
* **🔐 Wallet-Based Authentication**: Secure access for inspectors and operators using IOTA DIDs.
* **🛡️ Locked Notarizations**: Unalterable proof-of-inspection with SHA256 integrity hashes, locking documents on the blockchain to prevent backdating or deletion.
* **📊 Dual-Identity Attribution**: Independent tracking and verification for both the **Uploader** (inspector) and the **Activity Subject** (establishment).
* **📱 Public Verification Portal**: A dynamic `/landing/did:iota:address` interface accessible via QR code for consumers to instantly verify a venue's safety status and audit the latest documents, **no wallet required for verification.**

### Future Features (Roadmap)
* **📦 Digital Twin Tokenization (NFTs)**: Every safety device (extinguisher, alarm) will have a unique "Digital Passport" represented as an NFT, creating an unbreakable link between the maintenance history and the physical device.
* **📋 Mandatory Digital Checklists**: Technicians will access device history via NFC/QR and follow guided workflows to ensure every check complies with specific regulations.
* **🔌 API System Integration**: Seamless integration with the existing management software of maintenance companies, allowing them to send data transparently to our "Digital Notary" without altering their familiar software environments.

---

## ⛓️ Use of IOTA Technology
IOTA was chosen for its ability to handle frequent micro-data transactions without prohibitive fees, making safety notarizations that need to be repeated over time (like every semester or annually) economically viable.

* **IOTA Move Smart Contracts**: Manages the **User Registry** and coordinates the lifecycle of notarization objects directly on-chain.
* **IOTA Identity (DIDs)**: Every user and establishment is identified via a Decentralized Identifier, ensuring sovereign ownership of compliance history.
* **Locked Notarizations**: Provides a mathematical, cryptographic link between digital records and physical safety checks, acting as an incorruptible data logger.

---

## 🏗 System Architecture

### High-Level Design
PhloxCert consists of a **Vite/React FRONTEND** for user interaction, an **Express/TypeScript BACKEND** for secure transaction handling and authentication, **ON Chain Contracts** on IOTA as the final arbiter of truth, and **PINATA** for decentralized file storage.

```text
  ┌──────────────┐       ┌──────────────┐       ┌──────────────┐
  │   FRONTEND   │       │   BACKEND    │       │  IOTA LEDGER │
  │ (Vite/React) │       │ (Express TS) │       │ (Move Chain) │
  └──────┬───────┘       └──────┬───────┘       └──────┬───────┘
         │  1. Upload File &    │                      │
         │     Get PINATA CID   │                      │
         │                      │                      │
         │  2. Submit Metadata  │                      │
         ├─────────────────────►│  3. Sign & Notarize  │
         │                      │◄────────────────────►│
         │  4. Verify & Index   │                      │
         │◄─────────────────────┤                      │
```

### Technical Stack
* **Language**: TypeScript, Move, JavaScript
* **Frameworks**: React, Vite, Express, TailwindCSS
* **IOTA SDKs**: `@iota/iota-sdk`, `@iota/dapp-kit`, `@iota/identity-wasm`

---

## 🎬 Live Demo & Media
* **Live Demo Link:** [https://phloxcert-frontend.pages.dev/](https://phloxcert-frontend.pages.dev/)
* **Video Walkthrough:** [TODO]
* **Smart Contract Explorer:** 
    * [IOTA Explorer register_contract PackageID](https://explorer.iota.org/object/0x8fe48ce8c30d4c9d57cc288e47e915afb22c900857c78644cb4a01d63b25964b?network=testnet)
    * [IOTA Explorer register_contract RegistryID](https://explorer.iota.org/object/0x9bf863f059ae70e2cbdfff19feb782aa101ccd6b29304d61846e17beb77127be?network=testnet)


*(Dashboard Preview)*
![Technician Dashboard Preview](/Technician_Dashboard.png)
![Business Dashboard Preview](/Business_Dashboard.png)

---

## 📈 Startup Strategy & Market Feedback

Initially, we approached local venues (bars, retail) to offer self-verification tools, but our market research revealed a strategic pivot was necessary. Direct venue owners viewed the system as a "nice-to-have" rather than a critical need and were reluctant to invest unless legally mandated.

Consequently, we shifted our focus to the real stakeholders: **Fire Safety Maintenance Companies and Technicians**.  
* **General Manager Feedback (Leading Italian Safety Firm)**:
  * **Strong Interest for Structured Clients**: Confirmed that certified and immutable transparency is highly valuable for large clients (e.g., GDO, industry, multi-site realities). A significant value lies in the traceability of the entire lifecycles of safety devices, beyond just maintenance reports.
  * **Barriers to Adoption**: Identified economic and cultural barriers. Clients are reluctant to invest in extra services, expecting maintenance firms to absorb the cost. Additionally, the sector adopts innovation slowly, making "seamless integration with existing management software" via APIs an absolute necessity rather than an optional feature.
  * **Replacing Obsolete Systems**: Emphasized the value of transitioning from outdated physical punch-cards to a fully digital guarantee. Incorporating mandatory check-marks directly tied to regulations ensures consistency and reduces litigation, protecting brand reputation long-term.
* **15-Year Senior Technician Feedback**: Emphasized the urgent need for **Non-Repudiability**. With upcoming regulations (Decree 09/2021) placing total legal liability on the technician, our blockchain notarization acts as a shield. It allows technicians to legally prove what issues were reported at the exact moment of inspection, preventing internal cover-ups or vanished documents if an accident later occurs.

---

## 🛠 Setup & Installation

You can experience PhloxCert either through our live testnet deployment or by running the whole stack locally.

### Path A: Web Application (Testnet)
The easiest way to test the platform.
1. Download and install the [IOTA Wallet Extension](https://chromewebstore.google.com/detail/iota-wallet/iidjkmdceolghepehaaddojmnjnkkija).
2. Switch your wallet network to **IOTA Testnet**.
3. Obtain testnet funds from the [IOTA Faucet](https://faucet.testnet.iota.cafe/).
4. Create at least two accounts in your wallet to simulate different roles (e.g., The Technician uploading the document, and the Establishment viewing its documents).
5. Visit [https://phloxcert-frontend.pages.dev/](https://phloxcert-frontend.pages.dev/) and connect your wallet.

### Path B: Manual Local Development
If you wish to spin up the local nodes, smart contracts, and backend yourself.

1. **Clone the Repositories:**
   ```bash
   git clone https://github.com/PhloxCert/phloxCert_frontend.git
   git clone https://github.com/PhloxCert/phloxCert_backend.git
   git clone https://github.com/PhloxCert/phloxCert_movePackages.git
   ```

2. **Run the Local Environment:**
   Set up your local IOTA node (`iota node`) and configure your IOTA wallet for `http://localhost:9000`. Fund addresses using the local faucet.

3. **Deploy the Smart Contracts:**
   ```bash
   cd phloxCert_movePackages/register_contract
   iota move build
   iota client publish --gas-budget 20000000
   ```
   *(Note the Package ID and Registry Object ID)*

4. **Start the Backend:**
   ```bash
   cd phloxCert_backend
   npm install
   # Create a .env with your generated keys and IDs
   npm run dev
   ```

5. **Start the Frontend:**
   ```bash
   cd phloxCert_frontend
   npm install
   # Configure .env with VITE_PACKAGE_ID and VITE_REGISTRY_ID
   npm run dev
   ```

---

## 👥 The Team
- [PhloxCert Devs](https://github.com/orgs/PhloxCert/teams/phloxcertdevs) ([Andrea Ballarini](https://github.com/Aballarini), [Luca Claus](https://github.com/siegluke))
