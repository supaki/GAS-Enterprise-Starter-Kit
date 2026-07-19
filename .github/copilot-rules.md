# GitHub Copilot Project Rules

Version: 2.0

---

# Purpose

This document defines mandatory rules for GitHub Copilot Agent when generating, modifying, reviewing, or refactoring code in this repository.

These rules override personal coding preferences unless explicitly instructed otherwise.

---

# Primary Objective

Always generate:

- Production-ready code
- Maintainable architecture
- Secure implementation
- Modern UI
- Reusable components

---

# Technology Stack

Backend

- Google Apps Script (V8)

Database

- Google Sheets

Frontend

- HTML5
- Tailwind CSS
- JavaScript ES6+

Architecture

- MVC
- Clean Architecture
- Repository Pattern
- Service Layer

---

# Architecture Rules

ALWAYS

✔ Follow MVC

✔ Separate UI from Business Logic

✔ Use Service Layer

✔ Use Repository Pattern

✔ Keep components reusable

✔ Keep modules independent

NEVER

✘ Put business logic in HTML

✘ Access Google Sheets from UI

✘ Duplicate business logic

✘ Mix Controller and Service

---

# Google Apps Script Rules

Always

✔ Use const / let

✔ Use V8 Runtime

✔ Use getValues()

✔ Use setValues()

✔ Batch operations

✔ Use PropertiesService

✔ Use CacheService when appropriate

Never

✘ Read one cell at a time

✘ Write one row at a time

✘ Hard-code Spreadsheet IDs

✘ Hard-code credentials

---

# Google Sheets Rules

Every sheet should have:

- Primary Key
- Audit Fields
- Fixed Schema
- Validation

Every table should include:

- createdAt
- createdBy
- updatedAt
- updatedBy

---

# UI Rules

Always create:

- Responsive Layout
- Modern SaaS Design
- Sidebar
- Navbar
- Cards
- Tables
- Modal
- Toast Notification
- Loading State
- Empty State
- Dark Mode

Never use:

- Bootstrap
- jQuery
- Inline CSS
- Inline JavaScript

---

# JavaScript Rules

Use:

- ES6+
- Classes
- Arrow Functions
- Template Literals
- Destructuring
- Spread Operator

Avoid:

- var
- Callback Hell
- Global Variables

---

# Naming Convention

Files

PascalCase

Example

```
UserService.gs
```

Functions

camelCase

```
getUsers()
```

Classes

PascalCase

```
UserRepository
```

Constants

UPPER_CASE

```
MAX_RETRY
```

---

# API Rules

Every API must return:

Success

```json
{
  "success": true,
  "data": {}
}
```

Failure

```json
{
  "success": false,
  "message": "Error"
}
```

---

# Error Handling Rules

Every external operation must use:

```
try

↓

catch

↓

log

↓

return standard response
```

Never ignore exceptions.

---

# Security Rules

Always

✔ Validate Input

✔ Escape Output

✔ Check Permissions

✔ Use RBAC

✔ Protect Sensitive Data

Never

✘ Hard-code Passwords

✘ Hard-code Tokens

✘ Expose Stack Trace

✘ Trust Client Input

---

# Performance Rules

Prefer

- Batch Read
- Batch Write
- Cache
- Lazy Loading
- Pagination

Avoid

- Nested Spreadsheet calls
- Duplicate queries
- Heavy loops

---

# Documentation Rules

Whenever a new feature is added:

Update if needed:

- Database Schema
- API Specification
- Business Rules
- Release Note
- Changelog

---

# Copilot Workflow

Before Coding

1. Read Requirement
2. Review Existing Code
3. Review Documentation
4. Explain Implementation

During Coding

- Follow Architecture
- Keep Code Clean
- Add Validation
- Add Error Handling

After Coding

Provide:

- Summary
- Changed Files
- Testing Guide
- Improvement Suggestions

---

# Quality Checklist

Every generated code must satisfy:

- Clean Architecture
- MVC
- Responsive UI
- Security
- Validation
- Error Handling
- Performance
- Documentation

---

# Definition of Done

A task is complete only when:

- Code Compiles
- UI Works
- API Works
- Validation Exists
- Error Handling Exists
- Documentation Updated
- Ready for Production

---

# Final Rule

When documentation conflicts with generated code:

Documentation is the source of truth.

Never invent architecture.

Never ignore project standards.

Always prioritize maintainability over short code.
