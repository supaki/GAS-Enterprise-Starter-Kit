<!-- ====================================================================== -->
<!-- File: .github/copilot-rules.md -->
<!-- Version: 2.0 -->
<!-- ====================================================================== -->

# GitHub Copilot Development Rules

Version 2.0

GAS Enterprise Starter Kit

---

# Purpose

This document defines mandatory development rules for AI Agent and developers.

Rules apply to:

- Code generation
- Code modification
- Architecture decisions
- Security implementation
- Documentation updates

---

# General Rules

Always:

✓ Understand requirements first

✓ Follow repository architecture

✓ Reuse existing patterns

✓ Keep changes focused

✓ Document important decisions


Never:

✗ Create unnecessary complexity

✗ Ignore existing code structure

✗ Modify unrelated files

✗ Hard-code sensitive information

---

# File Organization Rules

Follow:
Feature

├── Controller

├── Service

├── Repository

├── Model

├── UI

└── Documentation


---

# Naming Convention

## JavaScript Variables

Use:

camelCase

Example:

```javascript
userProfile
patientData
Classes

Use:

PascalCase

Example:

UserService
ReportController
Functions

Use:

Verb + Description

Example:

getUserData()

createReport()

validatePermission()
JavaScript Rules

Use:

ES2022
const
let
Arrow Functions
Async/Await

Avoid:

var
Global variables
Duplicate functions
Google Apps Script Rules

Organize code:

Code.gs

↓

Controllers

↓

Services

↓

Repositories

↓

Utilities

Avoid:

Single large script file
Mixed responsibilities
Frontend Rules

Use:

HTML5
Tailwind CSS
Vanilla JavaScript

Must support:

Responsive design
Mobile first
Accessibility

Avoid:

Inline CSS
Inline JavaScript
Duplicate components
Database Rules

Google Sheets:

Must:

Define schema
Validate data
Use Repository layer
Protect sensitive columns

Never:

Access sheets directly from UI
Delete data without validation
API Rules

API must include:

Validation
Error handling
Response format
Logging

Example response:

{
 "success": true,
 "data": {}
}
Security Rules

Mandatory:

Validate input
Check authorization
Protect secrets
Log important actions

Never:

Commit credentials
Expose tokens
Skip permission checks
Authentication Rules

All protected features must:

Verify:

User

↓

Role

↓

Permission

↓

Action
Error Handling Rules

Always:

Catch errors
Return safe messages
Log details internally

Never:

Display system errors directly
Hide important failures
Testing Rules

Every feature should consider:

Unit Testing
Integration Testing
User Acceptance Testing
Documentation Rules

Update documentation when:

Adding feature
Changing architecture
Changing API
Changing database
Changing workflow
Git Rules

Commit format:

type: description

Allowed types:

feat
fix
docs
refactor
test
security

Example:

feat: add user dashboard
Deployment Rules

Before deployment:

Check:

Testing complete
Security reviewed
Backup available
Configuration verified
AI Agent Rules

AI Agent must:

✓ Explain plan before major changes

✓ Identify affected files

✓ Follow architecture

✓ Review generated code

✓ Suggest tests

AI Agent must not:

✗ Deploy without approval

✗ Change architecture silently

✗ Remove security controls

✗ Generate incomplete code

Quality Standard

Generated code must be:

Readable
Maintainable
Secure
Tested
Documented
End of Copilot Rules

Version 2.0
