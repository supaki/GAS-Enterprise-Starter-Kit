# AI Agent Memory Guide

## GAS Enterprise Starter Kit

Version 1.0

---

# Purpose

This document defines how AI Agents should manage project knowledge, context, and memory when working with this repository.

The purpose is to maintain:

- Consistent AI understanding
- Accurate implementation decisions
- Reduced repeated explanations
- Long-term project continuity

---

# AI Memory Philosophy

AI Agent memory should preserve:
Useful Knowledge

Project Context

Development Decisions

Technical Standards


AI memory should NOT store:


Sensitive Data

Temporary Information

Unverified Assumptions


---

# AI Context Layers

This project uses layered context management.


Permanent Knowledge

    ↓

Project Documentation

    ↓

Session Context

    ↓

Current Task Context


---

# Layer 1: Permanent Project Knowledge

Location:


.github/

docs/


Contains:

- Architecture
- Rules
- Coding standards
- Security policies
- Development workflow

Examples:


.github/copilot-instructions.md

.github/copilot-context.md

.github/copilot-rules.md

docs/30_AI_CONTEXT.md


---

# Layer 2: Documentation Knowledge

Documentation is the official project memory.

Source:


docs/


Important files:


README.md

30_AI_CONTEXT.md

33_SECURITY_GUIDE.md

34_DEPLOYMENT_GUIDE.md

35_DEVELOPMENT_WORKFLOW.md


---

# Layer 3: Session Memory

Session memory contains:

- Current feature
- Current problem
- Current implementation plan
- Current decisions

Example:


Feature:

User Management

Current Status:

Repository completed

Service in progress

Next Step:

Create Controller


---

# Layer 4: Task Context

Task context contains:

- User request
- Current files
- Expected output
- Testing requirements

Example:


Task:

Create patient dashboard

Affected Files:

PatientService.gs

Dashboard.html


---

# AI Memory Priority

When information conflicts:

Follow:

Security Rules

↓

Architecture Documentation

↓

Repository Rules

↓

AI Context

↓

Current Task Request

---

# What AI Should Remember

AI should remember:

## Architecture Decisions

Example:


Application uses:

MVC

Service Layer

Repository Pattern


---

## Technology Decisions

Example:


Backend:

Google Apps Script

Database:

Google Sheets


---

## Coding Standards

Example:


Use:

ES2022

JSDoc

camelCase


---

## Business Rules

Example:


User permissions are controlled by RBAC


---

## Integration Patterns

Example:


GAS

↓

API

↓

External System


---

# What AI Should NOT Remember

Never store:

## Credentials

Examples:


Passwords

API Keys

Tokens

Database Passwords


---

## Personal Data

Examples:


Patient information

Personal identifiers

Private records


---

## Temporary Debug Information

Examples:


Temporary errors

Console logs

Temporary fixes


---

## Unconfirmed Decisions

Never remember:


Maybe use technology X

Temporary workaround

Experimental idea


until officially documented.

---

# Context Update Rules

When a major decision is made:

Update documentation.

Examples:

## Architecture Change

Update:


docs/02_SYSTEM_ARCHITECTURE.md

docs/30_AI_CONTEXT.md


---

## Security Change

Update:


docs/33_SECURITY_GUIDE.md

.github/copilot-rules.md


---

## Workflow Change

Update:


docs/35_DEVELOPMENT_WORKFLOW.md


---

# AI Decision Memory

Important decisions should be documented.

Recommended format:

```markdown
## Decision

Use Repository Pattern for data access.


## Reason

Separate database logic from business logic.


## Impact

All data access must go through Repository Layer.
Context Drift Prevention

AI Context Drift happens when:

Documentation is outdated
Code changes without documentation
Different developers use different patterns

Prevent by:

Code Change

↓

Documentation Update

↓

AI Context Review

↓

Repository Consistency Check
AI Session Restart Procedure

When starting a new session:

Follow:

1. Read .github instructions

↓

2. Load project context

↓

3. Review repository rules

↓

4. Check current documentation

↓

5. Review previous implementation status

↓

6. Continue development
Large Project Memory Strategy

For large systems:

Divide knowledge into:

Core Knowledge

        ↓

Module Knowledge

        ↓

Feature Knowledge

        ↓

Task Knowledge

Example:

Core:

Architecture


Module:

Authentication


Feature:

Login


Task:

Fix validation issue
Module Memory Template

Each module should document:

# Module Name


## Purpose

What this module does.


## Architecture

Where it belongs.


## Dependencies

What it uses.


## Rules

Important constraints.


## Future Changes

Planned improvements.
AI Agent Handoff

When another developer continues work:

Provide:

Current Status

↓

Completed Work

↓

Pending Work

↓

Known Issues

↓

Next Recommended Action

Example:

Current Status:

Authentication module completed.


Completed:

- Login
- RBAC


Pending:

- Password reset


Known Issues:

- Need email integration
AI Knowledge Maintenance

Review periodically:

Monthly

or

After major releases

Check:

Documentation accuracy
Architecture consistency
Security rules
AI instructions
AI Memory Checklist

Before finishing a task:

[ ] Important decisions documented

[ ] Architecture updated if needed

[ ] Security impact reviewed

[ ] Documentation synchronized

[ ] No sensitive information stored
Relationship With Other AI Documents
Document	Purpose
copilot-instructions.md	AI behavior
copilot-context.md	Project context
copilot-rules.md	Enforcement rules
30_AI_CONTEXT.md	Complete knowledge
38_COPILOT_PROMPT_LIBRARY.md	Prompt collection
39_COPILOT_AGENT_EXAMPLES.md	Examples
40_AI_AGENT_INITIALIZATION_PROMPT.md	Session startup
41_AI_AGENT_MEMORY_GUIDE.md	Memory management
Final Principle

AI memory is a tool for consistency.

It should help AI:

Understand Better

+

Build Better

+

Maintain Better

But AI must always rely on:

Documented Knowledge

not

Assumptions
End of AI Agent Memory Guide

Version 1.0

GAS Enterprise Starter Kit
