<!-- ====================================================================== -->
<!-- File: docs/30_AI_CONTEXT.md -->
<!-- ====================================================================== -->

# AI Context Management Guide

Version 3.0 Enterprise Edition

GAS Enterprise Starter Kit

---

# Purpose

This document serves as the primary AI knowledge base for the GAS Enterprise Starter Kit repository.

Its purpose is to provide GitHub Copilot Agent and other AI coding assistants with a complete understanding of the project, including its architecture, development philosophy, business context, coding standards, and operational workflows.

The objectives are:

- Provide consistent AI behavior
- Improve architectural understanding
- Maintain development consistency
- Reduce implementation errors
- Preserve long-term project knowledge
- Enable scalable AI-assisted development

This document should be considered the **single source of truth** for AI context across the repository.

---

# AI Identity

When operating inside this repository, GitHub Copilot Agent shall assume the following professional roles:

- Principal Software Architect
- Enterprise Solution Architect
- Senior Google Apps Script Engineer
- Full Stack Web Developer
- Backend API Engineer
- Frontend UI/UX Engineer
- Google Workspace Specialist
- Database Designer
- Security Engineer
- DevOps Advisor
- QA Engineer
- Technical Writer

The AI Agent must work as an experienced software engineering team member rather than a simple code generator.

---

# AI Mission

The AI Agent exists to assist developers throughout the entire software development lifecycle.

Its responsibilities include:

- Understanding business requirements
- Designing maintainable architectures
- Producing production-ready code
- Reviewing code quality
- Identifying potential risks
- Improving security
- Generating documentation
- Supporting testing
- Assisting deployment planning
- Preserving project knowledge

The AI Agent should always optimize for long-term maintainability instead of short-term implementation speed.

---

# Project Identity

Project Name

GAS Enterprise Starter Kit

Project Type

Enterprise Web Application Framework

Primary Platform

Google Apps Script

Primary Database

Google Sheets

Supported Integrations

- REST API
- MySQL
- Local Proxy Server
- External APIs
- Google Workspace Services

Primary Goal

Provide a reusable enterprise application framework for rapidly developing secure, maintainable, and scalable web applications using Google Apps Script.

---

# Repository Vision

This repository is intended to become a reusable enterprise starter kit that enables developers to build multiple applications from a common architecture.

Examples include:

- Hospital Information Systems
- Primary Care Applications
- Internal Organization Portals
- Dashboard Systems
- Inventory Management
- HR Systems
- CRM Applications
- Workflow Automation
- Research Management
- Government Information Systems

Every implementation should reuse the same architecture, standards, and development workflow.

---

# Repository Philosophy

The project follows these core principles:

## 1. Simplicity

Solutions should remain easy to understand.

Avoid unnecessary complexity.

---

## 2. Maintainability

Every component should be maintainable by future developers.

Readable code is preferred over clever code.

---

## 3. Scalability

The architecture should support future expansion without requiring significant redesign.

---

## 4. Security

Security must be considered from the beginning of every implementation.

Security is never treated as an afterthought.

---

## 5. Reusability

Components should be reusable whenever possible.

Avoid duplicate implementations.

---

## 6. Documentation First

Documentation is considered part of the software.

Code without documentation is considered incomplete.

---

## 7. AI-Assisted Development

AI should accelerate development while maintaining engineering quality.

Human developers remain responsible for architecture decisions, business validation, and production approval.

---

# AI Operating Principles

Before generating code, the AI Agent shall:

1. Understand the business objective.

2. Read relevant documentation.

3. Analyze the existing architecture.

4. Identify affected components.

5. Evaluate security implications.

6. Consider performance.

7. Consider maintainability.

8. Create an implementation plan.

Only after these steps should implementation begin.

---

# Repository Knowledge Hierarchy

The repository is organized into multiple knowledge layers.

```text
Project Vision

↓

Architecture

↓

Business Rules

↓

Development Standards

↓

Security

↓

Implementation

↓

Testing

↓

Deployment

↓

Operation
```

The AI Agent should understand higher-level concepts before making lower-level implementation decisions.

---

# AI Context Priority

When multiple sources provide information, use the following priority order:

1. User requirements

2. Repository documentation

3. Project rules

4. Existing architecture

5. Existing implementation

6. Industry best practices

If conflicts exist, the AI Agent should explain the conflict and request clarification instead of making assumptions.

---

# AI Success Criteria

The AI Agent is considered successful when it can:

- Understand the project before coding.
- Produce maintainable solutions.
- Follow repository standards.
- Preserve architectural consistency.
- Improve developer productivity.
- Reduce technical debt.
- Maintain security.
- Keep documentation synchronized.

These goals take precedence over generating code quickly.

---

# End of Part 1

---

# Technology Stack

The GAS Enterprise Starter Kit is built using a modern, modular, and maintainable technology stack designed for enterprise web applications.

The technology stack has been selected to maximize:

- Maintainability
- Scalability
- Security
- Performance
- Ease of Deployment
- Google Workspace Integration

---

# Primary Technology Stack

| Layer | Technology |
|---------|------------|
| Frontend | HTML5 |
| Styling | Tailwind CSS |
| Client Script | Vanilla JavaScript (ES2022) |
| Backend | Google Apps Script V8 |
| Primary Database | Google Sheets |
| Authentication | Google Session + RBAC |
| Charts | Chart.js |
| Icons | Material Symbols |
| API | REST API |
| External Database | MySQL (Optional) |
| Proxy | Node.js + Express |
| Version Control | Git + GitHub |
| AI Development | GitHub Copilot Agent |

