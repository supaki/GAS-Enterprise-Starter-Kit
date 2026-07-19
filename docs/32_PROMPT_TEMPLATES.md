<!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 1A : Foundation Prompts -->
<!-- ====================================================================== -->

# Prompt Templates

Version 2.0

Enterprise Prompt Library for GitHub Copilot Agent

---

# Purpose

This document provides standardized prompts for GitHub Copilot Agent.

Objectives

- Produce consistent code
- Reduce development time
- Improve AI understanding
- Maintain Clean Architecture
- Follow MVC
- Generate production-ready applications

Supported Stack

- Google Apps Script
- Google Sheets
- HTML5
- Tailwind CSS
- JavaScript ES6+
- GitHub Copilot Agent

---

# How to Use

Every prompt should contain five sections.

| Section | Purpose |
|----------|----------|
| Context | Project Background |
| Goal | Objective |
| Requirements | Functional Requirements |
| Constraints | Project Rules |
| Output | Expected Result |

---

# Standard Prompt Structure

```
Context

↓

Goal

↓

Requirements

↓

Constraints

↓

Output
```

---

# Universal Project Context

Always include this context.

```
Project

GAS Enterprise Starter Kit

Technology

Google Apps Script

Google Sheets

HTML5

Tailwind CSS

JavaScript ES6+

Architecture

MVC

Clean Architecture

Repository Pattern

Service Layer

Coding Standard

Enterprise

Responsive

Dark Mode

Reusable Components
```

---

# Master System Prompt

```
You are an Enterprise Software Architect.

You are developing a production-ready web application.

Technology

Google Apps Script

Google Sheets

HTML5

Tailwind CSS

JavaScript ES6+

Architecture

MVC

Repository Pattern

Service Layer

Always

Analyze first.

Reuse existing modules.

Generate production-ready code.

Never duplicate code.

Never hard-code secrets.

Follow all project documentation.
```

---

# Requirement Analysis Prompt

Purpose

Analyze requirements before coding.

Prompt

```
Analyze the following requirement.

Identify

• Features

• Business Rules

• User Roles

• Database Entities

• UI Components

• APIs

• Risks

• Dependencies

Do not generate code.

Return the analysis as a structured document.
```

Expected Output

- Feature List
- User Stories
- Business Rules
- Development Scope

---

# Feature Breakdown Prompt

Prompt

```
Break this requirement into independent features.

For each feature provide

- Description

- Priority

- Complexity

- Dependencies

- Estimated Development Order
```

Example Output

| Feature | Priority |
|----------|-----------|
| Login | High |
| Dashboard | High |
| Users | High |
| Reports | Medium |
| Settings | Low |

---

# User Story Prompt

Prompt

```
Create User Stories.

Format

As a ...

I want ...

So that ...

Include acceptance criteria.
```

Example

```
As an administrator

I want to manage users

So that I can control system access.
```

---

# Acceptance Criteria Prompt

Prompt

```
Generate acceptance criteria.

Include

Happy Path

Validation

Permission

Performance

Error Cases
```

---

# Scope Definition Prompt

Prompt

```
Define project scope.

Separate

Included

Excluded

Future Development

Technical Constraints
```

---

# Functional Requirement Prompt

Prompt

```
Extract all functional requirements.

Return as numbered list.

Explain each requirement.
```

---

# Non-functional Requirement Prompt

Prompt

```
Identify all non-functional requirements.

Include

Performance

Security

Scalability

Maintainability

Accessibility

Availability
```

---

# Business Rule Prompt

Prompt

```
Extract business rules.

Return

Rule

Description

Reason

Affected Module
```

Example

| Rule | Description |
|-------|-------------|
| BR001 | Username must be unique |

---

# User Role Prompt

Prompt

```
Identify user roles.

For each role explain

Responsibilities

Permissions

Restrictions

Accessible Modules
```

---

# Permission Matrix Prompt

Prompt

```
Create RBAC Permission Matrix.

Roles

Admin

Manager

User

Guest

Return as table.
```

Example

| Module | Admin | User |
|----------|---------|--------|
| Dashboard | ✓ | ✓ |
| Settings | ✓ | ✗ |

---

# Entity Identification Prompt

Prompt

```
Identify all business entities.

Return

Entity

Purpose

Relationships

Owner

CRUD Required
```

---

# Data Flow Prompt

Prompt

```
Explain the complete data flow.

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

Google Sheets

Return a step-by-step explanation.
```

---

# Risk Analysis Prompt

Prompt

```
Analyze project risks.

Include

Security

Performance

Data Integrity

Maintainability

Deployment

Mitigation Plan
```

---

# Dependency Analysis Prompt

Prompt

```
List all project dependencies.

Classify

Internal

External

Third-party

Google Services
```

---

# Technical Constraint Prompt

Prompt

```
Identify technical constraints.

Include

Google Apps Script Limits

Google Sheets Limits

Browser Compatibility

Authentication

Deployment
```

---

# Architecture Readiness Prompt

Prompt

```
Determine whether the project is ready for implementation.

Verify

Requirements

Architecture

Database

Business Rules

Acceptance Criteria

Return missing items if any.
```

---

# AI Planning Prompt

Prompt

```
Create implementation roadmap.

Order tasks by dependency.

Estimate complexity.

Suggest implementation phases.

Do not generate code.
```

---

# Best Practices

Always

✓ Analyze first

✓ Define scope

✓ Identify entities

✓ Identify user roles

✓ Review business rules

✓ Review documentation

Never

✗ Generate code before analysis

✗ Assume missing requirements

✗ Ignore existing architecture

✗ Skip planning

---

# Foundation Workflow

```
Requirement

↓

Requirement Analysis

↓

Feature Breakdown

↓

Business Rules

↓

User Stories

↓

Acceptance Criteria

↓

Architecture Planning

↓

Database Planning

↓

Implementation
```

---

# Quick Prompt Index

| Prompt | Purpose |
|----------|----------|
| Master System | Initialize AI |
| Requirement Analysis | Analyze requirements |
| Feature Breakdown | Split project |
| User Story | Generate stories |
| Acceptance Criteria | Define success |
| Business Rule | Extract rules |
| Entity Identification | Discover data |
| User Role | RBAC planning |
| Risk Analysis | Identify risks |
| AI Planning | Development roadmap |

---

# End of Part 1A

Next

**Part 1B**

Architecture Prompts

Database Planning Prompts

Folder Structure Prompts

Google Sheets Design Prompts

API Planning Prompts

UI Planning Prompts

<!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 1B-1 : Architecture & Module Planning Prompts -->
<!-- ====================================================================== -->

# Part 1B-1 — Architecture & Module Planning Prompts

Version 2.0

---

# Purpose

This section provides prompt templates for designing the overall system architecture before implementation.

GitHub Copilot Agent should complete this phase before generating any source code.

Objectives

- Define application architecture
- Design project structure
- Identify modules
- Define responsibilities
- Plan development order
- Prevent architectural problems

---

# Architecture Design Workflow

```
Requirement

↓

Requirement Analysis

↓

Architecture Design

↓

Folder Structure

↓

Module Planning

↓

Component Planning

↓

Database Design

↓

Implementation
```

---

# Enterprise Architecture Prompt

## Purpose

Design the complete system architecture.

## Prompt

```text
Act as an Enterprise Software Architect.

Design the architecture for this project.

Technology

- Google Apps Script
- Google Sheets
- HTML5
- Tailwind CSS
- JavaScript ES6+

Architecture

- MVC
- Clean Architecture
- Repository Pattern
- Service Layer

Return

1. Overall Architecture
2. Data Flow
3. Layer Responsibilities
4. Folder Structure
5. Design Decisions
6. Risks
7. Best Practices

Do not generate code.
```

---

# MVC Planning Prompt

## Prompt

```text
Design the MVC architecture.

Explain

- View
- Controller
- Service
- Repository
- Model
- Utility

For each layer explain

- Responsibility
- Input
- Output
- Dependencies

Return diagrams using Markdown.
```

---

# Clean Architecture Prompt

## Prompt

```text
Review this project.

Design using Clean Architecture.

Identify

- Core Layer
- Application Layer
- Infrastructure Layer
- Presentation Layer

Explain communication between layers.

Do not generate implementation.
```

---

# Repository Pattern Prompt

## Prompt

```text
Design Repository Layer.

Requirements

- Google Sheets
- Batch Operations
- Reusable Methods

Return

Repository List

Responsibilities

Method List

Naming Convention
```

---

# Service Layer Prompt

## Prompt

```text
Design Service Layer.

Business Logic only.

No Spreadsheet code.

Return

Service Name

Responsibilities

Methods

Dependencies
```

---

# Controller Planning Prompt

## Prompt

```text
Design Controller Layer.

Responsibilities

- Request Handling

- Validation

- Service Calls

- Response

Return one controller per module.
```

---

# Module Identification Prompt

## Prompt

```text
Analyze requirements.

Identify all modules.

Return

Module Name

Purpose

Priority

Dependencies

Estimated Size

Owner
```

Example

| Module | Purpose |
|----------|------------|
| Dashboard | Home |
| Users | User Management |
| Reports | Analytics |

---

# Module Dependency Prompt

## Prompt

```text
Create module dependency graph.

Identify

Independent Modules

Dependent Modules

Reusable Modules

Core Modules

Infrastructure Modules
```

---

# Feature Priority Prompt

## Prompt

```text
Prioritize features.

Categories

Critical

High

Medium

Low

Explain why.
```

---

# Folder Structure Prompt

## Prompt

```text
Design project folder structure.

Requirements

Google Apps Script

MVC

Clean Architecture

Repository Pattern

Return complete folder tree.

Explain every folder.
```

---

# Standard Folder Structure

```text
src/

controllers/

services/

repositories/

models/

utils/

web/

components/

layouts/

pages/

css/

js/

assets/

tests/
```

---

# File Naming Prompt

## Prompt

```text
Define file naming conventions.

Include

Controllers

Services

Repositories

Models

HTML

JavaScript

Utilities

Examples required.
```

---

# Naming Convention

| Type | Example |
|----------|--------------------|
| Controller | UserController.gs |
| Service | UserService.gs |
| Repository | UserRepository.gs |
| Model | UserModel.gs |
| HTML | Dashboard.html |
| JS | dashboard.js |

---

# Component Planning Prompt

## Prompt

```text
Design reusable UI components.

Requirements

Tailwind CSS

Responsive

Dark Mode

Accessible

Reusable

Return

Component

Purpose

Properties

Events
```

---

# Shared Component Prompt

## Prompt

```text
List all reusable components.

Include

Navbar

Sidebar

Cards

Buttons

Forms

Tables

Modals

Alerts

Toast

Pagination

Loading

Empty State
```

---

# Layout Planning Prompt

## Prompt

```text
Design application layouts.

Include

Login

Dashboard

CRUD

Settings

Report

Responsive

Dark Mode
```

---

# Navigation Planning Prompt

## Prompt

```text
Design navigation.

Include

Sidebar

Top Navigation

Breadcrumb

Quick Actions

Search

Profile Menu

Notifications
```

---

# Routing Prompt

## Prompt

```text
Design routing strategy.

Include

Pages

Navigation

Authentication

Authorization

Error Pages

Loading State
```

---

# Module Responsibility Prompt

## Prompt

```text
For every module explain

Purpose

Responsibilities

Dependencies

Input

Output

Business Rules

Return as table.
```

---

# Project Bootstrap Prompt

## Prompt

```text
Prepare project bootstrap plan.

Return

Folder Creation

Configuration

Core Modules

Shared Components

Development Order
```

---

# Development Roadmap Prompt

## Prompt

```text
Create implementation roadmap.

Phase 1

Core System

Phase 2

Authentication

Phase 3

Dashboard

Phase 4

Business Modules

Phase 5

Reports

Phase 6

Deployment
```

---

# Architecture Review Prompt

## Prompt

```text
Review current architecture.

Verify

MVC

Repository Pattern

Service Layer

Scalability

Maintainability

Security

Suggest improvements.
```

---

# Refactoring Architecture Prompt

## Prompt

```text
Analyze current architecture.

Identify

Duplicated Layers

Unused Components

Tight Coupling

Large Classes

Suggest better architecture.

No code generation.
```

---

# Architecture Checklist

Before implementation verify

- Architecture documented

- Folder structure approved

- Module list complete

- Dependencies identified

- Naming convention defined

- Components identified

- Development roadmap approved

---

# Best Practices

Always

✓ Design before coding

✓ Create reusable modules

✓ Separate responsibilities

✓ Follow MVC

✓ Keep services independent

✓ Use Repository Pattern

✓ Plan for scalability

Never

✗ Put business logic inside HTML

✗ Mix Controller with Repository

✗ Duplicate modules

✗ Skip architecture review

✗ Generate code before planning

---

# Quick Prompt Index

| Prompt | Purpose |
|----------|----------|
| Enterprise Architecture | Overall design |
| MVC Planning | MVC responsibilities |
| Clean Architecture | Layer design |
| Repository Planning | Data layer |
| Service Planning | Business layer |
| Controller Planning | Request handling |
| Module Identification | Discover modules |
| Folder Structure | Project organization |
| Component Planning | UI components |
| Navigation Planning | UX flow |
| Architecture Review | Review architecture |
| Development Roadmap | Planning implementation |

---

# End of Part 1B-1

Next

**Part 1B-2**

- Database Planning Prompts
- Google Sheets Design Prompts
- API Planning Prompts
- UI Planning Prompts
- Design System Prompts
- Wireframe Prompts
- User Flow Prompts
- Information Architecture Prompts

  <!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 1B-2A : Database & Google Sheets Planning Prompts -->
<!-- ====================================================================== -->

# Part 1B-2A — Database & Google Sheets Planning Prompts

Version 2.0

---

# Purpose

This section provides prompt templates for designing the data layer of applications built with:

- Google Apps Script
- Google Sheets
- MVC
- Repository Pattern

The objective is to create scalable, maintainable, and production-ready spreadsheet databases before implementation begins.

---

# Database Design Workflow

```text
Business Requirement

↓

Business Rules

↓

Entities

↓

Relationships

↓

Google Sheets Structure

↓

Validation Rules

↓

Repository Design

↓

Implementation
```

---

# Database Design Prompt

## Purpose

Create a complete database design before coding.

## Prompt

```text
Act as a Database Architect.

Design the database for this project.

Technology

- Google Sheets
- Google Apps Script

Requirements

1. Identify entities
2. Define columns
3. Define data types
4. Define relationships
5. Define validation rules
6. Define indexes
7. Explain design decisions

Return documentation only.

Do not generate code.
```

---

# Entity Identification Prompt

## Prompt

```text
Analyze the project.

List every business entity.

For each entity explain

- Purpose
- Owner
- CRUD Required
- Relationships
- Expected Record Count

Return as table.
```

Example

| Entity | Purpose |
|----------|----------|
| Users | User Management |
| Patients | Patient Information |
| Appointments | Scheduling |

---

# Google Sheets Schema Prompt

## Prompt

```text
Design Google Sheets schema.

Return

Sheet Name

Purpose

Columns

Primary Key

Validation

Relationships

Sample Data
```

---

# Spreadsheet Structure Prompt

## Prompt

