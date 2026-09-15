# Team Work Division -- SE-SRS-2 (SAD & STP Submission)

## Team 11 | Section 5C | PES University | Software Engineering (5th Semester)

---

## 1. Team Members and Role Assignments

| Name | USN | Primary Role | Dedicated Branch |
| :--- | :--- | :--- | :--- |
| Darshan P Pawar | PES2UG24CS143 | Team Lead & Full-Stack Architect | `feature/darshan-sad-architecture` |
| DHATRI SHIVAPRASAD | PES2UG24CS158 | Frontend & UI/UX Lead | `feature/dhatri-sad-design-ux` |
| CHANDAN KUMAR K | PES2UG24CS128 | Backend & Database Architect | `feature/chandan-test-plan-core` |
| GURUBELLI YEKAMBAR ESHWAR RAO | PES2UG24CS173 | Full-Stack & QA/DevOps Lead | `feature/eshwar-test-execution-metrics` |

---

## 2. Document Ownership

### Software Architecture & Design (SAD) Document

| Section | Owner | Description |
| :--- | :--- | :--- |
| Sections 1-2 (Introduction, Document Overview) | Darshan P Pawar | Purpose, scope, audience, definitions, related documents |
| Section 3 (Architecture) | Darshan P Pawar | Goals, constraints, stakeholders, component diagram, architecture pattern, technology stack, security architecture (STRIDE) |
| Section 4 (Design) | DHATRI SHIVAPRASAD | Design overview, UML sequence diagrams, API design, error handling, UX design |
| Section 5 (Appendices) | DHATRI SHIVAPRASAD | Glossary, references, tools |

### Software Test Plan (STP) Document

| Section | Owner | Description |
| :--- | :--- | :--- |
| Sections 1-5 (Introduction through Test Strategy) | CHANDAN KUMAR K | Purpose, test items, features to test, approach, security validation |
| Sections 6-9 (Environment, Schedule, Deliverables, Roles) | CHANDAN KUMAR K | Test environment setup, schedule milestones, deliverables list, role assignments |
| Sections 10-12 (Risks, Assumptions, Suspension Criteria) | GURUBELLI YEKAMBAR ESHWAR RAO | Risk mitigation, dependency management, halt/resume criteria |
| Sections 13-15 (Traceability, Metrics, Approvals) | GURUBELLI YEKAMBAR ESHWAR RAO | RTM mapping, test metrics collection, sign-off procedures |

---

## 3. Git Workflow

All team members follow the feature branch workflow:

1. Each member works on their dedicated feature branch
2. Commits are attributed to the respective team member
3. Pull Requests are created from feature branches to `main`
4. PRs are reviewed and merged by designated team members

---

## 4. Viva Preparation Guide

### Darshan P Pawar (PES2UG24CS143) -- Architecture & Leadership
- Explain the layered component architecture and why it was chosen over alternatives
- Describe the dual-mode data persistence strategy (Supabase + LocalStorage)
- Walk through the UML component diagram and explain inter-component dependencies
- Discuss STRIDE threat modeling and security architecture decisions
- Demonstrate the live application and GitHub repository structure

### DHATRI SHIVAPRASAD (PES2UG24CS158) -- Design & UX
- Explain the UML sequence diagrams for authentication and task workflow
- Describe the API design for Supabase REST endpoints
- Discuss error handling strategies and monitoring approach
- Walk through the UX design principles applied to the Kanban board interface
- Demonstrate drag-and-drop interactions and responsive layout behavior

### CHANDAN KUMAR K (PES2UG24CS128) -- Test Planning & Strategy
- Explain the multi-level testing approach (unit, integration, system, acceptance)
- Describe the test environment setup and tool selection rationale
- Walk through the features-to-test mapping to SRS requirement IDs
- Discuss entry and exit criteria for each testing phase
- Demonstrate the Vitest test suite execution and CI/CD pipeline

### GURUBELLI YEKAMBAR ESHWAR RAO (PES2UG24CS173) -- Test Execution & Metrics
- Explain the Requirements Traceability Matrix and how it ensures coverage
- Describe test metrics collection methodology (pass rate, defect density, coverage)
- Walk through risk identification and mitigation strategies
- Discuss suspension and resumption criteria for testing activities
- Demonstrate the GitHub Actions CI/CD workflow and test reporting
