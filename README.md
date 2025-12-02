<div align="center">
  <h1>InsightLog Visual Timeline Capture Extension</h1>
</div>

<div align="center">
  <a href="https://github.com/chirag127/InsightLog-Visual-Timeline-Capture-Browser-Extension/actions/workflows/ci.yml">
    <img src="https://img.shields.io/github/actions/workflow/status/chirag127/InsightLog-Visual-Timeline-Capture-Browser-Extension/ci.yml?branch=main&style=flat-square&label=Build%20Status&logo=githubactions" alt="Build Status">
  </a>
  <a href="https://codecov.io/gh/chirag127/InsightLog-Visual-Timeline-Capture-Browser-Extension">
    <img src="https://img.shields.io/codecov/c/github/chirag127/InsightLog-Visual-Timeline-Capture-Browser-Extension?style=flat-square&label=Coverage&token=YOUR_TOKEN" alt="Code Coverage">
  </a>
  <img src="https://img.shields.io/badge/Language-JavaScript%20%7C%20Node.js-F7DF1E?style=flat-square&logo=javascript">
  <img src="https://img.shields.io/badge/Linter-Biome-38C764?style=flat-square&logo=biome">
  <img src="https://img.shields.io/badge/License-CC%20BY--NC%204.0-blue.svg?style=flat-square">
  <a href="https://github.com/chirag127/InsightLog-Visual-Timeline-Capture-Browser-Extension/releases">
    <img src="https://img.shields.io/github/v/release/chirag127/InsightLog-Visual-Timeline-Capture-Browser-Extension?style=flat-square&label=Version" alt="Latest Release">
  </a>
  <a href="https://github.com/chirag127/InsightLog-Visual-Timeline-Capture-Browser-Extension">
    <img src="https://img.shields.io/github/stars/chirag127/InsightLog-Visual-Timeline-Capture-Browser-Extension?style=flat-square&label=Stars&color=yellow" alt="GitHub Stars">
  </a>
</div>

<div align="center">
  <a href="https://github.com/chirag127/InsightLog-Visual-Timeline-Capture-Browser-Extension">⭐ Star this Repo</a>
</div>

---

## ⚡ Blazing Fast Context Capture Engine

**InsightLog** is an Apex-tier professional browser extension and self-hosted backend system designed for absolute visual history capture and retrieval. It records continuous, context-aware snapshots of user web activity, securely archiving the data via a dedicated Express/MongoDB backend, transforming fragmented browsing sessions into a searchable, high-fidelity visual timeline.

This project serves as a robust foundation for building advanced digital journey mapping, user research analysis tools, or secure, self-controlled personal history management systems, prioritizing performance, archival integrity, and privacy (through self-hosting).

## 📝 Table of Contents