```text
Create spreadsheet structure.

Requirements

Separate sheets by entity.

Avoid duplicated data.

Use lookup tables where appropriate.

Return complete workbook design.
```

---

# Sheet Naming Prompt

## Prompt

```text
Suggest sheet names.

Rules

Singular or plural consistently

Short

Meaningful

Alphabetical if possible
```

Example

```text
Users

Roles

Permissions

Departments

Patients

Visits

Settings
```

---

# Column Design Prompt

## Prompt

```text
Design columns.

Include

Column Name

Description

Data Type

Required

Default Value

Validation
```

Example

| Column | Type | Required |
|----------|---------|-----------|
| userId | UUID | Yes |
| username | Text | Yes |
| email | Email | Yes |
| status | Enum | Yes |

---

# Primary Key Prompt

## Prompt

```text
Choose primary key strategy.

Options

UUID

Auto Increment

Timestamp

Composite Key

Explain advantages.

Recommend one.
```

Recommended

```
UUID
```

---

# Relationship Prompt

## Prompt

```text
Identify relationships.

One-to-One

One-to-Many

Many-to-Many

Explain implementation using Google Sheets.
```

Example

```
Department

↓

Users

One-to-Many
```

---

# Lookup Table Prompt

## Prompt

```text
Identify lookup tables.

Explain

Purpose

Columns

Referenced By

Benefits
```

Example

```
Roles

Departments

Status

Gender

Countries
```

---

# Audit Fields Prompt

## Prompt

```text
Add audit fields.

Include

createdAt

createdBy

updatedAt

updatedBy

deletedAt

deletedBy
```

---

# Soft Delete Prompt

## Prompt

```text
Design soft delete strategy.

Requirements

Restore capability

Audit trail

No permanent deletion

Explain implementation.
```

---

# Validation Prompt

## Prompt

```text
Create validation rules.

Include

Required

Unique

Email

Phone

Date

Number Range

Reference Integrity
```

---

# Data Dictionary Prompt

## Prompt

```text
Generate Data Dictionary.

Include

Column

Description

Type

Length

Required

Validation

Example
```

---

# Sample Data Prompt

## Prompt

```text
Generate sample data.

Requirements

Realistic

Consistent

Valid

At least five records per table.
```

---

# Spreadsheet Configuration Prompt

## Prompt

```text
Design workbook configuration.

Include

Settings Sheet

Configuration Sheet

Master Data

Logs

Audit

System Variables
```

---

# Master Data Prompt

## Prompt

```text
Identify master data.

Explain

Purpose

Owner

Frequency of Update

Referenced Modules
```

---

# Transaction Data Prompt

## Prompt

```text
Identify transaction tables.

Explain

Purpose

Relationships

Volume

Lifecycle
```

---

# Repository Planning Prompt

## Prompt

```text
Design Repository Layer.

For every sheet define

Repository Name

Methods

Read

Create

Update

Delete

Search

Pagination
```

---

# Search Strategy Prompt

## Prompt

```text
Design search strategy.

Include

Exact Match

Partial Match

Multiple Conditions

Sorting

Pagination
```

---

# Import / Export Prompt

## Prompt

```text
Design import and export process.

Support

CSV

Excel

Google Sheets

Validation

Duplicate Detection

Error Report
```

---

# Backup Strategy Prompt

## Prompt

```text
Design backup strategy.

Include

Automatic Backup

Manual Backup

Restore

Versioning

Disaster Recovery
```

---

# Performance Planning Prompt

## Prompt

```text
Optimize Google Sheets.

Consider

Batch Read

Batch Write

CacheService

LockService

Pagination

Large Dataset
```

---

# Data Security Prompt

## Prompt

```text
Review database security.

Include

Sensitive Data

Encryption

Access Control

Audit

Logging

Backup
```

---

# Database Review Prompt

## Prompt

```text
Review current database design.

Verify

Normalization

Relationships

Validation

Performance

Maintainability

Scalability

Suggest improvements.
```

---

# Database Planning Checklist

Before implementation verify

- [ ] Entities identified
- [ ] Sheets defined
- [ ] Columns documented
- [ ] Primary keys selected
- [ ] Relationships documented
- [ ] Validation completed
- [ ] Audit fields added
- [ ] Master data identified
- [ ] Repository planned
- [ ] Performance reviewed

---

# Google Sheets Best Practices

Always

✓ One entity per sheet

✓ UUID as primary key

✓ Batch read/write

✓ Validation rules

✓ Audit fields

✓ Lookup tables

✓ Soft delete

✓ Configuration sheet

Never

✗ Duplicate data

✗ Hard-code row numbers

✗ Mix configuration with transaction data

✗ Read/write one cell at a time

✗ Store passwords in sheets

---

# Quick Prompt Index

| Prompt | Purpose |
|---------|---------|
| Database Design | Overall database planning |
| Entity Identification | Discover entities |
| Google Sheets Schema | Workbook structure |
| Column Design | Define columns |
| Relationship | Data relationships |
| Validation | Input validation |
| Repository Planning | Repository methods |
| Search Strategy | Query planning |
| Performance Planning | Optimize Sheets |
| Database Review | Architecture review |

---

# End of Part 1B-2A

Next

**Part 1B-2B**

- API Planning Prompts
- UI Planning Prompts
- Design System Prompts
- Wireframe Prompts
- User Flow Prompts
- Information Architecture Prompts
- Enterprise Checklists
- Best Practices
```

<!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 1B-2B-1 : API Planning Prompts -->
<!-- ====================================================================== -->

# Part 1B-2B-1 — API Planning Prompts

Version 2.0

Enterprise Prompt Library

---

# Purpose

This section contains prompt templates for designing APIs for Google Apps Script applications.

Supported Architecture

- MVC
- Clean Architecture
- Repository Pattern
- Service Layer

Supported Backend

- Google Apps Script Web App
- Google Sheets
- External REST API
- Local API Gateway
- MySQL API

---

# API Design Workflow

```text
Business Requirement

↓

Business Rules

↓

API Resources

↓

Endpoint Design

↓

Request Validation

↓

Business Logic

↓

Repository

↓

Google Sheets

↓

Response
```

---

# API Architecture Prompt

## Purpose

Design a complete API architecture.

## Prompt

```text
Act as an Enterprise API Architect.

Technology

Google Apps Script

Google Sheets

REST API

Design

- API Structure
- Endpoints
- Resources
- Authentication
- Validation
- Response Format
- Error Handling

Do not generate code.
```

---

# REST API Planning Prompt

## Prompt

```text
Design REST API.

Include

Resources

Methods

Routes

Status Codes

Response Format

Examples
```

---

# Endpoint Design Prompt

## Prompt

```text
Design API endpoints.

Return

Endpoint

HTTP Method

Purpose

Permission

Input

Output

Example

Expected Response
```

Example

| Method | Endpoint | Description |
|----------|-----------|------------|
| GET | /users | List Users |
| GET | /users/{id} | Detail |
| POST | /users | Create |
| PUT | /users/{id} | Update |
| DELETE | /users/{id} | Delete |

---

# Resource Identification Prompt

## Prompt

```text
Identify API resources.

Explain

Purpose

Relationships

CRUD Operations

Permissions

Dependencies
```

---

# Request Model Prompt

## Prompt

```text
Create request models.

Include

Required Fields

Optional Fields

Validation

Default Values

Example JSON
```

Example

```json
{
  "username": "",
  "email": "",
  "roleId": ""
}
```

---

# Response Model Prompt

## Prompt

```text
Create standard API response.

Include

Success

Failure

Validation Error

Permission Error

Server Error
```

---

# Success Response Standard

```json
{
    "success": true,
    "message": "Success",
    "data": {},
    "timestamp": ""
}
```

---

# Error Response Standard

```json
{
    "success": false,
    "message": "Validation failed",
    "errors": [],
    "timestamp": ""
}
```

---

# Pagination Prompt

## Prompt

```text
Design pagination.

Include

Page

Page Size

Total

Total Pages

Sorting

Filtering

Search
```

Example

```json
{
  "page":1,
  "pageSize":20,
  "total":150
}
```

---

# Search API Prompt

## Prompt

```text
Create search endpoint.

Support

Keyword

Filter

Sort

Pagination

Multiple Conditions
```

---

# Filter Design Prompt

## Prompt

```text
Design filtering system.

Include

Equals

Contains

Starts With

Ends With

Date Range

Status

Owner
```

---

# Sorting Prompt

## Prompt

```text
Design sorting.

Support

Ascending

Descending

Multiple Fields
```

---

# Validation Prompt

## Prompt

```text
Design request validation.

Include

Required

Unique

Email

Phone

Date

Number

Length

Regex

Reference Integrity
```

---

# Authentication Prompt

## Prompt

```text
Design API authentication.

Support

Google Account

Session

Token

API Key

OAuth

Explain advantages.
```

---

# Authorization Prompt

## Prompt

```text
Design authorization.

Roles

Admin

Manager

User

Guest

Return permission matrix.
```

---

# Error Handling Prompt

## Prompt

```text
Design API error handling.

Include

400

401

403

404

409

422

429

500

503

Return JSON examples.
```

---

# Logging Prompt

## Prompt

```text
Design API logging.

Capture

Request

Response

Execution Time

User

Errors

IP

Timestamp
```

---

# Audit Prompt

## Prompt

```text
Design audit logging.

Track

Create

Update

Delete

Login

Permission Changes
```

---

# Rate Limiting Prompt

## Prompt

```text
Design API rate limiting.

Include

Maximum Requests

Time Window

Retry

Response
```

---

# Security Prompt

## Prompt

```text
Review API security.

Verify

Authentication

Authorization

Validation

Sanitization

Sensitive Data

Logging

Replay Protection
```

---

# Google Apps Script API Prompt

## Prompt

```text
Design Google Apps Script Web App API.

Include

doGet()

doPost()

Routing

Controller

JSON Response

Error Handling
```

---

# External API Prompt

## Prompt

```text
Design integration with external API.

Include

Authentication

Headers

Retry

Timeout

Caching

Logging

Error Handling
```

---

# Local API Gateway Prompt

## Prompt

```text
Design communication with Local API.

Requirements

REST

HTTPS

JSON

Authentication

Retry

Timeout

Caching
```

---

# API Documentation Prompt

## Prompt

```text
Generate API documentation.

Include

Overview

Authentication

Endpoints

Parameters

Examples

Responses

Error Codes

Best Practices
```

---

# API Review Prompt

## Prompt

```text
Review API design.

Verify

REST Standards

Consistency

Security

Performance

Maintainability

Scalability

Suggest improvements.
```

---

# API Planning Checklist

Before implementation verify

- [ ] Resources identified
- [ ] Endpoints designed
- [ ] Request models defined
- [ ] Response models defined
- [ ] Validation rules documented
- [ ] Authentication selected
- [ ] Authorization completed
- [ ] Error handling standardized
- [ ] Logging strategy defined
- [ ] API documentation prepared

---

# API Best Practices

Always

✓ Use REST principles

✓ Return JSON

✓ Validate all inputs

✓ Use standard response format

✓ Return proper HTTP status

✓ Log all errors

✓ Secure every endpoint

✓ Separate Controller and Service

Never

✗ Return HTML from API

✗ Hard-code credentials

✗ Skip validation

✗ Expose stack traces

✗ Mix business logic with routing

✗ Return inconsistent response structures

---

# Standard API Response

Success

```json
{
  "success": true,
  "message": "Operation completed successfully.",
  "data": {},
  "timestamp": "2026-07-19T12:00:00Z"
}
```

Validation Error

```json
{
  "success": false,
  "message": "Validation failed.",
  "errors": [
    {
      "field": "email",
      "message": "Invalid email format."
    }
  ],
  "timestamp": "2026-07-19T12:00:00Z"
}
```

Server Error

```json
{
  "success": false,
  "message": "Internal server error.",
  "errorCode": "ERR-500",
  "timestamp": "2026-07-19T12:00:00Z"
}
```

---

# Quick Prompt Index

| Prompt | Purpose |
|---------|---------|
| API Architecture | Overall API design |
| REST API Planning | REST resource planning |
| Endpoint Design | Endpoint specification |
| Request Model | Input schema |
| Response Model | Output schema |
| Validation | Request validation |
| Authentication | Authentication strategy |
| Authorization | RBAC planning |
| Error Handling | Error response design |
| Logging | API logging |
| Audit | Audit trail |
| Security | Security review |
| Google Apps Script API | GAS Web App API |
| External API | Third-party integration |
| API Documentation | API reference |
| API Review | Final architecture review |

---

# End of Part 1B-2B-1

Next

**Part 1B-2B-2**

- UI Planning Prompts
- Design System Prompts
- SaaS Dashboard Prompts
- Tailwind CSS Prompts
- Wireframe Prompts
- User Flow Prompts
- Information Architecture Prompts
- UX Review Prompts
- Enterprise UI Checklist
- Modern SaaS Best Practices

  <!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 1B-2B-2A : UI Planning & SaaS Dashboard Prompts -->
<!-- ====================================================================== -->

# Part 1B-2B-2A — UI Planning & SaaS Dashboard Prompts

Version 2.0

Enterprise Prompt Library

---

# Purpose

This section provides prompt templates for planning and designing a modern SaaS user interface for applications built with:

- Google Apps Script
- HTML Service
- Tailwind CSS
- JavaScript ES6+

The goal is to create responsive, accessible, reusable, and enterprise-grade user interfaces before implementation.

---

# UI Design Workflow

```text
Requirement

↓

User Analysis

↓

Information Architecture

↓

Layout Planning

↓

Component Planning

↓

Wireframe

↓

Responsive Design

↓

Implementation
```

---

# UI Planning Prompt

## Purpose

Plan the complete UI before writing HTML.

## Prompt

```text
Act as a Senior UI/UX Designer.

Design a modern SaaS interface.

Technology

- Google Apps Script
- HTML Service
- Tailwind CSS

Requirements

- Responsive
- Clean
- Accessible
- Enterprise
- Dark Mode Ready

Return

1. Layout
2. Navigation
3. Components
4. User Journey
5. Responsive Strategy

Do not generate code.
```

---

# Dashboard Planning Prompt

## Prompt

```text
Design a modern SaaS Dashboard.

Include

- Sidebar
- Top Navigation
- KPI Cards
- Charts
- Recent Activity
- Quick Actions
- Notifications
- Responsive Layout

Explain each section.
```

---

# Login Screen Prompt

## Prompt

```text
Design Login Page.

Include

Logo

Welcome Message

Username

Password

Remember Me

Forgot Password

Dark Mode

Responsive

Accessibility
```

---

# Sidebar Prompt

## Prompt

```text
Design enterprise sidebar.

Include

Dashboard

Master Data

Transactions

Reports

Settings

User Profile

Collapse Mode

Icons

Badges

Permission-based Menu
```

---

# Top Navigation Prompt

## Prompt

```text
Design Top Navigation.

Include

Breadcrumb

Search

Notification

Theme Switch

Profile Menu

Language

Responsive Behavior
```

---

# Dashboard Card Prompt

## Prompt

```text
Design KPI Cards.

Each card contains

Title

Value

Trend

Icon

Color Indicator

Action

Loading State
```

---

# Table Planning Prompt

## Prompt

```text
Design reusable data table.

Support

Sorting

Searching

Filtering

Pagination

Export

Row Selection

