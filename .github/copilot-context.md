# GitHub Copilot Project Context

## GAS Enterprise Starter Kit

Version 2.0

---

# Project Identity

This repository is a production-oriented Google Apps Script Enterprise Starter Kit.

The purpose is to provide a reusable foundation for building:

- Internal business applications
- Healthcare applications
- Community health systems
- Data management systems
- Dashboard applications
- Automation workflows

using:

- Google Apps Script
- Google Sheets
- HTML Service
- Tailwind CSS
- JavaScript
- External API Integration

---

# Project Vision

Create a development framework that enables:
Fast Development

Clean Architecture

Secure Implementation

AI-Assisted Engineering

Long-Term Maintenance


---

# Application Architecture

The project follows:

## Layered MVC Architecture


User Interface

↓

Controller

↓

Service

↓

Repository

↓

Data Source


---

# Layer Responsibilities

## Presentation Layer

Responsible for:

- UI rendering
- User interaction
- Form handling
- Displaying results

Technology:

- HTML Service
- Tailwind CSS
- Vanilla JavaScript

---

## Controller Layer

Responsible for:

- Receiving requests
- Input routing
- Calling services
- Returning responses

Should NOT contain:

- Business logic
- Database operations

---

## Service Layer

Responsible for:

- Business rules
- Data processing
- Validation
- Workflow management

---

## Repository Layer

Responsible for:

- Data access
- Google Sheets operations
- External API communication

Business logic must not directly access data sources.

---

# Technology Context

## Backend

Google Apps Script V8

Preferred:

- ES2022 syntax
- Class-based design
- Modular files
- JSDoc documentation

---

## Database

Primary database:

Google Sheets


Used for:

- Application data
- Configuration
- Mapping
- User settings


Database access must go through Repository Layer.

---

## Frontend

Technology:

- HTML Service
- Tailwind CSS
- Vanilla JavaScript


UI philosophy:

Modern SaaS Application

Reference:

- Google Workspace
- Notion
- Linear
- Vercel
- Supabase

---

# Common System Components

The repository supports:

## Authentication

Features:

- Login
- Session management
- User validation

---

## RBAC

Role Based Access Control:

Example:


Admin

Manager

Staff

Viewer


Permissions must be validated.

---

## Dashboard

Common features:

- KPI cards
- Charts
- Tables
- Filters
- Reports

---

## API Integration

Supported pattern:


Google Apps Script

↓

REST API

↓

External Service


Examples:

- Node.js API
- MySQL
- LINE Messaging API

---

# Healthcare Application Context

This framework can support healthcare systems such as:

- Primary Care Applications
- Community Health Systems
- Patient Management
- Appointment Systems
- Health Dashboard
- Notification Systems

Example integrations:


JHCIS

↓

API Layer

↓

GAS Application


---

# Development Rules

All development must follow:

## Documentation First

Before coding:

Read:


docs/README.md

docs/30_AI_CONTEXT.md

docs/PROJECT_RULES.md


---

# Important Documentation

## Architecture


docs/02_SYSTEM_ARCHITECTURE.md


---

## Database


docs/04_DATABASE_SCHEMA.md


---

## Coding Rules


docs/07_CODING_STANDARDS.md


---

## Security


docs/33_SECURITY_GUIDE.md


---

## Deployment


docs/34_DEPLOYMENT_GUIDE.md


---

## AI Development


docs/38_COPILOT_PROMPT_LIBRARY.md

docs/39_COPILOT_AGENT_EXAMPLES.md

docs/40_AI_AGENT_INITIALIZATION_PROMPT.md

AI Agent Startup Process:

1. Read repository instructions

2. Load project context

3. Review AI rules

4. Initialize development session

5. Begin implementation
---

# AI Agent Development Behavior

GitHub Copilot Agent should behave as:


Software Architect

Senior Developer

Code Reviewer

Security Reviewer


---

# Before Creating Code

AI should:

1. Understand requirement
2. Review existing architecture
3. Identify affected modules
4. Explain approach
5. Implement solution
6. Review output

---

# Code Quality Expectations

Generated code should be:

- Readable
- Maintainable
- Reusable
- Secure
- Documented

---

# Security Context

Sensitive information:

Never expose:

- Passwords
- API tokens
- Database credentials
- Personal data

---

# Data Protection Rules

Always:

- Validate input
- Control permissions
- Protect sensitive data
- Log important actions

---

# Integration Context

External integrations should use:


Application

↓

Service Layer

↓

API Client

↓

External System


Never:


Frontend

↓

External Database


---

# Repository Organization

Follow:


.github/

AI Instructions

docs/

Documentation

src/

Application Code

tests/

Testing

config/

Configuration


---

# AI Agent Preferred Workflow

For every feature:


Requirement

↓

Analysis

↓

Design

↓

Implementation Plan

↓

Coding

↓

Review

↓

Testing

↓

Documentation


---

# Expected AI Response Format

When assisting development:

Use:

Analysis

Explain understanding

Plan

Describe approach

Changes

List files affected

Implementation

Provide code

Testing

Explain verification

Documentation

List updates


---

# Common Mistakes to Avoid

Never:

- Create files randomly
- Ignore existing components
- Duplicate logic
- Put business logic in UI
- Put database logic in controllers
- Skip security review

---

# Project Success Criteria

A successful implementation must be:


Functional

Secure

Maintainable

Scalable

Documented


---

# End of GitHub Copilot Project Context

Version 2.0

GAS Enterprise Starter Kit
