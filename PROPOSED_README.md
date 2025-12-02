# ChronoLens-Visual-Browsing-History-Browser-Extension

![Build Status](https://img.shields.io/github/actions/workflow/user/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/ci.yml?style=flat-square&logo=githubactions)
![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension?style=flat-square&logo=codecov)
![Tech Stack](https://img.shields.io/badge/tech-stack-JavaScript-blue?style=flat-square&logo=javascript)
![Linting](https://img.shields.io/badge/linting-Biome-orange?style=flat-square&logo=biome)
![License](https://img.shields.io/badge/license-CC%20BY--NC%204.0-red?style=flat-square&logo=creativecommons)
![GitHub Stars](https://img.shields.io/github/stars/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension?style=flat-square&logo=github)

**Elevate your digital journey with ChronoLens: an intelligent browser extension that transforms your browsing history into a visual, interactive timeline of screenshots.**

**Rediscover your past online activity through an automatically captured, organized, and searchable visual archive.**

## 🏗️ Architecture

mermaid
graph TD
    A[User Browsing] --> B{ChronoLens Extension}
    B --> C[Screenshot Capture Module]
    B --> D[History Storage (Local/Cloud)]
    C --> E[Image Processing]
    D --> F[Timeline Generation]
    F --> G[Search & Visualization UI]
    G --> H[User Interaction]

    subgraph Backend Services
        D
        F
    end

    subgraph Frontend
        B
        C
        G
        H
    end


## 📄 Table of Contents

*   [About ChronoLens](#about-chronolens)
*   [Key Features](#key-features)
*   [Technology Stack](#technology-stack)
*   [Installation](#installation)
*   [Usage](#usage)
*   [Development](#development)
*   [Contributing](#contributing)
*   [License](#license)
*   [Support](#support)

## 💡 About ChronoLens

ChronoLens is a sophisticated browser extension designed to revolutionize how you manage and recall your online explorations. Instead of a simple list of URLs and timestamps, ChronoLens captures the essence of your browsing sessions by taking automatic screenshots of visited pages. These visuals are then meticulously organized into an interactive, searchable timeline, allowing you to intuitively navigate your digital past and retrieve information with unprecedented ease.

## ✨ Key Features

*   **Visual Timeline:** An engaging, chronological display of your browsing history using actual page screenshots.
*   **Automatic Screenshotting:** Seamlessly captures snapshots of visited pages without user intervention.
*   **Intelligent Organization:** Stores and categorizes screenshots for efficient recall.
*   **Powerful Search:** Quickly find past pages and information using keyword searches across historical data.
*   **Cross-Browser Compatibility:** Designed to work across major browsers (Chrome, Firefox, etc.).
*   **Privacy-Focused:** Options for local storage or secure cloud synchronization, prioritizing user privacy.

## 🚀 Technology Stack

*   **Core Language:** JavaScript (ES6+)
*   **Extension Framework:** WebExtension API (compatible with Chrome, Firefox, Edge)
*   **Build Tool:** Vite (for fast development builds and optimized production output)
*   **UI Styling:** Tailwind CSS (for rapid, utility-first UI development)
*   **State Management:** (TBD - e.g., Context API, Zustand, or Signals if integrated with a framework like React/Vue)
*   **Storage:** WebExtensions Storage API (local), potentially IndexedDB for larger datasets.
*   **Optional Backend (for Cloud Sync):** Node.js, Express.js, MongoDB (for cloud-based history synchronization and advanced features).

## 📦 Installation

**For Development:**

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension.git
    cd ChronoLens-Visual-Browsing-History-Browser-Extension
    

2.  **Install dependencies:**
    bash
    npm install
    

3.  **Build the extension for development:**
    bash
    npm run dev
    

4.  **Load the extension in your browser:**
    *   **Chrome/Edge:** Go to `chrome://extensions` or `edge://extensions`, enable Developer Mode, and click "Load unpacked" pointing to the `dist` or `build` folder.
    *   **Firefox:** Go to `about:debugging#/runtime/this-firefox`, click "Load Temporary Add-on", and select the `manifest.json` file.

**For Production (Future):**

*   Packages will be available via browser web stores (Chrome Web Store, Firefox Add-ons).

## ▶️ Usage

*   Once installed, the ChronoLens icon will appear in your browser's toolbar.
*   Click the icon to open the visual timeline interface.
*   Browse the web as usual; ChronoLens will automatically capture screenshots.
*   Use the search bar to find specific past browsing sessions or content.

## 🛠️ Development

*   **Development Server:** Run `npm run dev` for a live-reloading development environment.
*   **Production Build:** Run `npm run build` to create optimized production assets.
*   **Linting & Formatting:** Use `npm run lint` and `npm run format` to maintain code quality. The project uses Biome for linting and formatting.

### 🧪 Testing

*   **Unit Tests:** Run `npm run test:unit` to execute unit tests using Vitest.
*   **End-to-End (E2E) Tests:** Run `npm run test:e2e` to execute E2E tests using Playwright.

## 🤝 Contributing

We welcome contributions! Please refer to our [CONTRIBUTING.md](https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/blob/main/.github/CONTRIBUTING.md) file for detailed guidelines on how to submit your ideas, bug reports, and pull requests.

## ⚖️ License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license. See the [LICENSE](https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/blob/main/LICENSE) file for more details.

## 💖 Support

If you encounter any issues or have suggestions, please open an issue on our GitHub repository.

---

<details>
<summary>🤖 AI Agent Directives & Tech Stack Definition (December 2025)</summary>

### 🚀 Mission Statement

You are an **Apex Technical Authority** operating with the precision of a Senior Principal Architect. Your prime directive is to ensure this repository adheres to **FAANG-level standards**, implements **Zero-Defect, High-Velocity, Future-Proof** principles, and embodies the wisdom of "Managing the Unmanageable." You prioritize clarity, efficiency, and robust architecture.

### 🎯 Core Principles

*   **SOLID:** Maintain robust, maintainable, and scalable code.
*   **DRY:** Avoid redundant code; strive for reusability.
*   **YAGNI:** "You Ain't Gonna Need It" - build only what is necessary now.
*   **KISS:** "Keep It Simple, Stupid" - favor simplicity over complexity.
*   **Convention over Configuration:** Adhere to established patterns and standards.

### 💻 Technology Stack (Apex Standard - Late 2025)

This repository is built using the following stack, designed for performance, maintainability, and developer velocity:

*   **Language:** JavaScript (ES6+)
*   **Extension Framework:** WebExtension API
*   **Build Tool:** Vite 7.x (with Rolldown integration for performance)
*   **UI Framework/Library:** N/A (Utility-first with Tailwind CSS)
*   **Styling:** Tailwind CSS v4.x
*   **State Management:** Standardized Signals (if integrated with a framework), or Context API/Zustand for pure JS.
*   **Linting & Formatting:** Biome 1.x (Ensures code quality and consistency with extreme speed).
*   **Testing Frameworks:**
    *   **Unit Testing:** Vitest 1.x (Fast, Vite-native unit testing).
    *   **End-to-End (E2E) Testing:** Playwright 1.x (Robust browser automation for E2E scenarios).
*   **Package Manager:** npm 10.x (or Yarn 4.x)
*   **Optional Cloud Sync Backend:** Node.js 20.x, Express.js 5.x, MongoDB 7.x (for advanced features requiring server-side processing and storage).

### ⚙️ Architectural Patterns

*   **Extension Architecture:** Adheres to the WebExtension API lifecycle and best practices. Modules are designed for clear separation of concerns (e.g., content scripts, background scripts, popup UI).
*   **UI Design:** Component-based approach utilizing Tailwind CSS for rapid UI development, ensuring responsiveness and aesthetic consistency.
*   **Data Management:** Leverages browser's native storage APIs (e.g., `chrome.storage` or `browser.storage`) for local persistence. IndexedDB may be employed for larger datasets. Cloud synchronization utilizes a defined API contract with a Node.js/Express backend.

### ✅ Verification Commands

*   **Install Dependencies:** `npm install`
*   **Run Linters & Formatters:** `npm run lint`, `npm run format`
*   **Run Unit Tests:** `npm run test:unit`
*   **Run E2E Tests:** `npm run test:e2e`
*   **Start Development Server:** `npm run dev`
*   **Build Production:** `npm run build`

### 🧠 AI Agent Directives (Execution Flow)

1.  **Analyze Input:** Understand the user's request and the repository's current state.
2.  **Validate Against Apex Standards:** Ensure all code, documentation, and configurations meet the highest industry benchmarks.
3.  **Execute Tasks:** Perform requested actions (e.g., code generation, refactoring, documentation updates) with zero hesitation.
4.  **Prioritize & Optimize:** Focus on high-impact changes that improve performance, security, and maintainability.
5.  **Maintain State:** Ensure all generated content is consistent and reflects the current state of the repository.
6.  **Report (Implicitly):** The output JSON represents the executed state. No explicit verbose reporting is required.

</details>

---

<details>
<summary>⭐ Star ⭐ this Repo!</summary>

If you find ChronoLens valuable, please consider starring this repository to show your support and help it gain visibility!

</details>
