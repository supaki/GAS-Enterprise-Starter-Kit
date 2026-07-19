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