Responsive
```

---

# Form Planning Prompt

## Prompt

```text
Design enterprise forms.

Support

Validation

Required Fields

Readonly

Disabled

Autocomplete

Date Picker

Lookup

File Upload

Responsive Layout
```

---

# Modal Prompt

## Prompt

```text
Design reusable modal.

Include

Header

Body

Footer

Buttons

Animation

Loading

Accessibility
```

---

# Toast Notification Prompt

## Prompt

```text
Design notification system.

Support

Success

Warning

Error

Information

Auto Close

Manual Close

Queue
```

---

# Empty State Prompt

## Prompt

```text
Design Empty State.

Include

Illustration

Title

Description

Primary Action

Secondary Action
```

---

# Loading State Prompt

## Prompt

```text
Design Loading UI.

Support

Skeleton

Spinner

Progress

Lazy Loading
```

---

# Responsive Layout Prompt

## Prompt

```text
Design responsive layout.

Breakpoints

Mobile

Tablet

Laptop

Desktop

Wide Screen

Explain layout changes.
```

---

# Mobile UI Prompt

## Prompt

```text
Optimize UI for mobile.

Include

Touch Target

Bottom Navigation

Collapsible Sidebar

Responsive Cards

Responsive Tables
```

---

# Dark Mode Prompt

## Prompt

```text
Design Dark Mode.

Requirements

High Contrast

Accessible Colors

Consistent Branding

Readable Typography

Smooth Switching
```

---

# Accessibility Prompt

## Prompt

```text
Review accessibility.

Verify

Keyboard Navigation

ARIA Labels

Focus Order

Contrast Ratio

Screen Reader Support

Responsive Typography
```

---

# Tailwind CSS Prompt

## Prompt

```text
Generate Tailwind CSS utility strategy.

Use

Flex

Grid

Gap

Spacing

Typography

Rounded

Shadow

Transitions

Dark Mode

Reusable Classes
```

---

# Component Library Prompt

## Prompt

```text
Create reusable UI component list.

Include

Buttons

Cards

Forms

Tables

Dialogs

Alerts

Badge

Tabs

Timeline

Accordion

Dropdown

Tooltip

Pagination
```

---

# Search Interface Prompt

## Prompt

```text
Design search interface.

Support

Quick Search

Advanced Filter

Saved Filter

Reset Filter

Search History
```

---

# Dashboard Widget Prompt

## Prompt

```text
Design dashboard widgets.

Include

Statistics

Chart

Calendar

Recent Activities

Tasks

Shortcuts

Weather (Optional)
```

---

# Error Page Prompt

## Prompt

```text
Design error pages.

Include

403

404

500

Offline

Retry Button

Back to Home
```

---

# Settings UI Prompt

## Prompt

```text
Design Settings module.

Sections

General

Theme

Profile

Security

Roles

Permissions

System Configuration
```

---

# Profile Page Prompt

## Prompt

```text
Design User Profile.

Include

Avatar

Information

Password Change

Preferences

Activity Log
```

---

# Enterprise UI Checklist

Before implementation verify

- [ ] Responsive Layout
- [ ] Sidebar Complete
- [ ] Navbar Complete
- [ ] Dashboard Planned
- [ ] Forms Planned
- [ ] Tables Planned
- [ ] Modals Planned
- [ ] Notifications Planned
- [ ] Dark Mode Ready
- [ ] Accessibility Considered

---

# Modern SaaS UI Best Practices

Always

✓ Mobile First

✓ Consistent Spacing

✓ Reusable Components

✓ Responsive Grid

✓ Accessible Colors

✓ Keyboard Navigation

✓ Lazy Loading

✓ Skeleton Loading

✓ Minimal Clicks

✓ Clear Visual Hierarchy

Never

✗ Fixed Width Layout

✗ Inline CSS

✗ Inconsistent Components

✗ Tiny Click Areas

✗ Hidden Navigation

✗ Mixed Design Styles

✗ Hard-coded Colors

✗ Duplicate Components

---

# Recommended Tailwind Utilities

| Category | Utilities |
|----------|-----------|
| Layout | flex grid container |
| Spacing | p-* m-* gap-* |
| Size | w-* h-* max-w-* |
| Typography | text-* font-* leading-* |
| Border | rounded-* border-* |
| Shadow | shadow shadow-md shadow-lg |
| Effects | transition duration-300 |
| Dark Mode | dark:* |
| Responsive | sm: md: lg: xl: 2xl: |

---

# Quick Prompt Index

| Prompt | Purpose |
|---------|---------|
| UI Planning | Overall UI planning |
| Dashboard | SaaS dashboard |
| Sidebar | Navigation |
| Navbar | Top navigation |
| Forms | Data entry |
| Tables | Data presentation |
| Modal | Dialog system |
| Notifications | Toast messages |
| Responsive | Multi-device UI |
| Tailwind CSS | Styling strategy |
| Accessibility | WCAG review |
| Settings | System settings |
| Profile | User profile |

---

# End of Part 1B-2B-2A

Next

**Part 1B-2B-2B**

- Design System Prompts
- Wireframe Prompts
- Information Architecture Prompts
- User Flow Prompts
- UX Review Prompts
- Enterprise Design Checklist
- Modern SaaS Design Best Practices
- UI Review Prompts
- Final Design Approval Prompts

  <!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 1B-2B-2B-1 : Design System Prompts -->
<!-- ====================================================================== -->

# Part 1B-2B-2B-1 — Design System Prompts

Version 2.0

Enterprise Prompt Library

---

# Purpose

This section provides prompt templates for creating a standardized Design System for enterprise web applications.

The Design System ensures:

- Consistent user interface
- Faster development
- Reusable components
- Better user experience
- Maintainable frontend architecture

Supported Technology:

- HTML5
- Tailwind CSS
- JavaScript ES6+
- Google Apps Script HTML Service

---

# Design System Workflow

```text
Brand Identity

↓

Design Principles

↓

Design Tokens

↓

Color System

↓

Typography

↓

Spacing System

↓

Component Rules

↓

UI Implementation

↓

Review
```

---

# Design System Planning Prompt

## Purpose

Create the foundation of the application UI.

## Prompt

```text
Act as a Senior Product Designer.

Create an enterprise Design System.

Technology

Tailwind CSS

HTML5

JavaScript

Requirements

Modern SaaS

Responsive

Accessible

Dark Mode Ready

Return

1. Design Principles
2. Design Tokens
3. Color System
4. Typography
5. Spacing
6. Components
7. Usage Guidelines

Do not generate code.
```

---

# Design Principle Prompt

## Prompt

```text
Define UI design principles.

Include

Visual Style

User Experience

Accessibility

Consistency

Scalability

Brand Personality

Return design rules.
```

---

# SaaS Design Style Prompt

## Prompt

```text
Create a modern SaaS design direction.

Include

Layout Style

Card Style

Navigation Style

Button Style

Form Style

Table Style

Animation Style

Dark Mode Strategy
```

---

# Design Token Prompt

## Prompt

```text
Create Design Tokens.

Include

Colors

Typography

Spacing

Border Radius

Shadow

Animation

Breakpoints

Return as table.
```

---

# Design Token Structure

Recommended:

```text
Design Tokens

├── Colors

├── Typography

├── Spacing

├── Radius

├── Shadow

├── Motion

└── Breakpoints
```

---

# Color System Prompt

## Prompt

```text
Design color system.

Include

Primary

Secondary

Success

Warning

Danger

Info

Background

Surface

Text

Border

Dark Mode Variant
```

---

# Color Token Example

| Token | Purpose |
|---|---|
| primary | Main action |
| secondary | Supporting action |
| success | Positive state |
| warning | Attention |
| danger | Error |
| surface | Card background |

---

# Semantic Color Prompt

## Prompt

```text
Create semantic colors.

Map colors to meaning.

Example

Success

Warning

Error

Information

Disabled

Hover

Active

Focus
```

---

# Dark Mode Color Prompt

## Prompt

```text
Design dark mode colors.

Ensure

High Contrast

Readable Text

Accessible Background

Consistent Components

Smooth Transition
```

---

# Typography System Prompt

## Prompt

```text
Create typography system.

Include

Font Family

Heading Levels

Body Text

Caption

Button Text

Table Text

Responsive Scaling
```

---

# Typography Scale

Example:

| Level | Usage |
|---|---|
| H1 | Page Title |
| H2 | Section Title |
| H3 | Card Title |
| Body | Content |
| Small | Helper Text |

---

# Font Strategy Prompt

## Prompt

```text
Select font strategy.

Requirements

Professional

Readable

SaaS Style

Thai Language Support

English Support

Explain recommendation.
```

---

# Spacing System Prompt

## Prompt

```text
Create spacing system.

Use consistent spacing scale.

Include

Page Padding

Section Gap

Card Padding

Form Gap

Table Spacing
```

---

# Border Radius Prompt

## Prompt

```text
Define border radius system.

Include

Button

Input

Card

Modal

Container

Explain usage.
```

---

# Shadow System Prompt

## Prompt

```text
Define shadow system.

Include

Small

Medium

Large

Modal

Dropdown

Card

Explain when to use.
```

---

# Animation System Prompt

## Prompt

```text
Define animation guidelines.

Include

Hover

Loading

Modal

Page Transition

Toast

Duration

Easing
```

---

# Responsive Design Token Prompt

## Prompt

```text
Define responsive breakpoints.

Include

Mobile

Tablet

Desktop

Large Desktop

Container Width

Grid Rules
```

---

# Component Standard Prompt

## Prompt

```text
Define component standards.

For each component specify

Purpose

Variants

Properties

States

Responsive Behavior

Accessibility
```

---

# Button Component Prompt

## Prompt

```text
Design Button System.

Include

Primary

Secondary

Outline

Danger

Ghost

Loading

Disabled

Icon Button
```

---

# Input Component Prompt

## Prompt

```text
Design Form Input System.

Include

Text

Email

Password

Select

Date

Textarea

Validation State

Error State

Disabled State
```

---

# Card Component Prompt

## Prompt

```text
Design Card System.

Include

Default Card

Statistic Card

Profile Card

Dashboard Card

Interactive Card

Loading Card
```

---

# Table Component Prompt

## Prompt

```text
Design Enterprise Table System.

Include

Header

Body

Sorting

Filtering

Pagination

Empty State

Loading State

Mobile View
```

---

# Modal Component Prompt

## Prompt

```text
Design Modal System.

Include

Confirmation

Form Modal

Information Modal

Large Modal

Responsive Behavior
```

---

# Navigation Component Prompt

## Prompt

```text
Design Navigation System.

Include

Sidebar

Navbar

Breadcrumb

Tabs

Menu

Permission Based Navigation
```

---

# Status Component Prompt

## Prompt

```text
Design status components.

Include

Badge

Chip

Label

Progress

Timeline

Alert
```

---

# Component State Prompt

## Prompt

```text
Define component states.

Include

Default

Hover

Active

Focus

Disabled

Loading

Error

Success
```

---

# Component Documentation Prompt

## Prompt

```text
Generate component documentation.

Include

Purpose

Usage

Props

Variants

Examples

Do and Don't
```

---

# Design System Review Prompt

## Prompt

```text
Review Design System.

Verify

Consistency

Accessibility

Scalability

Component Reusability

Dark Mode

Responsive Design

Suggest improvements.
```

---

# Design System Checklist

Before implementation verify:

- [ ] Design principles defined
- [ ] Color tokens created
- [ ] Typography defined
- [ ] Spacing system defined
- [ ] Component standards defined
- [ ] Responsive rules defined
- [ ] Dark mode planned
- [ ] Accessibility reviewed
- [ ] Documentation prepared

---

# Design System Best Practices

Always

✓ Use design tokens

✓ Create reusable components

✓ Keep visual consistency

✓ Use semantic colors

✓ Support accessibility

✓ Design mobile first

✓ Document components

Never

✗ Hard-code colors everywhere

✗ Create duplicate components

✗ Mix design styles

✗ Ignore accessibility

✗ Create pages without components

---

# Quick Prompt Index

| Prompt | Purpose |
|---|---|
| Design System Planning | Create UI foundation |
| Design Tokens | Define variables |
| Color System | Brand colors |
| Typography | Text hierarchy |
| Spacing | Layout consistency |
| Components | UI standards |
| Buttons | Action controls |
| Forms | Input standards |
| Tables | Data display |
| Navigation | Application structure |
| Review | Quality check |

---

# End of Part 1B-2B-2B-1

Next

**Part 1B-2B-2B-2**

- Wireframe Prompts
- Information Architecture Prompts
- User Flow Prompts
- UX Review Prompts
- Enterprise Design Checklist
- Modern SaaS Best Practices
- Final Design Approval Prompts

  <!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 1B-2B-2B-2 : Wireframe, UX Flow & Design Review Prompts -->
<!-- ====================================================================== -->

# Part 1B-2B-2B-2 — Wireframe, UX Flow & Design Review Prompts

Version 2.0

Enterprise Prompt Library

---

# Purpose

This section provides prompt templates for planning user experience, information architecture, user journeys, wireframes, and final UI review.

The objective is to ensure applications are:

- Easy to understand
- Easy to use
- Consistent
- Efficient
- User-centered
- Enterprise ready

Supported Stack:

- Google Apps Script Web App
- HTML5
- Tailwind CSS
- JavaScript ES6+

---

# UX Design Workflow

```text
Business Goal

↓

User Research

↓

User Persona

↓

Information Architecture

↓

User Flow

↓

Wireframe

↓

UI Design

↓

Usability Review

↓

Implementation

User Persona Prompt
Purpose

Understand users before designing screens.

Prompt
Create user personas.

For each persona include:

- Name
- Role
- Goal
- Problems
- Technical Skill
- Usage Scenario
- Required Features

Focus on enterprise application users.
User Journey Prompt
Prompt
Create user journey map.

Include:

User Goal

Steps

Actions

Screens

Possible Problems

Improvement Opportunities

Return as table.

Example:

Step	Action	Screen
1	Login	Login Page
2	View Data	Dashboard
3	Manage	CRUD Page
Information Architecture Prompt
Purpose

Define application structure.

Prompt
Design Information Architecture.

Include:

- Main Navigation
- Modules
- Sub Modules
- Page Hierarchy
- User Access

Return as tree structure.

Example:

Application

├── Dashboard

├── Users

│   ├── User List

│   └── User Detail

├── Reports

└── Settings
Navigation Structure Prompt
Prompt
Design navigation structure.

Include:

Sidebar

Top Menu

Breadcrumb

Quick Actions

User Menu

Notifications

Permission Based Visibility
Menu Permission Prompt
Prompt
Create menu permission matrix.

Roles:

Admin

Manager

User

Guest

Return table.

Example:

Menu	Admin	User
Settings	✓	✗
Dashboard	✓	✓
User Flow Prompt
Purpose

Define user interaction sequence.

Prompt
Create user flow.

Include:

Start Point

User Action

System Response

Decision Point

Success Path

Error Path

End State

Return using flow diagram.
Authentication Flow Prompt
Prompt
Design authentication flow.

Include:

Login

Validation

Session

Permission Check

Redirect

Logout

Error Handling

Flow:

Login

↓

Validate

↓

Authenticate

↓

Check Role

↓

Dashboard
CRUD User Flow Prompt
Prompt
Design CRUD user flow.

