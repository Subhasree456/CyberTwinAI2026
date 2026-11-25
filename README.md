# 🛡️ Digital Twin Cyber War – HUNTER AI

### AI-Powered Cybersecurity Digital Twin & Threat Simulation Platform

A full-stack cybersecurity platform that creates a virtual cyber-range environment to simulate security scenarios, monitor network telemetry, detect suspicious activities, investigate threats using AI, and manage incident response workflows.

**The platform combines Digital Twin technology, Machine Learning, Threat Intelligence, and AI-assisted security analysis to help security teams understand and investigate cyber threats in a controlled environment.**

> **Safety First:** All built-in attack simulations generate synthetic telemetry. They do not send attack traffic to real systems or external hosts.

---

## 🌐 Project Overview

Digital Twin Cyber War – HUNTER AI is designed as a centralized cybersecurity monitoring and simulation workspace.

It provides a virtual environment where security analysts can:

- Monitor network and security events.
- Simulate controlled cyberattack scenarios.
- Detect suspicious activities using rule-based detection.
- Identify anomalous behavior using Machine Learning.
- Investigate security incidents using HUNTER AI.
- Integrate external SIEM and EDR platforms.
- Analyze threat intelligence.
- Manage incident response through approval-based workflows.

The platform is built with a React frontend, Node.js and Express backend, and SQLite database.

---

## ✨ Key Features

### 1. Digital Twin Cybersecurity Environment
- Virtual cybersecurity workspace.
- Network and security event visualization.
- Controlled cyberattack simulations.
- Attack-path and risk evaluation.
- Workspace-based security management.

### 2. HUNTER AI Security Assistant
- AI-powered security investigation.
- Natural-language security queries.
- Context-aware analysis of telemetry and detections.
- Evidence-based responses with source references.
- Supports OpenAI-compatible LLM endpoints.

### 3. Real-Time Security Monitoring
- Live security telemetry ingestion.
- Server-Sent Events (SSE) streaming.
- Security event tracking.
- Network-flow monitoring.
- Centralized event investigation.

### 4. Machine Learning Anomaly Detection
- Isolation Forest-based anomaly detection.
- Behavioral feature analysis.
- Per-workspace model training.
- Anomaly scoring and severity classification.
- Feature-level explanations.

### 5. Advanced Threat Detection
- Brute-force attack detection.
- Port-scanning detection.
- Beaconing activity detection.
- Suspicious network fan-out detection.
- Known-bad destination and blocked-egress detection.
- Detection evidence and incident tracking.

### 6. Threat Intelligence Integration
- RDAP registration lookups.
- AbuseIPDB integration.
- AlienVault OTX integration.
- Threat indicator investigation.
- Cached threat intelligence results.

### 7. SIEM & EDR Integrations

Supports integration with:

- Splunk
- Elastic Security
- Microsoft Sentinel
- Microsoft Defender for Endpoint
- CrowdStrike Falcon
- Wazuh
- Generic SIEM and EDR APIs

Connectors become active when valid credentials and network access are configured.

### 8. Incident Response & Automation
- Security response playbooks.
- IP blocking proposals.
- Host isolation proposals.
- Session revocation.
- Identity disabling.
- Approval-based response execution.
- Reversible action support where applicable.

### 9. Authentication & Access Control
- Session-based authentication.
- Role-Based Access Control (RBAC).
- Workspace isolation.
- Password hashing.
- Secure session cookies.
- Rate limiting.
- Audit logging with hash-chain verification.

---

## 🏗️ System Architecture

```text
                SECURITY ANALYST
                       |
                       ▼
              REACT FRONTEND
             React 18 + Vite
                       |
                       ▼
              EXPRESS API SERVER
                 Node.js
                       |
        ┌──────────────┼──────────────┐
        |              |              |
        ▼              ▼              ▼
   Authentication  Telemetry       Security
      & RBAC        Ingestion      Detection
        |              |              |
        └──────────────┼──────────────┘
                       |
          ┌────────────┼────────────┐
          |            |            |
          ▼            ▼            ▼
       SQLite       ML Engine    Threat Intel
      Database     Isolation      Services
                    Forest
          |            |            |
          └────────────┼────────────┘
                       |
                       ▼
                  HUNTER AI
               Security Assistant
                       |
                       ▼
              INCIDENT RESPONSE
              & APPROVAL WORKFLOW
```

---

## 🧰 Technology Stack

| Category | Technologies |
|---|---|
| Frontend | React 18, JavaScript, Vite |
| Backend | Node.js, Express 5 |
| Database | SQLite |
| Machine Learning | Isolation Forest |
| AI Integration | OpenAI-compatible LLM APIs |
| Authentication | Session Authentication, bcrypt |
| Security | Helmet, RBAC, Rate Limiting |
| Network Monitoring | Zeek, Suricata, NetFlow |
| Threat Intelligence | RDAP, AbuseIPDB, AlienVault OTX |
| SIEM / EDR | Splunk, Elastic, Sentinel, Defender, CrowdStrike, Wazuh |
| Testing | Vitest, Playwright |
| Deployment | Vercel, Render |
| Version Control | Git, GitHub |
| CI/CD | GitHub Actions |

