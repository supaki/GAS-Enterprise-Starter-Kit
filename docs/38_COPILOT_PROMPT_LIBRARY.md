# GitHub Copilot Prompt Library

## GAS Enterprise Starter Kit

Version 1.0

---

# Introduction

This document provides reusable prompts for GitHub Copilot Agent when developing applications using the GAS Enterprise Starter Kit.

The purpose of this document is to help developers communicate effectively with AI Agents and ensure generated code follows repository standards.

This Prompt Library supports:

- Project Analysis
- Architecture Design
- Feature Development
- Debugging
- Code Review
- Refactoring
- Testing
- Documentation
- Deployment

---

# AI Development Philosophy

GitHub Copilot Agent should not be treated as a simple code generator.

The AI Agent should act as:

- Software Architect
- Senior Google Apps Script Developer
- Code Reviewer
- Security Reviewer
- Documentation Assistant
The recommended workflow is:
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

Test

↓

Document


---

# How to Use This Prompt Library

Before using any prompt:

1. Open GitHub Copilot Chat or Agent Mode

2. Ensure the repository is loaded

3. Start with the Repository Initialization Prompt

4. Provide the business requirement

5. Ask AI to analyze before generating code

---

# Important Rule

Do not start with:


Create code for this feature


Instead start with:


Analyze this requirement and explain the implementation approach.
Do not generate code yet.


This ensures AI understands:

- Existing architecture
- Coding standards
- Repository rules
- Existing components

---

# Prompt 01: Initialize GitHub Copilot Agent

## Purpose

Use this prompt when starting a new Copilot Agent session.

---

## Prompt


You are working inside the GAS Enterprise Starter Kit.

Before performing any development task:

Read:
.github/copilot-instructions.md
.github/copilot-context.md
.github/copilot-rules.md
Read:
docs/README.md
docs/PROJECT_RULES.md
docs/30_AI_CONTEXT.md
Understand:
Project architecture
Coding standards
Folder structure
Security requirements
Development workflow
Explain your understanding.
Do not generate code until the analysis is complete.

Your role:

Principal Software Architect
Senior Google Apps Script Engineer
UI/UX Designer
Security Reviewer

---

# Prompt 02: Understand Repository

## Purpose

ให้ AI วิเคราะห์ Repository ก่อนเริ่มพัฒนา

---

## Prompt


Analyze this repository.

Explain:

Project purpose
Architecture overview
Technology stack
Folder structure
Main application flow
Existing reusable components
Development standards
Potential risks

Do not modify any files.

Provide an analysis report.


---

# Prompt 03: Analyze Existing Code

## Purpose

ใช้ก่อนแก้ไขหรือเพิ่ม Feature

---

## Prompt


Analyze the existing implementation.

Review:

Current architecture
Code structure
Dependencies
Existing patterns
Possible impact

Identify:

Files involved
Components affected
Risks
Recommended approach

Do not write code yet.


---

# Prompt 04: Requirement Analysis

## Purpose

วิเคราะห์ Requirement ก่อน Coding

---

## Prompt


Analyze this requirement:

[PASTE REQUIREMENT]

Explain:

Business Objective

Functional Requirements

Non-functional Requirements

Affected Modules

Database Impact

API Impact

UI Impact

Security Considerations

Testing Requirements

Documentation Updates

Do not generate code yet.


---

# Prompt 05: Create Implementation Plan

## Purpose

ให้ AI วางแผนก่อนลงมือทำ

---

## Prompt


Create an implementation plan.

Include:

Files to create
Files to modify
Architecture approach
Data flow
Implementation steps
Testing strategy
Documentation updates
Potential risks

Wait for approval before coding.


---

# Prompt 06: Explain Architecture

## Purpose

ตรวจสอบว่า Solution เหมาะสมหรือไม่

---

## Prompt


Review this proposed solution.

Evaluate:

Architecture consistency
MVC compliance
Repository Pattern usage
Scalability
Security
Maintainability

Suggest improvements if needed.


---

# End of Part 1

Next:

Part 2 — Requirement Analysis, Architecture, Database and API Design Prompts

The recommended workflow is:
# Part 2 — Foundation Design Prompts

---

# Overview

Foundation Design is the most important stage before implementation.

The AI Agent should help developers understand:

- Business requirements
- System architecture
- Database structure
- API design
- Security model
- Data flow

