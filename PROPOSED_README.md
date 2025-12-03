<p align="center">
  <img src="https://raw.githubusercontent.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/main/.github/assets/chronolens-hero-banner.png" alt="ChronoLens Hero Banner" width="800">
</p>

<p align="center">
  <a href="https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/actions/workflows/ci.yml">
    <img src="https://img.shields.io/github/actions/workflow/status/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/ci.yml?branch=main&style=flat-square&label=Build%20Status" alt="Build Status">
  </a>
  <a href="https://codecov.io/gh/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension">
    <img src="https://img.shields.io/codecov/c/github/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension?style=flat-square&token=YOUR_CODECOV_TOKEN_HERE" alt="Code Coverage">
  </a>
  <a href="https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension">
    <img src="https://img.shields.io/badge/Tech%20Stack-TS%20%7C%20React%20%7C%20Vite%20%7C%20WXT%20%7C%20TailwindCSS-blueviolet?style=flat-square" alt="Tech Stack">
  </a>
  <a href="https://biomejs.dev/">
    <img src="https://img.shields.io/badge/Lint%2FFmt-Biome-38C538?style=flat-square" alt="Lint/Format">
  </a>
  <a href="https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey?style=flat-square" alt="License">
  </a>
  <a href="https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/stargazers">
    <img src="https://img.shields.io/github/stars/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension?style=flat-square&color=orange" alt="GitHub Stars">
  </a>
</p>

<p align="center">
  ⭐ Star this Repo! ⭐
</p>

## ChronoLens: Visual Browsing History Browser Extension

ChronoLens visually transforms your browsing history into an interactive, searchable timeline of screenshots, empowering you to rediscover and manage your digital journey with unparalleled ease and privacy. It's a cutting-edge productivity tool designed for Chrome and Firefox, meticulously crafted to enhance your web exploration experience.

## 🚀 Features

*   **Visual History Timeline:** Browse your past sessions with high-fidelity page screenshots.
*   **Intelligent Search:** Effortlessly find specific moments or content within your history.
*   **Privacy-First Design:** Local storage and optional encryption ensure your data remains yours.
*   **Cross-Browser Compatibility:** Seamlessly integrates with Chrome and Firefox.
*   **Interactive Snapshots:** Click on any screenshot to revisit the exact page state.
*   **Resource Management:** Configurable history retention and storage limits.

## 🏗️ Architecture: Feature-Sliced Design (FSD)

ChronoLens adheres to the Feature-Sliced Design (FSD) methodology, ensuring a scalable, maintainable, and highly organized codebase. This modular approach segregates application logic into distinct layers, promoting clear responsibilities and reducing coupling.

mermaid
graph TD
    A[App: Root of the application] --> P(Pages: Full-page components, routing)
    A --> W(Widgets: Independent, reusable UI blocks)
    A --> F(Features: Business logic, complex interactions)
    A --> E(Entities: Data models, API clients)
    A --> S(Shared: Utilities, constants, UI kit)
    P --> F
    W --> F
    F --> E
    E --> S
    W --> S
    F --> S
    style A fill:#f9f,stroke:#333,stroke-width:2px
    style P fill:#bbf,stroke:#333,stroke-width:2px
    style W fill:#bfb,stroke:#333,stroke-width:2px
    style F fill:#fbb,stroke:#333,stroke-width:2px
    style E fill:#ffb,stroke:#333,stroke-width:2px
    style S fill:#cff,stroke:#333,stroke-width:2px


## 📖 Table of Contents

