<!-- ====================================================================== -->
<!-- File: docs/31_COPILOT_AGENT_GUIDE.md -->
<!-- Part 1/3 -->
<!-- ====================================================================== -->

# GitHub Copilot Agent Guide

Version 2.0

---

# Purpose

This document is the official operating guide for GitHub Copilot Agent in the GAS Enterprise Starter Kit.

It explains how to work with the AI agent throughout the entire software development lifecycle, from requirement analysis to deployment and maintenance.

This guide applies to:

- GitHub Copilot Agent
- GitHub Copilot Chat
- VS Code
- Google Apps Script Projects
- Enterprise Web Applications

---

# Objectives

The objectives of this guide are to:

- Standardize AI-assisted development
- Improve code quality
- Reduce development time
- Maintain project architecture
- Ensure consistency across modules
- Prevent AI-generated technical debt

---

# AI Role

GitHub Copilot Agent must behave as:

- Enterprise Software Architect
- Full Stack Engineer
- Google Apps Script Expert
- UI/UX Designer
- Database Designer
- Security Reviewer
- Code Reviewer
- QA Engineer

The agent should always prioritize:

1. Quality
2. Security
3. Maintainability
4. Performance
5. User Experience

---

# AI Responsibilities

GitHub Copilot Agent is responsible for:

- Understanding requirements
- Reviewing project documentation
- Designing architecture
- Generating production-ready code
- Refactoring existing code
- Detecting issues
- Suggesting improvements
- Writing documentation
- Creating reusable components
- Assisting testing

---

# AI Limitations

GitHub Copilot Agent should NEVER assume:

- Business rules not documented
- Database structures that do not exist
- User permissions
- API behavior
- Sheet names
- Folder structures

When information is missing,

ASK FIRST.

Never invent project requirements.

---

# Repository Structure

The repository should follow:

```text
.github/

docs/

src/

assets/

tests/

README.md

CHANGELOG.md

LICENSE

appsscript.json
```

---

# Documentation Hierarchy

GitHub Copilot should read documentation in this order.

Priority 1

```
.github/copilot-instructions.md
```

Priority 2

```
.github/copilot-context.md
```

Priority 3

```
.github/copilot-rules.md
```

Priority 4

Relevant files inside

```
docs/
```

Priority 5

Existing source code

---

# Documentation Categories

The documentation is divided into four areas.

## Foundation

- AI Instructions
- Project Overview
- Architecture
- Database

---

## Development

- Coding Standards
- Folder Structure
- Components
- Authentication

---

## Enterprise

- Design System
- User Flow
- Business Rules
- Performance

---

## AI

- Prompt Library
- AI Context
- Copilot Workflow

---

# Before Starting Development

Before generating code, GitHub Copilot Agent should:

✓ Read project overview

✓ Understand system architecture

✓ Review coding standards

✓ Review database schema

✓ Review business rules

✓ Review existing implementation

Only after that should implementation begin.

---

# Standard Development Lifecycle

Every feature follows the same workflow.

```text
Requirement

↓

Analysis

↓

Architecture

↓

Database Design

↓

API Design

↓

UI Design

↓

Implementation

↓

Testing

↓

Documentation

↓

Deployment
```

Never skip a phase.

---

# Requirement Analysis

Before writing code, analyze:

Functional Requirements

Example

- User Login
- Dashboard
- Reports

Non-functional Requirements

Example

- Responsive
- Fast
- Secure
- Accessible

Constraints

Example

- Google Apps Script
- Google Sheets
- Tailwind CSS

---

# Requirement Checklist

Before implementation verify:

- Goal is clear
- Scope is defined
- User roles identified
- Data identified
- Success criteria defined

---

# Architecture Phase

During architecture design determine:

- Controllers
- Services
- Repositories
- Models
- Utilities
- Components

Every responsibility must belong to only one layer.

---

# MVC Overview

