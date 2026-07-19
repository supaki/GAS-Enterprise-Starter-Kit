# Contributing Guide

## GAS Enterprise Starter Kit

Version 1.0


---

# Introduction

Thank you for contributing to this project.

This guide explains how developers should contribute code, documentation, and improvements.


---

# Development Philosophy

All contributions should follow:
Quality

Security

Maintainability

Documentation


---

# Before Starting Development

Read:


docs/README.md

docs/30_AI_CONTEXT.md

docs/PROJECT_RULES.md


For AI-assisted development:

Read:


.github/copilot-instructions.md

.github/copilot-context.md

.github/copilot-rules.md


---

# Development Workflow

Follow:


Requirement

↓

Design

↓

Development

↓

Review

↓

Testing

↓

Documentation

↓

Merge


---

# Branch Strategy

Recommended:


main

|

develop

|

feature/*


---

# Branch Naming

Use:


feature/add-user-management

feature/create-dashboard

bugfix/fix-login-error

docs/update-readme


---

# Commit Convention

Use:


type: description


Examples:


feat: add patient module

fix: resolve login issue

docs: update architecture guide

refactor: improve repository layer

security: improve validation


---

# Pull Request Requirements

Every Pull Request should include:

## Description

Explain:

- What changed
- Why changed


## Testing

Explain:

- Test performed
- Expected result


## Documentation

Confirm:

- Documentation updated if required


---

# Code Review Checklist

Reviewer should check:

## Architecture

- Correct layer
- No duplicated logic


## Security

- No exposed secrets
- Validation implemented


## Quality

- Readable code
- Proper comments
- Error handling


---

# AI Generated Code Policy

AI-generated code is allowed.

However:

Developer MUST:

- Review generated code
- Understand implementation
- Verify security
- Test functionality

AI output is not automatically accepted.


---

# Contribution Rules

Never:

- Commit credentials
- Ignore architecture
- Skip testing
- Modify unrelated files


---

# Thank You

Every contribution helps improve this project.
