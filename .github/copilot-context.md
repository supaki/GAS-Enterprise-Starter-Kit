# GitHub Copilot Project Context

## GAS Enterprise Starter Kit

Version 2.1

---

# Purpose

This document provides project context information for GitHub Copilot Agent.

Its purpose is to help AI understand:

- What this project is
- Why it exists
- How it is structured
- Which technologies are used
- How development should be performed

This file is the **Project Context Layer**.

It does not replace detailed documentation.

For complete knowledge, AI MUST read:
docs/30_AI_CONTEXT.md


---

# AI Context Hierarchy

The repository uses a layered AI knowledge system.


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

Source Code


---

# AI Agent Startup Sequence

When starting a new development session:

Follow:


Understand AI behavior rules

 ↓

Load project context

 ↓

Apply repository rules

 ↓

Read documentation map

 ↓

Load AI knowledge base

 ↓

Initialize development context

 ↓
Start implementation

Reference:


docs/40_AI_AGENT_INITIALIZATION_PROMPT.md


---

# Project Identity

## Name

GAS Enterprise Starter Kit

---

## Project Type

Enterprise Application Development Framework

---

## Main Purpose

Provide a reusable foundation for building production-ready applications using:

- Google Apps Script
- Google Sheets
- HTML Service
- Tailwind CSS
- JavaScript
- External API Integration

---

# Project Vision

The project combines:


Rapid Development

Clean Architecture

Security

Maintainability

AI-Assisted Engineering


---

# Target Users

The framework supports:

## Developers

For:

- Web application development
- Internal systems
- Automation solutions


## Organizations

For:

- Data management systems
- Workflow systems
- Reporting systems


## Healthcare Teams

For:

- Primary care applications
- Community health systems
- Patient management
- Notification systems

---

# Core Technology Context

---

# Backend

Technology:


Google Apps Script V8


Development style:

- Modular
- Class-based
- Service-oriented

Preferred:

- ES2022 syntax
- JSDoc
- Clean Code

---

# Frontend

Technology:


HTML Service

Tailwind CSS

Vanilla JavaScript


UI goals:

- Responsive
- Mobile First
- Modern SaaS style
- Accessible

---

# Database

Primary database:


Google Sheets


Used for:

- Application data
- Configuration
- Master data
- Transaction data
- Logs

---

# External Database Integration

Supported architecture:


Application

↓

API Layer

↓

External Database


Example:


Google Apps Script

↓

Node.js API

↓

MySQL


Never connect directly from frontend or GAS to unsecured databases.

---

# System Architecture Context

The project follows:


MVC

Service Layer

Repository Pattern


Architecture:


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

# Layer Responsibility Summary

## Presentation Layer

Responsible:

- UI rendering
- User interaction
- Displaying information


Must not:

- Access database
- Implement business rules

---

## Controller Layer

Responsible:

- Request handling
- Input routing
- Response formatting


Must not:

- Contain complex business logic
- Directly access database

---

## Service Layer

Main business layer.

Responsible:

- Business rules
- Validation
- Workflow
- Permission checks

---

## Repository Layer

Responsible:

- Data access
- Spreadsheet operations
- External API communication

---

# Application Capabilities

The framework supports:

---

# Authentication

Features:

- User identity verification
- Session management
- User lifecycle

---

# Authorization

Uses:


RBAC

(Role Based Access Control)


Example:


Admin

Manager

Staff

Viewer


---

# Dashboard Systems

Supports:

- KPI dashboard
- Charts
- Reports
- Filtering
- Data visualization

---

# API Integration

Supports:

- REST API
- External services
- Notification systems

---

# Healthcare Context

Possible integrations:


JHCIS

↓

API Proxy

↓

Google Apps Script

↓

Healthcare Application


---

# Development Principles

All development follows:

## Documentation First

Before coding:

Read:


docs/README.md

docs/30_AI_CONTEXT.md

docs/PROJECT_RULES.md


---

## Architecture First

Design before implementation.

---

## Security First

Protect:

- Credentials
- Personal data
- System access

---

# AI Agent Behavior

AI should behave as:


Software Architect

Senior Developer

Security Reviewer

Code Reviewer


---

# AI Development Workflow

For every task:


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

# AI Response Expectation

Preferred response format:

Analysis

Understanding of problem

Plan

Implementation approach

Changes

Files affected

Implementation

Code or modifications

Testing

Verification

Documentation

Updates required


---

# Code Quality Expectations

Generated code should be:

- Readable
- Maintainable
- Secure
- Reusable
- Documented

---

# Security Context

Never expose:

- Passwords
- API keys
- Tokens
- Database credentials


Use:

- Script Properties
- Secure configuration

---

# Performance Context

Prefer:

- Batch operations
- Efficient data access
- Caching where appropriate

Avoid:

- Repeated Spreadsheet API calls
- Unnecessary processing

---

# Repository Structure Context

Expected structure:


.github/

AI Configuration

docs/

Documentation

src/

Application Code

tests/

Testing

config/

Configuration


---

# Documentation Relationship

Important files:

| File | Purpose |
|-|-|
| copilot-instructions.md | AI behavior |
| copilot-context.md | Project understanding |
| copilot-rules.md | Enforcement rules |
| 30_AI_CONTEXT.md | Complete AI knowledge |
| 40_AI_AGENT_INITIALIZATION_PROMPT.md | Session startup |

---

# Completion Definition

A task is complete only when:


Feature Works

Architecture Correct

Security Checked

Code Reviewed

Documentation Updated


---

# Final Context Instruction

You are working inside an enterprise software repository.

Understand the project first.

Follow the architecture.

Respect security rules.

Create maintainable solutions.

Use documentation as the source of truth.

---

# End of GitHub Copilot Project Context

Version 2.1

GAS Enterprise Starter Kit
