# Security Policy for ChronoLens

## 1. Our Commitment to Security

At ChronoLens, we consider the security and privacy of our users to be paramount. Our architecture is designed with a **privacy-first** approach, ensuring that your browsing data remains under your control. This document outlines our security policies, best practices, and the procedure for reporting vulnerabilities.

## 2. Supported Versions

Security updates are applied only to the most recent major version of ChronoLens available on the official Chrome and Firefox extension marketplaces.

| Version | Supported          |
| ------- | ------------------ |
| `1.x.x` | :white_check_mark: |

## 3. Reporting a Vulnerability

We take all security reports seriously. If you discover a potential security vulnerability, we ask that you help us by reporting it privately and responsibly.

**Please do not disclose the vulnerability publicly until it has been resolved.**

### How to Report

1.  **Primary Method:** Use GitHub's **Private Vulnerability Reporting** feature. This is the fastest and most secure way to reach us.
    -   [**Submit a new private report**](https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/security/advisories/new)

2.  **Report Details:** Please include the following information in your report:
    -   A clear and descriptive title.
    -   A detailed description of the vulnerability.
    -   Step-by-step instructions to reproduce the issue.
    -   The version of the extension and the browser you are using.
    -   Any proof-of-concept code, screenshots, or logs that demonstrate the vulnerability.

### Our Commitment to You

-   We will acknowledge receipt of your report within **48 hours**.
-   We will provide a status update on the investigation within **5 business days**.
-   We will work diligently to validate, patch, and release an update to address the vulnerability.
-   We will publicly credit you for your discovery (if you wish) once the vulnerability has been resolved.

## 4. Core Security Principles

-   **Privacy-First Architecture:** All user data, including captured screenshots and browsing history metadata, is processed and stored **exclusively on the user's local machine**. No user-generated data is ever transmitted to or stored on any external servers.

-   **Principle of Least Privilege:** The extension is designed to request the absolute minimum set of browser permissions required for its core functionality (e.g., accessing active tabs, history, and local storage).

-   **Dependency Management:** We use GitHub Dependabot and `npm audit` to proactively monitor our third-party dependencies for known vulnerabilities and apply patches in a timely manner.

-   **Secure Coding Practices:** Our codebase is regularly linted and reviewed to adhere to modern security standards for web extensions, including protection against Cross-Site Scripting (XSS) and other common web vulnerabilities.

## 5. Safe Usage Recommendations

-   **Official Sources Only:** Only install ChronoLens from the official Chrome Web Store or the Firefox Browser Add-ons marketplace.
-   **Keep Updated:** Ensure both your web browser and the ChronoLens extension are always updated to the latest version to receive the latest security patches.