Include:

Create

Read

Update

Delete

Search

Filter

Validation

Confirmation

Error Handling
Dashboard User Flow Prompt
Prompt
Design dashboard user flow.

Include:

Login

Dashboard Loading

View KPI

View Reports

Open Module

Take Action
Wireframe Prompt
Purpose

Create screen structure before UI coding.

Prompt
Create low fidelity wireframes.

For each screen provide:

Layout

Sections

Components

User Actions

Navigation

Responsive Behavior

Do not generate code.
Dashboard Wireframe Prompt
Prompt
Create dashboard wireframe.

Include:

Sidebar

Header

KPI Cards

Charts

Tables

Activity Feed

Quick Actions
Form Wireframe Prompt
Prompt
Create form wireframe.

Include:

Form Sections

Fields

Validation Message

Buttons

Help Text

Responsive Layout
Table Wireframe Prompt
Prompt
Create data table wireframe.

Include:

Search

Filter

Columns

Actions

Pagination

Empty State

Loading State
Mobile Wireframe Prompt
Prompt
Convert desktop layout to mobile.

Consider:

Screen Size

Touch Interaction

Navigation

Cards

Tables

Forms

Performance
UX Improvement Prompt
Prompt
Review this user interface.

Analyze:

User Experience

Navigation

Complexity

Number of Clicks

Confusion Points

Accessibility

Suggest improvements.
Usability Review Prompt
Prompt
Perform usability review.

Check:

Learnability

Efficiency

Error Prevention

Consistency

Feedback

User Satisfaction

Return findings.
Heuristic Evaluation Prompt
Prompt
Evaluate UI using Nielsen Heuristics.

Review:

Visibility

Match Real World

User Control

Consistency

Error Prevention

Recognition

Flexibility

Minimal Design
UX Error Prevention Prompt
Prompt
Analyze possible user errors.

Include:

Cause

Impact

Prevention

UI Improvement

Validation Strategy
Accessibility Review Prompt
Prompt
Perform accessibility review.

Check:

Keyboard Navigation

Screen Reader

Color Contrast

Font Size

Focus State

ARIA

Form Labels
Performance UX Prompt
Prompt
Review UI performance.

Consider:

Loading Time

Lazy Loading

Skeleton Screen

Large Tables

Image Optimization

Network Usage
Enterprise UX Checklist

Before approval verify:

Navigation
 Clear menu structure
 Breadcrumb available
 Search available
 User profile available
Layout
 Responsive
 Consistent spacing
 Clear hierarchy
 Mobile support
Components
 Reusable components
 Consistent states
 Loading states
 Error states
Forms
 Validation messages
 Required indicators
 Clear actions
 Error prevention
Tables
 Search
 Filter
 Pagination
 Export
Accessibility
 Keyboard support
 Color contrast
 Screen reader support
Modern SaaS UI Best Practices

Always:

✓ Show system status

✓ Provide feedback after actions

✓ Reduce unnecessary clicks

✓ Use consistent patterns

✓ Provide helpful empty states

✓ Confirm destructive actions

✓ Optimize common workflows

✓ Design mobile first

Avoid These UX Problems

Never:

✗ Hide important actions

✗ Use unclear icons

✗ Create inconsistent buttons

✗ Use too many colors

✗ Create complicated forms

✗ Remove user feedback

✗ Ignore mobile users

Final UI Approval Prompt
Prompt
Act as a Senior UX Lead.

Review the complete application UI.

Evaluate:

- Design System
- User Flow
- Information Architecture
- Accessibility
- Responsive Design
- SaaS Quality
- Usability

Return:

1. Approval Status

2. Issues Found

3. Recommended Improvements

4. Final Action List
Final Design Checklist

Before production release:

 Design System applied
 User Flow verified
 Wireframes approved
 Responsive tested
 Accessibility checked
 Performance reviewed
 Components reused
 UX reviewed
 Stakeholder approved
Complete UI Planning Workflow
Persona

↓

Information Architecture

↓

User Flow

↓

Wireframe

↓

Design System

↓

Component Design

↓

UI Development

↓

UX Review

↓

Production Release
Quick Prompt Index
Prompt	Purpose
User Persona	Understand users
User Journey	Map experience
Information Architecture	Structure application
User Flow	Define interaction
Wireframe	Screen planning
UX Review	Improve experience
Accessibility Review	Inclusive design
Performance UX	Improve speed
Final Approval	Production readiness
End of Part 1B-2B-2B-2
End of Part 1B-2B

<!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 2A : Google Apps Script Development Prompts -->
<!-- ====================================================================== -->

# Part 2A — Google Apps Script Development Prompts

Version 2.0

Enterprise Prompt Library

---

# Purpose

This section provides prompt templates for developing production-ready Google Apps Script applications.

Supported Architecture:

- MVC
- Clean Architecture
- Repository Pattern
- Service Layer

Technology:

- Google Apps Script
- Google Sheets
- HTML Service
- JavaScript ES6+

---

# Development Workflow

```text
Architecture

↓

Project Setup

↓

Backend Structure

↓

Database Layer

↓

Business Logic

↓

Frontend Communication

↓

Testing

↓

Deployment

GAS Project Setup Prompt
Purpose

Create initial Google Apps Script project structure.

Prompt
Act as a Senior Google Apps Script Developer.

Create a production-ready GAS project.

Requirements:

- MVC Architecture
- Clean Code
- Modular Files
- Separation of Responsibility
- Google Sheets Database

Create:

1. File Structure
2. Core Configuration
3. Entry Points
4. Utility Functions
5. Documentation

Do not write business logic yet.
GAS File Structure Prompt
Prompt
Design Google Apps Script file structure.

Follow:

MVC

Service Layer

Repository Pattern

Return:

File Name

Purpose

Responsibility

Dependency

Example:

Code.gs

├── Controllers

├── Services

├── Repositories

├── Models

├── Utils

├── Config

└── Tests
appsscript.json Configuration Prompt
Prompt
Create appsscript.json configuration.

Include:

Runtime Version

Timezone

OAuth Scopes

Dependencies

Web App Settings

Security Settings

Explain every configuration.
doGet Development Prompt
Purpose

Create Web App entry point.

Prompt
Create doGet() function.

Requirements:

- Load HTML Template
- Pass Configuration
- Handle Errors
- Set Page Title
- Support SPA Application

Follow clean architecture.
doPost API Prompt
Prompt
Create doPost() API endpoint.

Requirements:

- Receive JSON
- Validate Input
- Route Request
- Call Controller
- Return JSON Response
- Handle Errors
Router Pattern Prompt
Prompt
Create API Router.

Support:

GET

POST

PUT

DELETE

Route Parameters

Validation

Error Handling

Example:

/api/users

GET    → listUsers()

POST   → createUser()

PUT    → updateUser()

DELETE → deleteUser()
Controller Development Prompt
Prompt
Create GAS Controller.

Responsibilities:

- Receive Request
- Validate Input
- Call Service
- Return Response

Do not access Spreadsheet directly.
Service Layer Prompt
Prompt
Create Service Layer.

Rules:

- Business Logic Only
- No UI Code
- No Spreadsheet Code
- Reusable Functions

Return:

Class Name

Methods

Parameters

Return Values
Repository Layer Prompt
Prompt
Create Repository Layer.

Responsibilities:

- Google Sheets Access
- CRUD Operations
- Query Data
- Data Mapping

Do not contain business rules.
Model Prompt
Prompt
Create data model.

Include:

Properties

Validation

Default Values

Transformation Methods

JSON Conversion
HTML Service Prompt
Prompt
Design Google Apps Script HTML Service architecture.

Include:

HTML Template

CSS

JavaScript

Server Communication

Loading State

Error Handling
Client Server Communication Prompt
Prompt
Create client-server communication pattern.

Requirements:

Use:

google.script.run

Success Handler

Failure Handler

Loading State

Toast Notification

Promise Pattern
Promise Wrapper Prompt
Prompt
Create Promise wrapper for google.script.run.

Benefits:

- Async/Await Support
- Better Error Handling
- Cleaner Code

Return reusable utility.
Configuration Management Prompt
Prompt
Create application configuration system.

Use:

PropertiesService

Environment Variables

Config File

Support:

Development

Production
PropertiesService Prompt
Prompt
Implement PropertiesService.

Store:

Spreadsheet ID

Configuration

API Keys

System Settings

Never store passwords.
CacheService Prompt
Prompt
Implement CacheService.

Optimize:

Frequently Used Data

Dashboard Statistics

Master Data

API Responses

Explain expiration strategy.
LockService Prompt
Prompt
Implement LockService.

Prevent:

Concurrent Updates

Duplicate Records

Race Conditions

Explain usage.
Trigger Development Prompt
Prompt
Create Apps Script Trigger.

Support:

Time Trigger

On Edit

On Open

Scheduled Tasks

Error Logging

Notification
Batch Processing Prompt
Prompt
Optimize GAS operations.

Replace:

Cell by Cell Operations

with:

Batch Read

Batch Write

Array Processing

Explain performance improvement.
Spreadsheet Service Prompt
Prompt
Create Spreadsheet Service.

Requirements:

- Open Spreadsheet
- Read Data
- Write Data
- Update Data
- Delete Data
- Error Handling
Logging Prompt
Prompt
Create logging system.

Record:

Function Name

User

Timestamp

Input

Output

Error

Execution Time
Error Handling Prompt
Prompt
Create centralized error handling.

Include:

Custom Error Class

Error Code

User Message

Developer Log

Recovery Strategy
Validation Prompt
Prompt
Create validation framework.

Support:

Required

Type Check

Format

Length

Business Rules

Return Validation Result.
Security Prompt
Prompt
Review GAS security.

Check:

Authorization

Authentication

Sensitive Data

PropertiesService

Input Sanitization

Access Control

Logging
Performance Optimization Prompt
Prompt
Optimize Google Apps Script.

Analyze:

Execution Time

Spreadsheet Calls

Memory Usage

Caching

Batch Processing

Triggers

Suggest improvements.
Debugging Prompt
Prompt
Debug this Google Apps Script.

Analyze:

Error Message

Stack Trace

Root Cause

Fix

Prevention

Explain clearly.
Code Review Prompt
Prompt
Review GAS code.

Check:

Architecture

Security

Performance

Maintainability

Naming

Error Handling

Best Practices

Provide recommendations.
GAS Development Checklist

Before completion verify:

 Project structure created
 MVC applied
 Controllers separated
 Services separated
 Repository created
 Config managed safely
 Error handling added
 Logging added
 Batch operations used
 Security reviewed
 Performance optimized
Google Apps Script Best Practices

Always:

✓ Separate business logic

✓ Use Service Layer

✓ Use Repository Pattern

✓ Minimize Spreadsheet calls

✓ Use batch operations

✓ Use PropertiesService

✓ Handle errors centrally

✓ Document functions

✓ Validate input

Never:

✗ Put all code in Code.gs

✗ Access Sheets from HTML

✗ Store secrets in source code

✗ Use excessive API calls

✗ Ignore execution limits

✗ Mix UI and backend logic

Quick Prompt Index
Prompt	Purpose
Project Setup	Create GAS foundation
File Structure	Organize code
doGet	Web App entry
doPost	API entry
Controller	Request handling
Service	Business logic
Repository	Data access
Model	Data structure
HTML Service	Frontend integration
PropertiesService	Configuration
CacheService	Performance
LockService	Concurrency
Trigger	Automation
Debugging	Fix errors
Code Review	Quality control
End of Part 2A

<!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 2B : Google Sheets Development Prompts -->
<!-- ====================================================================== -->

# Part 2B — Google Sheets Development Prompts

Version 2.0

Enterprise Prompt Library

---

# Purpose

This section provides prompt templates for developing Google Sheets as an enterprise data layer.

The objective is to create:

- Structured data storage
- Reliable CRUD operations
- Maintainable repositories
- High performance access
- Data validation
- Audit capability

Supported Architecture:

- MVC
- Clean Architecture
- Repository Pattern
- Service Layer

Technology:

- Google Sheets
- Google Apps Script

---

# Google Sheets Development Workflow

```text
Business Entity

↓

Sheet Design

↓

Column Mapping

↓

Repository

↓

Service

↓

Controller

↓

UI

↓

Testing

Google Sheets Database Design Prompt
Purpose

Create spreadsheet database structure.

Prompt
Act as a Database Architect.

Design Google Sheets database.

Requirements:

- One Entity per Sheet
- Primary Key
- Audit Fields
- Validation Rules
- Relationship Mapping

Return:

1. Sheet List
2. Column Definition
3. Data Dictionary
4. Sample Data

Do not generate code.
Spreadsheet Repository Prompt
Purpose

Create data access layer.

Prompt
Create Repository Layer for Google Sheets.

Rules:

Repository only handles data access.

Include:

- Find All
- Find By ID
- Create
- Update
- Delete
- Search

Do not include business logic.
Repository Naming Prompt
Prompt
Define repository naming convention.

Example:

UserRepository

PatientRepository

AppointmentRepository

ReportRepository

Explain standard methods.
CRUD Development Prompt
Prompt
Create CRUD operations.

Entity:

[ENTITY_NAME]

Include:

Create

Read

Update

Delete

Validation

Error Handling

Logging

Return production-ready code.
Create Record Prompt
Prompt
Create function to insert data.

Requirements:

- Validate Input
- Generate ID
- Add Created Date
- Add Created User
- Return Created Object

Use batch operation.
Read Data Prompt
Prompt
Create read function.

Requirements:

- Read all records
- Convert rows to objects
- Handle empty data
- Optimize performance

Avoid cell-by-cell access.
Find By ID Prompt
Prompt
Create FindById method.

Requirements:

Input:

ID

Output:

Object

Handle:

Not Found

Invalid ID

Duplicate ID
Update Record Prompt
Prompt
Create update function.

Requirements:

- Validate ID
- Update only changed fields
- Maintain audit information
- Return updated record
Delete Record Prompt
Prompt
Implement delete strategy.

Preferred:

Soft Delete

Fields:

deletedAt

deletedBy

status

Explain reason.
Data Mapping Prompt
Purpose

Convert spreadsheet rows into objects.

Prompt
Create data mapper.

Convert:

Row Array

↓

Object

Include:

- Column Mapping
- Type Conversion
- Default Values
- Validation

Example:

{
 id:"",
 name:"",
 status:""
}
Column Configuration Prompt
Prompt
Create dynamic column configuration.

Include:

Column Name

Index

Type

Required

Validation

Default Value


Example:

Column	Index	Type
id	0	String
name	1	Text
Dynamic Sheet Configuration Prompt
Prompt
Create dynamic sheet manager.

Support:

- Spreadsheet ID
- Sheet Name
- Column Mapping
- CRUD Configuration

Allow changing database without modifying code.
Batch Read Prompt
Prompt
Optimize Google Sheets reading.

Replace:

getRange()

multiple calls

with:

Single Batch Read

Array Processing

Return optimized code.
Batch Write Prompt
Prompt
Optimize Google Sheets writing.

Requirements:

- Prepare data array
- Single write operation
- Error handling
- Performance measurement
Search Prompt
Prompt
Create search functionality.

Support:

- Keyword
- Multiple Columns
- Partial Match
- Case Insensitive

Return:

Filtered Records
Filter Prompt
Prompt
Create advanced filter.