```
User

↓

View

↓

Controller

↓

Service

↓

Repository

↓

Google Sheets
```

Never bypass the Service Layer.

---

# Clean Architecture

Each layer should depend only on lower-level abstractions.

Example

```
Controller

↓

Service

↓

Repository

↓

Spreadsheet
```

Never

```
HTML

↓

Spreadsheet
```

---

# Folder Responsibility

controllers/

Business entry points

services/

Business logic

repositories/

Google Sheets access

models/

Data models

utils/

Common utilities

web/

UI components

---

# Database Planning

Before implementation identify:

- Sheet names
- Columns
- Relationships
- Validation
- Primary Keys

Never create sheets without documentation.

---

# UI Planning

Before coding define:

- Layout
- Navigation
- Components
- Forms
- Tables
- Dialogs
- Notifications
- Responsive behavior

---

# UI Standard

Every application should include:

- Sidebar
- Navbar
- Dashboard
- Cards
- Tables
- Forms
- Search
- Filters
- Modals
- Toasts

Support:

- Desktop
- Tablet
- Mobile

---

# API Planning

Before implementation define:

Input

↓

Validation

↓

Business Logic

↓

Response

Every API should return a standard response.

Example

Success

```json
{
  "success": true,
  "data": {}
}
```

Error

```json
{
  "success": false,
  "message": "Error"
}
```

---

# Security Planning

Before implementation verify:

Authentication

Authorization

Input Validation

Output Encoding

Permission Checking

Audit Logging

Never postpone security until the end.

---

# Coding Phase

When writing code:

Keep functions:

- Small
- Readable
- Reusable
- Testable

Avoid:

- Long methods
- Duplicate code
- Hidden dependencies

---

# Definition of Ready

A task is ready for implementation when:

- Requirement approved
- Architecture completed
- Database defined
- UI planned
- Business rules documented
- Acceptance criteria confirmed

---

# Part 1 Summary

This section covered:

- AI responsibilities
- Repository structure
- Documentation hierarchy
- Development lifecycle
- Requirement analysis
- Architecture planning
- Database planning
- UI planning
- API planning
- Security planning
- Definition of Ready

Continue with:

**Part 2 — Prompt Engineering, Agent Commands, Prompt Templates, Best Practices**
<!-- ====================================================================== -->
<!-- File: docs/31_COPILOT_AGENT_GUIDE.md -->
<!-- Part 2/3 -->
<!-- ====================================================================== -->

# Part 2 — Prompt Engineering & Copilot Workflow

---

# Prompt Engineering Philosophy

GitHub Copilot Agent performs best when prompts are:

- Clear
- Specific
- Context-aware
- Incremental
- Goal-oriented

Avoid asking the AI to build an entire enterprise system in a single prompt.

Large projects should always be divided into small, manageable tasks.

---

# Golden Rules for Prompting

Always include:

- Objective
- Context
- Expected Output
- Constraints
- Technology Stack
- Coding Standard

Example

```
Goal

Create User Management Module

Technology

Google Apps Script
Google Sheets
Tailwind CSS

Architecture

MVC

Requirement

CRUD User

Output

Production-ready code
```

---

# Recommended Prompt Structure

```
Role

↓

Project Context

↓

Task

↓

Requirements

↓

Constraints

↓

Expected Output
```

---

# Prompt Template

```
You are a Senior Google Apps Script Engineer.

Project:

GAS Enterprise Starter Kit

Technology:

- Google Apps Script
- Google Sheets
- HTML5
- Tailwind CSS

Architecture:

MVC
Repository Pattern
Service Layer

Task:

<Create Task>

Requirements:

<List>

Output:

Production-ready code.
```

---

# Development Strategy

Never generate an entire application at once.

Instead:

```
Requirement

↓

Architecture

↓

Database

↓

UI

↓

Backend

↓

Testing
```

---

# Recommended Workflow

## Step 1

Analyze Requirement

Prompt

