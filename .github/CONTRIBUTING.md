# 🤝 Contribution Guidelines for ChronoLens-Visual-Browsing-History-Browser-Extension

As the Apex Technical Authority mandates, contributions to this repository must adhere to the highest standards of engineering discipline, architectural purity, and velocity. We enforce **Zero-Defect** quality.

This project is built using a modern **TypeScript/React/Vite/TailwindCSS** stack for the frontend extension layer, orchestrated via **Node.js** services where necessary. All contributions must respect the **Feature-Sliced Design (FSD)** pattern.

## 1. Code of Conduct

This project adheres to the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md). We expect all participants to maintain a professional, welcoming, and constructive environment.

## 2. The Apex Contribution Workflow

We utilize a strict Git Flow model optimized for high-velocity integration. All work must pass automated checks before manual review.

### A. Setup and Environment

1.  **Fork:** Fork this repository to your personal GitHub account.
2.  **Clone:** Clone your fork locally:
    bash
    git clone https://github.com/YOUR_USERNAME/ChronoLens-Visual-Browsing-History-Browser-Extension.git
    cd ChronoLens-Visual-Browsing-History-Browser-Extension
    
3.  **Install Dependencies:** We use `npm` for managing the TypeScript/Node ecosystem.
    bash
    npm install
    
4.  **Feature Branching:** Create a dedicated feature branch off `main` using the standardized prefix:
    bash
    git checkout -b feat/your-descriptive-feature-name
    # or for fixes:
    git checkout -b fix/issue-number-short-description
    

### B. Development & Verification

Before committing, ensure your changes pass local verification checks as defined in the `ci.yml` workflow.

1.  **Linting & Formatting (Biome):** Enforce code style immediately.
    bash
    npm run lint -- --fix
    
2.  **Unit Testing (Vitest):** Run all unit tests for affected modules.
    bash
    npm run test:unit
    
3.  **End-to-End Checks (Playwright):** Verify critical user flows are intact.
    bash
    npm run test:e2e
    

### C. Commit and Pull Request (PR)

1.  **Atomic Commits:** Commit changes in small, logical chunks. Each commit message must adhere to the **Conventional Commits** specification (e.g., `feat: add new history filtering API`, `fix: resolve memory leak in background script`).
2.  **Push:** Push your feature branch to your fork.
3.  **Open PR:** Open a Pull Request against `chirag127:main`.

**PR Template Usage:** You **MUST** use the provided `PULL_REQUEST_TEMPLATE.md` to detail the changes, architectural impact, and testing performed.

## 3. Architectural Alignment Directives

All new code must align with the 2026 Architectural Standards:

*   **TypeScript Strictness:** All new TypeScript files must utilize the strictest possible configuration (`tsconfig.json`). Errors are bugs.
*   **Feature-Sliced Design (FSD):** Organize code logically into `features/`, `entities/`, `shared/`, and `pages/` where applicable within the extension structure. Avoid deep nesting in shared utilities.
*   **Immutability & Purity:** Favor pure functions and immutable state management (Redux Toolkit/Zustand patterns). Side effects must be explicitly managed in dedicated boundary layers.
*   **Privacy by Design:** Given this is a history tool, any data handling, storage, or network calls **MUST** be transparently documented in the PR. Prefer local storage or encrypted storage over external services unless absolutely necessary and approved.

## 4. Reporting Issues and Security

*   **Bugs/Features:** Please use the provided issue templates (`.github/ISSUE_TEMPLATE/bug_report.md`) for all bug reports or feature requests.
*   **Security Vulnerabilities:** Report all security concerns privately following the guidelines in `.github/SECURITY.md`. **Do not** open public issues for security flaws.

## 5. Repository Metadata Standards

Contributors are encouraged to report inaccuracies in the project metadata:

*   **Topics:** Ensure topics accurately reflect the technology (e.g., `typescript`, `vite`, `tailwind-css`).
*   **License:** All contributions fall under the **CC BY-NC 4.0** license. By contributing, you agree to license your submission under these terms.

Thank you for contributing to the Apex standard of software engineering.