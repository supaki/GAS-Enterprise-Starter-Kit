<!-- ====================================================================== -->
<!-- File: docs/23_GOOGLE_SHEET_STRUCTURE.md -->
<!-- ====================================================================== -->

# Google Sheet Structure

Version 2.0

---

# Purpose

This document defines the standard database structure using Google Sheets as the primary database for Google Apps Script Enterprise Applications.

The objective is to provide:

- Database consistency
- Easy maintenance
- Clear data relationships
- AI-friendly development
- Migration readiness to SQL databases

---

# Database Concept

Google Sheets acts as:

```
Database Layer

↓

Repository Layer

↓

Service Layer

↓

Application
```

---

# Database Design Principles

Follow:

✓ Structured tables

✓ Fixed schema

✓ Clear relationships

✓ Data validation

✓ Audit tracking

✓ Backup strategy

---

# Spreadsheet Architecture

Recommended structure:

```
Enterprise_App_DB

│

├── Users

├── Roles

├── Permissions

├── UserRoles

├── Settings

├── Master_Data

├── Transactions

├── Logs

└── AuditLogs
```

---

# Sheet Naming Convention

Use:

```
PascalCase
```

Examples:

Correct:

```
Users

PatientRecords

TransactionLogs
```

Avoid:

```
user_data

tbl_users

sheet1
```

---

# Standard System Sheets

---

# 1. Users Sheet

Purpose:

Store user accounts.

Schema:

| Field | Type | Description |
|-|-|-|
| userId | String | Primary Key |
| username | String | Login name |
| passwordHash | String | Encrypted password |
| fullName | String | User name |
| email | String | Email |
| status | Enum | Active/Inactive |
| createdAt | DateTime | Created time |
| updatedAt | DateTime | Updated time |

---

Example:

| userId | username | status |
|-|-|-|
|USR001|admin|ACTIVE|

---

# 2. Roles Sheet

Purpose:

Define system roles.

Schema:

| Field | Type |
|-|-|
| roleId | String |
| roleName | String |
| description | String |

---

Example:

```
ADMIN

MANAGER

STAFF

VIEWER
```

---

# 3. Permissions Sheet

Purpose:

Define available permissions.

Schema:

| Field | Type |
|-|-|
| permissionId | String |
| permissionName | String |
| module | String |
| action | String |

---

Example:

```
users.create

users.delete

reports.export
```

---

# 4. UserRoles Sheet

Purpose:

Many-to-many relationship.

Schema:

| Field | Type |
|-|-|
| id | String |
| userId | FK |
| roleId | FK |

---

Relationship:

```
User

↓

UserRoles

↓

Role
```

---

# 5. Settings Sheet

Purpose:

Application configuration.

Schema:

| Field | Type |
|-|-|
| key | String |
| value | String |
| description | String |

---

Example:

|key|value|
|-|-|
|APP_NAME|Enterprise App|
|TIMEZONE|Asia/Bangkok|

---

# Master Data Pattern

Master data:

Changes rarely.

Examples:

```
Departments

Categories

Statuses

Types
```

---

Structure:

| Field | Type |
|-|-|
| id | String |
| code | String |
| name | String |
| status | String |

---

# Transaction Data Pattern

Transaction data:

Changes frequently.

Examples:

```
Orders

Appointments

Requests
```

---

Structure:

| Field | Type |
|-|-|
| transactionId | String |
| userId | FK |
| status | Enum |
| createdAt | DateTime |
| updatedAt | DateTime |

---

# Audit Fields

Every table should include:

| Field | Purpose |
|-|-|
| createdAt | Creation time |
| createdBy | Creator |
| updatedAt | Last update |
| updatedBy | Editor |

---

Example:

```json
{
"createdBy":"USR001",
"createdAt":"2026-07-19"
}
```

---

# Primary Key Standard

Every table requires:

```
id
```

or:

```
[module]Id
```

Examples:

```
userId

patientId

orderId
```

---

# ID Generation

Recommended:

Format:

```
PREFIX + Running Number
```

Example:

```
USR00001

ORD00001
```

---

Example:

```javascript
function generateId(prefix){

return prefix +
Utilities
.getUuid()
.slice(0,8);

}
```

---

# Foreign Key Standard

Reference another table:

Example:

Users:

```
userId
```

Orders:

```
userId
```

Relationship:

```
Users.userId

↓

Orders.userId
```

---

# Data Type Standard

| Type | Example |
|-|-|
| String | Text |
| Number | 100 |
| Boolean | TRUE |
| Date | 2026-01-01 |
| DateTime | Timestamp |
| Enum | ACTIVE |

---

# Enum Pattern

Avoid:

```
Free text
```

Example:

Bad:

```
active
Active
ACTIVE
```

---

Good:

```
ACTIVE

INACTIVE
```

---

# Data Validation Rules

Google Sheet should use:

- Dropdown
- Required fields
- Data validation
- Protected ranges

---

# Repository Mapping

Example:

Sheet:

```
Users
```

Repository:

```javascript
class UserRepository{


constructor(){

this.sheet =
SpreadsheetApp
.getActive()
.getSheetByName(
"Users"
);

}


}
```

---

# Data Access Rules

Never:

```javascript
SpreadsheetApp
.getActive()
```

inside UI code.

---

Correct:

```
UI

↓

Controller

↓

Service

↓

Repository

↓

Sheet
```

---

# Backup Strategy

Recommended:

Daily:

```
Database_Backup_YYYYMMDD
```

---

Backup includes:

- Structure
- Data
- Version

---

# Migration Ready Design

Although using Sheets:

Design as SQL compatible.

Example:

Google Sheet:

```
Users
```

can migrate to:

```sql
CREATE TABLE users(
user_id VARCHAR(20),
username VARCHAR(100)
);
```

---

# Database Review Checklist

## Structure

- [ ] Sheet names standardized
- [ ] Primary keys created
- [ ] Relationships defined

---

## Data Quality

- [ ] Validation rules added
- [ ] Enum controlled
- [ ] Duplicate prevention

---

## Security

- [ ] Sensitive sheets protected
- [ ] Access controlled
- [ ] Audit enabled

---

# GitHub Copilot Database Prompt

```
Act as Database Architect.

Design Google Sheets database schema.

Requirements:

- Enterprise standard
- Normalized structure
- Primary keys
- Foreign keys
- Validation rules
- Audit fields
- Repository mapping

Prepare:

1. Sheet structure
2. Data dictionary
3. Relationships
4. Sample data
```

---

# Database Improvement Prompt

```
Review this Google Sheets database.

Analyze:

- Data structure
- Performance
- Duplicate data
- Scalability
- Migration readiness

Suggest improvements.
```

---

# Final Database Approval

Process:

```
Requirement

↓

Schema Design

↓

Review

↓

Validation

↓

Implementation

↓

Backup
```

---

# End of Google Sheet Structure