```
Analyze this requirement.

Identify:

- Features
- User Roles
- Business Rules
- Database
- UI
- API

Do not write code.
```

---

## Step 2

Design Architecture

Prompt

```
Design the architecture.

Use:

MVC

Repository Pattern

Service Layer

Return:

Folder Structure

Responsibilities

Data Flow
```

---

## Step 3

Design Database

Prompt

```
Design Google Sheets schema.

Include:

Sheet names

Columns

Data Types

Relationships

Validation

Sample Data
```

---

## Step 4

Design UI

Prompt

```
Design a modern SaaS interface.

Requirements:

Responsive

Dark Mode

Tailwind CSS

Cards

Sidebar

Dashboard

Forms

Tables

Return HTML structure only.
```

---

## Step 5

Generate Backend

Prompt

```
Generate Controller.

Do not generate UI.

Use Service Layer.

Follow Coding Standards.
```

---

## Step 6

Generate Service

Prompt

```
Generate Service Layer.

Business logic only.

No Spreadsheet code outside Repository.
```

---

## Step 7

Generate Repository

Prompt

```
Generate Repository.

Only Google Sheets operations.

No business logic.
```

---

## Step 8

Generate UI Components

Prompt

```
Generate reusable UI components.

Requirements

Tailwind CSS

Responsive

Dark Mode

Accessible
```

---

## Step 9

Generate Testing

Prompt

```
Create testing scenarios.

Include:

Positive

Negative

Boundary

Permission

Performance
```

---

# Prompt Categories

## Requirement Analysis

Purpose

Understand project requirements.

---

## Architecture

Purpose

Create scalable structure.

---

## Database

Purpose

Create spreadsheet schema.

---

## API

Purpose

Define communication.

---

## UI

Purpose

Create modern interface.

---

## Testing

Purpose

Validate implementation.

---

## Review

Purpose

Improve code quality.

---

# Prompt Examples

## Create Login

```
Create Login Module.

Requirements

Google Apps Script

Google Sheets

Session Management

RBAC

Remember Me

Modern SaaS UI

Follow MVC.
```

---

## Create Dashboard

```
Create Dashboard.

Include

Sidebar

Navbar

Cards

Charts

Statistics

Notifications

Responsive

Dark Mode
```

---

## Create CRUD

```
Create CRUD Module.

Entity

Patient

Use

MVC

Repository Pattern

Validation

Search

Pagination

Export
```

---

## Create Report

```
Create Reporting Module.

Data Source

Google Sheets

Features

Filter

Export Excel

Print

Summary Cards

Charts
```

---

## Create Settings

```
Create System Settings Module.

Include

General

Theme

Roles

Permissions

Database Configuration
```

---

# Prompt Best Practices

Always

✓ One feature per prompt

✓ Clear objective

✓ Mention architecture

✓ Mention technology

✓ Mention constraints

✓ Mention output

---

Avoid

✗ Huge prompts

✗ Mixed requirements

✗ Missing context

✗ Ambiguous wording

---

# Prompt Chaining

Large projects should use Prompt Chaining.

```
Requirement

↓

Architecture

↓

Database

↓

API

↓

UI

↓

Backend

↓

Testing

↓

Review

↓

Optimization
```

---

# Copilot Review Prompt

```
Review this implementation.

Check:

Architecture

Coding Standards

Performance

Security

Maintainability

Error Handling

Suggest improvements.
```

---

# Refactoring Prompt

```
Refactor this code.

Requirements

Improve readability

Reduce duplication

Improve performance

Keep functionality unchanged.

Follow project standards.
```

---

# Documentation Prompt

```
Generate documentation.

Include

Purpose

Architecture

API

Database

Usage

Examples
```

---

# Bug Fix Prompt

```
Analyze this bug.

Explain:

Root Cause

Solution

Affected Files

Regression Risk

Then generate the fix.
```

---

# Optimization Prompt

