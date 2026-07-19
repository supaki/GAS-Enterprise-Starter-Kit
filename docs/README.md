# Documentation Guide

## GAS Enterprise Starter Kit

Version 2.1

---

# Overview

Welcome to the documentation center of the GAS Enterprise Starter Kit.

This documentation provides:

- System architecture guidance
- Development standards
- Security practices
- Deployment procedures
- AI-assisted development workflow
- GitHub Copilot Agent operating framework

The goal is to create maintainable, scalable, secure, and production-ready Google Apps Script applications.

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


All developers and AI Agents must follow this workflow.

---

# Documentation Reading Strategy

There are two documentation paths:

---

# Developer Path

For developers:


Project Understanding

↓

Architecture

↓

Coding Standards

↓

Development Workflow

↓

Implementation

↓

Deployment


---

# AI Agent Path

For GitHub Copilot Agent:


AI Instructions

↓

Project Context

↓

Repository Rules

↓

AI Knowledge Base

↓

Prompt Library

↓

Examples

↓

Initialization

↓

Development


---

# Step 1: Project Understanding

## 01_PROJECT_OVERVIEW.md

Purpose:

Understand:

- Project objectives
- Scope
- Features
- Target users

---

## 02_SYSTEM_ARCHITECTURE.md

Purpose:

Understand:

- Application architecture
- Components
- Data flow
- Integration design

---

## 03_UI_UX_GUIDELINES.md

Purpose:

Understand:

- Design system
- UI standards
- User experience principles

---

# Step 2: Data and Backend Foundation

## 04_DATABASE_SCHEMA.md

Defines:

- Google Sheets structure
- Data relationships
- Validation rules

---

## 05_API_SPECIFICATION.md

Defines:

- API contracts
- Request / Response format
- Integration rules

---

## 06_AUTHENTICATION_RBAC.md

Defines:

- Authentication
- Authorization
- Role permissions

---

# Step 3: Development Standards

## 07_CODING_STANDARDS.md

Defines:

- Coding style
- Naming conventions
- Best practices
- Documentation rules

---

## 08_COMPONENT_LIBRARY.md

Contains:

- UI components
- Reusable patterns
- Common utilities

---

## 09_FOLDER_STRUCTURE.md

Defines:

- Repository organization
- Module structure
- File placement

---

# Step 4: AI Development Documentation

This section defines how AI Agents should understand and work with this repository.

---

# AI Knowledge Layer

## 30_AI_CONTEXT.md

Purpose:

Provide AI Agents with:

- Project knowledge
- Architecture understanding
- Technical constraints
- Development context

This is the main AI knowledge base.

---

# Copilot Agent Guide

## 31_COPILOT_AGENT_GUIDE.md

Purpose:

Explain:

- Copilot workflow
- Agent capabilities
- AI collaboration model

---

# Prompt Templates

## 32_PROMPT_TEMPLATES.md

Contains:

- Requirement prompts
- Design prompts
- Coding prompts
- Review prompts

---

# Security Guide

## 33_SECURITY_GUIDE.md

Defines:

- Security principles
- Data protection
- Authentication rules
- Secure coding practices

---

# Deployment Guide

## 34_DEPLOYMENT_GUIDE.md

Contains:

- Deployment workflow
- Configuration
- Production checklist

---

# Development Workflow

## 35_DEVELOPMENT_WORKFLOW.md

Defines:

- Development lifecycle
- Review process
- Testing workflow

---

# AI Agent Operation Guide

## 36_AI_AGENT_OPERATION_GUIDE.md

Defines:

- AI Agent responsibilities
- Collaboration workflow
- Operating standards

---

# Repository Setup Guide

## 37_REPOSITORY_SETUP_GUIDE.md

Contains:

- Initial setup
- Repository configuration
- Developer onboarding

---

# Step 5: GitHub Copilot Agent Resources

---

# Copilot Prompt Library

## 38_COPILOT_PROMPT_LIBRARY.md

Purpose:

Provide reusable prompts for daily development.

Includes:

- Requirement analysis
- Architecture design
- Feature development
- Debugging
- Code review
- Testing
- Deployment

---

# Copilot Agent Examples

## 39_COPILOT_AGENT_EXAMPLES.md

Purpose:

Demonstrate real development scenarios.

Examples:

- CRUD systems
- Authentication
- Dashboard development
- API integration
- JHCIS integration
- LINE Messaging API
- Production workflow

---

# AI Agent Initialization Prompt

## 40_AI_AGENT_INITIALIZATION_PROMPT.md

Purpose:

Initialize GitHub Copilot Agent before development.

This prompt helps AI understand:

- Repository structure
- Architecture
- Development rules
- Security requirements
- Workflow expectations


Recommended usage:


Open Repository

↓

Run Initialization Prompt

↓

AI Reviews Documentation

↓

AI Confirms Understanding

↓

Start Development


Use when:

- Opening repository first time
- Starting a new Copilot Agent session
- Onboarding developers
- Starting major features

---

# AI Agent Development Workflow

Recommended sequence:

Read AI Instructions

.github/copilot-instructions.md

↓

Load Project Context

.github/copilot-context.md

↓

Apply Repository Rules

.github/copilot-rules.md

↓

Understand Project Knowledge

docs/30_AI_CONTEXT.md

↓

Initialize Agent

docs/40_AI_AGENT_INITIALIZATION_PROMPT.md

↓

Start Development

---

# Repository Documentation Map


docs/

README.md

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

PROJECT_RULES.md

30_AI_CONTEXT.md

31_COPILOT_AGENT_GUIDE.md

32_PROMPT_TEMPLATES.md

33_SECURITY_GUIDE.md

34_DEPLOYMENT_GUIDE.md

35_DEVELOPMENT_WORKFLOW.md

36_AI_AGENT_OPERATION_GUIDE.md

37_REPOSITORY_SETUP_GUIDE.md

38_COPILOT_PROMPT_LIBRARY.md

39_COPILOT_AGENT_EXAMPLES.md

40_AI_AGENT_INITIALIZATION_PROMPT.md

CHANGELOG.md

CONTRIBUTING.md

FAQ.md


---

# Quick Start Guide

## New Developer

Read:


README.md

↓

01_PROJECT_OVERVIEW.md

↓

02_SYSTEM_ARCHITECTURE.md

↓

07_CODING_STANDARDS.md

↓

37_REPOSITORY_SETUP_GUIDE.md


---

## AI-Assisted Developer

Read:


.github/copilot-instructions.md

↓

.github/copilot-context.md

↓

.github/copilot-rules.md

↓

30_AI_CONTEXT.md

↓

40_AI_AGENT_INITIALIZATION_PROMPT.md

↓

38_COPILOT_PROMPT_LIBRARY.md


---

## Before Production Release

Read:


33_SECURITY_GUIDE.md

↓

34_DEPLOYMENT_GUIDE.md

↓

35_DEVELOPMENT_WORKFLOW.md


---

# Documentation Maintenance Rules

After adding or changing features:

Update:

- README
- AI Context
- Architecture Documentation
- API Documentation
- Security Documentation

Documentation must always reflect the current implementation.

---

# Version History

| Version | Description |
|-|-|
| 2.1 | Added AI Agent Initialization Prompt workflow |
| 2.0 | Added AI Agent documentation system and Copilot workflow |
| 1.0 | Initial documentation structure |

---

# End of Documentation Guide

GAS Enterprise Starter Kit

GitHub Copilot Ready