---

# Technology Principles

Every technology used within this repository should satisfy the following goals:

- Easy to maintain
- Enterprise ready
- Modular
- Well documented
- AI friendly
- Secure by design

Avoid introducing technologies that increase unnecessary complexity.

---

# Enterprise Architecture Overview

The project follows a layered architecture.

Each layer has one responsibility.

Responsibilities must never overlap.

```text
Presentation Layer

↓

Controller Layer

↓

Service Layer

↓

Repository Layer

↓

Model Layer

↓

Data Source Layer
```

Each layer communicates only with adjacent layers.

---

# Layer Responsibilities

## Presentation Layer

Responsible for:

- User Interface
- User Experience
- Form Validation
- Client Interaction

Technology:

- HTML Service
- Tailwind CSS
- JavaScript

Presentation must never:

- Execute business logic
- Access Google Sheets directly
- Call database APIs directly

---

## Controller Layer

Responsible for:

- Receiving requests
- Routing
- Input processing
- Response formatting

Controllers coordinate application flow.

Controllers must remain lightweight.

Controllers should never contain business logic.

---

## Service Layer

Responsible for:

- Business rules
- Workflow
- Validation
- Process execution

The Service Layer is the heart of the application.

Most application logic belongs here.

Services should:

- Be reusable
- Be testable
- Be independent from UI

---

## Repository Layer

Responsible for:

- Reading data
- Writing data
- CRUD operations
- Query abstraction

Repositories isolate the data source from business logic.

Changing the database should require minimal Service changes.

---

## Model Layer

Models represent business entities.

Examples:

- User
- Patient
- Appointment
- Product
- Inventory
- Report

Models define:

- Structure
- Validation
- Relationships

Models should not contain presentation logic.

---

## Data Source Layer

Supported data sources:

Primary:

- Google Sheets

Optional:

- MySQL
- REST API
- External Services

Repositories communicate with Data Sources.

Services never communicate with databases directly.

---

# MVC Architecture

The project follows MVC principles.

```text
View

↓

Controller

↓

Model

↓

Repository

↓

Database
```

Views contain presentation.

Controllers handle requests.

Models represent business entities.

Repositories manage persistence.

---

# Repository Pattern

The Repository Pattern separates business logic from storage.

Benefits:

- Easy testing
- Easy maintenance
- Database independence
- Cleaner architecture

Example responsibilities:

UserRepository

- findAll()

- findById()

- save()

- update()

- delete()

---

# Service Pattern

Services coordinate application workflows.

Example:

AppointmentService

Responsibilities:

- Validate appointment
- Check duplicate booking
- Save appointment
- Send notification

Services should not know how data is stored.

---

# Controller Pattern

Controllers are application entry points.

Example:

PatientController

Responsibilities:

- Receive request
- Validate request
- Call service
- Return response

Controllers should contain minimal logic.

---

# UI Component Architecture

The frontend should be component-oriented.

Example:

```text
Dashboard

├── Sidebar

├── Navbar

├── Cards

├── Charts

├── Tables

├── Forms

└── Dialogs
```

Components should:

- Be reusable
- Be independent
- Be responsive

---

# Folder Architecture

Recommended structure:

```text
src/

├── controllers/

├── services/

├── repositories/

├── models/

├── views/

├── components/

├── utils/

├── config/

└── assets/
```

Each folder has a clearly defined purpose.

---

# Google Apps Script Architecture

Recommended Apps Script structure:

```text
Apps Script

├── Code.gs

├── Router.gs

├── Controllers/

├── Services/

├── Repositories/

├── Models/

├── Utilities/

├── Config/

└── API/
```

Avoid placing all logic inside a single `Code.gs` file.

---

# Google Sheets Architecture

Google Sheets acts as the primary database.

Each worksheet represents a logical entity.

Example:

```text
Spreadsheet

├── Users

├── Roles

├── Permissions

├── Settings

├── AuditLogs

├── Products

└── Transactions
```

Each sheet must have:

- Defined schema
- Primary key
- Validation rules
- Documentation

---

# MySQL Integration Architecture

When external databases are required:

```text
Google Apps Script

↓

REST API

↓

Node.js Proxy

↓

MySQL
```

The AI Agent must never bypass the API layer.

All communication with MySQL should occur through secure APIs.

---

# External API Architecture

External systems communicate using REST APIs.

Example:

```text
Application

↓

API Client

↓

REST API

↓

External Service
```

External APIs should:

- Use authentication
- Validate responses
- Handle errors
- Retry when appropriate

---

# Data Flow Architecture

Standard application flow:

```text
User

↓

UI

↓

Controller

↓

Service

↓

Repository

↓

Database

↓

Repository

↓

Service

↓

Controller

↓

UI
```

The flow should remain consistent across the entire project.

---

# Dependency Direction

Dependencies always flow downward.

```text
UI

↓

Controller

↓

Service

↓

Repository

↓

Database
```

Lower layers must never depend on upper layers.

---

# Separation of Concerns

Each module should have only one primary responsibility.

Examples:

Good:

- UserService handles users
- ProductService handles products
- ReportService handles reports

Avoid:

Large "Utility" classes that perform unrelated operations.

---

# Scalability Principles

The architecture should support:

- Additional modules
- New databases
- API expansion
- Authentication providers
- Reporting engines

without major redesign.

---

# AI Architecture Awareness

Before implementing any feature, the AI Agent should determine:

- Which layer is affected?
- Which modules are impacted?
- Which services require modification?
- Which repositories are involved?
- Which documentation requires updating?

The AI Agent must preserve architectural consistency throughout development.

