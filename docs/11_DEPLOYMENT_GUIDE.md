<!-- ====================================================================== -->
<!-- File: docs/11_DEPLOYMENT_GUIDE.md -->
<!-- ====================================================================== -->

# Deployment Guide

Version 2.0

---

# Purpose

This document defines the deployment process for Google Apps Script Web Applications.

The objective is to ensure:

- Stable deployment
- Secure configuration
- Version control
- Easy maintenance
- Production readiness

---

# Deployment Architecture

```text
User Browser

↓

Google Apps Script Web App

↓

HTML Service

↓

Apps Script Backend

↓

Google Sheets Database
```

---

# Deployment Environment

## Development

Purpose:

- Coding
- Testing
- Debugging

Configuration:

```
Environment = DEVELOPMENT
```

---

## Testing / Staging

Purpose:

- User testing
- Feature validation

Configuration:

```
Environment = STAGING
```

---

## Production

Purpose:

- Real users

Configuration:

```
Environment = PRODUCTION
```

---

# Pre-Deployment Checklist

Before deployment:

## Documentation

- [ ] Documentation updated
- [ ] API documented
- [ ] Database schema updated

---

## Code Quality

- [ ] No TODO
- [ ] No debug code
- [ ] No test data
- [ ] Error handling completed
- [ ] Code reviewed

---

## Security

- [ ] Secrets removed from source code
- [ ] Script Properties configured
- [ ] RBAC tested
- [ ] Permission reviewed

---

## Database

- [ ] Google Sheet backup created
- [ ] Schema verified
- [ ] Data validation completed

---

# Google Apps Script Setup

---

# Step 1: Create Project

Open:

```
https://script.google.com
```

Create:

```
GAS Enterprise Application
```

---

# Step 2: Enable V8 Runtime

Apps Script:

```
Project Settings

↓

Enable V8 Runtime
```

---

# Step 3: Configure Time Zone

Recommended:

```
Asia/Bangkok
```

---

# Step 4: Add Script Properties

Navigate:

```
Project Settings

↓

Script Properties
```

Example:

| Key | Value |
|-|-|
| APP_NAME | Enterprise App |
| ENVIRONMENT | PRODUCTION |
| SPREADSHEET_ID | xxx |
| LOG_LEVEL | INFO |

---

# Configuration Example

Config.gs

```javascript
const CONFIG = {

APP_NAME:
PropertiesService
.getScriptProperties()
.getProperty(
"APP_NAME"
),

ENVIRONMENT:
PropertiesService
.getScriptProperties()
.getProperty(
"ENVIRONMENT"
)

};
```

---

# Google Sheet Preparation

Before production:

Create:

```
Users

Roles

Permissions

Settings

Logs

AuditLogs
```

Verify:

- Header names
- Data types
- Permissions

---

# Web App Deployment

Steps:

```
Deploy

↓

New Deployment

↓

Select Web App

↓

Execute as

Me

↓

Who has access

According to requirement

↓

Deploy
```

---

# Access Settings

Options:

## Only Myself

Development

---

## Anyone within Organization

Internal System

---

## Anyone

Public Application

---

# Version Management

Never modify production directly.

Workflow:

```text
Development

↓

Testing

↓

Version Release

↓

Production
```

---

# Release Process

## Version Naming

Format:

```
vMAJOR.MINOR.PATCH
```

Example:

```
v1.0.0

v1.2.0

v1.2.1
```

---

# Release Notes

Example:

```markdown
# Release v1.1.0

Date:
2026-07-19


New Features

- User dashboard
- Report export


Bug Fixes

- Login issue fixed
```

---

# Backup Strategy

---

## Spreadsheet Backup

Recommended:

Daily

Format:

```
Database_Backup_YYYYMMDD
```

---

## Code Backup

Use:

- GitHub Repository
- Version History

---

# Rollback Strategy

If production fails:

1. Identify issue
2. Disable deployment
3. Restore previous version
4. Verify database
5. Notify users

---

# Monitoring

Monitor:

- Errors
- Execution time
- API failures
- User activities

---

# Logging

Use:

```javascript
Logger.log()
```

and store:

```
Logs Sheet
```

---

# Production Security Checklist

## Authentication

- [ ] Login works
- [ ] Session expires
- [ ] Password protected

---

## Authorization

- [ ] Roles verified
- [ ] Permission checked
- [ ] Unauthorized access blocked

---

## Data Protection

- [ ] No secrets exposed
- [ ] Input validated
- [ ] Output sanitized

---

# Performance Checklist

Before release:

- [ ] CacheService used
- [ ] Spreadsheet calls optimized
- [ ] Large tables paginated
- [ ] Images optimized
- [ ] Frontend loading optimized

---

# Deployment Troubleshooting

---

## Problem

Web App cannot load

Check:

- Deployment permission
- doGet function
- HTML file name

---

## Problem

Permission Error

Check:

- OAuth authorization
- User permission
- Script settings

---

## Problem

Slow Response

Check:

- Spreadsheet operations
- Missing cache
- Large data loading

---

# GitHub Copilot Deployment Review Prompt

```
Act as DevOps Engineer.

Review this Google Apps Script project before deployment.

Check:

- Configuration
- Security
- Performance
- Versioning
- Backup
- Production readiness

Generate deployment checklist.
```

---

# Final Production Checklist

## Application

- [ ] Works correctly
- [ ] Responsive
- [ ] Secure
- [ ] Documented

## Code

- [ ] Version tagged
- [ ] Reviewed
- [ ] No debug code

## Database

- [ ] Backup completed
- [ ] Schema verified

## Deployment

- [ ] Web App deployed
- [ ] Permissions tested
- [ ] Users notified

---

# End of Deployment Guide
