<!-- ====================================================================== -->
<!-- File: docs/18_USER_FLOW.md -->
<!-- ====================================================================== -->

# User Flow

Version 2.0

---

# Purpose

This document defines user interaction flows for GAS Enterprise Applications.

The objective is to create:

- Clear user journeys
- Consistent user experience
- Reduced user errors
- Better system usability

---

# User Flow Concept

User Flow describes:

```
User Goal

↓

User Action

↓

System Response

↓

Next Action
```

---

# User Flow Design Principles

The system should:

✓ Minimize user steps

✓ Provide clear feedback

✓ Prevent mistakes

✓ Show meaningful messages

✓ Support different user roles

---

# Application User Types

Default roles:

| Role | Description |
|-|-|
| Admin | System administrator |
| Manager | Business manager |
| Staff | Operational user |
| Viewer | Read-only user |

---

# Main Application Flow

```text
Open Application

↓

Authentication Check

↓

Login

↓

Load User Profile

↓

Load Permission

↓

Show Dashboard

↓

Use Features

↓

Logout
```

---

# Authentication Flow

## Login Process

```text
User

↓

Enter Username / Password

↓

Submit Login

↓

Validate Input

↓

Check User

↓

Verify Password

↓

Create Session

↓

Load Permission

↓

Dashboard
```

---

# Login User Flow

## Step 1: Login Screen

Display:

- Username
- Password
- Login Button

---

## Step 2: Validation

Check:

- Required fields
- Format
- Account status

---

## Step 3: Authentication

System checks:

```
Users Sheet

↓

User Record

↓

Password Hash

↓

Status
```

---

## Step 4: Success

System:

- Create session
- Record login log
- Redirect dashboard

---

## Step 5: Failed Login

Display:

```
Invalid username or password
```

Record:

```
Failed Login Attempt
```

---

# Dashboard Flow

```text
Login Success

↓

Dashboard

↓

View Summary

↓

Select Module

↓

Perform Action
```

---

# Dashboard User Experience

Components:

```
Header

↓

KPI Cards

↓

Charts

↓

Recent Activities

↓

Quick Actions
```

---

# CRUD User Flow

General CRUD pattern:

```text
List

↓

Search

↓

Select Record

↓

View Detail

↓

Create/Edit/Delete

↓

Confirm

↓

Save

↓

Refresh Data
```

---

# Create Data Flow

Example:

Create User

```text
Click Create

↓

Open Form

↓

Enter Data

↓

Validate

↓

Submit

↓

Save Database

↓

Create Audit Log

↓

Show Success Message
```

---

# Update Data Flow

```text
Select Record

↓

Click Edit

↓

Load Existing Data

↓

Modify

↓

Validate

↓

Update Database

↓

Record Change

↓

Show Result
```

---

# Delete Data Flow

```text
Select Record

↓

Click Delete

↓

Show Confirmation

↓

Confirm

↓

Check Permission

↓

Delete / Disable

↓

Create Audit Log

↓

Notify User
```

---

# Search Flow

```text
User Enter Keyword

↓

Debounce Input

↓

Send API Request

↓

Search Repository

↓

Return Result

↓

Update Table
```

---

# Report Flow

```text
User Select Report

↓

Select Filter

↓

Validate Criteria

↓

Load Data

↓

Process

↓

Display Chart/Table

↓

Export
```

---

# Notification Flow

```text
System Event

↓

Create Notification

↓

Store Notification

↓

Send To User

↓

User Reads

↓

Mark As Read
```

---

# Permission Flow

```text
User Request Action

↓

Check Session

↓

Get Role

↓

Check Permission

↓

Allow

OR

Deny
```

---

# Permission Example

User:

```
Staff
```

Action:

```
Delete User
```

Check:

```
users.delete
```

Result:

```
Access Denied
```

---

# Error Flow

All errors follow:

```text
Error Occurs

↓

Capture Error

↓

Log System Error

↓

Return Safe Message

↓

Show User Notification
```

---

# Error Message Standard

Good:

```
Unable to save data.
Please try again.
```

Bad:

```
Exception:
NullPointerError at line 152
```

---

# Loading Flow

For every async action:

```text
User Click

↓

Show Loading

↓

Process Request

↓

Hide Loading

↓

Show Result
```

---

# Empty State Flow

When no data:

```text
Search Result

↓

No Data Found

↓

Show Empty State

↓

Suggest Action
```

Example:

```
No users found

Create your first user
```

---

# Approval Workflow

For processes requiring approval:

```text
Create Request

↓

Pending

↓

Review

↓

Approve / Reject

↓

Update Status

↓

Notify User
```

---

# Status Management

Recommended status:

| Status | Meaning |
|-|-|
| Draft | Not completed |
| Pending | Waiting |
| Approved | Accepted |
| Rejected | Declined |
| Active | Available |
| Inactive | Disabled |

---

# User Flow Documentation Template

Use for new features:

```markdown
# Feature Name


## User Goal


## User Role


## Starting Point


## Steps


## System Response


## Error Cases


## Completion Criteria
```

---

# Example User Flow

Feature:

User Management

```
Admin Login

↓

Dashboard

↓

User Management

↓

Click Add User

↓

Fill Form

↓

Save

↓

System Validates

↓

Create User

↓

Show Success
```

---

# UX Improvement Checklist

Before release:

## User Experience

- [ ] User goal is clear
- [ ] Steps are minimized
- [ ] Feedback exists
- [ ] Errors are understandable

---

## Interaction

- [ ] Loading state exists
- [ ] Confirmation exists
- [ ] Success message exists

---

## Security

- [ ] Permission checked
- [ ] Sensitive action confirmed

---

# GitHub Copilot UX Prompt

```
Act as Senior UX Designer.

Analyze this feature.

Create:

- User journey
- User flow
- Screen transitions
- User actions
- System responses
- Error scenarios

Optimize for usability.
```

---

# AI Agent User Flow Prompt

```
Before developing this feature:

Create complete user flow documentation.

Include:

1. User roles
2. User journey
3. Screen flow
4. Data flow
5. Permission flow
6. Error handling flow

Do not generate code yet.
```

---

# Final User Flow Review

Before implementation:

```
User Flow Review

↓

UX Approval

↓

UI Design

↓

Development

↓

Testing
```

---

# End of User Flow