---

# End of Part 2

---

# Development Principles

The GAS Enterprise Starter Kit follows modern enterprise software engineering practices.

Every feature should be designed to be:

- Maintainable
- Testable
- Reusable
- Secure
- Scalable
- Well documented

Development decisions should always prioritize long-term sustainability over short-term convenience.

---

# Software Engineering Philosophy

The repository adopts the following engineering philosophy.

## Simplicity

Prefer simple solutions.

Avoid unnecessary abstraction.

Simple code is easier to maintain.

---

## Consistency

The same problem should always be solved using the same architectural approach.

Consistent code is easier for:

- Developers
- Reviewers
- AI Agents

to understand.

---

## Reusability

Whenever possible:

- Reuse components
- Reuse services
- Reuse utilities
- Reuse UI elements

Avoid duplicate implementations.

---

## Maintainability

Every implementation should remain understandable years later.

Future developers should be able to modify the project without rewriting the architecture.

---

## Scalability

New features should extend the existing architecture rather than replace it.

The framework should support gradual growth.

---

## Documentation First

Documentation is considered part of the software.

Every important architectural decision should be documented.

Code without documentation is considered incomplete.

---

# Coding Philosophy

Code should be written for humans first.

The compiler only needs correctness.

Developers need readability.

AI Agents should generate code that is:

- Clear
- Predictable
- Consistent
- Self-explanatory

---

# Clean Code Principles

The project follows Clean Code principles.

## Functions

Functions should:

- Perform one task
- Be short
- Have descriptive names
- Avoid side effects

Prefer:

```javascript
calculateTotal()
```

instead of

```javascript
calc()
```

---

## Variables

Variable names should describe their purpose.

Good:

```javascript
patientName
appointmentDate
totalAmount
```

Avoid:

```javascript
a
b
tmp
data1
```

---

## Constants

Use named constants instead of magic numbers.

Example:

```javascript
const MAX_LOGIN_ATTEMPTS = 5;
```

Avoid:

```javascript
if (attempts > 5)
```

---

## Comments

Comments should explain:

WHY

not

WHAT

Good:

```javascript
// Prevent duplicate appointments
```

Avoid:

```javascript
// Increment i
i++;
```

---

# Modular Development

The project encourages modular architecture.

Each module should encapsulate one business capability.

Examples:

- User Module
- Authentication Module
- Dashboard Module
- Reporting Module
- Inventory Module

Each module should include:

- Controller
- Service
- Repository
- Model
- UI Components
- Documentation

---

# Feature Development Strategy

Every feature should follow the same lifecycle.

```text
Requirement

↓

Analysis

↓

Planning

↓

Design

↓

Implementation

↓

Testing

↓

Documentation

↓

Deployment
```

Skipping steps is discouraged.

---

# Requirement Analysis

Before coding, the AI Agent should answer:

- What problem is being solved?
- Who will use this feature?
- What business rule applies?
- What data is required?
- What systems are affected?
- What risks exist?

Only after understanding the requirement should implementation begin.

---

# Planning Principles

Every implementation should begin with a plan.

The plan should include:

- Scope
- Architecture
- Affected files
- Dependencies
- Testing approach
- Documentation updates

The AI Agent should explain the plan before generating code.

---

# Code Organization

Files should remain focused.

Example:

```text
User Module

├── UserController

├── UserService

├── UserRepository

├── UserModel

└── user.html
```

Avoid combining multiple unrelated features into a single file.

---

# Reuse Before Create

Before creating new code, the AI Agent should determine whether:

- Similar logic already exists.
- Existing utilities can be reused.
- Existing components can be extended.
- Existing services can be enhanced.

Duplicate implementations should be avoided.

---

# Error Handling Philosophy

Errors should be:

- Detected early
- Logged appropriately
- Presented safely to users

Internal errors should never expose sensitive information.

---

# Validation Strategy

Validation should occur at multiple levels.

## Client-side Validation

Purpose:

- Improve user experience
- Reduce invalid submissions

---

## Server-side Validation

Purpose:

- Protect business logic
- Enforce business rules
- Prevent malicious input

Server-side validation is mandatory.

---

# Security by Design

Security should be integrated into every feature.

Consider:

- Authentication
- Authorization
- Input validation
- Output encoding
- Audit logging
- Data protection

The AI Agent should never treat security as optional.

---

# Performance Principles

Optimize only after correctness.

Focus on:

- Efficient data access
- Reusable queries
- Minimal API calls
- Reduced duplicate processing

Avoid premature optimization.

---

# Configuration Management

Configuration should be separated from implementation.

Examples:

- Spreadsheet IDs
- API URLs
- Feature Flags
- System Settings

Configuration should never be hard-coded into business logic.

---

# Dependency Management

Dependencies should remain minimal.

Before introducing a new dependency, evaluate:

- Business value
- Maintenance cost
- Security risk
- Compatibility
- Licensing

Prefer built-in platform capabilities whenever possible.

---

# Testing Philosophy

Every feature should be testable.

Testing should include:

- Happy path
- Invalid input
- Edge cases
- Security scenarios
- Error handling

The AI Agent should recommend appropriate test cases.

---

# Documentation Standards

Documentation should evolve with the code.

Whenever architecture changes:

Update:

- Architecture documents
- API documentation
- Workflow guides
- AI Context
- README files

Documentation and implementation should remain synchronized.

---

# AI Collaboration Principles

The AI Agent collaborates with developers.

The workflow is:

```text
Human Requirement

↓

AI Analysis

↓

AI Plan

↓

Human Review

↓

AI Implementation

↓

Human Validation

↓

Deployment
```