```
Optimize this implementation.

Focus on

Performance

Maintainability

Readability

Security

Google Apps Script Best Practices
```

---

# Daily Development Cycle

```
Read Requirement

↓

Read Documentation

↓

Plan

↓

Generate

↓

Review

↓

Test

↓

Commit
```

---

# Common Mistakes

Avoid asking:

```
Create entire ERP system.
```

Better

```
Create User Module.

Next

Create Authentication.

Next

Create Dashboard.

Next

Create Reports.
```

---

# Best Practices Checklist

Before generating code

- Read documentation
- Review architecture
- Understand business rules

During coding

- Keep modules small
- Separate responsibilities
- Reuse components

After coding

- Review code
- Test functionality
- Update documentation

---

# Part 2 Summary

This section covered:

- Prompt Engineering
- Prompt Templates
- Prompt Chaining
- Development Workflow
- Review Prompts
- Refactoring Prompts
- Documentation Prompts
- Best Practices

Continue with:

**Part 3 — Advanced Workflow, Troubleshooting, FAQ, Checklists, and Definition of Done**
<!-- ====================================================================== -->
<!-- File: docs/31_COPILOT_AGENT_GUIDE.md -->
<!-- Part 3/3 -->
<!-- ====================================================================== -->

# Part 3 — Advanced Workflow, Troubleshooting & Best Practices

---

# AI Development Lifecycle

Every feature should follow the same lifecycle.

```
Requirement

↓

Requirement Analysis

↓

Architecture Design

↓

Database Design

↓

API Design

↓

UI Design

↓

Implementation

↓

Testing

↓

Code Review

↓

Documentation

↓

Deployment
```

Never skip any stage.

---

# AI Decision Process

Before generating code, Copilot Agent should answer:

1. What problem is being solved?

2. Which modules are affected?

3. Does documentation already exist?

4. Can an existing component be reused?

5. Is database modification required?

6. Is API modification required?

7. Are security implications considered?

Only after answering these questions should implementation begin.

---

# Feature Development Workflow

For every new feature:

Step 1

Read

- Project Overview
- Architecture
- Business Rules

↓

Step 2

Analyze Requirement

↓

Step 3

Design Solution

↓

Step 4

Generate Backend

↓

Step 5

Generate UI

↓

Step 6

Test

↓

Step 7

Review

↓

Step 8

Update Documentation

---

# Code Review Workflow

Every generated code should be reviewed.

Checklist

Architecture

□ MVC

□ Service Layer

□ Repository Pattern

Security

□ Validation

□ Permission Check

□ Error Handling

Performance

□ Batch Operations

□ Cache

□ Optimized Spreadsheet Access

Maintainability

□ Naming Convention

□ Small Functions

□ Reusable Components

---

# Testing Workflow

Every feature requires:

## Functional Test

Verify:

- Business Logic
- UI
- API

---

## Validation Test

Verify:

- Required Fields
- Invalid Input
- Duplicate Data

---

## Permission Test

Verify:

- Admin
- Manager
- User
- Guest

---

## Performance Test

Verify:

- Loading Speed

- Spreadsheet Access

- Pagination

---

## Regression Test

Verify:

- Existing features still work.

---

# Documentation Workflow

After implementation update:

- Database Schema

- API Specification

- Business Rules

- Release Note

- CHANGELOG

Documentation must always match implementation.

---

# Git Workflow

Recommended workflow

```
Feature Branch

↓

Development

↓

Review

↓

Testing

↓

Merge

↓

Release
```

---

# Commit Standard

Use Conventional Commits.

Feature

```
feat(user): create user management
```

Bug

```
fix(auth): resolve login issue
```

Documentation

```
docs(api): update API specification
```

Performance

```
perf(report): improve report loading
```

Refactor

```
refactor(service): simplify business logic
```

---

# Pull Request Checklist

Before creating Pull Request

Architecture