-   [ChronoLens: Visual Browsing History Browser Extension](#chronolens-visual-browsing-history-browser-extension)
-   [🚀 Features](#-features)
-   [🏗️ Architecture: Feature-Sliced Design (FSD)](#%EF%B8%8F-architecture-feature-sliced-design-fsd)
-   [📖 Table of Contents](#-table-of-contents)
-   [🤖 AI Agent Directives](#-ai-agent-directives)
-   [⚙️ Getting Started](#%EF%B8%8F-getting-started)
    -   [Prerequisites](#prerequisites)
    -   [Installation](#installation)
    -   [Development Scripts](#development-scripts)
-   [🤝 Contributing](#-contributing)
-   [🛡️ Security](#%EF%B8%8F-security)
-   [📜 License](#-license)

<details>
<summary><h2>🤖 AI Agent Directives</h2></summary>

# SYSTEM: APEX TECHNICAL AUTHORITY & ELITE ARCHITECT (DECEMBER 2025 EDITION)

## 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
**Context:** Current Date is **December 2025**. You are building for the 2026 standard.
**Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

---

## 2. INPUT PROCESSING & COGNITION
*   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **MANDATORY MCP INSTRUMENTATION:**
    *   **No Guessing:** Do not hallucinate APIs.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends**.
    *   **Validation:** Use `docfork` to verify *every* external API signature.
    *   **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

---

## 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**Directives:** This project, `ChronoLens-Visual-Browsing-History-Browser-Extension`, is a browser extension. It adheres to the **WEB / APP / EXTENSION** scenario.

*   **PRIMARY SCENARIO: WEB / APP / EXTENSION (TypeScript)**
    *   **Stack:** This project leverages **TypeScript 6.x (Strict)**, **React 19+**, and **Vite 7** with **WXT** for robust browser extension development. **TailwindCSS v4 (JIT mode)** is used for highly efficient and scalable styling.
    *   **Architecture:** Adheres strictly to the **Feature-Sliced Design (FSD)** methodology, ensuring clear separation of concerns across app, pages, widgets, features, entities, and shared layers. This promotes maintainability, scalability, and testability.
    *   **Linting/Formatting:** Utilizes **Biome** for lightning-fast and opinionated code quality enforcement, covering both linting and formatting to ensure consistent code standards.
    *   **Testing:** Employs **Vitest** for rapid unit and integration tests, and **Playwright** for robust end-to-end testing across various browser environments (Chrome, Firefox, Edge) to ensure cross-browser compatibility and functionality.
    *   **Platform-Specifics:** Leverages **WebExtensions API** through WXT for seamless cross-browser compatibility, abstracting away differences between browser implementations.
    *   **Data Persistence:** Utilizes browser's local storage (and potentially IndexedDB for larger data sets) following privacy-first best practices.

*   **SECONDARY SCENARIO B: SYSTEMS / PERFORMANCE (Rust/Go) - *Not applicable for this project's primary function. Reference only for potential future native integrations.***

*   **SECONDARY SCENARIO C: DATA / AI / SCRIPTS (Python) - *Not applicable for this project's primary function. Reference only for potential future backend AI services.***

---

## 4. CODE QUALITY & STANDARDS (DECEMBER 2025)
*   **TEST COVERAGE:** Minimum **90% unit test coverage**. No exceptions. Utilize Vitest for all unit and integration tests. Playwright for E2E.
*   **LINTING/FORMATTING:** **Biome** must pass with zero warnings or errors. Hooks `pre-commit` and `pre-push` are mandatory.
*   **TYPING:** **TypeScript `strict` mode** must be enforced. No `any` types without explicit justification via `@ts-expect-error` or `@ts-ignore` with a detailed comment.
*   **DEPENDENCY MANAGEMENT:** **pnpm** is the mandated package manager for superior performance and strict dependency resolution. All dependencies must be current, with no known high-severity CVEs.
*   **API DESIGN:** All internal and external API interactions must follow **SOLID principles**. External APIs (e.g., WebExtensions) must have robust error handling, retry mechanisms, and graceful degradation.
*   **ERROR HANDLING:** Comprehensive error logging and user-friendly error messages are required. Sentry.io integration is recommended for production environments.
*   **PERFORMANCE:** Bundle size optimization with Vite, lazy loading for heavy components/features, and efficient use of browser storage mechanisms.
*   **ACCESSIBILITY (A11y):** All UI components must conform to WCAG 2.1 AA standards.
*   **SECURITY:** Adhere to OWASP Top 10 for browser extensions. Content Security Policy (CSP) enforcement. Data encryption for sensitive user data even in local storage.

---

## 5. VERIFICATION COMMANDS

To verify the system's integrity and performance:

bash
pnpm install
pnpm lint
pnpm typecheck
pnpm test:unit
pnpm test:e2e
pnpm build


</details>

## ⚙️ Getting Started

Follow these steps to set up and run ChronoLens locally.

### Prerequisites

Before you begin, ensure you have the following installed:

*   [Node.js](https://nodejs.org/en/download/) (v18.x or higher)
*   [pnpm](https://pnpm.io/installation/) (v8.x or higher)
*   A modern web browser (Chrome, Firefox, or Edge)

### Installation

1.  **Clone the repository:**

    bash
    git clone https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension.git
    cd ChronoLens-Visual-Browsing-History-Browser-Extension
    

2.  **Install dependencies:**

    bash
    pnpm install
    

3.  **Build the extension for development:**

    bash
    pnpm dev
    

    This will build the extension into the `dist` directory and watch for changes.

4.  **Load the extension in your browser:**

    *   **Chrome:**
        1.  Open Chrome and navigate to `chrome://extensions`.
        2.  Enable "Developer mode" in the top right corner.
        3.  Click "Load unpacked" and select the `dist` directory within your cloned repository.
    *   **Firefox:**
        1.  Open Firefox and navigate to `about:debugging#/runtime/this-firefox`.
        2.  Click "Load Temporary Add-on..." and select any file within the `dist` directory (e.g., `dist/manifest.json`).

### Development Scripts

| Script          | Description                                             |
| :-------------- | :------------------------------------------------------ |
| `pnpm dev`      | Starts the development server with hot-reloading.       |
| `pnpm build`    | Compiles the extension for production.                  |
| `pnpm lint`     | Runs Biome linter and formatter.                        |
| `pnpm typecheck`| Checks TypeScript types.                                |
| `pnpm test:unit`| Runs Vitest unit and integration tests.                 |
| `pnpm test:e2e` | Runs Playwright end-to-end tests across browsers.       |
| `pnpm test`     | Runs all tests (`unit` and `e2e`).                      |
| `pnpm format`   | Formats the codebase using Biome.                       |

## 🤝 Contributing

We welcome contributions to ChronoLens! Please read our [Contributing Guidelines](https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/blob/main/.github/CONTRIBUTING.md) to get started.

## 🛡️ Security

For information on security vulnerabilities and how to report them, please refer to our [Security Policy](https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/blob/main/.github/SECURITY.md).

## 📜 License

ChronoLens is distributed under the [CC BY-NC 4.0 License](https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/blob/main/LICENSE). See the `LICENSE` file for more details.