The AI Agent should never assume final authority over architectural decisions.

---

# Decision-Making Framework

When multiple implementation options exist, prioritize:

1. Simplicity
2. Maintainability
3. Reusability
4. Security
5. Performance

Explain trade-offs when recommending a solution.

---

# Repository Evolution

The repository is expected to grow over time.

Future enhancements may include:

- Additional application modules
- External databases
- Cloud integrations
- Mobile applications
- AI-powered automation
- Analytics platforms

The architecture should accommodate future growth without significant redesign.

---

# Continuous Improvement

After every completed feature, evaluate:

- What worked well?
- What can be simplified?
- What documentation should be updated?
- What reusable components were created?
- What lessons should be captured?

Continuous improvement is an ongoing process.

---

# AI Development Principles

Before every implementation, the AI Agent should:

✓ Read the relevant documentation.

✓ Understand the architecture.

✓ Review existing code.

✓ Explain the implementation plan.

✓ Consider security implications.

✓ Recommend testing.

✓ Update documentation if required.

These principles apply to all development activities within the repository.

---

# End of Part 3

---

# Repository Structure

The repository follows a standardized enterprise structure.

Every directory has a clearly defined responsibility.

The AI Agent should preserve this structure when creating new files.

```text
Repository

├── .github/
│
├── docs/
│
├── src/
│
├── tests/
│
├── config/
│
├── assets/
│
├── scripts/
│
├── README.md
│
└── .gitignore
```

New folders should only be introduced when they provide clear architectural value.

---

# Repository Directory Responsibilities

## .github

Contains AI and GitHub-related configuration.

Examples:

- Copilot Instructions
- Copilot Context
- Copilot Rules
- Issue Templates
- Pull Request Templates
- GitHub Workflows

The AI Agent should always consult this directory before development.

---

## docs

Contains all project documentation.

Documentation represents the knowledge layer of the repository.

Changes to architecture, workflow, or business rules should be reflected here.

---

## src

Contains application source code.

Recommended organization:

```text
src/

├── controllers/

├── services/

├── repositories/

├── models/

├── views/

├── components/

├── utilities/

├── config/
```

Source code should never be mixed with documentation.

---

## tests

Contains testing resources.

Examples:

- Unit Tests
- Integration Tests
- Test Data
- Mock Objects

---

## config

Contains project configuration.

Examples:

- Environment Settings
- Constants
- Application Configuration
- Feature Flags

Configuration should remain independent from business logic.

---

## assets

Contains static resources.

Examples:

- Images
- Icons
- Fonts
- CSS
- JavaScript Libraries

---

## scripts

Contains development utilities.

Examples:

- Deployment scripts
- Build scripts
- Data migration
- Backup utilities

---

# Repository Knowledge Model

The repository consists of multiple knowledge layers.

```text
Project Vision

↓

Business Knowledge

↓

Architecture Knowledge

↓

Development Knowledge

↓

Security Knowledge

↓

Deployment Knowledge

↓

Operational Knowledge
```

The AI Agent should understand higher-level knowledge before implementing lower-level details.

---

# Documentation Knowledge Base

Documentation serves as the institutional memory of the project.

Every important decision should be documented.

The documentation is organized into logical groups.

---

# Phase 1 — Foundation Documentation

Purpose:

Define the project fundamentals.

Files include:

```text
00_AI_INSTRUCTIONS.md

01_PROJECT_OVERVIEW.md

02_SYSTEM_ARCHITECTURE.md

03_UI_UX_GUIDELINES.md

04_DATABASE_SCHEMA.md

05_API_SPECIFICATION.md

06_AUTHENTICATION_RBAC.md

07_CODING_STANDARDS.md

08_COMPONENT_LIBRARY.md

09_FOLDER_STRUCTURE.md
```

These files establish the project's core architecture.

---

# Phase 2 — Development Documentation

Purpose:

Describe implementation details.

Examples:

```text
10_*

↓

29_*
```

These documents define:

- User Flows
- Business Rules
- Data Mapping
- UI Specifications
- API Usage
- Functional Requirements

---

# Phase 3 — AI Knowledge Base

Purpose:

Provide AI with repository-wide understanding.

Files:

```text
30_AI_CONTEXT.md

31_COPILOT_AGENT_GUIDE.md

32_PROMPT_TEMPLATES.md
```

These documents explain:

- AI context
- Prompt engineering
- AI development workflow

---

# Phase 4 — Enterprise Operations

Purpose:

Support production-ready development.

Files:

```text
33_SECURITY_GUIDE.md

34_DEPLOYMENT_GUIDE.md

35_DEVELOPMENT_WORKFLOW.md

36_AI_AGENT_OPERATION_GUIDE.md

37_REPOSITORY_SETUP_GUIDE.md
```

These documents define:

- Security
- Deployment
- Workflow
- AI Operations
- Repository Setup

---

# Documentation Dependency Map

Documentation should be read in dependency order.

```text
Repository Setup

↓

Project Overview

↓

Architecture

↓

Database

↓

API

↓

Coding Standards

↓

Business Rules

↓

AI Context

↓

AI Guides

↓

Development Workflow

↓

Deployment
```

Skipping prerequisite documents may result in incorrect implementation.

---

# AI Reading Order

Before implementing any feature, the AI Agent should review documents in the following sequence.

## Step 1

Repository Configuration

```text
.github/

copilot-instructions.md

↓

copilot-context.md

↓

copilot-rules.md
```

---

## Step 2

Repository Documentation

```text
docs/README.md
```

---

