<!-- ====================================================================== -->
<!-- File: docs/README.md -->
<!-- ====================================================================== -->

# Project Documentation

Version 2.0

GAS Enterprise Starter Kit Documentation

---

# Purpose

This folder contains the complete project documentation for the GAS Enterprise Starter Kit.

The documentation is designed for:

- Developers
- System Architects
- GitHub Copilot Agent
- AI Coding Assistants
- Project Managers
- System Administrators

The objectives are:

- Maintain project knowledge
- Support AI-assisted development
- Standardize development practices
- Improve software quality
- Enable long-term maintenance

---

# Documentation Structure

```text
docs/

├── Project Foundation

├── System Design

├── Development Guide

├── AI Agent Guide

├── Security Guide

├── Deployment Guide

└── Operation Guide

Documentation Index
Phase 1 — Project Foundation & Analysis
Project Understanding
File	Description
00_*	AI Instructions and Project Foundation
01_*	Project Overview
02_*	System Architecture
03_*	UI/UX Guidelines
04_*	Database Design
05_*	API Specification
06_*	Authentication and RBAC
07_*	Coding Standards
08_*	Component Library
09_*	Project Structure
Phase 2 — Development & Agent Workflow
Development Knowledge Base
File	Description
10_* - 20_*	Development Specifications
21_* - 29_*	Implementation Guides
30_AI_CONTEXT.md	AI Project Context Management
AI Development Documentation
GitHub Copilot Agent
File	Description
31_COPILOT_AGENT_GUIDE.md	How to use GitHub Copilot Agent
32_PROMPT_TEMPLATES.md	Enterprise Prompt Library
Phase 3 — Quality, Security & Production Readiness
Enterprise Operation Guides
File	Description
33_SECURITY_GUIDE.md	Security Standards and Practices
34_DEPLOYMENT_GUIDE.md	Deployment and Release Process
35_DEVELOPMENT_WORKFLOW.md	Software Development Workflow
36_AI_AGENT_OPERATION_GUIDE.md	AI Agent Operation Standard
AI Agent Reading Order

GitHub Copilot Agent should read documents in this order:

1. .github/copilot-instructions.md

↓

2. .github/copilot-context.md

↓

3. .github/copilot-rules.md

↓

4. docs/README.md

↓

5. docs/30_AI_CONTEXT.md

↓

6. docs/31_COPILOT_AGENT_GUIDE.md

↓

7. docs/32_PROMPT_TEMPLATES.md

↓

8. docs/33_SECURITY_GUIDE.md

↓

9. docs/34_DEPLOYMENT_GUIDE.md

↓

10. docs/35_DEVELOPMENT_WORKFLOW.md

↓

11. docs/36_AI_AGENT_OPERATION_GUIDE.md
Documentation Usage
Before Development

Read:

Project Overview
Architecture
Coding Standards
Security Rules
During Development

Use:

Prompt Templates
Development Workflow
AI Agent Guide
Before Release

Review:

Security Guide
Deployment Guide
Testing Guidelines
AI Agent Rules

When working with this repository:

The AI Agent must:

✓ Read documentation first

✓ Understand architecture

✓ Follow coding standards

✓ Follow security requirements

✓ Generate maintainable code

✓ Create tests

✓ Update documentation

The AI Agent must not:

✗ Ignore project rules

✗ Create unrelated files

✗ Introduce new architecture without approval

✗ Expose sensitive information

Documentation Maintenance

Documentation must be updated when:

Adding new features
Changing architecture
Changing database design
Changing API
Changing workflow
Changing security rules
Documentation Update Workflow
Change Request

↓

Implementation

↓

Documentation Update

↓

Review

↓

Release
Repository Knowledge Structure
Repository

├── .github

│   ├── copilot-instructions.md

│   ├── copilot-context.md

│   └── copilot-rules.md


├── docs

│   ├── Architecture Knowledge

│   ├── Development Knowledge

│   ├── AI Knowledge

│   ├── Security Knowledge

│   └── Operation Knowledge


└── Source Code
Future Documentation

Recommended future additions:

File	Purpose
37_REPOSITORY_SETUP_GUIDE.md	Environment Setup
38_ARCHITECTURE_DECISION_RECORD.md	Architecture Decisions
39_TROUBLESHOOTING_GUIDE.md	Problem Resolution
40_USER_MANUAL.md	End User Documentation
End of Documentation Index
