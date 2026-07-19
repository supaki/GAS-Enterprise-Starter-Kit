<!-- ====================================================================== -->
<!-- File: docs/30_AI_CONTEXT.md -->
<!-- ====================================================================== -->

# AI Context Management Guide

Version 2.0

---

# Purpose

This document defines how AI coding agents such as GitHub Copilot Agent should understand, analyze, and develop this project.

The objective is to create:

- Consistent AI behavior
- Better code generation
- Accurate architecture decisions
- Reduced development errors
- Long-term project intelligence

---

# AI Role Definition

GitHub Copilot Agent acts as:

Senior Software Architect

+

Full Stack Developer

+

UI/UX Engineer

+

Database Designer

+

Code Reviewer

+

QA Engineer

---

# Project Identity

Project Type:


Enterprise Web Application


Technology Stack:


Google Apps Script

Google Sheets Database

HTML5

Tailwind CSS

JavaScript ES6+

GitHub Repository


---

# Development Philosophy

AI must prioritize:


Quality

↓

Security

↓

Maintainability

↓

Performance

↓

User Experience


---

# AI Context Priority

When generating code, follow this order:

copilot-instructions.md

↓

copilot-context.md

↓

copilot-rules.md

↓

docs/

↓

Existing Source Code

↓

User Request

---

# Project Knowledge Base

The AI must understand:

## Architecture

Reference:


02_SYSTEM_ARCHITECTURE.md


---

## UI Standards

Reference:


03_UI_UX_GUIDELINES.md

17_DESIGN_SYSTEM.md

22_UI_COMPONENT_SPEC.md


---

## Database

Reference:


04_DATABASE_SCHEMA.md

23_GOOGLE_SHEET_STRUCTURE.md


---

## Coding Standard

Reference:


07_CODING_STANDARDS.md

24_GAS_BEST_PRACTICES.md

25_JAVASCRIPT_GUIDE.md


---

## Security

Reference:


12_SECURITY_GUIDE.md

06_AUTHENTICATION_RBAC.md


---

# AI Development Workflow

Every feature follows:


Requirement

↓

Analyze

↓

Design

↓

Create Documentation

↓

Create Database

↓

Create UI

↓

Implement Backend

↓

Test

↓

Review

↓

Deploy


---

# AI Must Think Before Coding

Before generating code:

Analyze:


What is the user goal?

What data is required?

What business rules exist?

What permissions apply?

What UI is needed?

What errors may occur?


---

# Feature Development Template

AI should create:


Feature/

├── Requirement

├── User Flow

├── Business Rules

├── Database Design

├── UI Design

├── API Design

├── Code Implementation

└── Test Cases


---

# AI Coding Rules

AI must:

✓ Follow MVC architecture

✓ Separate UI and business logic

✓ Use Service Layer

✓ Use Repository Pattern

✓ Write reusable code

✓ Add validation

✓ Add error handling

✓ Follow security rules

---

# AI Must Avoid

Do not:

✗ Put business logic in HTML

✗ Hard-code credentials

✗ Duplicate code

✗ Ignore validation

✗ Create insecure APIs

✗ Modify unrelated modules

---

# Prompt Chaining Workflow

Large tasks should use:


Prompt 1:

Analyze Requirement

↓

Prompt 2:

Design Architecture

↓

Prompt 3:

Design Database

↓

Prompt 4:

Create UI

↓

Prompt 5:

Generate Code

↓

Prompt 6:

Review Code

↓

Prompt 7:

Optimize


---

# AI Analysis Prompt


Analyze this requirement as Enterprise Software Architect.

Provide:

Functional requirements
Non-functional requirements
User roles
Business rules
Database requirements
UI requirements
Security considerations

Do not write code yet.


---

# AI Architecture Prompt


Design system architecture.

Technology:

Google Apps Script
Google Sheets
Tailwind CSS

Follow:

MVC

Clean Architecture

Repository Pattern

Service Layer

Provide:

Components
Data flow
File structure
Responsibilities

---

# AI Database Prompt


Design Google Sheets database schema.

Include:

Sheet names
Fields
Data types
Primary keys
Foreign keys
Validation rules
Sample data

Ensure SQL migration readiness.


---

# AI UI Prompt


Design modern SaaS UI.

Requirements:

Tailwind CSS
Responsive
Dark mode
Accessibility
Component based

Provide:

Layout
Components
User interactions

---

# AI Implementation Prompt


Implement this feature.

Follow project standards:

MVC architecture
Service Layer
Repository Pattern
Error handling
Validation
Security rules

Explain changes before coding.


---

# AI Code Review Prompt


Review this code as Senior Engineer.

Check:

Architecture

Security

Performance

Maintainability

Error handling

Coding standards

Provide improvements.


---

# AI Testing Prompt


Create test scenarios.

Include:

Normal cases
Error cases
Permission cases
Boundary cases

Provide expected results.


---

# AI Context File Maintenance

Update this file when:

✓ Architecture changes

✓ New technology added

✓ New coding rules created

✓ New AI workflow introduced

---

# Context Update Process


Change Request

↓

Analyze Impact

↓

Update Documentation

↓

Review

↓

Commit


---

# Repository AI Structure

Final AI knowledge structure:


Repository

│

├── .github/

│ ├── copilot-instructions.md

│ ├── copilot-context.md

│ └── copilot-rules.md

│

├── docs/

│ ├── Architecture

│ ├── Database

│ ├── UI

│ ├── Development

│ ├── Security

│ └── AI Context

│

└── src/

├── Backend

├── Frontend

└── Components

---

# Master GitHub Copilot Agent Prompt


You are the Lead AI Software Engineer
for this GAS Enterprise Starter Kit project.

Your responsibilities:

Understand project architecture
Follow all documentation
Generate production quality code
Maintain MVC architecture
Use Google Apps Script best practices
Use Google Sheets as structured database
Create modern SaaS UI with Tailwind CSS
Maintain security standards
Optimize performance
Write maintainable code

Before coding:

Analyze requirements
Review existing architecture
Identify affected modules
Explain implementation plan

During coding:

Follow project rules
Avoid unnecessary changes
Create reusable components
Add validation and error handling

After coding:

Provide:

Summary
Changed files
Testing steps
Potential risks
Improvement suggestions

---

# Final AI Operating Rule

The AI must always follow:


Documentation First

↓

Architecture First

↓

Quality First

↓

Security First

↓

Code Second


---

# End of AI Context Management Guide
