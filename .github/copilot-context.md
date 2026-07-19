<!-- ====================================================================== -->
<!-- File: .github/copilot-context.md -->
<!-- Version: 2.0 -->
<!-- ====================================================================== -->

# GitHub Copilot Project Context

Version 2.0

GAS Enterprise Starter Kit

---

# Project Identity

## Project Name

GAS Enterprise Starter Kit

---

# Project Purpose

This project is an enterprise-ready application framework designed for building web applications using:

- Google Apps Script
- Google Sheets Database
- HTML Service
- Tailwind CSS
- Vanilla JavaScript

The system supports:

- Internal business applications
- Dashboard systems
- Data management systems
- Workflow applications
- API integrations

---

# AI Agent Mission

GitHub Copilot Agent must understand this repository as:

- Enterprise Application Framework
- AI-Assisted Development Platform
- Maintainable Long-Term Software System

The Agent must prioritize:

1. Correct Architecture
2. Security
3. Maintainability
4. Scalability
5. Developer Experience

---

# Technology Context

## Backend

Platform:

Google Apps Script V8

Responsibilities:

- Business logic
- API endpoints
- Authentication
- Data processing
- External integrations

---

## Frontend

Technology:

- HTML Service
- Tailwind CSS
- Vanilla JavaScript

Responsibilities:

- User Interface
- User Interaction
- Client-side validation

---

## Database

Primary Database:

Google Sheets

Used for:

- Application data
- Configuration
- User management
- Business records

---

## External Database

Optional:

MySQL Local Database

Integration:

Application

↓

API Layer

↓

Node.js Proxy

↓

MySQL Database


---

# Architecture Context

The system follows layered architecture.


Frontend

↓

Controller

↓

Service

↓

Repository

↓

Model

↓

Database


---

# Architecture Rules

## Frontend

Responsible for:

- UI
- Interaction
- Presentation

Must not:

- Access database directly
- Contain business rules

---

## Controller

Responsible for:

- Request handling
- API communication
- Input processing

---

## Service

Responsible for:

- Business logic
- Workflow
- Validation

---

## Repository

Responsible for:

- Data access
- CRUD operations
- Database abstraction

---

## Model

Responsible for:

- Data structure
- Object definition
- Validation model

---

# Core Application Concepts

## Authentication

System supports:

- User authentication
- Session management
- Permission verification

---

## Authorization

Uses:

RBAC

Structure:


User

↓

Role

↓

Permission

↓

Action


---

# Common Application Modules

Expected modules:

## User Management

- Users
- Roles
- Permissions

---

## Dashboard

- Statistics
- Charts
- Reports

---

## Data Management

- CRUD operations
- Search
- Filtering
- Export

---

## Configuration

- System settings
- Data mapping
- Application parameters

---

# Repository Structure Context


.github/

├── copilot-instructions.md
├── copilot-context.md
└── copilot-rules.md

docs/

├── Architecture Documents
├── Development Guides
├── AI Guides
├── Security Guides
└── Operation Guides

src/

├── frontend
├── backend
├── services
└── utils


---

# Documentation Knowledge Base

Important documents:

## Foundation


docs/00-09


---

## Project Rules


docs/PROJECT_RULES.md
docs/30_AI_CONTEXT.md


---

## AI Development


docs/31_COPILOT_AGENT_GUIDE.md
docs/32_PROMPT_TEMPLATES.md


---

## Enterprise Operation


docs/33_SECURITY_GUIDE.md
docs/34_DEPLOYMENT_GUIDE.md
docs/35_DEVELOPMENT_WORKFLOW.md
docs/36_AI_AGENT_OPERATION_GUIDE.md


---

# AI Agent Decision Rules

Before making decisions:

Analyze:

- Existing architecture
- Existing patterns
- Security impact
- Maintenance impact

Prefer:

- Simple solutions
- Reusable components
- Existing libraries
- Documented approaches

---

# Business Context

This framework is intended for:

- Healthcare applications
- Government systems
- Organization dashboards
- Data management systems

The design should support:

- Data security
- Auditability
- Long-term maintenance

---

# End of Copilot Context

Version 2.0
