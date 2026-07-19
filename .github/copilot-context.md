# GitHub Copilot Project Context

Version: 2.0

---

# Project Overview

Project Name:

GAS Enterprise Starter Kit

Purpose:

Develop modern Enterprise Web Applications using Google Apps Script, Google Sheets, HTML5, Tailwind CSS and JavaScript.

This repository serves as a reusable starter kit for building scalable business applications with GitHub Copilot Agent.

---

# Technology Stack

Backend

- Google Apps Script (V8 Runtime)

Database

- Google Sheets
- PropertiesService
- CacheService
- LockService

Frontend

- HTML5
- Tailwind CSS
- JavaScript ES6+
- Google HTML Service

Development

- GitHub
- GitHub Copilot Agent
- VS Code
- clasp

---

# Architecture

The project follows:

- MVC Architecture
- Clean Architecture
- Repository Pattern
- Service Layer
- Component-Based UI

Application Flow

```
Browser

↓

HTML Service

↓

Controller

↓

Service

↓

Repository

↓

Google Sheets
```

---

# Project Goals

The generated application should be:

- Modern SaaS UI
- Responsive
- Fast
- Secure
- Easy to maintain
- AI-assisted
- Production-ready

---

# UI Standard

Use:

- Tailwind CSS
- Modern SaaS Dashboard
- Responsive Layout
- Dark Mode Support
- Card-based Interface
- Sidebar Navigation
- Top Navigation Bar
- Toast Notifications
- Modal Dialogs
- Loading Skeletons

Avoid:

- Bootstrap
- jQuery
- Inline CSS
- Inline JavaScript

---

# Coding Standard

JavaScript

- ES6+
- const / let
- Arrow Functions
- Classes
- Template Literals

Google Apps Script

- V8 Runtime
- Modular Files
- Small reusable functions
- Batch read/write
- Proper error handling

---

# Folder Structure

```
src/

├── controllers/
├── services/
├── repositories/
├── models/
├── utils/
├── web/
│   ├── components/
│   ├── css/
│   ├── js/
│   └── pages/
```

---

# Database Standard

Google Sheets is the primary database.

Each sheet should contain:

- Primary Key
- Audit Fields
- Validation Rules
- Fixed Schema

Example

Users

- userId
- username
- fullName
- email
- status
- createdAt
- updatedAt

---

# API Standard

Every API should return:

Success

```json
{
  "success": true,
  "data": {}
}
```

Error

```json
{
  "success": false,
  "message": "Error message"
}
```

---

# Security Standard

Always:

- Validate input
- Escape output
- Protect sensitive sheets
- Use Script Properties for secrets
- Check permissions before processing

Never:

- Hard-code passwords
- Hard-code API Keys
- Expose stack traces
- Trust client-side validation

---

# Performance Standard

Prefer:

- getValues()
- setValues()
- CacheService
- Batch Processing
- Lazy Loading
- Pagination

Avoid:

- Reading cells one by one
- Writing rows one by one
- Repeated Spreadsheet calls

---

# Development Workflow

Every feature should follow:

Requirement

↓

Analysis

↓

Architecture

↓

Database

↓

UI

↓

Backend

↓

Testing

↓

Documentation

↓

Deployment

---

# Documentation Reference

GitHub Copilot should use these documents as project knowledge.

Priority

1. .github/copilot-instructions.md

2. .github/copilot-rules.md

3. docs/00_AI_INSTRUCTIONS.md

4. docs/01_PROJECT_OVERVIEW.md

5. docs/02_SYSTEM_ARCHITECTURE.md

6. docs/03_UI_UX_GUIDELINES.md

7. docs/04_DATABASE_SCHEMA.md

8. docs/05_API_SPECIFICATION.md

9. docs/06_AUTHENTICATION_RBAC.md

10. docs/07_CODING_STANDARDS.md

11. docs/08_COMPONENT_LIBRARY.md

12. docs/09_FOLDER_STRUCTURE.md

13. docs/10-30 documentation

---

# Code Generation Principles

Before writing code:

- Understand the requirement.
- Review existing modules.
- Reuse existing components.
- Avoid duplicated logic.
- Follow project architecture.

When writing code:

- Keep functions small.
- Separate business logic.
- Add validation.
- Handle errors.
- Write readable code.

After writing code:

- Explain changes.
- List modified files.
- Suggest testing steps.
- Recommend improvements.

---

# Preferred Design Pattern

```
Controller

↓

Service

↓

Repository

↓

Google Sheets
```

Never access Spreadsheet directly from HTML or UI.

---

# GitHub Copilot Responsibilities

GitHub Copilot should behave as:

- Software Architect
- Google Apps Script Expert
- JavaScript Expert
- UI/UX Designer
- Database Designer
- Security Reviewer
- Code Reviewer

Copilot should prioritize quality over speed.

---

# Definition of Done

A feature is complete only when:

- Requirement implemented
- UI completed
- Backend completed
- Validation completed
- Error handling completed
- Documentation updated
- Testing completed
- No duplicated code
- Follows project standards

---

# Final Context

This repository is intended to become a reusable Enterprise Starter Kit.

Every generated file should be production-ready, modular, maintainable, secure and consistent with the project documentation.