Support:

- Status
- Date Range
- Category
- Owner
- Multiple Conditions
Sorting Prompt
Prompt
Create sorting system.

Support:

Ascending

Descending

Multiple Columns

Custom Priority
Pagination Prompt
Prompt
Create pagination for Google Sheets.

Input:

Page

Limit

Sort

Filter

Return:

Data

Total

Current Page

Total Pages

Example:

{
"data":[],
"page":1,
"total":100
}
Data Validation Prompt
Prompt
Create Google Sheets validation rules.

Include:

Required Fields

Data Type

Format

Dropdown

Reference Data

Error Message
Duplicate Detection Prompt
Prompt
Create duplicate detection.

Check:

Email

Phone

National ID

Code

Return:

Duplicate Records

Warning Message
Import CSV Prompt
Prompt
Create CSV import process.

Include:

Upload

Read File

Validate Data

Detect Duplicate

Import

Error Report
Export Report Prompt
Prompt
Create export system.

Support:

CSV

Excel

PDF

Summary Report

Filtered Export
Backup Prompt
Prompt
Create Google Sheets backup system.

Include:

Automatic Backup

Timestamp

Version

Restore

Backup Log
Version Control Prompt
Prompt
Design spreadsheet versioning.

Track:

Data Changes

User

Time

Old Value

New Value

Reason
Audit Data Prompt
Prompt
Create audit trail.

Capture:

Create

Update

Delete

Login

Permission Change

Export

Data Quality Prompt
Prompt
Analyze data quality.

Check:

Missing Data

Duplicate

Invalid Format

Inconsistent Values

Recommend improvements.
Large Dataset Prompt
Prompt
Optimize Google Sheets for large data.

Consider:

10000+

50000+

100000+

records

Use:

Pagination

Cache

Batch Processing

Archive Strategy
Performance Optimization Prompt
Prompt
Review Google Sheets performance.

Analyze:

Spreadsheet Calls

Execution Time

Memory

Cache Usage

Batch Operations

Provide optimization plan.
Security Prompt
Prompt
Review Google Sheets security.

Check:

Access Permission

Sensitive Data

Sharing

Audit

Backup

Data Exposure
Repository Review Prompt
Prompt
Review Repository implementation.

Verify:

Single Responsibility

Performance

Error Handling

Data Mapping

Maintainability

Security
Google Sheets Development Checklist

Before release:

 Sheet structure documented
 Column mapping completed
 Primary keys defined
 Repository created
 CRUD tested
 Validation implemented
 Audit fields added
 Backup strategy completed
 Performance reviewed
 Security reviewed
Google Sheets Best Practices

Always:

✓ One entity per sheet

✓ Use UUID

✓ Use header row

✓ Use batch operations

✓ Use repository layer

✓ Validate before save

✓ Add audit fields

✓ Backup regularly

✓ Use configuration-driven design

Never:

✗ Hard-code column index

✗ Access sheet directly everywhere

✗ Store secrets

✗ Use getRange repeatedly

✗ Mix UI logic with data logic

✗ Delete important data permanently

Recommended Google Sheets Structure
Spreadsheet

├── Users

├── Roles

├── Permissions

├── Settings

├── Master_Data

├── Transactions

├── Audit_Log

├── Error_Log

└── Backup_Log
Quick Prompt Index
Prompt	Purpose
Database Design	Plan Sheets
Repository	Data Layer
CRUD	Data Operations
Mapping	Object Conversion
Batch Read	Performance
Batch Write	Optimization
Search	Query
Filter	Data Filtering
Pagination	Large Data
Validation	Data Quality
Backup	Recovery
Audit	Tracking
Security	Protection
Review	Quality Check
End of Part 2B

<!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 2C : Backend Architecture Prompts -->
<!-- ====================================================================== -->

# Part 2C — Backend Architecture Prompts

Version 2.0

Enterprise Prompt Library

---

# Purpose

This section provides prompt templates for designing and implementing the backend architecture of Google Apps Script applications.

The objective is to create:

- Clean backend structure
- Separation of responsibilities
- Maintainable business logic
- Secure API processing
- Reusable services
- Enterprise-level code quality

Supported Architecture:

- MVC
- Clean Architecture
- Repository Pattern
- Service Layer

Technology:

- Google Apps Script
- JavaScript ES6+
- Google Sheets Database

---

# Backend Architecture Workflow

```text
Request

↓

Controller

↓

Validation

↓

Service

↓

Repository

↓

Google Sheets

↓

Response

↓

Logging

Backend Architecture Design Prompt
Purpose

Design backend architecture before coding.

Prompt
Act as a Senior Backend Architect.

Design backend architecture.

Technology:

Google Apps Script

Google Sheets

JavaScript ES6+

Architecture:

MVC

Clean Architecture

Repository Pattern

Service Layer

Return:

1. Backend Layers
2. Responsibilities
3. Data Flow
4. Dependencies
5. Error Handling Strategy
6. Security Strategy

Do not generate code.
Layer Responsibility Prompt
Prompt
Define backend layer responsibilities.

Layers:

Controller

Service

Repository

Model

Utility

Configuration

Explain:

Purpose

Input

Output

Dependencies

Rules
Controller Development Prompt
Purpose

Create request handling layer.

Prompt
Create Controller.

Responsibilities:

- Receive Request
- Validate Input
- Call Service
- Format Response
- Handle Errors

Rules:

Controller must not access Spreadsheet directly.
Controller Naming Prompt
Prompt
Create controller naming standard.

Example:

UserController

PatientController

ReportController

Include:

Methods

Responsibilities

Routes
Request Processing Prompt
Prompt
Design request processing flow.

Include:

Receive Request

Parse Data

Validate

Authorize

Execute Service

Return Response

Log Result
Response Formatting Prompt
Prompt
Create standard backend response.

Support:

Success

Validation Error

Authentication Error

Permission Error

Not Found

Server Error

Return JSON format.
Service Layer Development Prompt
Purpose

Implement business logic.

Prompt
Create Service Layer.

Rules:

- Business Logic Only
- No UI Logic
- No Spreadsheet Code
- Reusable Functions

Return:

Service Name

Methods

Parameters

Business Rules

Return Values
Business Logic Prompt
Prompt
Analyze business process.

Convert into Service methods.

For each method provide:

Purpose

Input

Process

Validation

Output

Error Cases
Transaction Flow Prompt
Prompt
Design transaction flow.

Example:

Create User

↓

Validate

↓

Check Duplicate

↓

Save

↓

Create Audit

↓

Return Result
Service Dependency Prompt
Prompt
Analyze service dependencies.

Identify:

Independent Services

Shared Services

External Services

Circular Dependencies

Suggest improvements.
Repository Integration Prompt
Prompt
Design Controller-Service-Repository flow.

Example:

Controller

↓

UserService

↓

UserRepository

↓

Users Sheet

Explain responsibilities.
Repository Error Handling Prompt
Prompt
Design repository error handling.

Include:

Database Error

Connection Error

Missing Data

Invalid Query

Logging Strategy
Model Design Prompt
Purpose

Create data structure layer.

Prompt
Create Model Class.

Include:

Properties

Constructor

Validation

Default Values

toJSON()

fromJSON()

Data Transformation
Entity Model Prompt
Prompt
Create entity model.

Entity:

[ENTITY_NAME]

Include:

ID

Attributes

Relationships

Validation Rules

Audit Fields
DTO Prompt
Prompt
Create Data Transfer Object.

Purpose:

Separate Database Model

from

API Response

Include:

Input DTO

Output DTO

Mapping Rules
Validation Framework Prompt
Prompt
Create backend validation framework.

Support:

Required

Type

Format

Range

Business Rules

Custom Validation

Return validation result.
Utility Framework Prompt
Purpose

Create reusable helper functions.

Date Utility Prompt
Create Date Utility.

Functions:

Format Date

Compare Date

Calculate Difference

Timezone Handling
String Utility Prompt
Create String Utility.

Functions:

Trim

Normalize

Generate Code

Mask Data

Validation
Response Utility Prompt
Create Response Utility.

Functions:

success()

error()

validationError()

notFound()

unauthorized()

Security Utility Prompt
Create Security Utility.

Support:

Hash

Token

Permission Check

Sensitive Data Masking

Audit
Middleware Architecture Prompt
Prompt
Design middleware system.

Include:

Authentication

Authorization

Validation

Logging

Error Handler

Explain execution order.
Authentication Middleware Prompt
Create authentication middleware.

Verify:

User Identity

Session

Token

Expiration

Return authenticated user.
Authorization Middleware Prompt
Create authorization middleware.

Support:

Role

Permission

Resource Access

Action Permission

Return access decision.
Logging Middleware Prompt
Create request logging middleware.

Capture:

User

Function

Request

Response

Duration

Error

Timestamp
Authentication Architecture Prompt
Prompt
Design authentication system.

Support:

Google Account

Session

User Table

Role Mapping

Logout

Session Expiration
Session Management Prompt
Design session management.

Include:

Create Session

Validate Session

Expire Session

Logout

Security Rules
RBAC Architecture Prompt
Prompt
Design RBAC system.

Entities:

Users

Roles

Permissions

Modules

Actions

Create:

Database Design

Permission Flow

Access Checking Logic
Permission Matrix Prompt
Prompt
Generate permission matrix.

Roles:

Admin

Manager

Staff

User

Guest

Actions:

View

Create

Update

Delete

Export

Approve

Example:

Role	View	Create	Delete
Admin	✓	✓	✓
User	✓	✗	✗
Error Handling Architecture Prompt
Prompt
Design centralized error handling.

Include:

Error Class

Error Code

User Message

Developer Message

Logging

Recovery
Error Code Standard

Example:

Code	Meaning
AUTH001	Login Failed
PERM001	Permission Denied
DATA001	Invalid Data
SYS001	System Error
Backend Testing Prompt
Prompt
Create backend testing strategy.

Test:

Controller

Service

Repository

Validation

Authentication

Error Handling

Return test cases.
Backend Code Review Prompt
Prompt
Review backend implementation.

Check:

Architecture

Code Quality

Security

Performance

Maintainability

Error Handling

Suggest improvements.
Backend Development Checklist

Before release:

 MVC implemented
 Controller separated
 Service layer created
 Repository isolated
 Models documented
 Validation completed
 Authentication implemented
 RBAC completed
 Error handling centralized
 Logging enabled
 Code reviewed
Backend Best Practices

Always:

✓ Separate layers

✓ Keep controllers thin

✓ Put business logic in services

✓ Use repository pattern

✓ Validate all inputs

✓ Centralize errors

✓ Log important actions

✓ Protect sensitive data

✓ Write reusable utilities

Never:

✗ Put business logic in Controller

✗ Access Sheets directly from UI

✗ Duplicate validation

✗ Hard-code permissions

✗ Ignore errors

✗ Store secrets in code

Quick Prompt Index
Prompt	Purpose
Architecture Design	Backend planning
Controller	Request handling
Service	Business logic
Repository Integration	Data flow
Model	Data structure
DTO	Data transfer
Validation	Input control
Utility	Reusable functions
Middleware	Request pipeline
Authentication	Identity
RBAC	Permission
Error Handling	Reliability
Testing	Quality
Review	Improvement
End of Part 2C

<!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 2D : Frontend Development Prompts -->
<!-- ====================================================================== -->

# Part 2D — Frontend Development Prompts

Version 2.0

Enterprise Prompt Library

---

# Purpose

This section provides prompt templates for developing modern frontend applications using Google Apps Script HTML Service and Tailwind CSS.

The objective is to create:

- Modern SaaS interface
- Reusable components
- Responsive design
- Clean frontend architecture
- Better user experience
- Maintainable JavaScript

Supported Technology:

- HTML5
- Tailwind CSS
- JavaScript ES6+
- Google Apps Script HTML Service

---

# Frontend Development Workflow

```text
UI Design

↓

HTML Structure

↓

Component Development

↓

JavaScript Logic

↓

GAS Communication

↓

Validation

↓

Testing

↓

Optimization

Frontend Architecture Prompt
Purpose

Design frontend architecture before coding.

Prompt
Act as a Senior Frontend Architect.

Design frontend architecture.

Technology:

HTML5

Tailwind CSS

JavaScript ES6+

Google Apps Script HTML Service

Architecture:

Component Based

Modular JavaScript

Reusable UI

Return:

1. Folder Structure
2. Component Strategy
3. State Management
4. Communication Pattern
5. Coding Rules

Do not generate code.
Frontend Folder Structure Prompt
Prompt
Design frontend folder structure.

Include:

HTML Pages

Components

Layouts

JavaScript Modules

CSS

Assets

Utilities

Return complete tree.

Example:

frontend/

├── pages/

├── components/

├── layouts/

├── js/

├── css/

└── assets/
HTML Template Development Prompt
Prompt
Create HTML template.

Requirements:

- Semantic HTML
- Responsive
- Tailwind CSS
- Accessibility
- Component Ready

Include:

Header

Sidebar

Main Content

Footer
SPA Architecture Prompt
Prompt
Design Single Page Application structure.

Include:

Routing

Page Switching

State Management

Loading

Error Handling

Browser History
Layout Component Prompt
Prompt
Create application layout.

Include:

Sidebar

Navbar

Content Area

Breadcrumb

Notification Area

Responsive Behavior
Tailwind CSS Strategy Prompt
Prompt
Create Tailwind CSS strategy.

Include:

Utility Usage

Component Classes

Responsive Rules

Dark Mode

Theme Variables

Avoid duplicated styles.
Responsive Layout Prompt
Prompt
Create responsive layout.

Support:

Mobile

Tablet

Desktop

Large Screen

Explain:

Grid

Flex

Spacing

Navigation Changes
Dark Mode Prompt
Prompt
Implement dark mode strategy.

Include:

Theme Toggle

Color Tokens

Component Support

Persistence

Accessibility
Component Development Prompt
Purpose

Create reusable frontend components.

Prompt
Create reusable UI component.

Component:

[COMPONENT_NAME]

Include:

Purpose

HTML Structure

Tailwind Classes

JavaScript Behavior

Props

Events

States

Accessibility
Button Component Prompt
Create button component.

Variants:

Primary

Secondary

Outline

Danger

Ghost

Loading

Disabled

Icon Button
Card Component Prompt
Create card component.

Support:

Dashboard Card

Information Card

Profile Card

Statistic Card

Loading Card

Interactive Card
Form Component Prompt
Create form component.

Include:

Input

Label

Validation

Error Message

Help Text

Loading State

Disabled State
Modal Component Prompt
Create modal component.

Include:

Open

Close

Confirm

Cancel

Loading

Validation

Keyboard Support
Dropdown Component Prompt
Create dropdown component.

Support:

Menu Items

Search

Keyboard Navigation

Permission Control

Mobile Support
Tabs Component Prompt
Create tab component.

Include:

Active State

Disabled State

Lazy Loading

Responsive Behavior
Toast Notification Prompt
Create toast system.

Support:

Success

Error

Warning

Information

Auto Close

Queue Management
Loading Component Prompt
Create loading components.

Include:

Spinner

Skeleton

Progress Bar

Page Loading

Button Loading
Empty State Prompt
Create empty state component.

Include:

Icon

Title

Description

Action Button

Custom Message
Dashboard Development Prompt
Prompt
Create SaaS Dashboard.