## Step 3

Project Foundation

```text
00

↓

09
```

---

## Step 4

Project Rules

```text
PROJECT_RULES.md
```

---

## Step 5

AI Context

```text
30_AI_CONTEXT.md
```

---

## Step 6

AI Development Guides

```text
31

↓

32
```

---

## Step 7

Enterprise Guides

```text
33

↓

37
```

---

# Context Synchronization

All documentation should remain synchronized.

When architecture changes:

Update:

- AI Context
- Architecture Guide
- README
- Development Workflow
- Copilot Context

When security changes:

Update:

- Security Guide
- Project Rules
- Copilot Rules

When deployment changes:

Update:

- Deployment Guide
- Repository Setup Guide

The AI Agent should recommend documentation updates whenever implementation affects repository knowledge.

---

# Repository Memory Model

The repository should be viewed as a persistent knowledge system.

Knowledge is divided into:

## Static Knowledge

Rarely changes.

Examples:

- Architecture
- Folder Structure
- Coding Standards
- Design Principles

---

## Dynamic Knowledge

Changes frequently.

Examples:

- Features
- Business Rules
- APIs
- Database Schema
- Workflows

---

## Operational Knowledge

Supports deployment and maintenance.

Examples:

- Security
- Deployment
- Monitoring
- Maintenance

---

# Repository Knowledge Graph

The relationship between documents can be represented as follows.

```text
README

↓

Project Overview

↓

Architecture

↓

Database

↓

API

↓

Coding Standards

↓

Business Rules

↓

AI Context

↓

AI Development

↓

Security

↓

Deployment

↓

Operations
```

Every implementation should fit into this knowledge graph.

---

# AI Context Synchronization Rules

Whenever a significant change occurs, determine whether the following documents require updates:

- README.md
- PROJECT_RULES.md
- 30_AI_CONTEXT.md
- Security Guide
- Deployment Guide
- Development Workflow
- Copilot Context
- Copilot Rules

Documentation consistency is considered part of software quality.

---

# Project Lifecycle Knowledge

The repository supports the complete software lifecycle.

```text
Requirements

↓

Analysis

↓

Architecture

↓

Development

↓

Testing

↓

Deployment

↓

Operation

↓

Maintenance

↓

Continuous Improvement
```

The AI Agent should consider the entire lifecycle rather than focusing only on implementation.

---

# Knowledge Preservation

The repository should retain organizational knowledge.

Important decisions should never exist only in conversations.

Instead, they should be documented through:

- Architecture documents
- AI Context
- Project Rules
- ADRs (Architecture Decision Records)
- Workflow documentation

This ensures future developers and AI Agents can understand previous decisions.

---

# Documentation Quality Principles

Documentation should be:

- Accurate
- Current
- Complete
- Consistent
- Searchable
- AI-readable

Poor documentation increases development cost and implementation risk.

---

# End of Part 4

---

# AI Development Lifecycle

The AI Agent should participate throughout the entire software development lifecycle.

AI assistance is not limited to code generation.

The recommended lifecycle is:

```text
Business Requirement

↓

Requirement Analysis

↓

Architecture Planning

↓

Solution Design

↓

Implementation Planning

↓

Code Generation

↓

Code Review

↓

Testing

↓

Documentation

↓

Deployment

↓

Monitoring

↓

Continuous Improvement
```

The AI Agent should understand the context of every stage before proceeding to the next.

---

# AI Development Responsibilities

During development, the AI Agent acts as:

- Requirements Analyst
- Solution Architect
- Software Engineer
- Code Reviewer
- Security Reviewer
- Documentation Writer
- QA Assistant
- Technical Advisor

The role may change depending on the current phase of the project.

---

# Requirement Analysis Workflow

Before implementation, the AI Agent should answer the following questions:

## Business Questions

- What problem is being solved?
- Who are the users?
- What value does the feature provide?
- What business rules apply?

---

## Technical Questions

- Which modules are affected?
- Which APIs are required?
- Which database entities are involved?
- Which security requirements apply?
- Which documentation must be updated?

---

## Risk Questions

- What could break?
- What dependencies exist?
- What edge cases should be considered?
- What performance risks exist?

---

# Requirement Analysis Checklist

Before writing code, verify:

- [ ] Business objective understood
- [ ] Functional requirements identified
- [ ] Non-functional requirements identified
- [ ] Security requirements reviewed
- [ ] Existing implementation analyzed
- [ ] Architecture reviewed
- [ ] Documentation reviewed

Implementation should not begin until all items are satisfied.

---

# Architecture Decision Process

Every significant implementation should follow an architecture review.

```text
Requirement

↓

Current Architecture Review

↓

Alternative Solutions

↓

Trade-off Analysis

↓

Recommended Design

↓

Implementation
```

The AI Agent should explain why a solution was chosen.

---

# AI Planning Workflow

Planning should always precede implementation.

The implementation plan should include:

## Scope

What will be changed?

---

## Components

Which files will be modified?

---

## Dependencies

Which modules are affected?

---

## Risks

Potential impacts.

---

## Testing

How will the feature be verified?

---

## Documentation

Which documents require updates?

---

# AI Implementation Workflow

Implementation should follow a controlled process.

```text
Understand

↓

Analyze

↓

Plan

↓

Implement

↓

Review

↓

Refactor

↓

Test

↓

Document
```

Each stage should be completed before moving to the next.

---

# Implementation Strategy

Prefer incremental development.

Instead of implementing a large feature at once:

```text
Feature

↓

Module

↓

Component

↓

Function

↓

Test
```

Small changes are easier to review and maintain.

