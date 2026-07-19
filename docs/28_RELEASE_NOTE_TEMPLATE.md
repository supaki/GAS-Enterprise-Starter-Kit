<!-- ====================================================================== -->
<!-- File: docs/28_RELEASE_NOTE_TEMPLATE.md -->
<!-- ====================================================================== -->

# Release Note Template

Version 2.0

---

# Purpose

This document defines the standard format for application release documentation.

The objective is to provide:

- Clear version history
- Transparent changes
- Easier maintenance
- Better team communication
- AI-assisted release management

---

# Release Management Concept

Every release must include:

```
Version

+

Changes

+

Testing

+

Deployment

+

Impact
```

---

# Versioning Standard

Use Semantic Versioning:

```
MAJOR.MINOR.PATCH
```

Example:

```
1.0.0
```

---

# Version Meaning

| Version | Meaning |
|-|-|
| MAJOR | Major architecture change |
| MINOR | New features |
| PATCH | Bug fixes |

---

# Release Types

---

# Major Release

Example:

```
2.0.0
```

Includes:

- Architecture changes
- Major UI redesign
- Database changes

---

# Feature Release

Example:

```
1.5.0
```

Includes:

- New modules
- New functions
- Improvements

---

# Bug Fix Release

Example:

```
1.5.1
```

Includes:

- Error fixes
- Performance improvements

---

# Release Note Structure

Every release should contain:

```
Header

↓

Summary

↓

New Features

↓

Improvements

↓

Bug Fixes

↓

Breaking Changes

↓

Testing

↓

Deployment
```

---

# Release Note Template

```markdown
# Release vX.X.X


Date:

Developer:


## Summary

Describe release purpose.


## New Features

- Feature 1
- Feature 2


## Improvements

- Improvement 1


## Bug Fixes

- Fixed issue


## Breaking Changes

None


## Testing

- Unit test
- User test


## Deployment

Environment:

Production


Status:

Completed
```

---

# Example Release Note

```markdown
# Release v1.2.0


Date:

2026-07-19


## Summary

Added user management module.


## New Features

- User CRUD
- Role management
- Permission control


## Improvements

- Faster dashboard loading


## Bug Fixes

- Fixed login issue


## Testing

Completed


## Deployment

Production
```

---

# Feature Documentation Template

Before releasing feature:

```markdown
# Feature Name


Purpose:


User Flow:


Business Rules:


Database Changes:


API Changes:


UI Changes:


Testing:
```

---

# Database Change Documentation

Required when schema changes.

Template:

```markdown
## Database Change


Table:

Users


Change:

Added field:


Field:

phone


Type:

String
```

---

# API Change Documentation

Template:

```markdown
## API Change


Endpoint:

getUsers()


Change:

Added pagination


Request:

page,size


Response:

data,total
```

---

# UI Change Documentation

Template:

```markdown
## UI Change


Page:

Dashboard


Change:

Added KPI Card


Impact:

Improved visibility
```

---

# Bug Fix Documentation

Template:

```markdown
## Bug Fix


Issue:

Login failed


Cause:

Invalid validation


Solution:

Updated validation logic


Testing:

Passed
```

---

# Deployment Checklist

Before release:

## Code

- [ ] Code reviewed
- [ ] No debug code
- [ ] Version updated

---

## Database

- [ ] Backup completed
- [ ] Schema verified

---

## Testing

- [ ] Feature tested
- [ ] Regression tested
- [ ] User accepted

---

## Deployment

- [ ] Production deployed
- [ ] Smoke test completed
- [ ] Release announced

---

# Git Tag Standard

Use:

```
vX.X.X
```

Example:

```
v1.0.0
```

---

# Git Commit Standard

Format:

```
type(scope): message
```

---

Examples:

Feature:

```
feat(user): add user management
```

Bug:

```
fix(auth): resolve login error
```

Documentation:

```
docs(api): update specification
```

---

# Change Log Structure

File:

```
CHANGELOG.md
```

Format:

```markdown
# Changelog


## v1.2.0

Added:

- User module


Fixed:

- Login bug
```

---

# Release Approval Process

```
Development

↓

Code Review

↓

Testing

↓

Approval

↓

Deployment

↓

Release Note
```

---

# GitHub Copilot Release Prompt

```
Act as Release Manager.

Generate release notes from git changes.

Include:

1. Version
2. Summary
3. New features
4. Improvements
5. Bug fixes
6. Breaking changes
7. Testing
8. Deployment notes

Use professional format.
```

---

# Copilot Change Analysis Prompt

```
Analyze these code changes.

Classify:

- New features
- Bug fixes
- Improvements
- Breaking changes

Generate release documentation.
```

---

# Release Quality Checklist

## Documentation

- [ ] Release note created
- [ ] Changelog updated
- [ ] Version tagged

---

## Technical

- [ ] Deployment successful
- [ ] Backup completed
- [ ] Monitoring active

---

## Communication

- [ ] Users informed
- [ ] Team notified

---

# Final Release Workflow

```
Code Complete

↓

Review

↓

Test

↓

Document

↓

Deploy

↓

Monitor
```

---

# End of Release Note Template