Include:

KPI Cards

Charts

Tables

Recent Activity

Quick Actions

Notifications

Responsive Layout
KPI Card Prompt
Create KPI card.

Include:

Title

Value

Trend

Percentage Change

Icon

Action

Loading State
Chart Component Prompt
Create chart component.

Support:

Line Chart

Bar Chart

Pie Chart

Area Chart

Responsive

Loading

Empty State
Activity Feed Prompt
Create activity feed.

Include:

User

Action

Time

Status

Icon

Pagination
Form Development Prompt
Prompt
Create enterprise form.

Requirements:

Validation

Required Fields

Error Handling

Submit State

Reset

Loading

Responsive
Dynamic Form Prompt
Create dynamic form generator.

Input:

Configuration Object

Output:

Form UI

Support:

Text

Select

Date

Checkbox

Radio

File Upload
File Upload Prompt
Create file upload component.

Include:

Drag Drop

File Validation

Preview

Progress

Error Handling
Table Development Prompt
Prompt
Create enterprise data table.

Support:

Search

Filter

Sorting

Pagination

Selection

Export

Responsive Mobile View
Advanced Table Prompt
Improve table performance.

Include:

Virtual Rendering

Lazy Loading

Server Pagination

Column Configuration

Caching
Search Component Prompt
Create search component.

Include:

Keyword Search

Advanced Filter

Clear Button

Search History

Loading State
Client-Side JavaScript Prompt
Prompt
Design frontend JavaScript architecture.

Include:

Modules

Events

State

API Calls

Error Handling

Utilities
State Management Prompt
Create simple state management.

Support:

Global State

Component State

Update

Subscribe

Persist
GAS Communication Prompt
Create communication layer.

Use:

google.script.run

Promise Wrapper

Success Handler

Error Handler

Loading Control
Event Handling Prompt
Create event handling strategy.

Include:

Click

Submit

Change

Keyboard

Dynamic Elements
Frontend Error Handling Prompt
Create frontend error handling.

Include:

API Error

Validation Error

Network Error

User Message

Logging
Animation Prompt
Create UI animation guidelines.

Include:

Hover

Transition

Modal

Toast

Loading

Page Change
Performance Optimization Prompt
Optimize frontend performance.

Analyze:

DOM

JavaScript

Network

Rendering

Images

Caching

Suggest improvements.
Frontend Testing Prompt
Create frontend testing strategy.

Test:

Components

Forms

Navigation

Validation

Responsive

Error Handling
Frontend Code Review Prompt
Review frontend code.

Check:

HTML Quality

CSS Structure

JavaScript

Accessibility

Performance

Security

Maintainability
Frontend Development Checklist

Before release:

 Responsive design completed
 Components reusable
 Tailwind structure clean
 Dark mode supported
 Forms validated
 Tables optimized
 Loading states added
 Error handling completed
 Accessibility reviewed
 Performance optimized
Frontend Best Practices

Always:

✓ Component-based design

✓ Mobile first

✓ Semantic HTML

✓ Reusable components

✓ Consistent Tailwind usage

✓ Clear state management

✓ Validate user input

✓ Provide feedback

✓ Optimize rendering

Never:

✗ Write duplicated HTML

✗ Mix business logic in UI

✗ Use inline styles everywhere

✗ Ignore accessibility

✗ Create inconsistent components

✗ Hard-code configuration

Quick Prompt Index
Prompt	Purpose
Frontend Architecture	UI structure
HTML Template	Page structure
Tailwind Strategy	Styling
Components	Reusable UI
Dashboard	SaaS dashboard
Forms	Data entry
Tables	Data display
JavaScript Module	Client logic
GAS Communication	Backend connection
Testing	Quality
Review	Improvement
End of Part 2D

<!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 2E : Feature Development Prompts -->
<!-- ====================================================================== -->

# Part 2E — Feature Development Prompts

Version 2.0

Enterprise Prompt Library

---

# Purpose

This section provides prompt templates for developing complete application features using GitHub Copilot Agent.

The objective is to enable AI agents to build features consistently using:

- Requirement Analysis
- Database Design
- Backend Development
- Frontend Development
- Testing
- Documentation

Supported Architecture:

- MVC
- Clean Architecture
- Repository Pattern
- Service Layer

Technology:

- Google Apps Script
- Google Sheets
- Tailwind CSS
- JavaScript ES6+

---

# Feature Development Workflow

```text
Requirement

↓

Business Analysis

↓

Database Design

↓

Backend Design

↓

Frontend Design

↓

Implementation

↓

Testing

↓

Review

↓

Release

Master Feature Development Prompt
Purpose

Generate complete feature implementation.

Prompt
Act as a Senior Full Stack Developer.

Develop the following feature:

Feature Name:

[FEATURE_NAME]

Technology:

Google Apps Script

Google Sheets

Tailwind CSS

JavaScript ES6+

Architecture:

MVC

Clean Architecture

Repository Pattern

Generate:

1. Requirement Analysis
2. Database Schema
3. Repository
4. Service Layer
5. Controller
6. API Specification
7. UI Components
8. Validation Rules
9. Error Handling
10. Testing Plan

Follow enterprise coding standards.
Feature Analysis Prompt
Prompt
Analyze this feature requirement.

Return:

1. Business Objective
2. User Roles
3. User Actions
4. Business Rules
5. Data Requirements
6. Possible Risks
7. Acceptance Criteria

Do not generate code.
CRUD Module Development Prompt
Purpose

Create standard CRUD modules.

Examples:

Users
Patients
Products
Inventory
Projects
Prompt
Create CRUD module.

Entity:

[ENTITY_NAME]

Generate:

Database

Model

Repository

Service

Controller

API

UI

Validation

Testing

Follow MVC architecture.
CRUD Architecture
Frontend

↓

Controller

↓

Service

↓

Repository

↓

Google Sheet

Entity Design Prompt
Design entity model.

Entity:

[ENTITY_NAME]

Include:

ID

Fields

Data Type

Required

Validation

Relationships

Audit Fields
CRUD Database Prompt
Create Google Sheets database.

Include:

Sheet Name

Columns

Data Types

Primary Key

Indexes

Validation Rules

Sample Data
CRUD UI Prompt
Create CRUD user interface.

Include:

List Page

Create Form

Edit Form

Detail View

Delete Confirmation

Search

Filter

Pagination

Responsive Design
User Management Feature
Purpose

Standard enterprise user system.

User Management Prompt
Create User Management Module.

Features:

Create User

Update Profile

Deactivate User

Assign Role

Reset Password

View Activity

Include:

Database

Backend

Frontend

Security
User Database Structure
Field	Description
userId	Primary Key
email	Account
name	Full Name
roleId	Permission
status	Active/Inactive
createdAt	Created Date
createdBy	Creator
Role Assignment Prompt
Create role assignment system.

Support:

Multiple Roles

Permission Mapping

Role History

Access Checking
Dashboard Feature
Prompt
Create enterprise dashboard.

Include:

KPI Cards

Charts

Summary

Recent Activity

Quick Actions

Notifications

Responsive Layout
KPI Prompt
Create KPI component.

Include:

Title

Value

Trend

Comparison

Icon

Color Status

Loading State
Dashboard Data Flow
Google Sheet

↓

Repository

↓

Dashboard Service

↓

API

↓

Chart Component
Report Feature
Prompt
Create reporting module.

Support:

Report Builder

Filter

Date Range

Summary

Export

Print

Permission Control
Report Filter Prompt
Create advanced report filtering.

Support:

Date

Category

Status

User

Multiple Conditions

Save Filter
Export Prompt
Create export functionality.

Support:

CSV

Excel

PDF

Print

Filtered Data

Audit Log
Settings Module
Prompt
Create system settings module.

Include:

Application Config

Theme

Data Source

Notification Settings

User Preferences

Security Settings
Data Source Configuration Prompt
Create dynamic data source settings.

Support:

Spreadsheet ID

Sheet Name

Column Mapping

API Configuration

Environment
Approval Workflow Feature
Prompt
Create approval workflow.

Include:

Request Creation

Approval Steps

Approver

Status

Comments

History

Notification
Approval Status Model
Status	Meaning
Draft	Initial
Pending	Waiting Approval
Approved	Completed
Rejected	Declined
Cancelled	Cancelled
Workflow Engine Prompt
Design workflow engine.

Support:

Multiple Steps

Different Approvers

Conditional Approval

History Tracking

Notification
Notification System
Prompt
Create notification system.

Support:

In-App

Email

LINE Messaging API

Reminder

Notification History
Notification Rule Prompt
Create notification rules.

Include:

Event

Condition

Recipient

Message Template

Channel

Schedule
Reminder System Prompt
Create reminder automation.

Include:

Schedule

Trigger Condition

Message

Recipient

Log
Search Feature
Prompt
Create global search system.

Support:

Multiple Modules

Keyword

Filter

Permission

Result Ranking
Advanced Search Prompt
Create advanced search.

Include:

Search Fields

Filters

Sorting

Saved Search

Export
File Management Feature
Prompt
Create file management module.

Support:

Upload

Download

Delete

Preview

Permission

Audit Log
File Security Prompt
Review file security.

Check:

Access Permission

File Type

File Size

Sensitive Data

Download Log
Complete Feature Generation Prompt
Prompt
You are a Senior Enterprise Software Architect.

Generate a complete feature.

Follow:

Requirement First

Database Second

Backend Third

Frontend Fourth

Testing Last

Rules:

Do not skip architecture.

Do not create duplicated logic.

Use reusable components.

Document every important decision.
Feature Code Review Prompt
Review this feature implementation.

Evaluate:

Architecture

Code Quality

Security

Performance

User Experience

Maintainability

Return:

Issues

Severity

Recommendation

Fix Plan
Feature Testing Prompt
Create feature testing plan.

Include:

Unit Test

Integration Test

UI Test

Security Test

User Acceptance Test

Expected Result
Feature Security Review Prompt
Perform security review.

Check:

Authentication

Authorization

Input Validation

Data Exposure

Audit

Permission

Sensitive Data
Feature Development Checklist

Before release:

Analysis
 Requirement documented
 Business rules defined
 User roles identified
 Acceptance criteria created
Database
 Schema designed
 Validation defined
 Audit fields added
Backend
 Controller created
 Service created
 Repository created
 Error handling added
Frontend
 Components reusable
 Responsive
 Loading state
 Error state
Quality
 Testing completed
 Security reviewed
 Documentation updated
Feature Development Best Practices

Always:

✓ Analyze before coding

✓ Design database first

✓ Separate layers

✓ Reuse components

✓ Document business rules

✓ Test before release

✓ Review security

Never:

✗ Start coding without requirements

✗ Put all logic in one file

✗ Duplicate components

✗ Skip validation

✗ Ignore permissions

Quick Prompt Index
Prompt	Purpose
Master Feature	Complete development
CRUD	Standard module
User Management	Account system
Dashboard	Analytics
Report	Data reporting
Settings	Configuration
Workflow	Approval
Notification	Communication
Search	Discovery
File Management	Document handling
Review	Quality
Testing	Verification
End of Part 2E

<!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 3A : Testing & Quality Assurance Prompts -->
<!-- ====================================================================== -->

# Part 3A — Testing & Quality Assurance Prompts

Version 2.0

Enterprise Prompt Library

---

# Purpose

This section provides prompt templates for quality assurance and testing activities.

The objective is to ensure the application is:

- Reliable
- Maintainable
- Secure
- Production-ready
- Easy to improve

Testing covers:

- Unit Testing
- Integration Testing
- User Acceptance Testing
- Regression Testing
- Code Review
- Bug Analysis
- Performance Testing

---

# Quality Assurance Workflow

```text
Requirement

↓

Test Planning

↓

Test Case Design

↓

Development

↓

Testing

↓

Bug Analysis

↓

Fix

↓

Regression Test

↓

Release

Testing Strategy Prompt
Purpose

Create overall testing approach.

Prompt
Act as a Senior QA Engineer.

Create testing strategy.

Application:

[APPLICATION_NAME]

Technology:

Google Apps Script

Google Sheets

HTML

Tailwind CSS

JavaScript

Include:

1. Testing Scope
2. Testing Types
3. Test Environment
4. Test Data Strategy
5. Test Schedule
6. Quality Criteria

Return professional QA document.
Test Planning Prompt
Prompt
Create test plan.

Include:

Feature

Objective

Test Scenario

Test Case

Expected Result

Priority

Tester

Status
Test Case Generation Prompt
Prompt
Generate test cases.

Feature:

[FEATURE_NAME]

Include:

Test ID

Scenario

Steps

Input

Expected Output

Actual Result

Status

Priority

Example:

ID	Scenario	Result
TC001	Login Success	Pass
Unit Testing Prompt
Purpose

Test individual functions.

Prompt
Create unit test cases.

Target:

[FUNCTION_NAME]

Check:

Input

Output

Validation

Error Case

Boundary Case

Expected Result
Controller Testing Prompt
Create controller tests.

Verify:

Request Handling

Input Validation

Service Calling

Response Format

Error Handling
Service Testing Prompt
Create service layer tests.

Verify:

Business Rules

Calculation

Workflow

Validation

Exception Handling
Repository Testing Prompt
Create repository tests.

Verify:

Create

Read

Update

Delete

Search

Data Mapping

Error Handling
Utility Testing Prompt
Create utility tests.

Test:

Date Functions

String Functions

Validation

Formatting

Security Functions
Integration Testing Prompt
Purpose

Verify system communication.

Prompt
Create integration testing plan.

Test:

Frontend

↓

Backend

↓

Repository

↓

Google Sheets

Include:

Scenario

Steps

Expected Result
API Testing Prompt
Create API test cases.

Endpoint:

[API_ENDPOINT]

Test:

Success

Invalid Input

Unauthorized

Permission Denied

Server Error

Response Format
Database Testing Prompt
Test database layer.

Verify:

Data Creation

Data Update

Data Deletion

Data Integrity

Duplicate Handling

Audit Log
User Acceptance Testing (UAT)
Purpose

Validate system from user perspective.

UAT Scenario Prompt
Create UAT scenarios.

User Role:

[ROLE]

Feature:

[FEATURE]

Include:

Business Goal

User Steps

Expected Outcome

Acceptance Criteria
Acceptance Criteria Prompt
Create acceptance criteria.

Feature:

[FEATURE_NAME]

Use format:

Given

When

Then

Example:

Given user is logged in

When user creates record

Then record appears in list
Regression Testing Prompt
Create regression test plan.

After change:

Analyze:

Affected Modules

Existing Features

Risk Areas

Required Tests
Bug Analysis Prompt
Purpose

Analyze problems systematically.

Prompt
Analyze this bug.

Information:

Error:

[ERROR]

System:

[MODULE]

Return:

1. Root Cause
2. Impact
3. Fix Recommendation
4. Prevention Strategy
Root Cause Analysis Prompt
Perform root cause analysis.

Use:

5 Why Analysis

Problem

Cause

Solution

Prevention
Debugging Prompt
Debug this code.

Analyze:

Error Message

Stack Trace

Execution Flow

Root Cause

Solution

Improvement
Code Quality Review Prompt
Review code quality.

Check:

Architecture

Naming

Complexity

Duplication

Maintainability

Security

Performance

