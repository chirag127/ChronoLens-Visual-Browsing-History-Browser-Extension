# Security Policy for ChronoLens-Visual-Browsing-History-Browser-Extension

As the **Apex Technical Authority**, security is treated as a first-class citizen, adhering to the principle of 'Security by Design' mandated for all high-velocity projects.

This repository follows the **Zero-Defect** philosophy. All dependencies are rigorously vetted during the CI/CD pipeline (`.github/workflows/ci.yml`).

## 1. Supported Versions

This project is actively maintained and actively monitored. We support the latest stable release of the core components:

*   **Browser Extension API:** Latest stable Manifest V3 compliance.
*   **Runtime Environment:** Current Node.js LTS (as of December 2025).
*   **Frontend Stack:** TypeScript, Vite, React/Preact (as appropriate).

## 2. Vulnerability Reporting

We welcome responsible disclosure of security vulnerabilities. We treat all security reports with the highest priority.

If you discover a security vulnerability, please follow these steps:

1.  **Do NOT** create a public GitHub Issue.
2.  Email the dedicated security channel immediately: `security@apex-architect.io` (Placeholder for security contact).
3.  Describe the vulnerability in detail, including:
    *   Affected component(s) and version(s).
    *   Steps to reproduce the exploit.
    *   Any proof-of-concept (PoC) code (preferably in a secure, encrypted format if necessary).

We aim to acknowledge receipt of all reports within **48 hours** and provide a timeline for resolution.

## 3. Security Audits and Practices

### Dependency Scanning

The CI/CD pipeline (`ci.yml`) automatically executes dependency scanning tools to check for known vulnerabilities in npm packages. Any build failure due to a high-severity vulnerability will halt merging to the main branch.

### Data Handling and Privacy

Given this project handles sensitive browsing history data, strict adherence to privacy principles is non-negotiable:

*   **Data Minimization:** Only necessary metadata required for the visual timeline feature is collected.
*   **Local Processing Preference:** The architecture prioritizes local browser storage or secure, ephemeral backend processing where feasible. Any transmission of history data requires explicit user consent and secure, encrypted channels (TLS 1.3+).
*   **OWASP Top 10 Awareness:** Code reviews explicitly check for common web vulnerabilities (XSS, CSRF) related to any potential extension service workers or background scripts.

## 4. Disclosure Timeline (Best Effort)

| Severity | Target Response Time | Target Fix Time (If Confirmed) |
| :--- | :--- | :--- |
| Critical | 12 Hours | 7 Days |
| High | 24 Hours | 14 Days |
| Medium | 3 Days | 30 Days |
| Low | 5 Days | Best Effort in Next Release |

--- 

*This security policy is subject to revision in line with evolving threat landscapes and best practices dictated by the Apex Technical Authority framework.*