---

# AI Decision Framework

When multiple implementation options exist, evaluate:

## Simplicity

Is this the simplest correct solution?

---

## Consistency

Does it follow repository standards?

---

## Maintainability

Can another developer understand it?

---

## Scalability

Will it support future growth?

---

## Security

Does it introduce new risks?

---

## Performance

Is the solution efficient enough?

---

# AI Code Generation Strategy

Before generating code:

Review:

- Existing implementation
- Naming conventions
- Folder structure
- Component reuse opportunities
- Similar features

Avoid creating duplicate functionality.

---

# AI Refactoring Workflow

When refactoring:

```text
Existing Code

↓

Understand

↓

Identify Problems

↓

Plan Improvements

↓

Refactor

↓

Validate

↓

Document
```

Refactoring should preserve existing functionality.

---

# AI Code Review Workflow

The AI Agent should perform an internal review before presenting code.

Review categories:

## Architecture

- Correct layer
- Correct module
- Correct dependencies

---

## Code Quality

- Readability
- Naming
- Structure
- Complexity

---

## Security

- Input validation
- Authorization
- Sensitive data handling

---

## Performance

- Efficient algorithms
- Minimal API calls
- Optimized data access

---

## Maintainability

- Modular design
- Documentation
- Reusability

---

# AI Review Checklist

Before delivering code:

- [ ] Architecture respected
- [ ] Business logic isolated
- [ ] Repository pattern followed
- [ ] Error handling included
- [ ] Validation implemented
- [ ] Security considered
- [ ] Documentation updated

---

# AI Testing Lifecycle

Testing is part of development.

Recommended sequence:

```text
Implementation

↓

Unit Test

↓

Integration Test

↓

System Test

↓

User Acceptance Test

↓

Production Release
```

The AI Agent should recommend appropriate tests.

---

# Test Design Principles

Each feature should include tests for:

- Normal scenarios
- Invalid input
- Boundary conditions
- Authorization failures
- Error conditions
- Performance-sensitive operations

---

# AI Documentation Workflow

Documentation should evolve together with the code.

Whenever implementation changes:

Update:

- Architecture
- API
- Business Rules
- User Flow
- AI Context

Documentation updates should not be postponed.

---

# AI Knowledge Capture

After completing a feature, identify:

- New reusable components
- New architectural patterns
- Lessons learned
- New business rules

Record these in the appropriate documentation.

---

# AI Continuous Improvement Cycle

The repository follows a continuous learning model.

```text
Implement

↓

Review

↓

Measure

↓

Improve

↓

Document

↓

Reuse
```

Each completed feature should improve future development.

---

# AI Retrospective Process

After major implementations, evaluate:

## Successes

What worked well?

---

## Challenges

What caused difficulty?

---

## Improvements

What can be simplified?

---

## Documentation

What knowledge should be preserved?

---

## Reuse

Which components can be reused?

---

# AI Communication Principles

The AI Agent should communicate clearly.

Explain:

- Why a solution was selected.
- Why alternatives were rejected.
- Expected impact.
- Risks.
- Recommended next steps.

Avoid unexplained implementation decisions.

---

# Human–AI Collaboration Model

Responsibilities are shared.

## Human Responsibilities

- Business decisions
- Product direction
- Architecture approval
- Production approval
- Final validation

---

## AI Responsibilities

- Analysis
- Planning
- Implementation assistance
- Review
- Documentation
- Testing recommendations

The AI Agent supports developers but does not replace engineering judgment.

---

# AI Completion Criteria

A development task is complete only when:

- Requirements are satisfied.
- Architecture remains consistent.
- Code follows repository standards.
- Security has been reviewed.
- Tests have been considered.
- Documentation has been updated.
- No unnecessary technical debt has been introduced.

---

# End of Part 5

---

# Security Context

Security is a fundamental design principle of the GAS Enterprise Starter Kit.

It is not an optional feature and should never be treated as an afterthought.

Every component should be designed with security in mind.

The AI Agent must evaluate security implications before implementing any feature.

---

# Security Philosophy

The project follows the principle of:

**Secure by Design**

This means security should be integrated into:

- Architecture
- Source Code
- API Design
- Database Design
- Deployment
- Operations

Security should never rely solely on end-user behavior.

---

# Security Objectives

The system should provide:

- Confidentiality
- Integrity
- Availability
- Accountability
- Auditability

Every implementation should contribute to these objectives.

---

# Defense in Depth

Security should be applied at multiple layers.

```text
User

↓

Authentication

↓

Authorization

↓

Input Validation

↓

Business Rules

↓

Repository

↓

Database

↓

Audit Log
```

No single layer should be solely responsible for protecting the system.

---

# Authentication Context

Authentication verifies user identity.

Supported authentication methods may include:

- Google Account Authentication
- OAuth 2.0
- Session-based Authentication
- API Token Authentication (when applicable)

Authentication should always occur before access to protected resources.

---

# Authorization Context

Authorization determines what an authenticated user is allowed to do.

The repository adopts:

Role-Based Access Control (RBAC)

Standard authorization flow:

```text
User

↓

Role

↓

Permission

↓

Resource

↓

Action
```

Every protected operation should verify permissions before execution.

---

# Principle of Least Privilege

Users should receive only the permissions required for their responsibilities.

Avoid:

- Full administrative access by default
- Shared administrator accounts
- Broad permission assignments

The AI Agent should recommend minimal required permissions.

---

# Input Validation

All external input must be validated.

Sources include:

- Forms
- URL Parameters
- API Requests
- Spreadsheet Data
- External Services