Return score and recommendations.
Code Refactoring Prompt
Refactor this code.

Goals:

Improve readability

Reduce duplication

Improve performance

Maintain behavior

Explain changes.
Technical Debt Analysis Prompt
Analyze technical debt.

Identify:

Problem

Risk

Impact

Priority

Recommendation

Estimated Effort
Performance Testing Prompt
Create performance test plan.

Measure:

Execution Time

Response Time

Memory Usage

Spreadsheet Calls

Concurrent Users

Optimization
Load Testing Prompt
Analyze system under load.

Scenario:

Multiple Users

Large Dataset

Frequent Requests

Return:

Bottleneck

Risk

Solution
Security Quality Testing Prompt
Perform security testing.

Check:

Authentication

Authorization

Input Validation

Data Exposure

Permission

Audit
Accessibility Testing Prompt
Perform accessibility testing.

Check:

Keyboard Navigation

Color Contrast

Screen Reader

Form Labels

Focus State
QA Review Prompt
Act as QA Lead.

Review application readiness.

Evaluate:

Functionality

Performance

Security

Usability

Maintainability

Return:

Pass/Fail

Issues

Recommendation
Quality Checklist

Before Production:

Testing
 Test plan created
 Test cases completed
 Unit tests passed
 Integration tested
 UAT approved
Quality
 Code reviewed
 Refactoring completed
 Technical debt identified
 Documentation updated
Security
 Authentication tested
 Permission tested
 Data protection reviewed
Performance
 Loading tested
 Large data tested
 Optimization completed
QA Best Practices

Always:

✓ Test before release

✓ Automate repeat tests

✓ Document bugs

✓ Analyze root causes

✓ Review code regularly

✓ Test user scenarios

✓ Measure performance

Never:

✗ Test only happy paths

✗ Ignore errors

✗ Skip regression testing

✗ Deploy without review

✗ Fix symptoms only

Quick Prompt Index
Prompt	Purpose
Testing Strategy	QA Planning
Test Case	Scenario Creation
Unit Test	Function Testing
Integration Test	System Testing
UAT	User Validation
Bug Analysis	Problem Solving
Refactoring	Code Improvement
Technical Debt	Long-term Quality
Performance Test	Speed
Security Test	Protection
QA Review	Release Decision
End of Part 3A

<!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 3B : Security & Compliance Prompts -->
<!-- ====================================================================== -->

# Part 3B — Security & Compliance Prompts

Version 2.0

Enterprise Prompt Library

---

# Purpose

This section provides prompt templates for security analysis, security implementation, and compliance review.

The objective is to ensure applications are:

- Secure
- Reliable
- Auditable
- Protected against unauthorized access
- Compliant with organizational requirements

Security scope:

- Authentication
- Authorization
- RBAC
- Data Protection
- Input Validation
- Secrets Management
- Audit Logging
- Vulnerability Review

Supported Technology:

- Google Apps Script
- Google Sheets
- HTML5
- Tailwind CSS
- JavaScript ES6+

---

# Security Workflow

```text
Security Requirement

↓

Threat Analysis

↓

Architecture Review

↓

Authentication

↓

Authorization

↓

Data Protection

↓

Security Testing

↓

Audit

↓

Continuous Improvement

Security Architecture Review Prompt
Purpose

Analyze application security architecture.

Prompt
Act as a Senior Application Security Architect.

Review this application security architecture.

Technology:

Google Apps Script

Google Sheets

HTML5

JavaScript

Analyze:

1. Authentication
2. Authorization
3. Data Protection
4. Access Control
5. Logging
6. Vulnerability Risks
7. Security Improvements

Return professional security assessment.
Threat Modeling Prompt
Prompt
Perform threat modeling.

Application:

[APPLICATION_NAME]

Identify:

Assets

Users

Entry Points

Threats

Attack Scenarios

Risk Level

Mitigation Strategy
Security Risk Assessment Prompt
Prompt
Perform security risk assessment.

For each risk include:

Risk ID

Description

Impact

Probability

Severity

Mitigation

Priority

Example:

Risk	Impact	Level
Unauthorized Access	High	Critical
Authentication Security Prompt
Purpose

Review identity verification.

Prompt
Review authentication system.

Check:

Login Process

Identity Verification

Session Management

Password Policy

Account Lock

Logout

Session Expiration

Security Recommendations
Google Authentication Prompt
Design Google Authentication.

Include:

Google Account Login

User Verification

User Mapping

Session Creation

Access Control

Logout Flow
Session Management Prompt
Create secure session management.

Include:

Session Creation

Session Validation

Expiration

Logout

Session Storage

Security Rules
Authentication Error Handling Prompt
Design authentication error handling.

Include:

Invalid Login

Expired Session

Unauthorized User

Account Disabled

Security Message
Authorization Security Prompt
Prompt
Review authorization system.

Check:

Permission Validation

Resource Access

Role Checking

Action Control

Privilege Escalation Prevention
RBAC Security Audit Prompt
Perform RBAC audit.

Review:

Users

Roles

Permissions

Modules

Actions

Access Rules

Identify:

Over Permission

Missing Permission

Security Risk
Permission Matrix Prompt
Generate permission matrix.

Roles:

Admin

Manager

Staff

User

Guest

Actions:

View

Create

Update

Delete

Approve

Export

Manage Settings

Example:

Role	View	Edit	Delete
Admin	✓	✓	✓
User	✓	✗	✗
Privilege Escalation Review Prompt
Analyze privilege escalation risks.

Check:

Role Manipulation

Direct API Access

Hidden Features

Parameter Tampering

Unauthorized Actions

Provide prevention strategy.
Input Validation Security Prompt
Prompt
Review input validation.

Check:

Required Fields

Data Type

Length

Format

Special Characters

Injection Risk

Validation Location
Data Sanitization Prompt
Create data sanitization rules.

Protect against:

Invalid Input

Script Injection

HTML Injection

Malicious Data

Unexpected Format
XSS Protection Prompt
Review application for XSS vulnerabilities.

Check:

User Input

HTML Rendering

Output Encoding

Dynamic Content

Provide fixes.
Injection Prevention Prompt
Analyze injection risks.

Check:

Spreadsheet Formula Injection

Script Injection

Parameter Injection

Data Manipulation

Recommend protection.
Sensitive Data Protection Prompt
Prompt
Review sensitive data handling.

Check:

Personal Data

Confidential Data

Storage

Display

Export

Logging

Masking Strategy
Data Masking Prompt
Create data masking rules.

Examples:

Email

Phone

ID Number

Personal Information

Define:

Display Format

Storage Rule

Access Permission
Secrets Management Prompt
Purpose

Prevent credential exposure.

Prompt
Review secrets management.

Check:

API Keys

Tokens

Passwords

Configuration

PropertiesService

Environment Variables

Recommend secure approach.
Google Apps Script Security Prompt
Review Google Apps Script security.

Check:

Authorization Scope

PropertiesService

Spreadsheet Permission

Web App Deployment

User Access

Execution Identity
Google Sheets Security Prompt
Review Google Sheets database security.

Check:

Sharing Permission

Sensitive Columns

Data Exposure

Backup

Audit

Access Control
Audit Logging Prompt
Prompt
Create security audit log.

Capture:

User

Action

Module

Timestamp

IP Information

Old Value

New Value

Result
Security Monitoring Prompt
Design security monitoring.

Track:

Failed Login

Permission Change

Sensitive Export

Data Modification

Suspicious Activity
Vulnerability Review Prompt
Prompt
Perform vulnerability assessment.

Check:

Authentication

Authorization

Injection

Data Exposure

Configuration

Dependency Risk

Return:

Finding

Severity

Recommendation
OWASP Security Review Prompt
Review application using OWASP principles.

Check:

Authentication Failure

Access Control

Injection

Security Misconfiguration

Data Exposure

Logging

Vulnerabilities
Security Testing Prompt
Create security test cases.

Include:

Authentication Test

Authorization Test

Input Validation Test

Data Protection Test

Session Test

Audit Test
Incident Response Prompt
Create security incident response plan.

Include:

Detection

Containment

Investigation

Recovery

Communication

Prevention
Compliance Review Prompt
Review application compliance.

Check:

Data Privacy

Access Control

Audit Trail

Retention

Security Policy

Documentation
Security Code Review Prompt
Review code security.

Analyze:

Authentication

Authorization

Input Handling

Sensitive Data

Error Handling

Logging

Configuration

Return security findings.
Security Checklist

Before Production:

Authentication
 Login secured
 Session handled
 Logout implemented
 Unauthorized access blocked
Authorization
 RBAC implemented
 Permission checked
 Privilege escalation prevented
Data Protection
 Sensitive data protected
 Data masking applied
 Export controlled
 Logs secured
Application Security
 Input validation completed
 XSS reviewed
 Injection reviewed
 Error messages secured
Audit
 Audit log enabled
 User actions tracked
 Security events monitored
Security Best Practices

Always:

✓ Apply least privilege

✓ Validate all inputs

✓ Protect sensitive data

✓ Keep audit logs

✓ Review permissions

✓ Separate secrets from code

✓ Monitor security events

✓ Update documentation

Never:

✗ Store passwords in source code

✗ Expose API keys

✗ Trust user input

✗ Give excessive permissions

✗ Disable security checks

✗ Log sensitive information

Quick Prompt Index
Prompt	Purpose
Security Architecture	Security Design
Threat Modeling	Risk Discovery
Authentication	Identity
Authorization	Access Control
RBAC Audit	Permission Review
Input Validation	Data Safety
Data Protection	Privacy
Secrets Management	Credential Security
Audit Log	Tracking
Vulnerability Review	Security Testing
Compliance	Governance
End of Part 3B

<!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 3C : Performance Optimization & Scalability Prompts -->
<!-- ====================================================================== -->

# Part 3C — Performance Optimization & Scalability Prompts

Version 2.0

Enterprise Prompt Library

---

# Purpose

This section provides prompt templates for analyzing and improving application performance.

The objective is to ensure the application can:

- Respond quickly
- Handle increasing users
- Process large datasets
- Reduce resource consumption
- Scale efficiently

Performance scope:

- Google Apps Script Optimization
- Google Sheets Optimization
- Frontend Performance
- Backend Performance
- Caching
- Data Processing
- Scalability Planning

Supported Technology:

- Google Apps Script
- Google Sheets
- HTML5
- Tailwind CSS
- JavaScript ES6+

---

# Performance Optimization Workflow

```text
Performance Requirement

↓

Measure Current State

↓

Identify Bottleneck

↓

Analyze Root Cause

↓

Optimize

↓

Measure Improvement

↓

Monitor Continuously

Performance Architecture Review Prompt
Purpose

Analyze overall system performance.

Prompt
Act as a Senior Performance Engineer.

Review application architecture.

Technology:

Google Apps Script

Google Sheets

HTML

JavaScript

Analyze:

1. Performance Bottlenecks
2. Data Processing
3. API Calls
4. Frontend Rendering
5. Caching Opportunity
6. Scalability Risk

Return optimization recommendations.
Performance Assessment Prompt
Perform performance assessment.

Evaluate:

Response Time

Execution Time

Memory Usage

Database Operations

Network Requests

User Experience

Provide:

Issue

Impact

Priority

Solution
Google Apps Script Performance Prompt
Purpose

Optimize GAS execution.

Prompt
Review Google Apps Script performance.

Analyze:

Function Execution

Spreadsheet Calls

Loops

API Calls

Triggers

Memory Usage

Recommend optimization.
GAS Execution Optimization Prompt
Optimize this Google Apps Script function.

Check:

Execution Time

Repeated Operations

Unnecessary Calls

Batch Processing

Memory Usage

Return optimized approach.
Spreadsheet Operation Optimization Prompt
Optimize Google Sheets operations.

Analyze:

getRange()

setValue()

getValues()

setValues()

Formula Usage

Batch Updates

Return improvement strategy.
Batch Processing Prompt
Convert this process to batch processing.

Current:

Multiple Spreadsheet Operations

Improve:

Read Once

Process Memory

Write Once

Reduce API Calls
Google Sheets Database Optimization Prompt
Prompt
Review Google Sheets database design.

Analyze:

Sheet Structure

Column Design

Data Volume

Formula Usage

Query Pattern

Archiving Strategy

Provide optimization plan.
Large Dataset Handling Prompt
Design large dataset handling strategy.

Dataset:

[DATA_SIZE]

Include:

Pagination

Filtering

Lazy Loading

Archiving

Index Strategy

Caching
Data Pagination Prompt
Create pagination system.

Support:

Page Number

Page Size

Total Records

Sorting

Filtering

Efficient Query
Backend Performance Prompt
Review backend performance.

Analyze:

Controller

Service

Repository

Data Access

Business Logic

Error Handling

Provide optimization.
API Performance Prompt
Optimize API communication.

Analyze:

Request Size

Response Size

Payload

Frequency

Caching

Compression

Error Handling
Frontend Performance Prompt
Purpose

Improve user interface speed.

Prompt
Review frontend performance.

Analyze:

HTML

CSS

JavaScript

DOM

Rendering

Network

User Interaction

Provide optimization.
JavaScript Optimization Prompt
Optimize JavaScript code.

Check:

Loops

Functions

Event Handling

Memory Leak

DOM Access

Async Processing
DOM Performance Prompt
Analyze DOM performance.

Review:

Large Lists

Repeated Rendering

Event Binding

Component Updates

Recommend improvement.
Component Performance Prompt
Optimize UI component.

Component:

[COMPONENT_NAME]

Analyze:

Rendering

State Update

Events

Memory Usage

User Experience
Loading Performance Prompt
Improve application loading.

Optimize:

Initial Load

Assets

Scripts

CSS

API Calls

Lazy Loading
Caching Strategy Prompt
Purpose

Design caching system.

Prompt
Design caching strategy.

Include:

Cache Location

Cache Duration

Cache Key

Invalidation

Refresh Strategy

Consistency Rules
Google Apps Script Cache Prompt
Implement GAS CacheService strategy.

Support:

Temporary Data

API Response

User Session Data

Expiration

Cache Clearing
Client-Side Cache Prompt
Design browser caching strategy.

Include:

LocalStorage

SessionStorage

Cache Expiration

Data Refresh

Security Consideration
Data Loading Strategy Prompt
Design efficient data loading.

Support:

Initial Load

Lazy Load

Pagination

Background Refresh

Loading State
Scalability Review Prompt
Purpose

Prepare system growth.

Prompt
Perform scalability review.

Analyze:

Users

Data Volume

Transactions

Execution Limits

Storage

Future Growth

Provide scaling roadmap.
Capacity Planning Prompt
Create capacity plan.

Estimate:

Current Usage

Future Usage

User Growth

Data Growth

Performance Limit

Optimization Plan
Bottleneck Analysis Prompt
Analyze performance bottleneck.

Input:

System Behavior

Slow Function

Error

Delay

Return:

Root Cause

Measurement

Solution

Priority
Performance Monitoring Prompt
Design performance monitoring.

Monitor:

Execution Time

Error Rate

API Usage

Data Size

User Activity

Performance Trend
Optimization Priority Prompt
Prioritize performance improvements.

Rank:

Critical

High

Medium

Low

Based on:

Impact

Effort

Risk

Benefit
Performance Testing Prompt
Create performance test plan.

Test:

