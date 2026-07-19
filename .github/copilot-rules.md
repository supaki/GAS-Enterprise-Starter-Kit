# GitHub Copilot Repository Rules

## GAS Enterprise Starter Kit

Version 2.1

---

# Purpose

This document defines mandatory rules for GitHub Copilot Agent operating inside this repository.

These rules enforce:

- Architecture consistency
- Security compliance
- Development quality
- Documentation accuracy
- AI Agent workflow consistency

The AI Agent MUST follow these rules.

---

# Rule Priority

When conflicts occur, follow this priority:
Security Rules

↓

Architecture Rules

↓

Repository Rules

↓

Coding Standards

↓

Feature Requirements

Security and architecture always take priority over convenience.

---

# Rule 01: AI Session Initialization

At the beginning of a new AI Agent session:

The AI MUST initialize repository understanding.

Required reading order:


.github/copilot-instructions.md

↓

.github/copilot-context.md

↓

.github/copilot-rules.md

↓

docs/README.md

↓

docs/30_AI_CONTEXT.md

↓

docs/40_AI_AGENT_INITIALIZATION_PROMPT.md


The AI MUST NOT start implementation before initialization is complete.

---

# Rule 02: Initialization Confirmation

After initialization:

AI MUST confirm:


✓ Instructions reviewed

✓ Project context understood

✓ Repository rules loaded

✓ Architecture understood

✓ Documentation structure understood


Then request the development task.

---

# Rule 03: Documentation First

Documentation is the source of truth.

Before modifying code:

Review:


docs/README.md

docs/30_AI_CONTEXT.md

docs/PROJECT_RULES.md


For specific changes:

Database:


docs/04_DATABASE_SCHEMA.md


API:


docs/05_API_SPECIFICATION.md


Security:


docs/33_SECURITY_GUIDE.md


Deployment:


docs/34_DEPLOYMENT_GUIDE.md


---

# Rule 04: Documentation Synchronization

Code and documentation must always match.

After significant changes, update:


README

Architecture Documentation

AI Context

API Documentation

Security Documentation

Deployment Documentation


Never leave documentation outdated.

---

# Rule 05: Source of Truth

The following documents are authoritative.

## AI Behavior


.github/copilot-instructions.md


---

## Project Context


.github/copilot-context.md


---

## Repository Rules


.github/copilot-rules.md


---

## Complete Knowledge Base


docs/30_AI_CONTEXT.md


---

## Documentation Index


docs/README.md


---

# Rule 06: Architecture Compliance

All code MUST follow:


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

# Rule 07: Layer Responsibility

## UI Layer

Allowed:

- Display data
- User interaction
- Client validation


Forbidden:

- Database access
- Business logic

---

## Controller Layer

Allowed:

- Receive requests
- Route operations
- Return responses


Forbidden:

- Direct database operations
- Complex business rules

---

## Service Layer

Responsible for:

- Business logic
- Workflow
- Validation
- Authorization checks

---

## Repository Layer

Responsible for:

- Data access
- Spreadsheet operations
- API communication

---

# Rule 08: File Organization

Before creating files:

Review:


docs/09_FOLDER_STRUCTURE.md


Never:

- Create random files
- Duplicate modules
- Ignore existing components

---

# Rule 09: Coding Standards

Generated code MUST:

Use:


ES2022

const / let

async / await

JSDoc

camelCase

PascalCase classes


Functions should be:

- Small
- Clear
- Testable
- Reusable

---

# Rule 10: Google Apps Script Rules

When developing GAS:

Follow:

- V8 Runtime
- Modular design
- Efficient Spreadsheet operations
- Proper authorization handling

Prefer:


Batch Read

↓

Process Data

↓

Batch Write


Avoid:


Loop

↓

Spreadsheet API Call


---

# Rule 11: Google Sheets Database Rules

Never:


Frontend

↓

Spreadsheet


Required:


Service

↓

Repository

↓

Spreadsheet


Every data operation requires:

- Validation
- Error handling
- Logging

---

# Rule 12: Security Rules

NEVER:

Store in source code:

- Password
- API Key
- Token
- Secret
- Database Credential

Use:

- Script Properties
- Secure configuration

---

# Rule 13: Input Validation

All external input MUST be validated.

Examples:

- Forms
- API requests
- User parameters

Validate:

- Type
- Format
- Permission
- Business rules

---

# Rule 14: Authentication Rules

Authentication must include:

- Identity verification
- Session handling
- Secure access

Never trust:

- Client-side authentication
- Hidden UI elements

---

# Rule 15: RBAC Rules

Authorization must be server-side.

Required:


User

↓

Role

↓

Permission

↓

Resource

↓

Action


Never allow:


Frontend controls permission


---

# Rule 16: API Rules

Every API must define:

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
Rule 17: External Integration Rules

External systems:

Examples:

MySQL

LINE API

REST API

Must use:

Service Layer

↓

API Client

↓

External System

Never expose internal systems directly.

Rule 18: UI/UX Rules

UI must follow:

Responsive design
Mobile First
Accessibility
Reusable components

Include when appropriate:

Loading state
Empty state
Error state
Toast notification
Rule 19: Change Impact Analysis

Before major modifications:

AI MUST provide:

Files affected

Reason

Architecture impact

Security impact

Testing approach

Deployment impact
Rule 20: Debugging Rules

Do not immediately change code.

Analyze:

Problem

↓

Root Cause

↓

Impact

↓

Solution

↓

Fix
Rule 21: Code Review Rules

When reviewing code:

Check:

Architecture
Correct layers
Separation of concerns
Security
No secrets
Permission checks
Quality
Maintainability
Readability
Performance
Efficient operations
Rule 22: Testing Rules

Before completion:

Verify:

Requirement

↓

Implementation

↓

Expected Result

Consider:

Functional testing
Error testing
Security testing
Rule 23: Production Readiness

A task is complete only when:

[ ] Requirement understood

[ ] Architecture followed

[ ] Security reviewed

[ ] Error handling complete

[ ] Validation implemented

[ ] Testing considered

[ ] Documentation updated

[ ] Deployment impact reviewed
Rule 24: Forbidden Actions

AI MUST NOT:

❌ Skip initialization

❌ Ignore documentation

❌ Break architecture

❌ Hard-code secrets

❌ Duplicate existing modules

❌ Modify unrelated files

❌ Remove features without approval

❌ Generate incomplete placeholder code

Rule 25: AI Response Format

For development tasks, prefer:

## Analysis

Understanding


## Plan

Approach


## Changes

Affected files


## Implementation

Code changes


## Testing

Verification


## Documentation

Updates
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

Enterprise Readiness

The objective is not only to make software work.

The objective is to build software that can be maintained and trusted long term.

End of GitHub Copilot Repository Rules

Version 2.1

GAS Enterprise Starter Kit