The goal is to reduce incorrect implementation and avoid technical debt.

Recommended workflow:
Requirement

↓

Architecture

↓

Database

↓

API

↓

Security

↓

Implementation


---

# Prompt 07: Business Requirement Analysis

## Purpose

Use this prompt when receiving a new business requirement.

---

## Prompt


Analyze this business requirement.

Requirement:

[PASTE REQUIREMENT]

Provide:

Business objective
Target users
User problems being solved
Functional requirements
Non-functional requirements
Business rules
Constraints
Risks
Success criteria

Do not generate code.

Create a requirement analysis document.


---

# Prompt 08: Convert Requirement into User Stories

## Purpose

Convert business needs into development tasks.

---

## Prompt


Convert this requirement into User Stories.

For each User Story provide:

User role
Goal
User action
Expected result
Acceptance criteria
Priority

Format:

As a [user]

I want [action]

So that [benefit]

Acceptance Criteria:


---

# Prompt 09: System Architecture Design

## Purpose

Design architecture before implementation.

---

## Prompt


Design the system architecture for this feature.

Follow:

MVC Architecture
Service Layer Pattern
Repository Pattern

Explain:

Components
Responsibilities
Data flow
Dependencies
Integration points
Security considerations
Scalability considerations

Do not write code yet.


---

# Prompt 10: Module Design

## Purpose

Define application modules.

---

## Prompt


Design application modules for this system.

For each module define:

Module name
Purpose
Responsibilities
Input
Output
Dependencies
Related files

Ensure modules follow:

Single Responsibility Principle
Separation of Concerns
Reusability

---

# Prompt 11: Google Apps Script Architecture Design

## Purpose

Design GAS application structure.

---

## Prompt


Design a Google Apps Script application architecture.

Requirements:

Google Apps Script V8
HTML Service
Google Sheets Database
REST API support

Include:

Server-side structure

Client-side structure

Controllers

Services

Repositories

Utilities

Configuration management

Error handling strategy


---

# Prompt 12: Google Sheets Database Design

## Purpose

Create database schema using Google Sheets.

---

## Prompt


Design the Google Sheets database schema.

System requirement:

[PASTE REQUIREMENT]

Define:

Spreadsheet structure
Sheet names
Column names
Data types
Primary key
Relationships
Validation rules
Indexing strategy
Sample data

Follow database normalization principles where appropriate.


---

# Prompt 13: Database Review

## Purpose

Review existing database design.

---

## Prompt


Review this database design.

Analyze:

Data structure
Naming conventions
Data types
Relationships
Duplicate data
Data integrity
Performance concerns

Suggest improvements.


---

# Prompt 14: MySQL Integration Design

## Purpose

สำหรับระบบที่เชื่อมต่อ MySQL ผ่าน API Proxy

---

## Prompt


Design MySQL integration architecture.

Environment:

Google Apps Script

↓

REST API

↓

Node.js Express Proxy

↓

MySQL Database

Provide:

Architecture diagram
API communication flow
Authentication approach
Error handling
Security considerations
Data synchronization strategy

---

# Prompt 15: REST API Design

## Purpose

ออกแบบ API ก่อน Coding

---

## Prompt


Design REST API for this feature.

Requirement:

[PASTE REQUIREMENT]

Define:

API endpoints

HTTP methods

Request parameters

Request body

Response format

Validation rules

Error responses

Authentication requirements

Example requests and responses


---

# Prompt 16: API Response Standard

## Purpose

กำหนดรูปแบบ Response ให้เหมือนกันทั้งระบบ

---

## Prompt


Create a standard API response format.

Include:

Success response

Error response

Validation error response

Authentication error response

Server error response

Include JSON examples.


---

# Prompt 17: Authentication Design

## Purpose

ออกแบบระบบ Login

---

## Prompt


Design authentication architecture.

Requirements:

Google Apps Script Web App

RBAC support

Secure session handling

Define:

Authentication flow

User identity verification

Session management

Token handling

Security risks

Implementation approach


---

# Prompt 18: RBAC Design

## Purpose

ออกแบบ Role Based Access Control

---

## Prompt


Design RBAC permission system.

Define:

Users

Roles

Permissions

Resources

Actions

Permission checking flow

Database structure

Administration process

Example:

Admin

Manager

Staff

Viewer


---

# Prompt 19: Security Architecture Review

