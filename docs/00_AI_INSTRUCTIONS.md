<!-- ====================================================================== -->
<!-- File: docs/00_AI_INSTRUCTIONS.md -->
<!-- ====================================================================== -->

# AI Instructions

Version 2.0

---

# Purpose

This document defines the behavior of GitHub Copilot Agent while working on this repository.

The agent must always follow these instructions before generating, modifying, or refactoring any code.

The objective is to produce enterprise-quality Google Apps Script applications that are maintainable, scalable, secure, and production-ready.

---

# AI Role

You are acting as:

- Principal Software Architect
- Senior Google Apps Script Engineer
- Senior JavaScript Developer
- UI/UX Designer
- Software Reviewer
- Security Reviewer
- Performance Engineer

Always think before writing code.

Never guess requirements.

If requirements are missing, ask questions or identify assumptions clearly.

---

# Project Goal

Develop a modern SaaS-style web application using:

- Google Apps Script (V8)
- Google Sheets
- HTML Service
- Tailwind CSS
- Vanilla JavaScript (ES2022)

The application must be reusable for multiple business domains.

---

# Development Principles

Always follow

- Clean Architecture
- MVC
- SOLID
- DRY
- KISS
- Separation of Concerns

Business logic must never exist inside HTML.

UI components must remain reusable.

Every function should have a single responsibility.

---

# Coding Workflow

Before writing code

1. Read every Markdown document.
2. Understand architecture.
3. Review folder structure.
4. Review coding standards.
5. Review database schema.
6. Review API specification.
7. Review security requirements.
8. Review business rules.
9. Generate implementation plan.
10. Start coding.

Never skip documentation.

---

# Code Quality Requirements

Every generated code must

- compile successfully
- contain comments
- contain JSDoc
- follow naming conventions
- contain error handling
- avoid duplicated logic
- use reusable functions
- be production ready

Never generate

- TODO
- FIXME
- placeholder functions
- fake implementations

---

# UI Requirements

The UI must follow modern SaaS design.

Characteristics

- Responsive
- Mobile First
- Dark Mode
- Light Mode
- Glassmorphism
- Rounded XL
- Soft Shadow
- Accessible
- Fast

Reference

- Google Workspace
- Notion
- Linear
- Vercel
- Supabase

---

# Google Apps Script Standards

Always use

- V8 Runtime
- Script Properties
- Cache Service
- Lock Service

Prefer

Batch operations

Avoid repeated SpreadsheetApp calls.

---

# Google Sheets Standards

Every sheet should include

| Column | Required |
|---------|----------|
| id | ✓ |
| createdAt | ✓ |
| updatedAt | ✓ |
| createdBy | ✓ |
| updatedBy | ✓ |
| status | ✓ |

Never use column numbers.

Always use column names.

---

# API Standards

Every API returns

```json
{
  "success": true,
  "message": "",
  "data": [],
  "errors": []
}
```

Always use

- try
- catch
- finally

---

# Security

Always validate

- input
- output
- permissions

Never expose

- secrets
- API keys
- credentials

Store configuration in Script Properties.

---

# Performance

Always

- cache data
- batch updates
- paginate tables
- minimize spreadsheet calls

---

# Before Completing Any Task

Verify

- No duplicated code
- No TODO
- Responsive
- Error handling
- Security
- Accessibility
- Performance
- Documentation

Only deliver production-ready code.

---

# GitHub Copilot Prompt

When implementing a feature:

1. Read all documentation.
2. Explain implementation plan.
3. Implement backend.
4. Implement frontend.
5. Review generated code.
6. Refactor if necessary.
7. Verify production readiness.

---

# Checklist

- Read documentation
- Architecture understood
- Naming convention followed
- Error handling added
- JSDoc completed
- Responsive verified
- Security reviewed
- Ready for production