---

## 📂 Project Structure

```text
CyberTwinAI2026/
│
├── .github/
│   └── workflows/
│
├── api/
│   └── API entry point
│
├── collectors/
│   └── flow-shipper.mjs
│
├── public/
│   └── Static assets
│
├── server/
│   ├── connectors/
│   ├── ml/
│   ├── services/
│   ├── app.js
│   ├── auth.js
│   ├── db.js
│   ├── detections.js
│   ├── simulation.js
│   ├── telemetry.js
│   └── index.js
│
├── src/
│   ├── components/
│   ├── data/
│   ├── lib/
│   ├── state/
│   └── App.jsx
│
├── tests/
│
├── .env.example
├── .gitignore
├── DEPLOY-RENDER.md
├── DEPLOY-VERCEL.md
├── package.json
├── README.md
├── render.yaml
├── vercel.json
└── vite.config.js
```

---

## ⚙️ Installation & Setup

### Prerequisites

Install the following:

- Node.js 24 or newer
- npm
- Git

### Step 1: Clone the Repository

```bash
git clone https://github.com/Subhasree456/CyberTwinAI2026.git
```

### Step 2: Navigate to the Project

```bash
cd CyberTwinAI2026
```

### Step 3: Install Dependencies

```bash
npm ci
```

### Step 4: Configure Environment Variables

Create your local environment file:

**Windows PowerShell:**

```powershell
Copy-Item .env.example .env
```

**Linux / macOS:**

```bash
cp .env.example .env
```

Update `.env` with your local configuration.

For a local development environment, configure a strong, unique demo password:

```env
NODE_ENV=development
SEED_DEMO_USERS=true
DEMO_PASSWORD=your-strong-local-demo-password
```

Never commit your actual `.env` file or publish real API keys, passwords, or access tokens.

### Step 5: Start the Application

```bash
npm run dev
```

The application starts the frontend and backend.

| Service | Local URL |
|---|---|
| Frontend | http://localhost:5173 |
| Backend API | http://127.0.0.1:8787 |
| Health Check | http://127.0.0.1:8787/api/health |

The SQLite database is initialized automatically on the first startup.

---

## 🧪 Testing

The project includes automated unit, API, and end-to-end tests.

Run unit and API tests:

```bash
npm test
```

Run end-to-end tests:

```bash
npm run build
npm run test:e2e
```

Run the CI checks:

```bash
npm run ci
```

The automated test suite covers authentication, RBAC, anomaly detection, telemetry ingestion, attack simulations, connectors, and application workflows.

---

## 🔐 Security & Responsible Use

Security is a core design consideration.

The platform includes:

- Password hashing.
- Secure session management.
- Role-based permissions.
- Request validation.
- Rate limiting.
- Security headers.
- Audit logging.
- Workspace-level data isolation.
- Approval-based incident response.

**Important limitations:**

- Built-in attack simulations generate synthetic events and do not attack real systems.
- Network monitoring requires authorized sensors and configured telemetry sources.
- External SIEM/EDR integrations require valid credentials.
- The ML model identifies statistical anomalies; an anomaly is not proof of compromise.
- Production deployments require appropriate persistent storage and security configuration.
- Vercel's temporary SQLite storage is intended only for disposable previews, not durable production data.

Use this platform only in environments you own or are explicitly authorized to monitor and test.

---

## 🚀 Deployment

Deployment configuration is included for:

### Vercel
See [`DEPLOY-VERCEL.md`](DEPLOY-VERCEL.md).

### Render
See [`DEPLOY-RENDER.md`](DEPLOY-RENDER.md).

**Note:** For persistent application data, use an appropriate persistent deployment configuration. The included SQLite database is designed for a single-instance deployment.

---

## 🎯 Project Objectives

1. Build a digital twin environment for cybersecurity simulation.
2. Improve threat visibility through centralized telemetry monitoring.
3. Apply Machine Learning to identify unusual security behavior.
4. Enable AI-assisted security investigation.
5. Integrate external security monitoring platforms.
6. Support controlled and auditable incident response workflows.
7. Demonstrate how modern AI and cybersecurity technologies can work together.

---

## 🔮 Future Enhancements

- Advanced predictive threat analytics.
- More intelligent attack-path visualization.
- Improved AI-based root cause analysis.
- Expanded threat intelligence integrations.
- PostgreSQL and Redis support for scalable deployments.
- Multi-factor authentication.
- Advanced security reporting.
- Enhanced automated incident correlation.

---

## 👩‍💻 Developer

**Subhasree**

GitHub: [@Subhasree456](https://github.com/Subhasree456)

Project Repository: [CyberTwinAI2026](https://github.com/Subhasree456/CyberTwinAI2026)

---

## 📜 License

Add an appropriate open-source license before distributing this project. Until a license is added, the repository's source code remains subject to the default copyright rules.

---

### ⭐ Support

If you find this project interesting, consider giving the repository a star!

**Digital Twin Cyber War – HUNTER AI**

*Simulate. Detect. Investigate. Defend.*
