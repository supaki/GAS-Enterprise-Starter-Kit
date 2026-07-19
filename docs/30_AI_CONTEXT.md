# AI Context Documentation

## GAS Enterprise Starter Kit

Version 3.0

---

# Purpose

This document is the primary knowledge source for AI Agents working with this repository.

It provides:

- Project understanding
- Architecture context
- Development philosophy
- Technical constraints
- Business context
- AI collaboration rules

GitHub Copilot Agent MUST understand this document before generating or modifying code.

---

# AI Knowledge Hierarchy

The AI Agent should understand the repository using this order:
.github/copilot-instructions.md

↓

.github/copilot-context.md

↓

.github/copilot-rules.md

↓

docs/30_AI_CONTEXT.md

↓

Other Documentation

↓

Source Code


---

# Project Identity

## Name

GAS Enterprise Starter Kit

---

## Description

A production-ready framework for building enterprise web applications using:

- Google Apps Script
- Google Sheets
- HTML Service
- Tailwind CSS
- JavaScript
- External API Integration

---

# Project Goal

The project aims to provide:


Rapid Application Development

Enterprise Architecture

Security

Maintainability

AI-Assisted Development


---

# Target Applications

This framework supports:

## Business Applications

Examples:

- Internal management systems
- Data collection systems
- Reporting systems
- Workflow applications

---

## Healthcare Applications

Examples:

- Primary care systems
- Community health applications
- Patient management
- Appointment systems
- Health dashboards
- Notification systems

---

# Core Technology Stack

---

# Backend

## Google Apps Script

Runtime:


V8 Engine


Language:


JavaScript ES2022


Development style:

- Modular
- Class-based
- Service oriented

---

# Frontend

Technology:


HTML Service

Tailwind CSS

Vanilla JavaScript


---

# Visualization

Library:


Chart.js


Used for:

- Dashboard
- Analytics
- Reports

---

# Icons

Library:


Material Symbols


---

# Database

Primary:


Google Sheets


Used as:

- Application database
- Configuration database
- Mapping database

---

# External Database Support

The system may integrate with external databases.

Example:


Google Apps Script

↓

REST API

↓

Node.js

↓

MySQL


Direct database connection from GAS is prohibited.

---

# System Architecture

The system follows:

## Layered MVC Architecture


Presentation Layer

↓

Controller Layer

↓

Service Layer

↓

Repository Layer

↓

Data Source


---

# Layer Responsibilities

---

# Presentation Layer

Responsibilities:

- Display interface
- User interaction
- Form submission
- Client-side validation

Must NOT:

- Access database directly
- Contain business rules

---

# Controller Layer

Responsibilities:

- Receive request
- Validate request
- Call service
- Return response

Must NOT:

- Query database
- Handle complex logic

---

# Service Layer

Responsibilities:

- Business rules
- Workflow
- Data processing
- Permission checking

This is the main application logic layer.

---

# Repository Layer

Responsibilities:

- Data access
- Google Sheets operations
- API communication

Must hide data source implementation.

---

# Data Layer

Examples:


Google Sheets

REST API

MySQL


---

# Application Design Principles

The project follows:

## Separation of Concerns

Each layer has a clear responsibility.

---

## Single Responsibility Principle

A module should have one main purpose.

---

## Reusable Components

Prefer:


Component

↓

Reuse

↓

Maintain


---

## Clean Architecture

Business logic should not depend on:

- UI
- Database implementation
- External systems

---

# Google Sheets Database Design

Google Sheets acts as structured data storage.

Recommended structure:


Configuration

↓

Master Data

↓

Transaction Data

↓

Logs


---

# Database Rules

Every table/sheet should define:

- Primary identifier
- Required fields
- Validation rules
- Created timestamp
- Updated timestamp

Example:


Patients

id

name

birthDate

status

createdAt

updatedAt


---

# Authentication Context

Authentication provides:

- Identity verification
- Session handling
- User management

---

# Authorization Context

Authorization uses:

## RBAC

Role Based Access Control


Example:


Admin

Manager

Staff

Viewer


---

# Permission Model

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


---

# Security Context

Security priorities:


Protect Data

↓

Protect Access

↓

Protect Credentials

↓

Protect System Integrity


---

# Security Requirements

Never:

- Hard-code secrets
- Store passwords directly
- Expose tokens
- Expose database credentials

---

Use:

- Script Properties
- Environment variables
- Secure configuration

---

# API Design Context

APIs should follow:


Request

↓

Validation

↓

Controller

↓

Service

↓

Repository

↓

Response


---

# Standard Response Format

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
UI/UX Context

The application follows modern SaaS design.

Reference:

Google Workspace
Notion
Linear
Vercel
Supabase
UI Requirements

Prefer:

Responsive layout
Mobile First
Dark Mode
Loading skeleton
Empty state
Error state
Toast notification
Development Workflow

Every feature follows:

Requirement

↓

Analysis

↓

Architecture

↓

Database Design

↓

Implementation

↓

Review

↓

Testing

↓

Documentation

↓

Deployment
AI Agent Working Model

The AI Agent acts as:

Architect

+

Developer

+

Reviewer

+

Security Analyst
AI Must Do

Before coding:

Understand requirement
Review documentation
Analyze impact
Explain approach

During coding:

Follow architecture
Follow coding standards
Protect security

After coding:

Review
Test
Update documentation
AI Must Avoid

Never:

Generate code without context
Break architecture
Duplicate modules
Ignore security
Modify unrelated files
Feature Development Template

When creating a feature:

Step 1

Define:

Purpose
Users
Requirements
Step 2

Design:

Database
Components
API
Step 3

Implement:

Model
Repository
Service
Controller
UI
Step 4

Validate:

Testing
Security
Performance
Step 5

Document:

README
Architecture
Usage
Integration Context

Supported integrations:

LINE Messaging API

Purpose:

Notifications
Reminders
Alerts
JHCIS Integration

Architecture:

JHCIS MySQL

↓

API Proxy

↓

Google Apps Script

↓

Application
Performance Guidelines

Prefer:

Batch operations
Caching
Minimal API calls
Efficient queries

Avoid:

Repeated Spreadsheet calls
Unnecessary processing
Maintenance Guidelines

After changes:

Update:

Documentation

AI Context

Security Notes

API Documentation
Repository Knowledge Map
.github/

AI Behavior


docs/

AI Knowledge


src/

Implementation


tests/

Validation


config/

Settings
AI Completion Criteria

A task is complete only when:

Feature Works

+

Architecture Correct

+

Security Checked

+

Code Reviewed

+

Documentation Updated
Final Message to AI Agent

You are working on an enterprise software repository.

Your responsibility is not only to generate code.

Your responsibility is to help build:

Secure

Maintainable

Scalable

Production-Ready

Enterprise Software

Always understand first.

Always design before coding.

Always review before completion.



# AI Agent Initialization

Before starting development:

The AI Agent should initialize by reviewing:

- Repository instructions
- Project context
- Repository rules
- Documentation system

Reference:

docs/40_AI_AGENT_INITIALIZATION_PROMPT.md