## Purpose

ตรวจสอบ Security ก่อน Implement

---

## Prompt


Review this architecture from a security perspective.

Analyze:

Authentication

Authorization

Data protection

Input validation

API security

Secret management

Logging

Potential vulnerabilities

Provide recommendations.


---

# Prompt 20: UI/UX Architecture Design

## Purpose

ออกแบบหน้าจอก่อนสร้าง UI

---

## Prompt


Design UI/UX architecture.

Technology:

HTML Service

Tailwind CSS

Vanilla JavaScript

Requirements:

Responsive

Mobile First

Dark Mode

Modern SaaS Style

Define:

Pages

Components

Layouts

User flows

Interactions

Loading states

Error states


---

# Prompt 21: Data Flow Diagram

## Purpose

เข้าใจการไหลของข้อมูล

---

## Prompt


Create a data flow explanation.

Include:

User interaction

Frontend process

Controller

Service

Repository

Database

External API

Response flow

Explain step by step.


---

# Prompt 22: Architecture Decision Review

## Purpose

ตรวจสอบก่อนเลือก Solution

---

## Prompt


Review this architecture decision.

Evaluate:

Advantages

Disadvantages

Alternative solutions

Trade-offs

Long-term impact

Security impact

Maintenance impact

Recommend the best approach.


---

# Foundation Design Checklist

Before implementation confirm:

- [ ] Requirement understood
- [ ] Architecture approved
- [ ] Database designed
- [ ] API designed
- [ ] Authentication considered
- [ ] Security reviewed
- [ ] UI flow defined
- [ ] Testing approach planned
- [ ] Documentation impact identified

---

# End of Part 2

Next:

Part 3 — Feature Development, CRUD, UI, Google Apps Script Implementation Prompts
# Part 3 — Feature Development, CRUD, UI, Google Apps Script Implementation Prompts

---

# Overview

This section contains prompts used during actual implementation.

The AI Agent should generate code only after:

- Requirement analysis completed
- Architecture reviewed
- Database designed
- API design completed

Recommended workflow:
Design

↓

Implementation Plan

↓

Code Generation

↓

Code Review

↓

Testing

↓

Documentation Update


---

# Prompt 23: Implement New Feature

## Purpose

ใช้สำหรับเริ่มพัฒนา Feature ใหม่หลังจากวางแผนแล้ว

---

## Prompt


Implement this feature based on the approved design.

Feature:

[PASTE FEATURE DESCRIPTION]

Requirements:

Follow MVC Architecture
Follow Repository Pattern
Follow Service Layer Pattern
Reuse existing components
Follow coding standards
Include error handling
Include JSDoc comments
Keep code maintainable

Before generating code:

List files to create
List files to modify
Explain implementation approach

Then generate code.


---

# Prompt 24: Create New Module

## Purpose

สร้าง Module ใหม่ตาม Architecture

---

## Prompt


Create a new application module.

Module:

[MODULE NAME]

Follow this structure:

Controller

Service

Repository

Model

Utility (if required)

Frontend Component

Define:

File structure
Responsibilities
Data flow
Dependencies

Generate production-ready code.


---

# Prompt 25: Create CRUD Feature

## Purpose

สร้างระบบ Create Read Update Delete

---

## Prompt


Create a complete CRUD feature.

Entity:

[ENTITY NAME]

Requirements:

Backend:

Controller
Service
Repository
Validation
Error handling

Frontend:

List view
Create form
Edit form
Delete confirmation
Loading state
Success notification
Error notification

Database:

Google Sheets schema
Validation rules

Follow project architecture.


---

# Prompt 26: Create Google Apps Script Backend

## Purpose

สร้าง Backend ด้วย GAS

---

## Prompt


Create Google Apps Script backend.

Requirements:

Google Apps Script V8
MVC architecture
Service layer
Repository pattern

Include:

Controller functions
Business logic
Data access layer
Validation
Error handling
Logging

Use:

const / let

ES2022 syntax

JSDoc comments


---

# Prompt 27: Create Repository Layer

## Purpose

สร้าง Data Access Layer

---

## Prompt


Create a repository class.

Entity:

[ENTITY NAME]

Responsibilities:

Read data
Create data
Update data
Delete data
Search data

Requirements:

Hide database implementation
Handle errors
Return clean data objects
Follow Repository Pattern

---