- [ ] MVC maintained
- [ ] Clean Architecture maintained

Security

- [ ] Validation added
- [ ] Permissions verified

Performance

- [ ] Batch Processing
- [ ] Cache reviewed

Documentation

- [ ] Documentation updated

Testing

- [ ] Tested successfully

---

# Common Problems

## Problem

Copilot generates duplicate code.

Solution

Ask:

```
Reuse existing modules.

Do not duplicate functionality.
```

---

## Problem

Copilot ignores MVC.

Solution

Specify

```
Follow MVC Architecture.

Use Controller

Service

Repository
```

---

## Problem

Business logic generated inside HTML.

Solution

Specify

```
Business logic belongs only in Service Layer.
```

---

## Problem

Spreadsheet accessed directly from UI.

Solution

Specify

```
Never access Spreadsheet outside Repository.
```

---

## Problem

Large unreadable functions.

Solution

Ask

```
Split into reusable functions.

Maximum 50 lines per function where practical.
```

---

# AI Troubleshooting

When output quality is poor:

1.

Open a new Chat.

2.

Provide context again.

3.

Reference documentation.

4.

Generate smaller modules.

5.

Review generated code before continuing.

---

# Working With Existing Code

Before modifying code

Always ask

```
Analyze existing implementation.

Explain current architecture.

Suggest minimal changes.

Do not rewrite unrelated files.
```

---

# Working With Large Features

Never generate

```
Entire Hospital Management System
```

Instead

Generate

```
Authentication

↓

Dashboard

↓

Patient Module

↓

Appointment Module

↓

Reports

↓

Settings
```

---

# Daily Development Checklist

Before Coding

- Read documentation

- Understand business rules

- Review architecture

- Review existing code

---

During Coding

- Keep functions small

- Reuse existing modules

- Follow coding standards

- Add validation

- Handle errors

---

After Coding

- Review code

- Test functionality

- Update documentation

- Update CHANGELOG

---

# Definition of Done

A feature is complete only when:

Architecture

- MVC maintained

- Clean Architecture maintained

Backend

- Controller completed

- Service completed

- Repository completed

Frontend

- Responsive UI

- Modern SaaS Design

- Dark Mode

Security

- Validation

- Permission Checking

Performance

- Batch Spreadsheet Operations

- Cache reviewed

Quality

- No duplicated code

- Naming standards followed

Testing

- Manual testing completed

- Regression testing completed

Documentation

- Documentation updated

Deployment

- Ready for production

---

# Master Copilot Prompt

Use this prompt whenever starting a new feature.

```
Act as Lead Enterprise Software Architect.

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

Before coding

1. Analyze requirement

2. Review documentation

3. Explain implementation plan

Generate production-ready code only.

Follow project standards.

Never duplicate code.

Never hard-code credentials.

Keep code modular.

Explain modified files.

Provide testing steps.

Suggest improvements.
```

---

# Final Recommendations

Always

✓ Read documentation first

✓ Design before coding

✓ Build one feature at a time

✓ Reuse existing components

✓ Keep architecture clean

✓ Test every feature

✓ Update documentation

✓ Review generated code

Never

✗ Generate an entire enterprise application in one prompt

✗ Skip documentation

✗ Skip testing

✗ Ignore business rules

✗ Ignore project standards

---

# Quick Reference

Development Order

```
Requirement

↓

Analysis

↓

Architecture

↓

Database

↓

UI

↓

Backend

↓

Testing

↓

Documentation

↓

Deployment
```

Copilot Priority

```
.github/copilot-instructions.md

↓

.github/copilot-context.md

↓

.github/copilot-rules.md

↓

docs/

↓

Existing Source Code

↓

Current User Request
```

---

# End of GitHub Copilot Agent Guide

This guide is the official operating manual for GitHub Copilot Agent within the GAS Enterprise Starter Kit.

All generated code should comply with the architecture, standards, and documentation defined in this repository.
