# Documentation Guide

## GAS Enterprise Starter Kit

Version 2.0

---

# Overview

Welcome to the documentation center of the GAS Enterprise Starter Kit.

This documentation provides:

- System architecture guidance
- Development standards
- Security practices
- Deployment procedures
- AI-assisted development workflow
- GitHub Copilot Agent instructions

The goal is to create a maintainable, scalable, and production-ready Google Apps Script application.

---

# Documentation Philosophy

This repository follows:
Understand

↓

Design

↓

Develop

↓

Review

↓

Test

↓

Deploy

↓

Maintain


All developers and AI Agents should follow this workflow.

---

# Getting Started

If you are new to this repository, read documents in this order:

---

## Step 1: Project Understanding

### 01_PROJECT_OVERVIEW.md

Purpose:

Understand:

- Project objectives
- Scope
- Main features
- Target users

---

### 02_SYSTEM_ARCHITECTURE.md

Purpose:

Understand:

- Application architecture
- Data flow
- Components
- Integration design

---

### 03_UI_UX_GUIDELINES.md

Purpose:

Understand:

- Design system
- UI standards
- User experience principles

---

# Step 2: Data and Backend Foundation

### 04_DATABASE_SCHEMA.md

Understand:

- Google Sheets structure
- Data relationships
- Validation rules

---

### 05_API_SPECIFICATION.md

Understand:

- API design
- Request / Response format
- Integration rules

---

### 06_AUTHENTICATION_RBAC.md

Understand:

- Authentication
- Authorization
- Role permissions

---

# Step 3: Development Standards

### 07_CODING_STANDARDS.md

Defines:

- Naming conventions
- Code style
- Best practices
- Documentation rules

---

### 08_COMPONENT_LIBRARY.md

Contains:

- Reusable UI components
- Common patterns
- Shared utilities

---

### 09_FOLDER_STRUCTURE.md

Defines:

- Project organization
- File placement
- Module structure

---

# Step 4: AI Development Documentation

The following documents define how AI Agents should work with this repository.

---

## AI Context

### 30_AI_CONTEXT.md

Purpose:

Provide AI Agents with:

- Project knowledge
- Architecture rules
- Development context
- Important constraints

AI Agents should read this file before development.

---

## GitHub Copilot Agent Guide

### 31_COPILOT_AGENT_GUIDE.md

Purpose:

Learn:

- Copilot workflow
- Agent usage
- Development approach

---

## Prompt Templates

### 32_PROMPT_TEMPLATES.md

Contains:

- Requirement prompts
- Architecture prompts
- Coding prompts
- Review prompts

---

## Security Guide

### 33_SECURITY_GUIDE.md

Defines:

- Security principles
- Authentication rules
- Data protection
- Secure coding practices

---

## Deployment Guide

### 34_DEPLOYMENT_GUIDE.md

Contains:

- Deployment process
- Configuration
- Release checklist

---

## Development Workflow

### 35_DEVELOPMENT_WORKFLOW.md

Defines:

- Development lifecycle
- Branch strategy
- Review process
- Testing workflow

---

## AI Agent Operation Guide

### 36_AI_AGENT_OPERATION_GUIDE.md

Defines:

- AI Agent workflow
- Agent responsibilities
- Interaction standards

---

## Repository Setup Guide

### 37_REPOSITORY_SETUP_GUIDE.md

Contains:

- Initial setup
- Repository configuration
- Developer onboarding

---

# Step 5: GitHub Copilot Agent Resources

---

## Copilot Prompt Library

### 38_COPILOT_PROMPT_LIBRARY.md

A collection of reusable prompts.

Includes:

- Project analysis
- Architecture design
- Feature development
- Debugging
- Code review
- Testing
- Deployment

Recommended for daily development.

---

## Copilot Agent Examples

### 39_COPILOT_AGENT_EXAMPLES.md

Practical examples:

- CRUD development
- Authentication
- Dashboard creation
- API integration
- JHCIS integration
- LINE Messaging API
- Debugging
- Production workflow

---

# Recommended AI Agent Workflow

When using GitHub Copilot Agent:

Read:

.github/copilot-instructions.md

.github/copilot-context.md

.github/copilot-rules.md

↓

Read:

docs/30_AI_CONTEXT.md

↓

Analyze requirement

↓

Design solution

↓

Request approval

↓

Generate code

↓

Review

↓

Test

↓

Update documentation

---

# Repository Documentation Map


docs/

├── 00_AI_INSTRUCTIONS.md

├── 01_PROJECT_OVERVIEW.md

├── 02_SYSTEM_ARCHITECTURE.md

├── 03_UI_UX_GUIDELINES.md

├── 04_DATABASE_SCHEMA.md

├── 05_API_SPECIFICATION.md

├── 06_AUTHENTICATION_RBAC.md

├── 07_CODING_STANDARDS.md

├── 08_COMPONENT_LIBRARY.md

├── 09_FOLDER_STRUCTURE.md

│
├── PROJECT_RULES.md

│
├── 30_AI_CONTEXT.md

├── 31_COPILOT_AGENT_GUIDE.md

├── 32_PROMPT_TEMPLATES.md

├── 33_SECURITY_GUIDE.md

├── 34_DEPLOYMENT_GUIDE.md

├── 35_DEVELOPMENT_WORKFLOW.md

├── 36_AI_AGENT_OPERATION_GUIDE.md

├── 37_REPOSITORY_SETUP_GUIDE.md

├── 38_COPILOT_PROMPT_LIBRARY.md

├── 39_COPILOT_AGENT_EXAMPLES.md

└── 40_AI_AGENT_INITIALIZATION_PROMPT.md

---

# Developer Quick Start

## New Developer

Read:


01

↓

02

↓

07

↓

09

↓

37


---

## AI-Assisted Developer

Read:


30

↓

31

↓

38

↓

39


---

## Before Production Release

Read:


33

↓

34

↓

35


---

# Documentation Maintenance Rules

After adding a new feature:

Update:

- README
- AI Context
- Architecture documentation
- API documentation
- Security documentation

---

# Version History

| Version | Description |
|-|-|
| 2.0 | Added AI Agent documentation system and Copilot workflow |
| 1.0 | Initial documentation structure |

---

# End of Documentation Guide

GAS Enterprise Starter Kit

GitHub Copilot Ready
หลัง Update docs/README.md Version 2.0

โครงสร้าง Documentation ตอนนี้เป็นระบบมากขึ้น:

Developer Journey

New Developer
      |
      ↓
Project Understanding
      |
      ↓
Architecture
      |
      ↓
Coding Standards
      |
      ↓
AI Context
      |
      ↓
Copilot Prompt Library
      |
      ↓
Development
      |
      ↓
Review
      |
      ↓
Deployment

---

## AI Agent Initialization Prompt

### 40_AI_AGENT_INITIALIZATION_PROMPT.md

Purpose:

Initialize GitHub Copilot Agent
before starting development.

Use when:

- Opening repository first time
- Starting new AI session
- Onboarding new developer
- Beginning major feature development


Workflow:

Read documentation

↓

Initialize AI Agent

↓

Confirm understanding

↓

Start development