# Prompt 28: Create Service Layer

## Purpose

สร้าง Business Logic

---

## Prompt


Create service layer.

Business requirement:

[DESCRIPTION]

Responsibilities:

Validate business rules
Coordinate repositories
Handle workflow
Return processed results

Do not include UI logic.

Follow Single Responsibility Principle.


---

# Prompt 29: Create Controller Layer

## Purpose

สร้าง Controller

---

## Prompt


Create controller layer.

Responsibilities:

Receive requests
Validate input
Call services
Return responses

Do not include:

Database logic
Business rules
UI code

Include:

Error handling
Logging
Response formatting

---

# Prompt 30: Create Data Model

## Purpose

กำหนด Object Structure

---

## Prompt


Create data model for:

[ENTITY]

Define:

Properties
Data types
Required fields
Validation rules
Default values
Serialization format

Use clean object structure.


---

# Prompt 31: Create Frontend Component

## Purpose

สร้าง UI Component

---

## Prompt


Create a frontend component.

Technology:

HTML Service

Tailwind CSS

Vanilla JavaScript

Requirements:

Responsive
Mobile First
Dark Mode
Accessible
Reusable

Include:

HTML structure

JavaScript logic

Loading state

Empty state

Error state

Success notification


---

# Prompt 32: Create Dashboard Page

## Purpose

สร้างหน้า Dashboard

---

## Prompt


Create a modern SaaS dashboard.

Requirements:

Tailwind CSS
Responsive layout
Sidebar navigation
Navbar
Cards
Charts
Tables
Loading skeleton
Toast notifications

Style reference:

Google Workspace

Notion

Linear

Vercel

Supabase


---

# Prompt 33: Create Form Interface

## Purpose

สร้าง Form

---

## Prompt


Create a form interface.

Requirements:

Fields:

[LIST FIELDS]

Include:

Input validation
Error messages
Required indicators
Loading state
Submit handling
Success message
Mobile responsive layout

---

# Prompt 34: Create Data Table

## Purpose

สร้าง Table Component

---

## Prompt


Create reusable data table component.

Features:

Pagination
Search
Sorting
Filtering
Loading state
Empty state
Responsive mobile view
Action buttons

Use:

Tailwind CSS

Vanilla JavaScript


---

# Prompt 35: Create Modal Component

## Purpose

สร้าง Dialog / Modal

---

## Prompt


Create reusable modal component.

Requirements:

Open / Close control
Confirmation mode
Form mode
Accessibility
Keyboard support
Responsive design

Provide reusable implementation.


---

# Prompt 36: Create Notification System

## Purpose

สร้าง Toast Notification

---

## Prompt


Create toast notification system.

Support:

Success

Error

Warning

Information

Requirements:

Reusable
Global access
Auto dismiss
Animation
Mobile friendly

---

# Prompt 37: Create Loading System

## Purpose

สร้าง Loading Experience

---

## Prompt


Create loading system.

Include:

Global loading indicator
Button loading state
Skeleton loading
API request loading

Follow modern SaaS UX patterns.


---

# Prompt 38: Integrate External API

## Purpose

เชื่อมต่อ API ภายนอก

---

## Prompt


Integrate external API.

API:

[API INFORMATION]

Implement:

Request handling
Authentication
Error handling
Timeout handling
Response validation
Logging

Keep API logic separated from business logic.


---

# Prompt 39: Integrate MySQL Through Proxy

## Purpose

เชื่อม GAS กับ MySQL ผ่าน Node.js Proxy

---

## Prompt


Implement MySQL integration.

Architecture:

Google Apps Script

↓

REST API

↓

Node.js Express Proxy

↓

MySQL

Include:

API design
Authentication
Query handling
Error handling
Security considerations

Do not expose database credentials.


---

# Prompt 40: Generate Configuration System

## Purpose

สร้างระบบ Configuration

---

## Prompt


Create configuration management system.

Requirements:

Environment separation
Script Properties support
Secure secret handling
Central configuration access

Avoid hard-coded values.


---

# Implementation Checklist

Before completing feature development:

- [ ] Architecture followed
- [ ] MVC respected
- [ ] Repository Pattern used
- [ ] Validation implemented
- [ ] Error handling included
- [ ] Security considered
- [ ] UI responsive
- [ ] Documentation updated

---

# End of Part 3

Next:

