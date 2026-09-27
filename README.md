
# TaskMaster

TaskMaster is a lightweight full-stack task management application built using React and Node.js.

The application allows users to create, view, manage, and track tasks through a simple interface.

This repository also serves as the Proof of Concept (POC) for the **Automated Documentation Sync** capstone project.

## 1. Project Overview

TaskMaster demonstrates a structured software development workflow involving:

- Frontend and backend development
- Automated testing
- GitHub-based version control
- CI/CD integration
- Automated technical documentation
- Human approval and review checkpoints

The objective is to keep application documentation synchronized with changes made to the source code.

## 2. Technology Stack

| Component | Technology |
|-----------|------------|
| Frontend | React |
| Build Tool | Vite |
| Backend | Node.js |
| API Framework | Express.js |
| Language | JavaScript |
| Version Control | GitHub |
| CI/CD | GitHub Actions |
| E2E Testing | Playwright |
| Documentation | Confluence |

## 3. Application Features

TaskMaster provides the following functionality:

- View available tasks
- Create and manage tasks
- Mark tasks as completed
- Toggle completed tasks back to pending
- Display task status
- Communicate with backend APIs

## 4. Repository Structure

```text
taskmaster/
│
├── src/
│   ├── App.jsx
│   └── components/
│       ├── Header.jsx
│       └── TaskCard.jsx
│
├── backend/
│   └── app.js
│
├── e2e/
│   └── tests/
│
├── scripts/
│   ├── docs-sync.js
│   ├── docs-sync.test.js
│   └── docs-map.json
│
├── .github/
│   └── workflows/
│
├── docs/
│
├── package.json
├── README.md
└── CHANGELOG.md
```

Note: Directory names may vary depending on the implementation.

## 5. Local Setup

### Prerequisites

Ensure the following tools are installed:

- Node.js
- npm
- Git

### Clone Repository

```bash
git clone https://github.com/ishanm120/taskmaster-eliteA.git
cd taskmaster
```

### Install Dependencies

```bash
npm install
```

### Start Frontend

```bash
npm run dev
```

### Start Backend

```bash
node backend/app.js
```

Open the local URL displayed by Vite in your browser.

## 6. Testing

The project includes automated testing to validate application functionality.

### Run Tests

```bash
npm test
```

### Run End-to-End Tests

```bash
npm --prefix e2e test
```

### Build Application

```bash
npm run build
```

## 7. Automated Documentation Sync

The repository supports an automated documentation synchronization workflow.

Whenever application source code is added, modified, or deleted, the documentation sync process identifies relevant changes and updates the corresponding technical documentation.

### Documentation Workflow

```text
Developer Updates Source Code
           |
           v
GitHub Repository
           |
           v
Detect Source Code Changes
           |
           v
Analyze Application Metadata
           |
           v
Map Changes to Documentation Fields
           |
           v
Update Technical Documentation
           |
           v
Publish to Confluence
           |
           v
Generate Execution Summary
```

### Confluence Template

The documentation follows the standard template:

Technical-App-Manifest-v1

The template contains seven sections:

1. Executive Summary
2. System Architecture
3. Integration & Dependencies
4. Technical Configuration
5. Quality & Compliance
6. Documentation & Resources
7. Deployment Status

Repository-supported information is populated automatically.

Information that cannot be determined is marked as:

**Not Specified**

## 8. Documentation Sync Rules

The POC follows these principles:

- Process only relevant source code changes.
- Update only mapped documentation fields.
- Preserve unrelated documentation content.
- Avoid duplicate documentation updates.
- Do not expose secrets or sensitive configuration.
- Report missing information without inventing values.
- Generate a human-readable execution summary.

## 9. GitHub Workflow

Development follows a feature-branch approach.

Example:

```text
main
 |
 └── feature/automated-doc-sync
```

Each change follows this lifecycle:

```text
Requirement
    |
    v
Implementation
    |
    v
Automated Testing
    |
    v
Documentation Sync
    |
    v
Code Review
    |
    v
Pull Request
    |
    v
Human Approval
    |
    v
Merge
```

## 10. POC Scope

This project focuses on validating the happy-path implementation of automated documentation synchronization.

The POC demonstrates:

- Source code change detection
- Technical metadata extraction
- Documentation field mapping
- Confluence template population
- Automated workflow execution
- Human review and approval

Advanced exception handling, production deployment, and enterprise-scale integrations are outside the initial POC scope.

## 11. Expected Outcome

The successful execution of this POC demonstrates that technical documentation can remain synchronized with application changes through an automated, repeatable, and reviewable process.

The workflow reduces manual documentation effort while maintaining consistency between the application repository and its technical documentation.

## 12. Project Status

**Status:** Proof of Concept (POC)

**Project:** TaskMaster

**Use Case:** Automated Documentation Sync

**Documentation Platform:** Atlassian Confluence

**Repository Platform:** GitHub