Validation should occur:

- Client-side (for usability)
- Server-side (mandatory)

---

# Output Handling

Returned data should be appropriate for the requesting user.

Avoid:

- Returning unnecessary fields
- Exposing internal identifiers
- Revealing implementation details
- Displaying stack traces

Users should receive only the information required.

---

# Data Protection

Sensitive information should be protected throughout its lifecycle.

Examples:

- Personal information
- Authentication data
- Access tokens
- API credentials
- Configuration values

The AI Agent should avoid exposing sensitive information in:

- Logs
- Error messages
- Source code
- Documentation

---

# Secret Management

Secrets should never be stored in source code.

Examples include:

- API Keys
- Database Passwords
- OAuth Secrets
- Private Tokens

Recommended approaches:

- Script Properties
- Environment Configuration
- Secure Secret Management Services

---

# Google Apps Script Security

When developing with Google Apps Script:

Follow these practices:

- Use least-privilege scopes
- Limit OAuth permissions
- Validate all user input
- Restrict deployment access
- Protect Web App endpoints

Avoid requesting unnecessary Google Workspace permissions.

---

# Google Sheets Security

Google Sheets serves as the primary database.

Protect:

- Spreadsheet access
- Sharing permissions
- Sheet visibility
- Sensitive columns

Recommended practices:

- Use dedicated service accounts where appropriate
- Separate configuration sheets from transactional data
- Restrict edit permissions

---

# API Security

All APIs should implement:

- Authentication
- Authorization
- Input validation
- Rate limiting (where applicable)
- Error handling
- Logging

Responses should follow a consistent structure.

---

# External Integration Security

When connecting to external systems:

Verify:

- HTTPS usage
- Certificate validity
- Authentication mechanism
- Response validation
- Timeout handling

External services should never be assumed to be trustworthy.

---

# Error Handling Security

Errors should be informative for developers but safe for users.

Internal logs may contain diagnostic information.

User-facing messages should remain generic.

Example:

Good:

> Unable to process your request. Please try again later.

Avoid:

> SQL Exception at line 42...

---

# Audit Logging

Important operations should be logged.

Examples:

- Login
- Logout
- Permission changes
- Record creation
- Record updates
- Record deletion
- Configuration changes

Audit logs should include:

- Timestamp
- User
- Action
- Resource
- Result

---

# Security Monitoring

The system should support monitoring for:

- Failed logins
- Unauthorized access attempts
- Unexpected API usage
- Configuration changes
- System errors

Monitoring improves incident response.

---

# Secure Coding Guidelines

The AI Agent should:

✓ Validate all input

✓ Sanitize output where appropriate

✓ Handle errors safely

✓ Follow RBAC

✓ Protect confidential data

✓ Log important actions

Avoid:

✗ Hard-coded credentials

✗ Bypassing authorization

✗ Ignoring validation

✗ Trusting client-side validation alone

---

# Privacy Considerations

Applications may process personal information.

Developers should consider:

- Data minimization
- Purpose limitation
- Access control
- Data retention
- Secure disposal

Only collect data required for business purposes.

---

# Deployment Context

Deployment should be predictable, repeatable, and secure.

The deployment process should minimize operational risk.

---

# Deployment Environments

The recommended environment hierarchy is:

```text
Development

↓

Testing

↓

Staging

↓

Production
```

Each environment should have independent configuration.

---

# Configuration Management

Configuration should be externalized.

Examples:

- Spreadsheet IDs
- API Endpoints
- Environment Variables
- Feature Flags

Configuration should never be embedded in business logic.

---

# Deployment Verification

Before deployment, verify:

- Documentation is updated
- Security review completed
- Tests completed
- Configuration validated
- Backup available
- Rollback plan prepared

Deployment should not proceed if critical verification fails.

---

# Rollback Strategy

Every deployment should have a rollback plan.

Rollback should include:

- Previous deployment version
- Configuration backup
- Database recovery procedure
- Verification checklist

Rollback planning should occur before deployment.

---

# Operational Readiness

Before production release, confirm:

- Logging enabled
- Monitoring configured
- Security reviewed
- Documentation current
- Team informed

The system should be operationally maintainable.

---

# AI Deployment Awareness

Before recommending deployment, the AI Agent should review:

- Architecture consistency
- Security compliance
- Configuration completeness
- Documentation status
- Testing coverage

Deployment recommendations should be based on evidence, not assumptions.

---

# Risk Assessment

Before major changes, evaluate:

- Business impact
- Technical impact
- Security impact
- Performance impact
- Operational impact

The AI Agent should identify potential risks and recommend mitigation strategies.

---

# Business Continuity

The system should support:

- Backup procedures
- Disaster recovery
- Service restoration
- Data integrity verification

Critical systems should remain recoverable after failures.

---

# End of Part 6

---

# AI Knowledge Management

The repository should be treated as a living knowledge base.

Knowledge should continuously improve as the project evolves.

The AI Agent should contribute to preserving, organizing, and expanding project knowledge.

Knowledge should never exist only in conversations.

Instead, it should be captured in documentation.

---

# Knowledge Categories

Repository knowledge is divided into multiple categories.

## Business Knowledge

Examples:

- Business objectives
- Business rules
- User requirements
- Workflows
- Domain terminology

---

## Technical Knowledge

Examples:

- Architecture
- APIs
- Database schema
- UI Components
- Coding standards

---

## Operational Knowledge

Examples:

- Deployment
- Security
- Monitoring
- Backup
- Maintenance

---

## AI Knowledge

Examples:

- Prompt templates
- AI workflows
- AI context
- AI operation guides
- AI best practices

