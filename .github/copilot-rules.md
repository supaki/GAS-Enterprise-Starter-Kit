# GitHub Copilot Repository Rules

## GAS Enterprise Starter Kit

Version 2.0

---

# Purpose

This document defines mandatory rules for GitHub Copilot Agent when working inside this repository.

These rules ensure:

- Consistent architecture
- Secure development
- Maintainable code
- Production readiness
- Documentation synchronization

The AI Agent MUST follow these rules.

---

# Rule Priority

When generating or modifying code, follow this priority:
Security Rules

↓

Architecture Rules

↓

Repository Rules

↓

Coding Standards

↓

Feature Requirements

Security and architecture always override convenience.

---

# Rule 01: Documentation First

Before any implementation:

AI MUST review:


.github/copilot-instructions.md

.github/copilot-context.md

.github/copilot-rules.md

docs/README.md

docs/30_AI_CONTEXT.md

docs/PROJECT_RULES.md


For specific tasks, review related documentation.

Examples:

Database:


docs/04_DATABASE_SCHEMA.md


Security:


docs/33_SECURITY_GUIDE.md


Deployment:


docs/34_DEPLOYMENT_GUIDE.md


---

# Rule 02: Analyze Before Coding

AI MUST NOT immediately generate code.

Required process:


Requirement Analysis

↓

Impact Analysis

↓

Implementation Plan

↓

Code Generation


For complex changes:

Ask for approval before implementation.

---

# Rule 03: Respect Existing Architecture

The application MUST follow:


MVC

Service Layer

Repository Pattern


Required flow:


UI

↓

Controller

↓

Service

↓

Repository

↓

Data Source


---

# Rule 04: Separation of Responsibility

Forbidden:

## Controller

Must NOT contain:

- Database queries
- Complex business logic

---

## Service

Must NOT contain:

- UI rendering
- Direct spreadsheet manipulation

---

## Repository

Must NOT contain:

- User interface logic
- Business decisions

---

# Rule 05: File Organization

AI MUST follow:


Existing folder structure


Before creating files:

Check:


docs/09_FOLDER_STRUCTURE.md


Never create:

- Random files
- Duplicate modules
- Unused components

---

# Rule 06: Naming Convention

Use:

## Files


PascalCase


Example:


PatientService.gs

UserRepository.gs


---

## Functions


camelCase


Example:


getPatientList()

validateUser()


---

## Classes


PascalCase


Example:


class PatientService


---

# Rule 07: Code Quality

Generated code MUST:

- Be readable
- Be maintainable
- Include comments
- Include JSDoc
- Handle errors
- Avoid duplication

---

# Rule 08: Google Apps Script Rules

When writing GAS:

Follow:

- V8 Runtime
- ES2022 syntax
- Efficient Spreadsheet operations
- Proper authorization handling


Prefer:


Batch read

↓

Process data

↓

Batch write


Avoid:


Loop

↓

Spreadsheet API call


---

# Rule 09: Google Sheets Database Rules

Never access Sheets directly from UI.

Required:


Service

↓

Repository

↓

Spreadsheet


---

All database operations must include:

- Validation
- Error handling
- Logging

---

# Rule 10: Security Rules

NEVER:

Store:

- Password
- Token
- API Key
- Secret

inside source code.

---

Use:

- Script Properties
- Environment variables
- Secure configuration

---

# Rule 11: Input Validation

All external input MUST be validated.

Examples:

- Form data
- API requests
- User parameters

Validate:

- Type
- Format
- Permission
- Business rules

---

# Rule 12: Authentication Rules

Authentication implementation must include:

- Identity verification
- Session handling
- Access control

---

Never trust:

- Client-side permission
- Hidden UI elements

Authorization must happen server-side.

---

# Rule 13: RBAC Rules

Permission checks MUST exist.

Required flow:


User

↓

Role

↓

Permission

↓

Resource Access


---

Never allow:


Frontend decides permission


---

# Rule 14: API Rules

All APIs must define:

- Request format
- Response format
- Authentication
- Error handling

Standard response:

Success:

```json
{
 "success": true,
 "data": {}
}

Error:

{
 "success": false,
 "message": ""
}
Rule 15: External Integration Rules

External systems:

Example:

MySQL

LINE API

External REST API

Must use:

Service Layer

↓

API Client

↓

External System

Never expose:

Credentials
Internal database
Private endpoints
Rule 16: UI Development Rules

UI must:

Be responsive
Support mobile
Follow design system
Use reusable components

Include when appropriate:

Loading state
Empty state
Error message
Toast notification
Rule 17: Error Handling

Every important function MUST handle errors.

Required:

try {

}

catch(error){

}

Error messages:

Must be:

User friendly
Logged internally

Never expose:

Stack traces
Secrets
Database information
Rule 18: Testing Requirement

Every feature should include:

Functional testing
Error testing
Security testing

Before completion:

Verify:

Requirement

↓

Implementation

↓

Expected Result
Rule 19: Documentation Update

After significant changes:

Update:

README

AI Context

Architecture

API Documentation

Security Documentation

Documentation must match implementation.

Rule 20: Code Review Requirement

Before finalizing:

AI should review:

Architecture
Correct layers
No duplicated logic
Security
No exposed secrets
Permission validation
Quality
Maintainability
Readability
Performance
Efficient operations
Rule 21: Change Management

Before modifying multiple files:

Provide:

Files affected

Reason

Expected impact

Risk

Avoid unnecessary changes.

Rule 22: Production Readiness

Before marking complete:

Confirm:

[ ] Architecture compliant

[ ] Security reviewed

[ ] Error handling complete

[ ] Validation added

[ ] Testing performed

[ ] Documentation updated

[ ] Deployment considered
Rule 23: AI Response Rules

AI responses should include:

Analysis

↓

Plan

↓

Changes

↓

Implementation

↓

Testing

↓

Documentation
Forbidden Actions

AI MUST NOT:

❌ Ignore documentation

❌ Bypass security

❌ Hard-code secrets

❌ Create duplicate architecture

❌ Modify unrelated files

❌ Remove existing features without approval

❌ Generate incomplete placeholder code

Final Rule

The AI Agent must optimize for:

Security

+

Quality

+

Maintainability

+

Scalability

+

Long-term Success

Not only immediate functionality.

End of GitHub Copilot Repository Rules

Version 2.0

GAS Enterprise Starter Kit
