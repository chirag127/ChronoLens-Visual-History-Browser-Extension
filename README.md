# ChronoLens-Visual-Browsing-History-Browser-Extension

[![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/ci.yml?style=flat-square&logo=github)](https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/actions/workflows/ci.yml)
[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension?style=flat-square&logo=codecov)](https://codecov.io/gh/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension)
[![Tech Stack](https://img.shields.io/badge/Tech%20Stack-JavaScript%2C%20Node.js%2C%20Express.js%2C%20MongoDB-blue?style=flat-square&logo=javascript)](https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension)
[![License](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgray?style=flat-square&logo=creativecommons)](https://creativecommons.org/licenses/by-nc/4.0/)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension?style=flat-square&logo=github)](https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension/stargazers)

> A browser extension that captures a visual timeline of your browsing history. Automatically screenshots tabs and organizes them into an interactive, searchable history viewer, allowing you to revisit your digital journey.

--- A visually rich, interactive timeline of your digital explorations. ---

## 🚀 Project Overview

ChronoLens transforms your browsing history from a mundane list into a dynamic, visual narrative. By intelligently capturing screenshots of your visited pages, it constructs an interactive timeline that allows you to effortlessly navigate, search, and rediscover your digital journey. Built with modern web technologies and designed for productivity and privacy.

## 🌳 Project Structure

bash
ChronoLens-Visual-Browsing-History-Browser-Extension/
├── src/
│   ├── background/
│   │   ├── background.js          # Core extension logic, event listeners
│   │   └── screenshotService.js   # Handles tab screenshotting
│   ├── content/
│   │   ├── content.js             # Injects into web pages
│   │   └── ui.js                  # Handles UI elements on web pages
│   ├── popup/
│   │   ├── popup.html
│   │   ├── popup.js               # UI logic for the extension popup
│   │   └── popup.css
│   ├── service-worker/
│   │   └── service-worker.js      # For Manifest V3 compatibility
│   ├── utils/
│   │   └── helpers.js             # Common utility functions
│   └── manifest.json              # Extension manifest file
├── api/
│   ├── index.js                   # Express.js server for potential API interactions
│   └── routes/
│       └── history.js
├── config/
│   └── db.js                      # MongoDB connection configuration
├── node_modules/
├── .gitignore
├── .prettierrc.json
├── AGENTS.md
├── CONTRIBUTING.md
├── LICENSE
├── package.json
├── README.md
├── SECURITY.md
├── ISSUE_TEMPLATE/
│   └── bug_report.md
├── PULL_REQUEST_TEMPLATE.md
└── badges.yml


## 🧭 Table of Contents

*   [Project Overview](#-project-overview)
*   [Project Structure](#-project-structure)
*   [Table of Contents](#-table-of-contents)
*   [Core Features](#-core-features)
*   [Technology Stack](#-technology-stack)
*   [Getting Started](#-getting-started)
*   [Development Workflow](#-development-workflow)
*   [Contributing](#-contributing)
*   [License](#-license)
*   [Security](#-security)
*   [🤖 AI Agent Directives](#-ai-agent-directives)

## ✨ Core Features

*   **Visual Timeline:** Auto-captures screenshots of visited pages, creating an interactive timeline.
*   **Intelligent Organization:** Sorts and categorizes history entries based on time, domain, and user-defined tags.
*   **Powerful Search:** Quickly find past browsing sessions or specific pages using keyword and semantic search.
*   **Privacy-Focused:** Designed with user privacy in mind, offering clear control over data capture and storage.
*   **Cross-Browser Compatibility:** Supports Chrome and Firefox (with future plans for others).
*   **Local or Cloud Sync:** Option to store history locally or sync via a secure backend (e.g., MongoDB).

## 🛠️ Technology Stack

*   **Frontend (Extension UI):** Vanilla JavaScript, HTML, CSS.
*   **Background/Service Worker:** JavaScript (ES6+), WebExtensions APIs.
*   **Backend API (Optional):** Node.js, Express.js.
*   **Database (Optional):** MongoDB.
*   **Package Management:** npm.
*   **Linting/Formatting:** Prettier.
*   **Testing:** Jest (for backend logic), potentially browser-specific testing frameworks for extension features.

## 🏁 Getting Started

### 1. Clone the Repository

bash
git clone https://github.com/chirag127/ChronoLens-Visual-Browsing-History-Browser-Extension.git
cd ChronoLens-Visual-Browsing-History-Browser-Extension


### 2. Install Dependencies

bash
npm install


### 3. Browser Setup

*   **Chrome:**
    1.  Open `chrome://extensions/` in your browser.
    2.  Enable "Developer mode" using the toggle in the top-right corner.
    3.  Click "Load unpacked" and select the `src` directory (or a specific build output directory if you configure a build step).
*   **Firefox:**
    1.  Open `about:debugging#/runtime/this-firefox` in your browser.
    2.  Click "Load Temporary Add-on..." and select the `manifest.json` file from the `src` directory (or build output).

### 4. Running the Backend API (Optional)

If you intend to use the cloud sync features:

bash
cd api
npm install
NODE_ENV=development nodemon index.js


*Ensure your MongoDB instance is running and connection details are correctly configured in `config/db.js`.*

## 🧑‍💻 Development Workflow

### Development Server

For extensions, there isn't a traditional "dev server" like in web apps. You typically make changes and then reload the extension manually in `chrome://extensions/` or `about:debugging`.

### Build Scripts

bash
npm run build  # (If a build script is configured, e.g., for bundling)
npm run lint   # Runs Prettier for formatting checks
npm run test   # Runs Jest tests (if configured for backend/utility code)


### Principles

*   **SOLID:** Ensure code is maintainable and scalable.
*   **DRY (Don't Repeat Yourself):** Abstract common logic into utility functions.
*   **YAGNI (You Ain't Gonna Need It):** Implement features only as they are required.

## 🤝 Contributing

Contributions are welcome! Please refer to the [CONTRIBUTING.md](.github/CONTRIBUTING.md) file for guidelines on how to submit issues, feature requests, and pull requests.

## 📜 License

This project is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** license. See the [LICENSE](LICENSE) file for more details.

## 🔒 Security

This project is committed to security best practices. For reporting vulnerabilities or security concerns, please refer to the [SECURITY.md](.github/SECURITY.md) file.

## 🤖 AI Agent Directives

<details>
<summary>View AI Agent Directives</summary>

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
**Directives:** Detect the project type and apply the corresponding **Apex Toolchain**.

*   **PRIMARY SCENARIO: WEB / APP / EXTENSION (JavaScript/TypeScript)**
    *   **Stack:** This project leverages **JavaScript (ES6+)** targeting modern browser and WebExtension APIs. Dependency management uses **npm**. Linting and formatting are handled by **Prettier**. Testing is primarily performed using **Jest** for backend/utility modules. Consider `Vitest` for future refactoring towards Vite-based build processes if applicable.
    *   **Architecture:** Follows the **Feature-Sliced Design (FSD)** principles adapted for browser extensions, ensuring clear separation of concerns between background scripts, content scripts, UI components (popup), and shared utilities.
    *   **Build Tools:** If a build step is required (e.g., for transpilation or bundling), **Vite** is the recommended tool, configured for extension development (e.g., via `vite-plugin-webextension`).
    *   **UI Frameworks:** Vanilla JS/HTML/CSS is preferred for minimal footprint. Frameworks like React or Vue may be considered for complex UIs, but must be carefully evaluated against bundle size and performance.

*   **SECONDARY SCENARIO B: SYSTEMS / PERFORMANCE (Not applicable for this project's primary function.)**
    *   **Stack:** Rust (Cargo), Go (Modules).
    *   **Lint:** Clippy / GolangCI-Lint.
    *   **Architecture:** Hexagonal Architecture (Ports & Adapters).

*   **TERTIARY SCENARIO C: DATA / AI / SCRIPTS (Python - *Not applicable for this project's primary function.*)**
    *   **Stack:** uv (Manager), Ruff (Linter), Pytest (Test).
    *   **Architecture:** Modular Monolith or Microservices.

---

## 4. APEX NAMING CONVENTION (THE "STAR VELOCITY" ENGINE)
**Formula:** `<Product-Name>-<Primary-Function>-<Platform>-<Type>`
**Format:** `Title-Case-With-Hyphens`
**Rules:**
1.  **Length:** 3 to 10 words.
2.  **Keywords:** MUST include high-volume terms.
3.  **Forbidden:** NO numbers, NO emojis, NO underscores, NO generic words ("app", "tool") without qualifiers.
4.  **Archival Protocol:** If `action` is "ARCHIVE", you MUST still generate a new everything (name, description, topics, README) (e.g., `Advanced-Python-CLI-Tool`). The name must be **just as descriptive and professional** as an active repo. And everything should be updated also. But the archive archival should happen after the Updation

---

## 5. THE README REPLICATION PROTOCOL (THE ULTIMATE ARTIFACT)
The README is a self-contained **Project Operating System**.

**Required Sections:**
1.  **VISUAL AUTHORITY (Above the Fold):**
    *   Hero Banner/Logo (Conceptual).
    *   **Live Badges** (Shields.io):
        *   **Style:** `flat-square` (MANDATORY).
        *   **User:** `chirag127` (MANDATORY).
        *   **Required Badges:** Build Status (GitHub Actions), Code Coverage (Codecov), Tech Stack (Language, Frameworks), Lint/Format (Biome/Ruff - *Adapted to Prettier/Jest for JS*), License (CC BY-NC 4.0), GitHub Stars.
    *   **Social Proof:** "Star ⭐ this Repo" button.

2.  **STRUCTURAL CLARITY:**
    *   **BLUF:** 2-sentence value proposition.
    *   **Architecture:** ASCII `tree` or Mermaid diagram.
    *   **Table of Contents.**

3.  **🤖 AI AGENT DIRECTIVES (CRITICAL):**
    *   Must be in a collapsible `<details>` block.
    *   **Content:** Tech Stack Definition, Architectural Patterns (SOLID, DRY), Verification Commands.
    *   **Purpose:** Allows future agents to align immediately.

4.  **DEVELOPMENT STANDARDS:**
    *   Setup commands (`git clone` -> `npm install`).
    *   Scripts table.
    *   Principles (SOLID, DRY, YAGNI).

---

## 6. CHAIN OF THOUGHT (CoT) PROTOCOL
Before generating JSON, perform deep analysis in `<thinking>` block:
1.  **Audit:** Analyze repo content and purpose.
2.  **Pivot/Archive Decision:** Is it junk? If so, rename to `Archived-...`. If not, PIVOT to elite status.
3.  **Naming Strategy:** Apply `<Product>-<Function>-<Type>` formula.
4.  **Replication Protocol:** Draft the "AI Agent Directives" block.
5.  **File Generation:** Plan the content for all 11 required files (including `PROPOSED_README.md` and `badges.yml`).
6.  **Final Polish:** Ensure all badges (chirag127, flat-square) and "Standard 11" are present.
7.  **Strict Adherence:** Ensure `PROPOSED_README.md` strictly follows the `AGENTS.md` directives.

---

## 7. DYNAMIC URL & BADGE PROTOCOL
**Mandate:** All generated files MUST use the correct dynamic URLs based on the **New Repository Name**.

**Rules:**
1.  **Base URL:** `https://github.com/chirag127/<New-Repo-Name>`
2.  **Badge URLs:** All badges (Shields.io) must point to this Base URL or its specific workflows (e.g., `/actions/workflows/ci.yml`).
3.  **Consistency:** Never use the old/original repository name in links. Always use the new "Apex" name.
4.  **AGENTS.md Customization:** The generated `AGENTS.md` **MUST** be customized for the specific repository's technology stack (e.g., if Rust, use Rust tools; if Python, use Python tools), while retaining the core Apex principles. Do not just copy the generic template; adapt it.

</details>
