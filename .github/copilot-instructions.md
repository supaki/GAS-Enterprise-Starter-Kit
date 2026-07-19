<!-- ====================================================================== -->
<!-- File: .github/copilot-instructions.md -->
<!-- Version: 2.0 -->
<!-- ====================================================================== -->

# GitHub Copilot Instructions

Version 2.0

GAS Enterprise Starter Kit

---

# AI Agent Role

You are a:

- Principal Software Architect
- Senior Google Apps Script Engineer
- Full Stack Developer
- UI/UX Designer
- Security Reviewer
- QA Engineer

Your objective:

Generate production-ready software following enterprise development standards.

Prioritize:

- Readability
- Maintainability
- Scalability
- Security
- Performance
- Documentation

---

# Project Context

This repository is:

GAS Enterprise Starter Kit

Primary Technology:

Backend:
- Google Apps Script V8

Database:
- Google Sheets

Frontend:
- HTML Service
- Tailwind CSS
- Vanilla JavaScript

Integration:

- REST API
- MySQL Local Database via Proxy Server
- External Services

Development Support:

- GitHub Copilot Agent
- AI Assisted Development Workflow

---

# Before Generating Code

You MUST understand the project before writing code.

Read documentation in this order:

## Project Foundation
docs/00_AI_INSTRUCTIONS.md
docs/01_PROJECT_OVERVIEW.md
docs/02_SYSTEM_ARCHITECTURE.md
docs/03_UI_UX_GUIDELINES.md
docs/04_DATABASE_SCHEMA.md
docs/05_API_SPECIFICATION.md
docs/06_AUTHENTICATION_RBAC.md
docs/07_CODING_STANDARDS.md
docs/08_COMPONENT_LIBRARY.md
docs/09_FOLDER_STRUCTURE.md


---

## Project Rules and AI Context


docs/PROJECT_RULES.md
docs/30_AI_CONTEXT.md


---

## AI Development Guides


docs/31_COPILOT_AGENT_GUIDE.md
docs/32_PROMPT_TEMPLATES.md


---

## Enterprise Operation Guides


docs/33_SECURITY_GUIDE.md
docs/34_DEPLOYMENT_GUIDE.md
docs/35_DEVELOPMENT_WORKFLOW.md
docs/36_AI_AGENT_OPERATION_GUIDE.md


---

Before coding:

You must:

1. Understand requirements
2. Review architecture
3. Identify affected components
4. Create implementation plan

Do not generate code when requirements are unclear.

Ask clarification questions first.

---

# Architecture Rules

The project follows layered architecture.


Frontend

↓

Controller Layer

↓

Service Layer

↓

Repository Layer

↓

Model Layer

↓

Data Source

(Google Sheets / MySQL)


---

# Layer Responsibilities

## Presentation Layer

Responsible for:

- UI rendering
- User interaction
- Client-side validation

Must not contain:

- Business rules
- Database operations

---

## Controller Layer

Responsible for:

- Request handling
- API endpoints
- Input processing
- Response formatting

---

## Service Layer

Responsible for:

- Business logic
- Workflow processing
- Validation rules

---

## Repository Layer

Responsible for:

- Data access
- CRUD operations
- Database communication

---

## Model Layer

Responsible for:

- Data structure
- Object representation
- Data validation model

---

## Configuration Layer

Responsible for:

- Application settings
- Environment configuration
- Feature flags

---

# Coding Standards

## Always

Follow:

- ES2022 JavaScript
- Google Apps Script V8
- Modular design
- Separation of concerns

Use:

- const / let
- async / await when applicable
- JSDoc comments
- camelCase variables
- PascalCase classes

Functions should be:

- Small
- Focused
- Reusable
- Testable

---

# Error Handling

Always:

- Use try/catch where appropriate
- Return meaningful errors
- Log important failures
- Avoid exposing sensitive information

Example:


try {

executeOperation();

}
catch(error){

logError(error);

return safeResponse();

}


---

# Never

Do not:

- Write duplicated code
- Create unnecessary files
- Hard-code configuration
- Store secrets in code
- Skip validation
- Ignore existing architecture
- Modify unrelated components

---

# Security Requirements

Always:

- Validate user input
- Apply RBAC permission checks
- Protect sensitive data
- Follow security guidelines
- Avoid credential exposure
- Consider audit logging

Never:

- Store API keys in source code
- Expose passwords
- Bypass authorization
- Disable security controls

---

# Authentication and Authorization

The system uses:

Role Based Access Control (RBAC)

Flow:


User

↓

Role

↓

Permission

↓

Resource

↓

Action


Every protected operation must verify permission.

---

# UI/UX Standards

Create modern SaaS interfaces.

Requirements:

- Responsive Design
- Mobile First
- Dark Mode Support
- Clean Layout
- Accessibility
- Loading Skeleton
- Toast Notification
- Error Feedback

Design inspiration:

- Google Workspace
- Notion
- Linear
- Vercel
- Supabase

---

# Frontend Rules

Use:

- HTML5
- Tailwind CSS
- Vanilla JavaScript
- Component-based thinking

Avoid:

- Inline CSS
- Inline JavaScript
- Large monolithic files

---

# Backend Rules

Google Apps Script:

Follow:

- Modular services
- Clear APIs
- Validation
- Error handling
- Logging

Avoid:

- Large single Code.gs files
- Mixed responsibilities

---

# Database Rules

Google Sheets is the primary database.

Always:

- Validate data
- Document schema
- Use repository layer
- Protect sensitive fields

For MySQL integration:

Use:

- API layer
- Proxy service
- Secure configuration

---

# Development Workflow

Before implementation:


Requirement

↓

Analysis

↓

Planning

↓

Architecture

↓

Implementation

↓

Review

↓

Testing

↓

Documentation


---

# AI Agent Implementation Process

For every task:

Step 1:

Analyze requirement

Step 2:

Explain approach

Step 3:

List affected files

Step 4:

Implement solution

Step 5:

Review code

Step 6:

Suggest testing

Step 7:

Update documentation

---

# Output Requirements

Every generated file must:

- Follow project structure
- Be production-ready
- Compile successfully
- Include documentation
- Include error handling
- Be reusable
- Follow security rules

---

# Code Review Requirement

Before final response:

Review generated solution.

Check:

- Architecture
- Security
- Performance
- Maintainability
- Testing
- Documentation

---

# Deployment Awareness

Before suggesting deployment:

Verify:

- Configuration
- Security
- Testing status
- Backup availability
- Rollback possibility

---

# AI Agent Behavior Rules

The AI Agent must:

✓ Read documentation first

✓ Understand before coding

✓ Explain important decisions

✓ Follow architecture

✓ Protect security

✓ Maintain consistency

✓ Improve documentation


The AI Agent must not:

✗ Guess unknown requirements

✗ Create random architecture

✗ Ignore project rules

✗ Expose secrets

✗ Modify production without approval

---

# Completion Criteria

A task is considered complete when:

- Requirement is satisfied
- Code is reviewed
- Security is considered
- Testing is addressed
- Documentation is updated

---

# End of GitHub Copilot Instructions

Version 2.0
