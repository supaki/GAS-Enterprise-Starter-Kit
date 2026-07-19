<!-- ====================================================================== -->
<!-- File: docs/33_SECURITY_GUIDE.md -->
<!-- ====================================================================== -->

# Security Guide

Version 2.0

Enterprise Application Security Documentation

---

# Purpose

This document defines security standards, practices, and implementation guidelines for this project.

The objectives are:

- Protect application resources
- Prevent unauthorized access
- Secure user data
- Maintain auditability
- Reduce security risks
- Support production readiness

This guide is designed for:

- Developers
- GitHub Copilot Agent
- System Administrators
- Security Reviewers
- Project Maintainers

---

# Security Principles

The project follows these principles:

## 1. Least Privilege

Users and systems should receive only the minimum permissions required.

Rules:

- Do not grant unnecessary roles
- Restrict sensitive operations
- Review permissions regularly

---

## 2. Defense in Depth

Security must exist in multiple layers.

Layers:

```text
User Authentication

↓

Authorization

↓

Input Validation

↓

Business Rules

↓

Data Protection

↓

Audit Logging

. Secure by Design

Security must be considered during:

Requirement Analysis
Architecture Design
Development
Testing
Deployment
Security Architecture
User

↓

Authentication

↓

Authorization

↓

Application Layer

↓

Business Logic

↓

Data Access Layer

↓

Database

↓

Audit Log
Authentication Security
Purpose

Verify user identity before allowing access.

Authentication Requirements

The system must support:

User Identification
Session Management
Account Status Checking
Logout
Session Expiration
Authentication Flow
User Login

↓

Verify Identity

↓

Check Account Status

↓

Load User Role

↓

Create Session

↓

Allow Access
Authentication Rules
Must

✓ Validate user identity

✓ Check account status

✓ Record login activity

✓ Expire inactive sessions

Must Not

✗ Store passwords in source code

✗ Trust client-side authentication only

✗ Skip identity verification

Authorization Security
Purpose

Control what users can access.

Authorization Model
User

↓

Role

↓

Permission

↓

Module

↓

Action
Permission Types

Supported actions:

Action	Description
View	Read information
Create	Create data
Update	Modify data
Delete	Remove data
Approve	Approve workflow
Export	Export information
Manage	System administration
RBAC Security
Role Based Access Control

Structure:

Users

↓

Roles

↓

Permissions

↓

Resources
RBAC Rules
Must

✓ Check permission before action

✓ Maintain permission records

✓ Review role assignment

✓ Log permission changes

Must Not

✗ Hard-code permissions

✗ Allow hidden admin access

✗ Bypass authorization

Input Validation Security

All external inputs must be validated.

Sources:

User Forms
API Requests
URL Parameters
Imported Files
External Data
Validation Rules

Check:

Validation	Example
Required	Name required
Type	Number/Text
Format	Email
Length	Max characters
Range	Date range
Business Rule	Status transition
Data Sanitization

Before storing data:

Remove invalid characters
Normalize format
Validate content
Prevent malicious input
Cross Site Scripting (XSS) Prevention

Protection:

Escape output
Validate input
Avoid unsafe HTML rendering
Sanitize user content
Injection Prevention

Prevent:

Formula Injection
Script Injection
Data Manipulation

Rules:

Validate all inputs
Avoid dynamic execution
Use controlled data mapping
Data Protection
Sensitive Data Categories

Examples:

Personal Information
Account Information
Confidential Records
System Configuration
Data Protection Rules
Storage

Must:

✓ Restrict access

✓ Protect configuration

✓ Backup securely

Must Not:

✗ Store secrets in code

✗ Expose sensitive fields

Data Masking

Sensitive information should be masked.

Examples:

Email:

supakit@example.com

↓

s******@example.com

Phone:

0812345678

↓

081****678
Export Security

Before exporting data:

Check:

User permission
Data sensitivity
Export purpose
Audit requirement
Secrets Management
Protected Information

Examples:

API Keys
Tokens
Passwords
Credentials
Configuration Secrets
Secret Management Rules

Must:

✓ Use secure storage

✓ Limit access

✓ Rotate credentials

Must Not:

✗ Commit secrets to GitHub

✗ Put keys inside JavaScript files

✗ Share credentials publicly

Google Apps Script Security

Security considerations:

Deployment Permission
Execution Identity
OAuth Scope
PropertiesService
Spreadsheet Access
GAS Security Checklist

Review:

 Web App access setting
 User permission
 Script authorization
 Sensitive configuration
 Deployment version
Google Sheets Security

Google Sheets is used as database.

Security requirements:

Restrict sharing
Protect sheets
Limit editors
Backup data
Monitor changes
Audit Logging

All important actions should be recorded.

Audit Log Structure

Example:

Field	Description
logId	Log ID
userId	User
action	Activity
module	Feature
timestamp	Time
result	Success/Fail
Audit Events

Record:

Login
Logout
Create Data
Update Data
Delete Data
Export Data
Permission Change
Security Monitoring

Monitor:

Failed Login
Suspicious Activity
Permission Changes
Data Export
System Errors
Security Review Process

Before Release:

Architecture Review

↓

Code Review

↓

Security Testing

↓

Permission Review

↓

Production Approval
Security Testing Checklist
Authentication
 Login tested
 Logout tested
 Session expiration tested
Authorization
 Role tested
 Permission tested
 Restricted access tested
Data
 Sensitive data protected
 Export controlled
 Logs reviewed
Application
 Input validation tested
 Error handling reviewed
 Configuration secured
Security Incident Response
Incident Process
Detect

↓

Analyze

↓

Contain

↓

Fix

↓

Recover

↓

Prevent
Incident Classification
Level	Description
Critical	Data breach / System compromise
High	Major security impact
Medium	Limited impact
Low	Minor issue
Security Maintenance

Regular activities:

Review permissions
Update documentation
Check vulnerabilities
Review logs
Improve controls
AI Agent Security Rules

GitHub Copilot Agent must:

✓ Follow security guidelines

✓ Review permissions

✓ Validate inputs

✓ Avoid exposing secrets

✓ Protect sensitive data

✓ Explain security impact

AI Agent must not:

✗ Generate insecure shortcuts

✗ Store credentials

✗ Disable security checks

✗ Ignore authorization

Security Checklist Before Production

Final approval:

 Authentication completed
 Authorization completed
 RBAC reviewed
 Validation completed
 Sensitive data protected
 Audit logging enabled
 Security testing completed
 Documentation updated
End of Security Guide