Part 4 — Debugging, Code Review, Refactoring, Security Review Prompts

# Part 4 — Debugging, Code Review, Refactoring, Security Review Prompts

---

# Overview

This section provides prompts for maintaining and improving existing code.

The purpose is to help GitHub Copilot Agent act as:

- Debugging Assistant
- Senior Code Reviewer
- Software Architect
- Security Reviewer
- Performance Consultant

The AI Agent should analyze before modifying code.

Recommended workflow:
Issue

↓

Analysis

↓

Root Cause

↓

Solution Plan

↓

Implementation

↓

Verification


---

# Prompt 41: Debug Application Error

## Purpose

ใช้สำหรับวิเคราะห์ Error ทั่วไป

---

## Prompt


Debug this issue.

Error:

[PASTE ERROR MESSAGE]

Context:

[EXPLAIN CONTEXT]

Analyze:

Root cause
Affected files
Why this happened
Possible solutions
Recommended fix

Do not change code yet.

Explain your findings first.


---

# Prompt 42: Debug Google Apps Script Error

## Purpose

สำหรับ GAS โดยเฉพาะ

---

## Prompt


Debug this Google Apps Script issue.

Error:

[PASTE ERROR]

Review:

Server-side functions
doGet / doPost
Spreadsheet access
Permissions
Services
Triggers
API calls

Explain:

Root cause

Solution

Prevention strategy


---

# Prompt 43: Debug Frontend Issue

## Purpose

แก้ปัญหา HTML / JavaScript

---

## Prompt


Debug this frontend problem.

Issue:

[DESCRIPTION]

Review:

HTML structure
JavaScript logic
DOM handling
Event listeners
API communication
Browser compatibility

Provide:

Root cause

Fix approach

Code changes required


---

# Prompt 44: Debug Data Problem

## Purpose

ตรวจสอบข้อมูลผิดพลาด

---

## Prompt


Analyze this data issue.

Problem:

[DESCRIPTION]

Review:

Data structure
Validation
Database operation
Data transformation
Business rules

Identify:

Root cause

Data impact

Correction method

Prevention strategy


---

# Prompt 45: Performance Analysis

## Purpose

ปรับปรุง Performance

---

## Prompt


Analyze application performance.

Review:

Execution time
API calls
Google Sheets operations
Memory usage
Frontend rendering
Duplicate processing

Identify:

Performance bottlenecks

Optimization opportunities

Recommended improvements


---

# Prompt 46: Code Review

## Purpose

ตรวจสอบ Code Quality

---

## Prompt


Perform a professional code review.

Review:

Architecture

Code quality

Naming

Readability

Maintainability

Error handling

Security

Performance

Testing

Documentation

Provide:

Issues found

Severity level

Recommended improvements


---

# Prompt 47: Senior Architect Review

## Purpose

ตรวจระดับ Architecture

---

## Prompt


Act as a Principal Software Architect.

Review this implementation.

Evaluate:

Architecture compliance
Design patterns
Scalability
Maintainability
Technical debt
Future extension capability

Provide an architecture review report.


---

# Prompt 48: Refactor Code

## Purpose

ปรับปรุง Code

---

## Prompt


Refactor this code.

Goals:

Improve readability
Reduce duplication
Improve maintainability
Follow coding standards
Preserve existing behavior

Requirements:

Do not change business logic
Explain changes
Identify potential risks

---

# Prompt 49: Refactor Google Apps Script

## Purpose

ปรับปรุง GAS Code

---

## Prompt


Refactor this Google Apps Script code.

Improve:

Function structure
Service separation
Repository pattern usage
Error handling
Logging
Performance

Ensure compatibility with GAS V8.


---

# Prompt 50: Remove Technical Debt

## Purpose

ลดหนี้ทางเทคนิค

---

## Prompt


Analyze this codebase for technical debt.

Identify:

Duplicate code
Poor structure
Missing documentation
Security risks
Performance issues
Hard-coded values

Prioritize improvements by impact.


---

# Prompt 51: Security Review

## Purpose

ตรวจสอบ Security

---

## Prompt


Perform a security review.

Analyze:

Authentication

Authorization

Input validation

Data protection

API security

Secret management

Access control

Logging

Error handling

Identify vulnerabilities and recommend fixes.


---

# Prompt 52: Google Apps Script Security Review

## Purpose

ตรวจ GAS Security

