<!-- ====================================================================== -->
<!-- File: docs/10_AGENT_WORKFLOW.md -->
<!-- ====================================================================== -->

# Development & Agent Workflow

Version 2.0

---

# Purpose

This document defines the workflow for using GitHub Copilot Agent to develop applications based on the GAS Enterprise Starter Kit.

The goal is to make Copilot work as a professional development team consisting of:

- Software Architect
- Backend Developer
- Frontend Developer
- UI/UX Designer
- QA Engineer
- Security Reviewer

---

# Copilot Agent Working Principle

GitHub Copilot Agent must not immediately generate code.

The correct workflow:

```text
Understand

↓

Analyze

↓

Plan

↓

Generate

↓

Review

↓

Refactor

↓

Test

↓

Document
```

---

# Phase 1: Project Understanding

## Objective

Allow Agent to understand the entire system.

Prompt:

```
Read all documentation inside docs folder.

Understand:

- Project architecture
- Coding standards
- Database design
- API specification
- UI guidelines

Do not generate code yet.

Summarize your understanding.
```

Expected Result:

Agent should explain:

- Architecture
- Technology stack
- Folder structure
- Development approach

---

# Phase 2: Requirement Analysis

Before creating features:

Prompt:

```
Analyze this feature requirement.

Identify:

- Business requirements
- Database changes
- API requirements
- UI components needed
- Security considerations
- Testing requirements

Do not write code yet.
```

---

# Phase 3: Implementation Planning

Prompt:

```
Create an implementation plan.

Include:

1. Database changes
2. Backend files
3. Frontend files
4. API endpoints
5. Security rules
6. Testing approach

Wait for approval before coding.
```

---

# Phase 4: Database Development

Workflow:

```text
Schema

↓

Model

↓

Repository

↓

Validation
```

Prompt:

```
Create database implementation.

Requirements:

- Follow DATABASE_SCHEMA.md
- Create Repository Layer
- Use Header Mapping
- Add Validation
- Add Error Handling
```

---

# Phase 5: Backend Development

Order:

```text
Config

↓

Model

↓

Repository

↓

Service

↓

Controller

↓

API
```

Prompt:

```
Implement backend following Clean Architecture.

Requirements:

- MVC
- Service Layer
- Repository Pattern
- Error Handling
- Logging
- Security
```

---

# Phase 6: Frontend Development

Order:

```text
Layout

↓

Components

↓

Pages

↓

API Integration

↓

UX Enhancement
```

Prompt:

```
Create frontend implementation.

Follow:

- UI_UX_GUIDELINES.md
- COMPONENT_LIBRARY.md

Requirements:

- Tailwind CSS
- Responsive
- Dark Mode
- SaaS UI
- Reusable Components
```

---

# Phase 7: Authentication Implementation

Prompt:

```
Implement authentication and RBAC.

Requirements:

- Login
- Session Management
- Roles
- Permissions
- Authorization Middleware
- Audit Logs
```

---

# Phase 8: Testing

Prompt:

```
Review the implementation.

Create test scenarios.

Check:

- CRUD
- Authentication
- Permission
- Validation
- Responsive UI
- Error handling
```

---

# Phase 9: Code Review

Prompt:

```
Act as Senior Code Reviewer.

Review this project.

Find:

- Security issues
- Performance problems
- Architecture violations
- Duplicate code
- Bad practices

Provide fixes.
```

---

# Phase 10: Refactoring

Prompt:

```
Refactor the project.

Improve:

- Code quality
- Performance
- Maintainability
- Security

Do not change business behavior.
```

---

# Feature Development Workflow

For every feature:

```text
Requirement

↓

Analysis

↓

Database Design

↓

Backend

↓

Frontend

↓

Testing

↓

Review

↓

Documentation
```

---

# Example Feature Request

User:

```
Create patient management module.
```

Wrong:

```
Generate patient page.
```

Correct:

```
Analyze patient management module.

Define:

- Database schema
- Repository
- Service
- Controller
- API
- UI components
- Security permission

Create implementation plan first.
```

---

# Prompt Library

---

## Generate New Module

```
Create a new module.

Follow:

- MVC architecture
- Repository Pattern
- Service Layer
- Database Schema
- UI Component Library

Before coding provide implementation plan.
```

---

## Debug Problem

```
Analyze this problem.

Check:

- Error cause
- Architecture impact
- Security impact
- Performance impact

Provide solution before modifying code.
```

---

## Improve UI

```
Improve this UI.

Follow:

- Modern SaaS Design
- Tailwind CSS
- Responsive Design
- Accessibility

Do not change functionality.
```

---

## Optimize Performance

```
Optimize this application.

Check:

- Spreadsheet calls
- Cache usage
- API response
- Frontend rendering

Provide measurable improvements.
```

---

# Agent Rules

Copilot must:

✓ Read documentation first

✓ Explain plan before coding

✓ Follow architecture

✓ Reuse components

✓ Write clean code

✓ Add documentation


Copilot must not:

✗ Generate random structure

✗ Ignore documentation

✗ Create duplicate logic

✗ Put business logic in HTML

✗ Access Sheets from UI

---

# Development Checklist

Before completing feature:

## Architecture

- [ ] MVC followed
- [ ] Service Layer used
- [ ] Repository created

## Backend

- [ ] Validation added
- [ ] Error handling added
- [ ] Logging added

## Frontend

- [ ] Responsive
- [ ] Dark mode
- [ ] Components reused

## Security

- [ ] Authentication checked
- [ ] Permission checked
- [ ] Input validated

## Quality

- [ ] Code reviewed
- [ ] Documentation updated
- [ ] Testing completed

---

# Final Agent Command

Before release:

```
Perform complete project review.

Act as:

- Architect
- Developer
- Security Engineer
- QA Engineer

Verify:

- Architecture
- Code quality
- Security
- Performance
- UI consistency
- Documentation

Fix all issues before release.
```

---

# End of Workflow
