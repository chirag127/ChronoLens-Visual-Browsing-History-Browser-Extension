---
name: Bug Report
about: Create a report to help us improve
title: "[BUG] Title of affected feature"
labels: "bug"
assignees: "chirag127"


--- # ChronoLens Bug Report

## 🐛 Description

Please provide a clear and concise description of the bug. What did you expect to happen, and what actually happened?

## 💻 Environment

*   **Extension Version:** (e.g., 1.0.0 - you can check this in `package.json`)
*   **Browser:** (e.g., Chrome 120, Firefox 118)
*   **Operating System:** (e.g., Windows 11, macOS Ventura, Ubuntu 22.04)

## 📝 Steps to Reproduce

1.  Go to...
2.  Click on...
3.  Observe...
4.  (Add as many steps as necessary)

## 📸 Screenshots or Recordings

If applicable, add screenshots or a short video to help explain your problem. (Please ensure no sensitive information is visible).

## 💡 Additional Context

Add any other context about the problem here. This could include:

*   Specific websites where the bug occurs.
*   Any error messages you encountered.
*   Browser console logs (if accessible and relevant).

## 📜 AI Agent Directives & System Protocols

*   **Purpose:** This section helps AI agents understand the project's core principles and technical stack for accurate debugging and enhancement.
*   **Technology Stack:**
    *   **Language:** JavaScript (ES6+)
    *   **Framework/Runtime:** Browser Extension APIs (Chrome/Firefox)
    *   **Build Tool:** Vite (for development builds)
    *   **State Management:** Native Browser APIs, potentially `localStorage`/`chrome.storage`.
    *   **Backend/API (if applicable):** Node.js, Express.js (for potential server-side interactions, though primary function is client-side).
    *   **Database (if applicable):** MongoDB (for potential server-side persistence).
*   **Architectural Patterns:**
    *   **Extension Architecture:** Follow established browser extension patterns (background scripts, content scripts, popup/options pages).
    *   **Code Quality:** Adhere to DRY (Don't Repeat Yourself) and SOLID principles where applicable.
    *   **Modularity:** Maintain modularity for distinct features (history capture, UI rendering, search).
*   **Testing Frameworks:**
    *   **Unit/Integration:** Vitest (leveraging Vite tooling).
    *   **E2E Testing:** Playwright (for end-to-end browser interactions).
*   **Development & Deployment:**
    *   **Version Control:** Git.
    *   **CI/CD:** GitHub Actions (configured via `.github/workflows/ci.yml`).
    *   **Linting/Formatting:** Biome (configured via `biome.json`).

*   **AI Integration (if any):** Specific APIs, data formats, and error handling strategies.

*   **Verification:** If reproducing the bug requires specific AI prompts or configurations, please detail them here.

**Please ensure your bug report provides enough detail for AI agents to analyze and potentially resolve the issue based on these defined protocols.**