---

## Prompt


Review this Google Apps Script application security.

Check:

Spreadsheet permissions
User authentication
Script Properties
External API credentials
Web App deployment settings
Data exposure risks
Access control

Provide recommendations.


---

# Prompt 53: RBAC Security Review

## Purpose

ตรวจระบบสิทธิ์

---

## Prompt


Review the RBAC implementation.

Analyze:

User roles
Permissions
Permission validation
Privilege escalation risks
Unauthorized access risks

Recommend improvements.


---

# Prompt 54: API Security Review

## Purpose

ตรวจ API

---

## Prompt


Review this API design.

Check:

Authentication

Authorization

Input validation

Rate limiting

Error responses

Data exposure

Injection risks

Logging

Provide security recommendations.


---

# Prompt 55: Data Privacy Review

## Purpose

ตรวจข้อมูลสำคัญ

---

## Prompt


Review data privacy considerations.

Analyze:

Sensitive data handling
Data access control
Data storage
Data transmission
Logging information

Recommend privacy improvements.


---

# Prompt 56: Error Handling Review

## Purpose

ตรวจ Error Management

---

## Prompt


Review error handling.

Check:

Try/catch usage
Error messages
User feedback
Logging
Recovery process
Security leakage

Recommend improvements.


---

# Prompt 57: Logging Review

## Purpose

ตรวจระบบ Log

---

## Prompt


Review application logging.

Analyze:

What should be logged
What should not be logged
Error tracking
Audit requirements
Debug information

Recommend logging strategy.


---

# Prompt 58: Dependency Review

## Purpose

ตรวจ Library และ Dependency

---

## Prompt


Review project dependencies.

Analyze:

Security risks
Version compatibility
Unused dependencies
Performance impact

Recommend updates.


---

# Prompt 59: Production Readiness Review

## Purpose

ตรวจว่าพร้อมใช้งานจริงหรือไม่

---

## Prompt


Evaluate if this application is production ready.

Review:

Architecture

Security

Performance

Testing

Documentation

Error handling

Deployment

Maintenance

Provide a production readiness checklist.


---

# Debug & Review Checklist

Before accepting changes:

- [ ] Root cause identified
- [ ] Solution reviewed
- [ ] Security checked
- [ ] Performance considered
- [ ] Tests completed
- [ ] Documentation updated
- [ ] No technical debt introduced

---

# End of Part 4

Next:

Part 5 — Testing, Documentation, Deployment, AI Agent Workflow, Quick Prompt Reference
# Part 5 — Testing, Documentation, Deployment, AI Agent Workflow, Quick Prompt Reference

---

# Overview

This section contains final-stage prompts used after implementation.

The purpose is to ensure:

- Quality assurance
- Complete documentation
- Deployment readiness
- AI Agent consistency
- Long-term maintainability

Recommended workflow:
Implementation

↓

Testing

↓

Documentation

↓

Deployment Review

↓

Production Release

↓

Maintenance


---

# Prompt 60: Create Testing Plan

## Purpose

วางแผนการทดสอบก่อน Deploy

---

## Prompt


Create a complete testing plan for this feature.

Feature:

[FEATURE NAME]

Include:

Unit tests
Integration tests
Functional tests
User acceptance tests
Security tests
Performance tests
Edge cases

Provide test scenarios and expected results.


---

# Prompt 61: Generate Test Cases

## Purpose

สร้าง Test Case

---

## Prompt


Generate test cases for this feature.

Include:

Test ID

Test Scenario

Precondition

Test Steps

Expected Result

Priority

Negative Cases

Edge Cases


---

# Prompt 62: Test Code Review

## Purpose

ตรวจสอบคุณภาพ Test

---

## Prompt


Review the existing tests.

Analyze:

Test coverage
Missing scenarios
Edge cases
Test reliability
Maintainability

Recommend improvements.


---

# Prompt 63: Create Documentation

## Purpose

สร้างเอกสารประกอบ Feature

---

## Prompt


Create documentation for this feature.

Include:

Overview

Purpose

Architecture

User Flow

Configuration

Usage Instructions

API Reference

Database Changes

Security Considerations

Testing Information

Troubleshooting


---

# Prompt 64: Update README

## Purpose

ปรับ README หลังเพิ่ม Feature

---

## Prompt


Update README.md based on this new feature.

Include:

Feature description

Installation