Small Data

Medium Data

Large Data

Multiple Users

Peak Usage

Expected Result
Load Simulation Prompt
Simulate high usage scenario.

Scenario:

Users:

[NUMBER]

Data:

[SIZE]

Actions:

[WORKFLOW]

Analyze:

Response

Risk

Optimization
Performance Code Review Prompt
Review code for performance.

Check:

Algorithm

Loops

API Calls

Memory

Caching

Database Access

Return recommendations.
Performance Checklist

Before Production:

Backend
 Function optimized
 API calls minimized
 Batch processing used
 Error handling efficient
Database
 Sheet structure optimized
 Large data strategy defined
 Pagination implemented
Frontend
 Loading optimized
 DOM minimized
 Components optimized
 Assets optimized
Scalability
 Growth plan created
 Monitoring enabled
 Bottlenecks identified
Performance Best Practices

Always:

✓ Measure before optimizing

✓ Reduce unnecessary calls

✓ Use batch operations

✓ Cache repeated data

✓ Optimize data loading

✓ Monitor performance

✓ Design for growth

Never:

✗ Optimize without measurement

✗ Read/write Sheets repeatedly

✗ Load unnecessary data

✗ Ignore large datasets

✗ Block user interaction

Quick Prompt Index
Prompt	Purpose
Architecture Review	Performance Design
GAS Optimization	Script Speed
Sheets Optimization	Data Access
Backend Performance	Server Logic
Frontend Performance	UI Speed
Caching	Faster Response
Scalability	Future Growth
Monitoring	Continuous Improvement
Testing	Performance Validation
End of Part 3C

<!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 3D : Deployment & Release Management Prompts -->
<!-- ====================================================================== -->

# Part 3D — Deployment & Release Management Prompts

Version 2.0

Enterprise Prompt Library

---

# Purpose

This section provides prompt templates for deploying, releasing, and operating applications in production environments.

The objective is to ensure:

- Safe deployment
- Controlled releases
- Version tracking
- Environment separation
- Easy rollback
- Stable production operation

Deployment scope:

- GitHub Repository Management
- Google Apps Script Deployment
- Environment Configuration
- Version Control
- Release Planning
- Production Monitoring

Supported Technology:

- GitHub
- GitHub Copilot Agent
- Google Apps Script
- Google Sheets
- JavaScript ES6+

---

# Deployment Workflow

```text
Development

↓

Code Review

↓

Testing

↓

Build Preparation

↓

Deployment

↓

Verification

↓

Monitoring

↓

Release

Deployment Strategy Prompt
Purpose

Design deployment approach.

Prompt
Act as a Senior DevOps Engineer.

Design deployment strategy.

Application:

[APPLICATION_NAME]

Technology:

GitHub

Google Apps Script

Google Sheets

JavaScript

Include:

1. Deployment Process
2. Environment Strategy
3. Version Control
4. Backup Strategy
5. Rollback Plan
6. Monitoring Plan

Return professional deployment document.
Environment Management Prompt
Purpose

Separate development and production environments.

Prompt
Design environment management.

Environments:

Development

Testing

Production

Include:

Configuration

Permissions

Data Separation

Deployment Rules

Security Controls
Environment Configuration Prompt
Create configuration management strategy.

Include:

Environment Variables

Application Settings

API Configuration

Spreadsheet ID

Feature Flags

Secret Management
Git Repository Strategy Prompt
Design Git repository structure.

Include:

Branches

Folders

Documentation

Version Tags

Pull Requests

Code Review Rules
Branching Strategy Prompt
Create Git branching strategy.

Support:

main

develop

feature branches

hotfix

release branches

Explain:

Purpose

Workflow

Merge Rules
Git Commit Standard Prompt
Create commit message standard.

Include:

Feature

Fix

Refactor

Documentation

Test

Security

Example format.

Example:

feat: add patient dashboard
fix: resolve login validation issue
docs: update API specification
Pull Request Review Prompt
Review this Pull Request.

Analyze:

Code Quality

Architecture

Security

Performance

Testing

Documentation

Return:

Approve

Request Changes

Comments
Google Apps Script Deployment Prompt
Design GAS deployment process.

Include:

Script Version

Deployment ID

Web App Settings

Access Permission

Environment

Rollback Method
GAS Version Management Prompt
Create Google Apps Script version strategy.

Include:

Version Number

Release Note

Deployment Date

Changes

Rollback Reference
Release Planning Prompt
Purpose

Create controlled release process.

Prompt
Create release plan.

Release:

[VERSION]

Include:

Features

Bug Fixes

Database Changes

Testing Status

Deployment Steps

Rollback Plan
Release Note Generation Prompt
Generate release notes.

Version:

[VERSION]

Include:

New Features

Improvements

Bug Fixes

Breaking Changes

Migration Notes
Change Management Prompt
Create change management document.

Change:

[CHANGE_DESCRIPTION]

Include:

Reason

Impact

Risk

Approval

Implementation

Verification
Migration Planning Prompt
Create migration plan.

Change:

[DATABASE_OR_SYSTEM_CHANGE]

Include:

Before

Migration Steps

After

Validation

Rollback
Backup Strategy Prompt
Design backup strategy.

Include:

Google Sheets Backup

Code Backup

Configuration Backup

Frequency

Retention

Restore Process
Rollback Strategy Prompt
Create rollback plan.

Scenario:

Deployment Failure

Include:

Detection

Rollback Steps

Data Recovery

Verification

Communication
Production Deployment Checklist Prompt
Create production deployment checklist.

Include:

Pre Deployment

Deployment

Post Deployment

Verification

Monitoring

Approval
Production Readiness Review Prompt
Perform production readiness review.

Evaluate:

Functionality

Security

Performance

Documentation

Backup

Monitoring

Operational Readiness
Smoke Test Prompt
Create production smoke test.

Verify:

Application Access

Login

Main Features

Database Connection

API

Notification

Critical Workflow
Post Deployment Verification Prompt
Verify deployment result.

Check:

Version

Functionality

Performance

Errors

Logs

User Access

Data Integrity
Production Monitoring Prompt
Design production monitoring.

Track:

Errors

Performance

User Activity

Execution Limit

Data Growth

Security Events
Incident Management Prompt
Create production incident response.

Include:

Detection

Severity

Response Team

Resolution

Root Cause

Prevention
Hotfix Management Prompt
Create hotfix workflow.

Include:

Issue Analysis

Quick Fix

Testing

Deployment

Documentation

Version Update
Documentation Update Prompt
Review documentation after release.

Update:

README

Architecture

API

Database

User Guide

Release Notes
Deployment Security Review Prompt
Review deployment security.

Check:

Permissions

Secrets

Access Control

Configuration

Deployment Account

Audit Log
Release Automation Prompt
Design release automation.

Include:

Version Tagging

Release Notes

Checklist

Deployment Steps

Notification
CI/CD Workflow Prompt
Design CI/CD workflow.

Include:

Code Push

Validation

Testing

Review

Deployment

Monitoring

Rollback
Production Operation Prompt
Create operation guide.

Include:

Daily Monitoring

Backup

User Support

Issue Handling

Maintenance

Optimization
Deployment Checklist

Before Release:

Repository
 Code committed
 Branch reviewed
 Pull Request approved
 Version tagged
Testing
 Unit tests passed
 Integration tested
 UAT completed
Security
 Permission reviewed
 Secrets protected
 Access verified
Deployment
 Backup completed
 Deployment completed
 Smoke test passed
Operations
 Monitoring enabled
 Documentation updated
 Release notes created
Deployment Best Practices

Always:

✓ Separate environments

✓ Review before release

✓ Backup before deployment

✓ Keep version history

✓ Prepare rollback

✓ Monitor production

✓ Document changes

Never:

✗ Deploy untested code

✗ Modify production directly

✗ Ignore backups

✗ Skip security review

✗ Release without documentation

Quick Prompt Index
Prompt	Purpose
Deployment Strategy	Release Design
Environment	Configuration
Git Workflow	Version Control
GAS Deployment	App Release
Release Plan	Controlled Delivery
Rollback	Recovery
Monitoring	Operations
Incident	Problem Response
CI/CD	Automation
Production Review	Readiness
End of Part 3D

<!-- ====================================================================== -->
<!-- File: docs/32_PROMPT_TEMPLATES.md -->
<!-- Part 3E : AI Agent Operation & Continuous Improvement Prompts -->
<!-- ====================================================================== -->

# Part 3E — AI Agent Operation & Continuous Improvement Prompts

Version 2.0

Enterprise Prompt Library

---

# Purpose

This section defines how to operate AI coding agents such as GitHub Copilot Agent effectively.

The objective is to create:

- Consistent AI behavior
- Better code quality
- Accurate architecture decisions
- Faster development workflow
- Continuous improvement process

AI Agent Role:

- Software Architect Assistant
- Senior Developer Assistant
- Code Reviewer
- QA Engineer
- Security Reviewer
- Documentation Assistant

---

# AI Agent Development Workflow

```text
Human Requirement

↓

AI Analysis

↓

Architecture Decision

↓

Implementation Plan

↓

Code Generation

↓

Code Review

↓

Testing

↓

Improvement

↓

Documentation

Master AI Agent Prompt
Purpose

Initialize AI Agent behavior.

Prompt
You are an Enterprise Software Development AI Agent.

Project:

[PROJECT_NAME]

Your responsibilities:

1. Understand project architecture
2. Follow repository rules
3. Respect coding standards
4. Generate maintainable code
5. Review before implementation
6. Explain important decisions
7. Avoid unnecessary complexity

Before coding:

Analyze requirements.

Design solution.

Confirm architecture.

Then implement.
AI Context Loading Prompt
Purpose

Make Agent understand project.

Prompt
Analyze this repository.

Read:

.github/copilot-instructions.md

.github/copilot-context.md

.github/copilot-rules.md

docs/

Understand:

Architecture

Technology

Coding Standards

Business Rules

Development Workflow

Return project understanding summary.
Repository Understanding Prompt
Analyze repository structure.

Explain:

Folder Purpose

Important Files

Architecture

Development Flow

Documentation System

Identify missing elements.
Documentation Analysis Prompt
Review project documentation.

Check:

Completeness

Consistency

Missing Information

Outdated Sections

Recommend improvements.
Feature Planning Prompt
Purpose

Before development.

Prompt
Plan implementation for feature:

[FEATURE_NAME]

Analyze:

Requirement

User Flow

Business Rules

Database Changes

Backend Changes

Frontend Changes

Testing

Documentation

Do not write code yet.
AI Code Generation Prompt
Generate code for:

[FEATURE]

Follow:

Project Architecture

Coding Standards

Existing Patterns

Security Rules

Performance Guidelines

Include explanation.
AI Code Modification Prompt
Modify existing code.

Requirements:

[CHANGE]

Rules:

Keep existing behavior

Avoid breaking changes

Follow architecture

Explain affected files.
AI Refactoring Prompt
Refactor this code.

Goals:

Improve readability

Reduce duplication

Improve performance

Maintain functionality

Follow project standards.
AI Debugging Prompt
Debug this issue.

Error:

[ERROR_MESSAGE]

Analyze:

Possible Cause

Affected Component

Root Cause

Solution

Prevention
AI Code Review Prompt
Act as Senior Code Reviewer.

Review:

[CODE]

Check:

Architecture

Security

Performance

Maintainability

Naming

Error Handling

Return:

Issues

Severity

Recommendation
AI Security Review Prompt
Act as Security Engineer.

Review implementation.

Check:

Authentication

Authorization

Data Exposure

Input Validation

Secrets

Audit

Return security findings.
AI Testing Prompt
Create testing plan.

Feature:

[FEATURE]

Include:

Unit Test

Integration Test

UAT

Security Test

Performance Test
AI Documentation Generation Prompt
Generate documentation.

Target:

[FEATURE]

Include:

Purpose

Architecture

Installation

Configuration

Usage

API

Troubleshooting
AI Architecture Decision Prompt
Act as Software Architect.

Evaluate this technical decision.

Option A:

[OPTION]

Option B:

[OPTION]

Compare:

Performance

Security

Maintainability

Complexity

Cost

Recommend best approach.
AI Problem Solving Framework Prompt
Solve this technical problem.

Use framework:

1. Understand Problem
2. Analyze Context
3. Identify Options
4. Compare Trade-offs
5. Recommend Solution
6. Implementation Plan
AI Agent Review Loop
Generate

↓

Review

↓

Improve

↓

Test

↓

Document

↓

Approve
AI Self Review Prompt
Before finalizing:

Review your generated solution.

Check:

Does it follow architecture?

Is it secure?

Is it maintainable?

Is it optimized?

Are there edge cases?

Suggest improvements.
AI Decision Log Prompt
Create architecture decision record.

Decision:

[DECISION]

Include:

Context

Options

Decision

Reason

Impact

Future Consideration
AI Knowledge Update Prompt
Update project knowledge.

Analyze:

New Feature

New Rule

New Architecture Decision

Update:

Documentation

AI Context

Development Rules
AI Agent Task Management Prompt
Break this project task into smaller tasks.

Task:

[TASK]

Return:

Epic

Feature

Tasks

Dependencies

Priority

Estimated Effort
AI Agent Collaboration Prompt
Act as multiple roles:

Software Architect

Backend Developer

Frontend Developer

QA Engineer

Security Engineer

Analyze this requirement from all perspectives.
AI Agent Rules

The Agent must:

✓ Read documentation first

✓ Understand architecture before coding

✓ Follow existing patterns

✓ Ask when requirements are unclear

✓ Explain major decisions

✓ Validate security

✓ Consider performance

✓ Update documentation

The Agent must not:

✗ Create random architecture

✗ Ignore existing rules

✗ Duplicate functionality

✗ Hard-code secrets

✗ Skip validation

✗ Modify unrelated files

Continuous Improvement Workflow
Collect Feedback

↓

Analyze Issues

↓

Improve Code

↓

Update Documentation

↓

Update AI Context

↓

Improve Future Development
AI Retrospective Prompt
Perform project retrospective.

Analyze:

What Worked

What Failed

Technical Issues

Process Issues

Improvement Actions
AI Optimization Prompt
Analyze project improvement opportunities.

Review:

Architecture

Code Quality

Performance

Security

Documentation

Developer Experience

Recommend roadmap.
AI Agent Operation Checklist

Before using Agent:

 Repository instructions loaded
 Context understood
 Architecture reviewed
 Requirements clear

During development:

 Plan before coding
 Review generated code
 Test implementation
 Check security

After development:

 Update documentation
 Review quality
 Record decisions
 Improve AI context
AI Agent Best Practices

Always:

✓ Provide clear requirements

✓ Give enough context

✓ Use structured prompts

✓ Review AI output

✓ Combine AI + Human judgment

✓ Maintain documentation

Never:

✗ Accept generated code blindly

✗ Skip review

✗ Ignore security

✗ Remove human validation

✗ Let AI change architecture without approval

Quick Prompt Index
Prompt	Purpose
Master Agent	Initialize AI
Context Loading	Understand Project
Planning	Design Before Code
Coding	Generate Solution
Review	Quality Check
Debug	Problem Solving
Testing	Validation
Security	Protection
Documentation	Knowledge
Improvement	Evolution
End of Part 3E
End of Phase 3 — Quality, Security & Production Readiness


