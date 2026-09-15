# SprintFlow -- Agile Project Management System

## Software Architecture & Design (SAD) and Software Test Plan (STP)

**Course:** Software Engineering (5th Semester B.Tech, Section 5C)  
**Institution:** PES University, Department of Computer Science and Engineering  
**Academic Year:** 2025-2026

---

## 1. Project Information

| Field | Details |
| :--- | :--- |
| **Project Name** | SprintFlow -- Agile Project Management System |
| **Team Number** | Team 11 |
| **Repository** | [SE-SRS-2](https://github.com/Darshanpawar7/SE-SRS-2) |
| **Related Repository** | [SE-SRS](https://github.com/Darshanpawar7/SE-SRS) (SRS Document & Source Code) |

### Team Members

| Name | USN | Role | Feature Branch |
| :--- | :--- | :--- | :--- |
| **Darshan P Pawar** | `PES2UG24CS143` | Team Lead & Full-Stack Architect | `feature/darshan-sad-architecture` |
| **DHATRI SHIVAPRASAD** | `PES2UG24CS158` | Frontend & UI/UX Lead | `feature/dhatri-sad-design-ux` |
| **CHANDAN KUMAR K** | `PES2UG24CS128` | Backend & Database Architect | `feature/chandan-test-plan-core` |
| **GURUBELLI YEKAMBAR ESHWAR RAO** | `PES2UG24CS173` | Full-Stack & QA/DevOps Lead | `feature/eshwar-test-execution-metrics` |

---

## 2. Document Deliverables

This repository contains the following formal engineering documents for the SprintFlow project:

| Document | Description | Location |
| :--- | :--- | :--- |
| **Software Architecture & Design (SAD)** | Architecture patterns, UML component diagram, sequence diagrams, API design, security architecture (STRIDE), and technology stack documentation | `docs/SAD_Document_Team11.md` |
| **Software Test Plan (STP)** | Test strategy, test items, features to be tested, test environment, schedule, roles, traceability matrix, metrics, and security validation procedures | `docs/STP_Document_Team11.md` |
| **Team Work Division** | Detailed work breakdown and responsibility mapping across all 4 team members | `docs/Team_Work_Division.md` |

### Formal Submission Reports

| Format | File |
| :--- | :--- |
| SAD Report (PDF) | `Team11_SAD_Report.pdf` |
| STP Report (PDF) | `Team11_STP_Report.pdf` |
| SAD Report (Word) | `docs/Team11_SAD_Report.docx` |
| STP Report (Word) | `docs/Team11_STP_Report.docx` |

---

## 3. System Architecture Overview

SprintFlow employs a **component-based single-page application architecture** with a dual-mode data persistence layer:

```
+-----------------------------------------------------------------------+
|                      React 18 Single Page App (Vite 5)                |
|  - Kanban Workflow   - Visibility Dashboard   - Sprint Management     |
+-----------------------------------------------------------------------+
                                  |
                                  v
+-----------------------------------------------------------------------+
|                     Dual-Mode Data Service Layer                      |
|                (src/services/supabaseClient.js)                       |
+-----------------------------------------------------------------------+
            |                                           |
            v                                           v
+-----------------------+                   +---------------------------+
| Supabase PostgreSQL   |                   | Persistent Offline Engine |
| Cloud Database (RLS)  |                   | (Browser LocalStorage)    |
+-----------------------+                   +---------------------------+
```

### Architecture Pattern

**Layered Component Architecture** was chosen for the following reasons:
- Clear separation of concerns between presentation, state management, and data access
- React component composability enables independent module development by each team member
- Dual-mode data layer provides resilient operation (cloud sync with offline fallback)

---

## 4. Technology Stack

| Layer | Technology | Version |
| :--- | :--- | :--- |
| Frontend Framework | React | 18.x |
| Build Toolchain | Vite | 5.x |
| State Management | React Context API | Built-in |
| Cloud Database | Supabase PostgreSQL | Latest |
| Offline Persistence | Browser LocalStorage | Web API |
| Unit Testing | Vitest | 2.x |
| CI/CD | GitHub Actions | Latest |
| Security | Row Level Security (RLS), TLS 1.3 | -- |

---

## 5. Quick Start and Installation

### Prerequisites
- Node.js version 18.0.0 or higher
- npm version 9.0.0 or higher

### Local Setup
```bash
# Clone the repository
git clone https://github.com/Darshanpawar7/SE-SRS-2.git
cd SE-SRS-2

# Install dependencies
npm install

# Launch development server
npm run dev
```
Navigate to `http://localhost:5173` in a web browser. The system initializes immediately with pre-configured seed data.

### Automated Testing
```bash
# Execute Vitest test suite
npm test

# Verify production build compilation
npm run build
```

---

## 6. Repository Structure

```
SE-SRS-2/
+-- .github/workflows/
|   +-- ci.yml                    # GitHub Actions CI/CD Pipeline
+-- database/
|   +-- schema.sql                # Supabase PostgreSQL DDL Schema
+-- docs/
|   +-- SAD_Document_Team11.md    # Software Architecture & Design Specification
|   +-- STP_Document_Team11.md    # Software Test Plan
|   +-- Team_Work_Division.md     # Work Breakdown & Viva Guide
|   +-- CONTRIBUTION_DARSHAN.md   # Individual Contribution Log
|   +-- CONTRIBUTION_DHATRI.md
|   +-- CONTRIBUTION_CHANDAN.md
|   +-- CONTRIBUTION_ESHWAR.md
+-- src/
|   +-- components/               # React UI Components
|   +-- context/                  # AuthContext, ProjectContext
|   +-- services/                 # Supabase Client & Data Service
|   +-- utils/                    # Estimation Logic & Constants
|   +-- tests/                    # Vitest Unit Test Suite
|   +-- App.jsx
|   +-- index.css
|   +-- main.jsx
+-- package.json
+-- vite.config.js
+-- README.md
```

---

## 7. Related Documents

- **SRS Document (First Submission):** [SE-SRS Repository](https://github.com/Darshanpawar7/SE-SRS)
- **IEEE 42010** -- Systems and Software Engineering: Architecture Description
- **IEEE 829** -- Standard for Software and System Test Documentation
- **OWASP Top 10** -- Web Application Security Risks