Configuration

Usage example

Screenshots (if applicable)

Related documentation

Keep the existing README structure.


---

# Prompt 65: Update AI Context

## Purpose

ปรับปรุง AI Knowledge Base

---

## Prompt


Update AI Context documentation.

Analyze this implementation change.

Identify:

New modules
New patterns
New rules
New components
New dependencies

Update docs/30_AI_CONTEXT.md accordingly.


---

# Prompt 66: Create Deployment Checklist

## Purpose

ตรวจสอบก่อน Deploy

---

## Prompt


Create deployment checklist.

Application:

[APPLICATION NAME]

Include:

Configuration

Environment setup

Permissions

Database preparation

Security review

Testing

Backup

Rollback plan

Post-deployment verification


---

# Prompt 67: Google Apps Script Deployment Review

## Purpose

ตรวจ GAS Deployment

---

## Prompt


Review Google Apps Script deployment readiness.

Check:

Web App settings
Permissions
Script Properties
Spreadsheet access
OAuth scopes
Trigger configuration
Version management

Provide deployment recommendations.


---

# Prompt 68: Production Deployment Plan

## Purpose

วางแผน Deploy จริง

---

## Prompt


Create production deployment plan.

Include:

Pre-deployment checklist
Deployment steps
Configuration changes
Validation steps
Monitoring
Rollback strategy
Post-deployment tasks

---

# Prompt 69: Create Release Notes

## Purpose

สร้าง Release Note

---

## Prompt


Create release notes.

Version:

[VERSION]

Include:

New features

Bug fixes

Improvements

Breaking changes

Migration steps

Known issues


---

# Prompt 70: AI Agent Self Review

## Purpose

ให้ AI ตรวจงานตัวเอง

---

## Prompt


Review your previous implementation.

Check:

Did you follow repository rules?
Did you follow architecture?
Did you introduce security issues?
Did you update documentation?
Is the code production ready?

Provide a self-review report.


---

# Prompt 71: AI Agent Planning Mode

## Purpose

ให้ AI ทำงานแบบ Architect

---

## Prompt


Act as a Principal Software Architect.

Do not write code.

Analyze:

Problem

Architecture

Solution options

Trade-offs

Risks

Implementation plan

Wait for approval.


---

# Prompt 72: AI Agent Implementation Mode

## Purpose

ให้ AI เริ่ม Coding หลังวางแผน

---

## Prompt


Based on the approved plan:

Implement the solution.

Rules:

Follow repository architecture
Follow coding standards
Reuse existing components
Include error handling
Include documentation

After implementation:

Explain changes and testing approach.


---

# Prompt 73: AI Agent Maintenance Mode

## Purpose

ดูแลระบบหลังใช้งาน

---

## Prompt


Act as a maintenance engineer.

Analyze this application.

Review:

Current health

Known issues

Performance

Security

Technical debt

Improvement opportunities

Create maintenance recommendations.


---

# Quick Prompt Reference

## Start Project


Read repository documentation and explain the architecture.
Do not code yet.


---

## Analyze Feature


Analyze this requirement and create an implementation plan.


---

## Design Architecture


Design a scalable architecture following project standards.


---

## Create Feature


Implement this feature following MVC and Repository Pattern.


---

## Create CRUD


Create complete CRUD with validation and error handling.


---

## Debug


Analyze this error and identify root cause before fixing.


---

## Review Code


Perform professional code review.


---

## Refactor


Refactor this code without changing behavior.


---

## Security


Perform security review and identify vulnerabilities.


---

## Testing


Create test cases and validation scenarios.


---

## Documentation


Update documentation according to this change.


---

## Deployment


Create deployment checklist and rollback plan.


---

# Recommended AI Agent Workflow

For every development task:

Understand

↓

Analyze

↓

Plan

↓

Approve

↓

Implement

↓

Review

↓

Test

↓

Document

---

# Golden Rules for GitHub Copilot Agent

Always:

✅ Read documentation first

✅ Understand architecture

✅ Explain before coding

✅ Reuse existing code

✅ Follow security practices

✅ Update documentation

✅ Review generated code

---

Never:

❌ Generate random code

❌ Ignore architecture

❌ Duplicate components

❌ Hard-code secrets

❌ Skip testing

❌ Skip documentation

---

# End of 38_COPILOT_PROMPT_LIBRARY.md