1.  [Core Feature Set](#-core-feature-set)
2.  [Architecture Overview](#-architecture-overview)
3.  [AI Agent Directives](#-ai-agent-directives-ssot)
4.  [Getting Started](#-getting-started)
5.  [Development Standards](#-development-standards)
6.  [Contributing](#-contributing)
7.  [License](#-license)

---

## ✨ Core Feature Set

InsightLog is engineered for reliability and deep visual context capture:

*   **High-Fidelity Snapshotting:** Automatically triggers background capture of the active viewport based on configurable intervals or significant DOM changes.
*   **Serverless Manifest V3 Architecture:** Utilizes modern extension standards for performance, minimal footprint, and efficient background worker management.
*   **Self-Hosted Archival:** Leverages a dedicated Node.js (Express) API layer to interface with MongoDB, guaranteeing data sovereignty and scalability for massive history archives.
*   **Visual Retrieval Dashboard:** Provides a separate client interface (not included in the core extension, but supported by the backend API) for browsing the timeline, performing semantic searches, and revisiting captured states.
*   **Data Integrity:** Implements robust queuing mechanisms to ensure capture events are reliably transmitted to the backend, even during brief network interruptions.

## 🏗️ Architecture Overview

This system follows a hybrid Client-Server architecture tailored for extension-to-service communication.

mermaid
C4Context

  Person(user, "Web User", "Interacts with the Browser.")

  System(ext, "InsightLog Browser Extension", "Manifest V3 extension managing visual capture and data transmission.")
  System(api, "InsightLog Data API", "Node.js/Express Backend handling data ingestion and retrieval.")
  System(db, "MongoDB Archive", "Persistent storage for snapshots, metadata, and timeline indices.")

  Rel(user, ext, "Generates Browsing Activity")
  Rel(ext, api, "Transmits Visual Snapshot Data (REST/WebSockets)", "HTTPS")
  Rel(api, db, "Reads and Writes Timeline Data")
  Rel(api, user, "Provides Searchable Timeline Dashboard (External Client)")

  Container_Boundary(Extension, "Browser Context") {
    Container(background, "Background Worker", "Handles event listeners, API queuing, and orchestration.")
    Container(content, "Content Scripts", "Injects into pages, monitors DOM, and captures viewport data.")
    Container(popup, "Extension UI", "User controls and status display.")
    Rel(popup, background, "Sends Commands")
    Rel(content, background, "Sends Captured Data")
    Rel(background, api, "POST Snapshot Payloads")
  }

  Rel(ext, Extension, "Is composed of")


## 🤖 AI Agent Directives (SSOT)

This repository is governed by the Apex Agent Directives. This block provides immediate context for future automated development agents.

<details>
<summary>Click to view Apex Agent Directives (Node.js/JS Extension Stack)</summary>

### APEX ARCHITECTURAL MANIFEST

**1. Technology Stack Definition:**
*   **Primary Language:** JavaScript (ES2023+).
*   **Runtime:** Node.js (LTS).
*   **Backend Framework:** Express.js.
*   **Database:** MongoDB (using Mongoose for schema definition).
*   **Extension Standard:** Manifest V3 (MV3).
*   **Build/Bundler:** Recommended: Vite/WXT or standard Webpack/Rollup tailored for MV3.

**2. Core Architectural Patterns:**
*   **Modular Monolith:** The backend (`server/`) is structured as a modular monolith, separating concerns into modules (e.g., `capture`, `storage`, `auth`, `api`).
*   **SOLID Principles:** High emphasis on Single Responsibility Principle (SRP) for content scripts and background workers.
*   **Stateless API:** The Express API must remain stateless, relying solely on MongoDB for session and archival persistence.
*   **Async/Await Control:** All asynchronous operations (DB calls, API requests, extension messaging) must be handled using modern `async/await` syntax with robust `try...catch` blocks for error propagation.

**3. Verification & Testing Commands:**
*   **Linter/Formatter:** Biome is the mandated tool for speed and quality.
    bash
    # Enforce formatting and linting rules
    npm run lint:fix
    
*   **Unit Testing:** Vitest is used for front-end extension logic; Supertest is used for backend API integration tests.
    bash
    # Run all tests, including coverage report
    npm run test
    

**4. Security and Privacy Mandates (P0):**
*   All communication between the extension and the self-hosted API MUST be secured (HTTPS/WSS).
*   Input validation (Joi/Zod) is mandatory on all incoming Express routes to prevent injection and malformed data attacks.
*   Sensitive data (user keys, timestamps) must be stored and accessed via encrypted environment variables or secrets management solutions.

**5. Deployment Strategy:**
*   CI/CD pipeline must separately build and package the Extension (ZIP file) and containerize the Backend (Docker image).
</details>

---

## 🚀 Getting Started

This project requires two operational components: the Node.js backend server and the browser extension package.

### Prerequisites

1.  Node.js (LTS version, 18+ recommended)
2.  MongoDB instance (local or cloud-hosted)
3.  `uv` or `npm` (for dependency management)

### 1. Backend Server Setup

bash
# 1. Clone the repository
git clone https://github.com/chirag127/InsightLog-Visual-Timeline-Capture-Browser-Extension.git
cd InsightLog-Visual-Timeline-Capture-Browser-Extension/server

# 2. Install dependencies
npm install

# 3. Configure Environment Variables
# Create a .env file and set your MongoDB URI and API port.
# Example: MONGODB_URI="mongodb://localhost:27017/insightlog_db"
#          API_PORT=3000

# 4. Start the server
npm start
# The API will be running on http://localhost:3000


### 2. Browser Extension Setup

Navigate to the `extension/` directory and build the final distributable package:

bash
cd ../extension
npm install
npm run build

# The compiled extension files will be located in the 'dist' directory.


**Installation in Browser (Chrome/Edge/Firefox):**
1.  Open your browser's extension management page (`chrome://extensions` or equivalent).
2.  Enable Developer Mode.
3.  Click "Load unpacked" and select the `dist` folder generated above.
4.  Ensure the extension's API endpoint setting points to your running backend (`http://localhost:3000`).

## 🛠️ Development Standards

### Available Scripts (Root Level)

| Command | Description | Component |
| :--- | :--- | :--- |
| `npm run start:server` | Starts the Express API server (Development mode). | Server |
| `npm run build:extension` | Compiles the MV3 extension files. | Extension |
| `npm run test` | Executes all unit and integration tests (Vitest/Supertest). | All |
| `npm run lint` | Runs the Biome linter against all JavaScript files. | All |
| `npm run lint:fix` | Automatically formats and fixes linting issues using Biome. | All |

### Core Design Principles

*   **DRY (Don't Repeat Yourself):** Abstract shared functionality, especially API interfaces and storage utilities.
*   **YAGNI (You Aren't Gonna Need It):** Focus development strictly on the core archival and retrieval loop, avoiding feature bloat.
*   **High Performance:** Content scripts must be non-blocking and have minimal impact on page load times. Offload heavy processing to the background worker or the server.

## 🤝 Contributing

Contributions are governed by the guidelines detailed in the [CONTRIBUTING.md](.github/CONTRIBUTING.md) file. All pull requests must pass 100% of the CI/CD checks, including Biome linting and test coverage gates.

## ⚖️ License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** License. See the [LICENSE](LICENSE) file for details.