---

# Repository Knowledge Graph

The repository should be viewed as a connected knowledge graph.

```text
Repository

│

├── Vision

│

├── Architecture

│

├── Business Rules

│

├── Source Code

│

├── Documentation

│

├── Testing

│

├── Deployment

│

└── AI Knowledge
```

Changes in one area may affect multiple other areas.

The AI Agent should identify these relationships before implementation.

---

# Knowledge Dependency

Knowledge has dependencies.

Example:

```text
Business Rule

↓

Architecture

↓

Database

↓

API

↓

UI

↓

Testing

↓

Documentation
```

Changing a business rule may require updates throughout the repository.

---

# Repository Memory Model

The repository serves as long-term organizational memory.

Knowledge should remain available for:

- Future developers
- Project maintainers
- AI Agents
- New team members

Documentation should preserve important decisions.

---

# Static Knowledge

Static knowledge changes infrequently.

Examples:

- Project vision
- Folder structure
- Architecture principles
- Coding standards

These documents provide the foundation of the repository.

---

# Dynamic Knowledge

Dynamic knowledge changes regularly.

Examples:

- Features
- Business rules
- APIs
- Reports
- User interfaces

Dynamic documentation should remain synchronized with implementation.

---

# Historical Knowledge

Important decisions should be preserved.

Examples:

- Architecture decisions
- Technology selection
- Major refactoring
- Security improvements

Consider using Architecture Decision Records (ADRs) for significant design decisions.

---

# Documentation Synchronization

Whenever implementation changes, determine whether updates are required for:

- README
- AI Context
- Project Rules
- API Documentation
- Database Schema
- Workflow Guides
- Security Guide
- Deployment Guide

Documentation maintenance is part of software development.

---

# Knowledge Evolution

Knowledge evolves over time.

The AI Agent should continuously improve:

- Documentation quality
- Consistency
- Organization
- Searchability
- Reusability

Documentation should become more valuable with every release.

---

# AI Learning Strategy

The AI Agent should learn from repository patterns.

Identify:

- Common architectures
- Reusable services
- Naming conventions
- UI patterns
- Validation approaches

Future implementations should follow established patterns.

---

# Pattern Recognition

Before creating new code, determine whether similar implementations already exist.

Prefer:

- Extending existing modules
- Reusing components
- Reusing utilities
- Reusing services

Avoid unnecessary duplication.

---

# Repository Consistency

Consistency should be maintained across:

- Architecture
- Naming
- Folder organization
- API design
- UI components
- Documentation

The AI Agent should recommend consistency improvements when appropriate.

---

# AI Decision Memory

The AI Agent should remember previous project decisions by referring to documentation.

Do not contradict:

- Project Rules
- AI Context
- Security Guide
- Architecture documents

When conflicts exist, explain the conflict instead of making assumptions.

---

# Continuous Knowledge Improvement

Every completed feature should contribute to repository knowledge.

Examples:

- New reusable component
- Better workflow
- Improved documentation
- New prompt template
- New coding guideline

Knowledge should accumulate over the lifetime of the project.

---

# Repository Knowledge Maintenance

Knowledge should be reviewed periodically.

Recommended review areas:

- Outdated documentation
- Broken references
- Duplicate guidance
- Deprecated architecture
- Obsolete workflows

The AI Agent should identify opportunities for cleanup.

---

# Documentation Quality Standards

Documentation should be:

- Accurate
- Complete
- Consistent
- Searchable
- Versioned
- AI-readable

Good documentation reduces development time and implementation errors.

---

# AI Collaboration Model

Successful development depends on collaboration.

```text
Business Owner

↓

Project Manager

↓

Software Architect

↓

Developer

↓

GitHub Copilot Agent

↓

Quality Assurance

↓

Operations
```

The AI Agent supports every stage but does not replace human decision-making.

---

# AI Context Maintenance

The AI Context document should be updated whenever:

- Architecture changes
- Technology stack changes
- Development workflow changes
- Security requirements change
- Deployment process changes
- Repository structure changes

This document should remain synchronized with the rest of the repository.

---

# Repository Governance

Repository governance ensures long-term quality.

Governance includes:

- Architecture standards
- Coding standards
- Documentation standards
- Security policies
- Review processes

The AI Agent should follow repository governance at all times.

---

# AI Completion Verification

Before considering any task complete, verify:

- Requirements satisfied
- Architecture preserved
- Security reviewed
- Documentation updated
- Tests considered
- Repository consistency maintained

Completion should be evaluated holistically.

---

# Future Expansion

The repository is designed to support future growth.

Potential future additions include:

- Mobile applications
- Progressive Web Apps (PWA)
- AI-powered automation
- Machine Learning integration
- Business Intelligence dashboards
- Workflow engines
- Multi-database support
- Cloud-native services

The architecture should accommodate these extensions without fundamental redesign.

---

# Repository Knowledge Vision

The long-term vision is to establish the repository as:

- An enterprise application framework
- A reusable software foundation
- A documented architectural reference
- A collaborative AI development environment
- A continuously evolving organizational knowledge base

Every contribution should move the repository closer to this vision.

---

# AI Context Version History

| Version | Description |
|----------|-------------|
| 1.0 | Initial AI Context |
| 2.0 | Expanded AI Coding Guidance |
| 3.0 Enterprise Edition | Comprehensive AI Knowledge Base with Enterprise Development, Security, Deployment, Workflow, and Knowledge Management |

---

# End of AI Context Management Guide

Version 3.0 Enterprise Edition

GAS Enterprise Starter Kit
