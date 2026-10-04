# 🛡️ SURAKSHA AI — Public Safety & Justice Intelligence Platform

> **Report. Connect. Investigate. Protect.**  
> *Responsible AI for safer communities and smarter case intelligence.*

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![React 18](https://img.shields.io/badge/Frontend-React_18_%7C_TypeScript-1677FF.svg)](https://react.dev/)
[![Vite](https://img.shields.io/badge/Bundler-Vite_8-646CFF.svg)](https://vitejs.dev/)
[![Responsible AI](https://img.shields.io/badge/Framework-Responsible_AI-22C55E.svg)](#-responsible-ai-principles)
[![Hackathon Prototype](https://img.shields.io/badge/Status-Hackathon_Winner_Prototype-FFB020.svg)](#)

---

## 📌 Executive Summary

**Suraksha AI** is an end-to-end, mission-critical public safety platform designed to bridge common citizens, law enforcement investigators, police command, and judicial benches into a unified, explainable intelligence ecosystem. 

Rather than functioning as a black-box autonomous policing tool, Suraksha AI acts strictly as **human-in-the-loop decision-support software**. It connects fragmented citizen complaints, extracts multi-modal entities, detects spatial-temporal pattern signals, constructs interactive Knowledge Graphs, and powers source-backed RAG copilots with exact paragraph-level document citations.

---

## 🚀 Key Modules & Capabilities

### 1. 📝 Citizen Experience & Multi-Step Incident Reporting
- **Simple Dashboard**: Quick action cards for Emergency SOS, Incident Reporting, Report Tracking, and Safety Hub.
- **5-Step Incident Wizard**: Classification (Stalking, Harassment, Threat, Cybercrime, Fraud, Missing Person), interactive map location picker, date/time, detailed description, multi-modal evidence uploader (PNG, MP4, MP3, PDF), and anonymity toggles.
- **Live AI Extraction Engine**: Encrypts evidence payloads, extracts key entities (`@handles`, vehicle plates, Wi-Fi MACs), and generates instant Case Reference IDs (`#SA-10428`).

### 2. 👁️ Investigator Command Center
- **Tactical Dark Map**: Leaflet-style dark canvas with pulsing radar incident signals (🔴 Critical, 🟠 Pattern Signal, 🔵 Citizen Report).
- **Interactive Knowledge Graph Mesh**: D3/SVG node-link visualizer mapping persons, cases, digital handles, IP routers, vehicles, and evidence files. Includes click-to-explain relationship sidebar.
- **Suraksha Copilot (RAG)**: Case-contextual AI assistant delivering answers backed strictly by confidence scores, document paragraph citations, and *"View Source"* popovers.
- **Case Timeline Engine**: Milestone cards linked directly to verified forensic evidence files.

### 3. 🗃️ Criminal Data Record & Warrant Registry Portal
- **State Offender Index**: Search by Name, Alias (*"Vicky Ghost"*), Record ID (`CR-8092`), FIR Number, or Court Case Reference.
- **Warrant Status Badges**: Filter by `Warrant Issued` (High Alert), `Prior Offender Record`, or `Under Investigation`.
- **Biometric SHA-256 Hashes**: Cryptographic identity verification tags.
- **Cross-Case Association**: Single-click cross-referencing between offender records and active investigative cases.

### 4. ⚖️ Judicial Support Workspace
- **Courtroom Bench**: Source-backed case chronology table.
- **Digital Chain of Custody**: Cryptographic SHA-256 hash verification for evidence integrity.
- **Paragraph Reader**: Direct page and paragraph citations to original sworn witness statements & cyber forensic logs (*Doc DOC-104 · Page 4 · Paragraph 2*).

### 5. 🛡️ SURAKSHA Women Safety Center
- **One-Touch Emergency SOS**: Prominent 1-click alert dispatch broadcasting live location to emergency services and trusted contacts.
- **Safety Check-In Timer**: Active countdown timer with automatic alert dispatch if unconfirmed.
- **Trusted Contacts Circle**: Add/manage emergency contact numbers.
- **Safe Hub Locator**: Interactive map locator for nearby Pink Police Booths & 24/7 Shelters.

### 6. 🔒 Responsible AI & Governance Center
- **Decision-Support Lifecycle**: 6-step explainable AI workflow visualizer.
- **Immutable System Audit Log**: Real-time audit log stream tracking every case view, Copilot execution, and document inspection with actor metadata and access justifications.
- **Global Command Palette**: `Cmd+K` / `Ctrl+K` keyboard shortcut for instant cross-platform search.

---

## ⚖️ Responsible AI Principles

Suraksha AI adheres strictly to the following guardrails:
- ❌ **No Autonomous Guilt Assignment**: The system NEVER declares someone guilty, predicts criminal probability, or suggests automated punishment.
- ❌ **No Black-Box AI**: Every AI output provides explicit explanation, supporting source references, and confidence metrics.
- ✅ **Objective Terminology**: Uses *"Safety Signal"*, *"Potentially Related Incident"*, *"Spatial-Temporal Cluster"*, and *"Requires Human Review"*.
- ✅ **Privacy by Design**: Anonymous reporting support and strict role-based access control (RBAC).

---

## 💻 Tech Stack

- **Frontend Framework**: React 18 + TypeScript + Vite 8
- **Styling & Design Token System**: Vanilla CSS + Tailwind CSS utilities with a custom Deep Space Navy Command Center theme (`#07111F`, `#0D1B2A`, `#16263B`)
- **Icons**: Lucide React
- **Mapping**: Leaflet / Custom Tactical Dark Canvas
- **Knowledge Graph**: Interactive SVG Node-Link Canvas Engine
- **Mock RAG Engine**: Simulated retrieval service with document paragraph citation parser

---

## 📂 Project Directory Structure

```text
suraksha-ai/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── citizen/
│   │   │   ├── CitizenPortal.tsx       # Citizen Dashboard & Report Tracking
│   │   │   └── IncidentWizard.tsx      # 5-step incident reporter & AI extraction
│   │   ├── command-center/
│   │   │   ├── CommandCenter.tsx       # Master Investigator Command Center
│   │   │   ├── IncidentMap.tsx         # Tactical Dark Map with radar signals
│   │   │   ├── KnowledgeGraph.tsx      # Interactive SVG Entity Graph Mesh
│   │   │   └── SurakshaCopilotModal.tsx# RAG Assistant with paragraph citations
│   │   ├── criminal-records/
│   │   │   └── CriminalRecordsPortal.tsx # Offender Registry & Warrant Database
│   │   ├── judicial/
│   │   │   └── JudicialWorkspace.tsx   # Courtroom bench & Chain of Custody
│   │   ├── landing/
│   │   │   └── LandingPage.tsx         # Hero page with interactive pipeline
│   │   ├── layout/
│   │   │   └── Navbar.tsx              # Navigation bar & Role Switcher
│   │   ├── responsible-ai/
│   │   │   └── ResponsibleAIPage.tsx   # AI Governance & Real-time Audit Logs
│   │   └── common/
│   │       └── CommandPaletteModal.tsx # Cmd+K Search dialog
│   ├── mock/
│   │   └── syntheticData.ts            # Connected demo dataset (Cases, Incidents, Graph)
│   ├── services/
│   │   └── copilotService.ts           # RAG retrieval service with source citations
│   ├── styles/
│   │   └── theme.css                   # Navy design tokens & glassmorphism CSS
│   ├── types/
│   │   └── index.ts                    # TypeScript interfaces
│   ├── App.tsx                         # App Shell & Router
│   ├── main.tsx                        # Entry point
│   └── index.css                       # Global styles
├── index.html                          # HTML template
├── package.json                        # NPM dependencies
├── tsconfig.json                       # TypeScript config
└── vite.config.ts                      # Vite configuration
```

---

## ⚡ Quickstart & Installation

### Prerequisites
- [Node.js](https://nodejs.org/) (v18 or higher)
- `npm` or `yarn`

### 1. Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/suraksha-ai.git
cd suraksha-ai
```

### 2. Install dependencies
```bash
npm install
```

### 3. Start development server
```bash
npm run dev
```
Open [`http://localhost:5173/`](http://localhost:5173/) in your browser.

### 4. Build for production
```bash
npm run build
```

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

**SURAKSHA AI** — *Responsible AI for Safer Communities & Smarter Case Intelligence.*
