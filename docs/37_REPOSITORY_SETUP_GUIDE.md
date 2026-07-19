<!-- ====================================================================== -->
<!-- File: docs/37_REPOSITORY_SETUP_GUIDE.md -->
<!-- ====================================================================== -->

# Repository Setup Guide

Version 2.0

Enterprise Development Environment Setup Documentation

---

# Purpose

This document defines the standard process for setting up the project repository and development environment.

The objectives are:

- Enable developers to start development quickly
- Standardize environment configuration
- Reduce setup errors
- Support AI-assisted development
- Ensure consistent project structure

This guide is designed for:

- Developers
- GitHub Copilot Agent Users
- Project Maintainers
- System Administrators

---

# Project Overview

## Project Name

GAS Enterprise Starter Kit

---

# Technology Stack

## Frontend

- HTML5
- Tailwind CSS
- JavaScript ES6+

---

## Backend

- Google Apps Script (GAS)

---

## Database

Primary:

- Google Sheets

Optional Integration:

- MySQL Local Database
- REST API
- Node.js Proxy Server

---

## AI Development

Supported:

- GitHub Copilot Agent
- AI Coding Assistant
- Prompt Engineering Workflow

---

# Repository Structure

Recommended structure:

```text id="h2o5c6"
GAS-Enterprise-Starter-Kit/

│
├── .github/

│   ├── copilot-instructions.md

│   ├── copilot-context.md

│   └── copilot-rules.md

│
├── docs/

│   ├── README.md

│   ├── PROJECT_RULES.md

│   ├── 30_AI_CONTEXT.md

│   ├── 31_COPILOT_AGENT_GUIDE.md

│   ├── 32_PROMPT_TEMPLATES.md

│   ├── 33_SECURITY_GUIDE.md

│   ├── 34_DEPLOYMENT_GUIDE.md

│   ├── 35_DEVELOPMENT_WORKFLOW.md

│   ├── 36_AI_AGENT_OPERATION_GUIDE.md

│   └── 37_REPOSITORY_SETUP_GUIDE.md

│
├── src/

│   ├── frontend/

│   ├── backend/

│   ├── services/

│   └── utils/

│
├── tests/

│
├── config/

│
├── README.md

Prerequisites

Before starting development, install:

Required Software
Git

Purpose:

Version control
Repository management

Verify:

git --version
Node.js

Purpose:

Development tools
Build tools
Local utilities

Verify:

node --version
Visual Studio Code

Recommended editor:

VS Code

Recommended extensions:

GitHub Copilot
GitHub Copilot Chat
ESLint
Prettier
Markdown Preview
Google Account

Required for:

Google Apps Script
Google Sheets
Deployment
Clone Repository
Clone Command
git clone <repository-url>

Example:

git clone https://github.com/<organization>/<repository>.git
Enter Project Folder
cd GAS-Enterprise-Starter-Kit
Install Dependencies

If Node.js tools are used:

npm install
Environment Configuration

Create:

config/

└── environment.config
Configuration Categories

Include:

Application Settings
Google Spreadsheet Mapping
API Configuration
Feature Flags
Configuration Rules

Must:

✓ Separate configuration from source code

✓ Document configuration values

✓ Protect sensitive information

Must Not:

✗ Commit secrets

✗ Store passwords in code

✗ Share production configuration

Google Apps Script Setup
Create GAS Project

Steps:

Open Google Apps Script
Create new project
Connect repository
Configure script files
GAS Project Structure

Recommended:

Apps Script Project

├── appsscript.json

├── Code.gs

├── Config.gs

├── Auth.gs

├── Services.gs

├── Utils.gs

└── API.gs
Google Sheets Setup
Create Database Spreadsheet

Required:

Sheet structure
Column mapping
Permission setup
Spreadsheet Configuration

Document:

Spreadsheet ID
Sheet Names
Columns
Data Types

Example:

Users Sheet

id

name

email

role

status
Local Development Setup

Recommended workflow:

VS Code

↓

Git Repository

↓

Google Apps Script

↓

Google Sheets

↓

Testing
Git Configuration

Set user information:

git config --global user.name "Your Name"

git config --global user.email "your@email.com"
Development Branch Setup

Create development branch:

git checkout -b develop
Feature Branch Workflow

Create feature branch:

git checkout -b feature/<feature-name>

Example:

git checkout -b feature/user-authentication
First Commit

Recommended:

git add .

git commit -m "docs: initialize project documentation"
GitHub Copilot Agent Setup

Before using AI Agent:

Verify:

.github/

├── copilot-instructions.md

├── copilot-context.md

└── copilot-rules.md
First AI Agent Prompt

Use:

You are working on GAS Enterprise Starter Kit.

First:

1. Read .github/copilot-instructions.md
2. Read .github/copilot-context.md
3. Read .github/copilot-rules.md
4. Read docs/README.md

Then summarize:

- Project purpose
- Architecture
- Development rules
- Security requirements

Do not write code yet.
Development Environment Checklist
Tools
 Git installed
 Node.js installed
 VS Code installed
 Copilot enabled
Repository
 Repository cloned
 Folder structure verified
 Documentation available
Google Services
 Google Account ready
 GAS project created
 Google Sheets created
 Permissions configured
AI Agent
 Context loaded
 Rules understood
 Prompt workflow ready
Troubleshooting
Problem: Copilot Does Not Understand Project

Solution:

Check:

copilot-context.md exists
docs/README.md exists
Documentation is complete
Problem: GAS Permission Error

Check:

Authorization status
Deployment settings
Google Account permission
Problem: Data Access Error

Check:

Spreadsheet ID
Sheet name
Permission settings
Setup Completion Criteria

Repository is ready when:

 Code repository created
 Documentation loaded
 AI context configured
 Development environment ready
 Google services connected
 First AI Agent session completed
Next Development Steps

After setup:

Review architecture
Define first feature
Create development branch
Use AI planning workflow
Implement
Test
Deploy
End of Repository Setup Guide

│

└── .gitignore
