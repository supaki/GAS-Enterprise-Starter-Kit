<!-- ====================================================================== -->
<!-- File: docs/12_TESTING_GUIDE.md -->
<!-- ====================================================================== -->

# Testing Guide

Version 2.0

---

# Purpose

This document defines the testing strategy for Google Apps Script Enterprise Applications.

The goal is to ensure:

- Correct functionality
- Stable operation
- Security
- Performance
- Maintainability

---

# Testing Strategy

The project follows:

```text
Test Strategy

↓

Test Planning

↓

Test Implementation

↓

Test Execution

↓

Bug Fix

↓

Regression Test

↓

Release
```

---

# Testing Levels

| Level | Purpose |
|-|-|
| Unit Testing | Test individual functions |
| Integration Testing | Test module communication |
| API Testing | Test backend APIs |
| UI Testing | Test user interface |
| Security Testing | Test protection |
| Performance Testing | Test speed |

---

# Testing Architecture

```text
Frontend

↓

API

↓

Controller

↓

Service

↓

Repository

↓

Google Sheets
```

Every layer should be tested independently.

---

# Test Environment

## Development

Purpose:

- Developer testing

---

## Staging

Purpose:

- User acceptance testing

---

## Production

Purpose:

- Monitoring only

---

# Unit Testing

## Purpose

Verify individual functions.

Example:

Function:

```javascript
calculateTotal()
```

Input:

```javascript
[
10,
20,
30
]
```

Expected:

```javascript
60
```

---

# Unit Test Example

```javascript
function testCalculateTotal(){

const result =
calculateTotal(
[
10,
20
]
);


if(result !== 30){

throw new Error(
"Test failed"
);

}

}
```

---

# Repository Testing

Test:

- Create
- Read
- Update
- Delete

Example:

```javascript
function testUserRepository(){

const repo =
new UserRepository();


const user =
{
id:"USR001",
name:"Test"
};


repo.save(user);


const result =
repo.findById(
"USR001"
);


if(!result){

throw new Error(
"User not found"
);

}

}
```

---

# Service Testing

Verify:

- Business rules
- Validation
- Calculation
- Permission

Example:

```javascript
function testUserService(){

const service =
new UserService();


const user =
service.create(
{
name:"John"
}
);


if(!user.id){

throw new Error(
"Invalid user"
);

}

}
```

---

# API Testing

## API Checklist

Every API must test:

- Request validation
- Authentication
- Authorization
- Response format
- Error handling

---

# API Test Example

Request:

```json
{
"name":"John"
}
```

Expected:

```json
{
"success":true
}
```

---

# Response Testing

Verify:

```javascript
response.success

response.message

response.data

response.errors
```

---

# CRUD Testing

Every CRUD module must test:

## Create

Test:

- Valid data
- Missing field
- Duplicate record

---

## Read

Test:

- Existing record
- Empty result
- Permission

---

## Update

Test:

- Update success
- Invalid ID
- Permission denied

---

## Delete

Test:

- Delete success
- Confirmation
- Audit log

---

# Authentication Testing

Test:

## Login

Cases:

| Case | Expected |
|-|-|
| Correct password | Success |
| Wrong password | Error |
| Disabled user | Block |
| Missing user | Error |

---

# RBAC Testing

Example:

Admin:

```
users.create
users.delete
reports.export
```

Staff:

```
users.read
```

Test:

```text
Admin

Allow

Delete User


Staff

Deny

Delete User
```

---

# Security Testing

Check:

## Authentication

- Session validation
- Expiration

---

## Authorization

- Permission checking
- Role validation

---

## Input Validation

Prevent:

- Empty input
- Invalid format
- Injection

---

## Data Protection

Verify:

- No password exposure
- No API keys in code
- No sensitive logs

---

# UI Testing

Check:

## Responsive

Devices:

- Mobile
- Tablet
- Desktop

---

## Components

Verify:

- Button
- Form
- Modal
- Table
- Navigation

---

# UI Checklist

| Item | Test |
|-|-|
| Layout | Pass |
| Navigation | Pass |
| Form validation | Pass |
| Loading | Pass |
| Error message | Pass |
| Dark mode | Pass |

---

# Browser Testing

Test:

Chrome

Edge

Firefox

Mobile Browser

---

# Performance Testing

Measure:

- Page loading
- API response
- Spreadsheet operations

---

# Performance Rules

Avoid:

```javascript
for(row){

SpreadsheetApp
.getRange()

}
```

Use:

```javascript
getValues()

setValues()
```

---

# Load Testing

Test:

- Large data
- Multiple users
- Large reports

---

# Regression Testing

Before release:

Retest existing features.

Example:

New Feature:

User Module

Check:

- Login
- Dashboard
- Reports
- Permission

---

# Bug Report Template

```markdown
# Bug Report

## Title

## Environment

## Steps

1.

2.

3.


## Expected Result


## Actual Result


## Severity

Low
Medium
High
Critical

## Solution
```

---

# Test Case Template

```markdown
# Test Case

Feature:

Scenario:

Input:

Expected:

Actual:

Status:
```

---

# GitHub Copilot Testing Prompt

```
Act as QA Engineer.

Analyze this application.

Generate:

- Unit test cases
- Integration test cases
- API test cases
- Security test cases
- UI test cases
- Performance checklist

Find possible bugs.
```

---

# Final Testing Checklist

## Functional

- [ ] CRUD works
- [ ] API works
- [ ] Forms validated

## Security

- [ ] Authentication tested
- [ ] RBAC tested
- [ ] Input protected

## UI

- [ ] Responsive
- [ ] Accessible
- [ ] Dark mode

## Performance

- [ ] Cache optimized
- [ ] Spreadsheet optimized

## Release

- [ ] Regression completed
- [ ] Documentation updated

---

# End of Testing Guide
