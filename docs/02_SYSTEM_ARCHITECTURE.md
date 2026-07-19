<!-- ====================================================================== -->
<!-- File: docs/02_SYSTEM_ARCHITECTURE.md -->
<!-- ====================================================================== -->

# System Architecture

Version 2.0

---

# Purpose

This document defines the enterprise architecture of the project.

All implementations must follow this architecture.

---

# Architecture Style

- Clean Architecture
- MVC Pattern
- Service Layer
- Repository Pattern
- Component-based UI

---

# High-Level Architecture

```text
Browser
    │
    ▼
HTML Service (View)
    │
    ▼
Controller
    │
    ▼
Service
    │
    ▼
Repository
    │
    ▼
Google Sheets
```

External APIs (Optional)

```text
Browser
    │
    ▼
Controller
    │
    ▼
API Service
    │
    ▼
REST API
```

---

# Layer Responsibilities

| Layer | Responsibility |
|--------|----------------|
| View | Display UI and collect user input |
| Controller | Receive requests and coordinate workflow |
| Service | Business logic |
| Repository | Read/write data |
| Database | Google Sheets |

---

# MVC Responsibilities

## View

Responsible for

- HTML
- Tailwind CSS
- User interaction

Never

- Access SpreadsheetApp
- Contain business logic

---

## Controller

Responsible for

- Request handling
- Validation
- Calling services

Never

- Read Sheets directly

---

## Service

Responsible for

- Business rules
- Data transformation
- Validation
- Authorization

Never

- Generate HTML

---

## Repository

Responsible for

- CRUD
- Query
- Batch update

Never

- Apply business rules

---

# Directory Architecture

```text
src/

controllers/
services/
repositories/
models/
helpers/
config/

views/

assets/

css/

js/

images/
```

---

# Request Flow

```text
User

↓

View

↓

Controller

↓

Service

↓

Repository

↓

Google Sheets

↓

Repository

↓

Service

↓

Controller

↓

View
```

---

# Google Apps Script Files

| File | Responsibility |
|------|----------------|
| Code.gs | Entry Point |
| Router.gs | Routing |
| Auth.gs | Authentication |
| API.gs | Web API |
| Database.gs | Repository |
| Config.gs | Configuration |
| Logger.gs | Logging |
| Utils.gs | Utilities |

---

# Frontend Structure

```text
assets/

css/
js/
icons/
images/

views/

partials/

pages/
```

---

# JavaScript Modules

```text
app.js

api.js

auth.js

dashboard.js

table.js

modal.js

toast.js

chart.js

utils.js
```

Each module must have a single responsibility.

---

# Data Flow

```text
Google Sheet

↓

Repository

↓

Service

↓

Controller

↓

JSON

↓

Frontend

↓

UI
```

---

# Dependency Rule

Allowed

View

↓

Controller

↓

Service

↓

Repository

↓

Database

Not Allowed

Repository

↓

Controller

Service

↓

View

View

↓

SpreadsheetApp

---

# Error Flow

```text
Exception

↓

Logger

↓

Controller

↓

Toast Notification

↓

User
```

---

# Logging Strategy

Log

- Login
- Logout
- CRUD
- Errors
- Permission Denied
- API Calls

Store logs in

AuditLogs Sheet

---

# Best Practices

✓ Small modules

✓ Single Responsibility

✓ Reusable Services

✓ Stateless Controllers

✓ Batch Spreadsheet operations

✓ Configuration outside source code

✓ Avoid duplicated logic

---

# GitHub Copilot Prompt

Before implementing any feature:

- Identify affected layers.
- Create Controller.
- Create Service.
- Create Repository.
- Update View.
- Test complete request flow.

Never bypass Service Layer.

---

# Checklist

- MVC followed
- Repository Pattern used
- No Spreadsheet access from UI
- Business logic isolated
- Reusable modules
- Logging implemented
- Error handling completed
