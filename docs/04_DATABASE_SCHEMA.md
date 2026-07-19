<!-- ====================================================================== -->
<!-- File: docs/04_DATABASE_SCHEMA.md -->
<!-- ====================================================================== -->

# Database Schema

Version 2.0

---

# Purpose

This document defines the database design standard for applications using Google Sheets as the primary database.

The database layer must be designed to support:

- CRUD operations
- Data validation
- Audit tracking
- Scalability
- Reporting
- API integration

---

# Database Concept

Google Sheets is used as a lightweight database.

Architecture:

```text
Application

↓

Repository Layer

↓

Database Service

↓

Google Sheets
```

---

# Database Design Principles

Always:

- Use structured sheets
- Define columns clearly
- Use unique identifiers
- Track creation/update history
- Validate data
- Maintain audit logs

Never:

- Hardcode column positions
- Store secrets
- Mix unrelated data
- Delete important records permanently

---

# Standard Sheet Structure

Every business table should include:

| Column | Type | Required | Description |
|---|---|---|---|
| id | String | Yes | Unique identifier |
| createdAt | DateTime | Yes | Creation timestamp |
| updatedAt | DateTime | Yes | Last update timestamp |
| createdBy | String | Yes | Creator |
| updatedBy | String | Yes | Last updater |
| status | String | Yes | Active/Inactive |

---

# System Sheets

## Users

Purpose:

Store application users.

Structure:

| Field | Type | Description |
|-|-|-|
| id | String | User ID |
| username | String | Login name |
| email | String | Email |
| passwordHash | String | Encrypted password |
| roleId | String | User role |
| status | String | Account status |
| createdAt | Date | Created date |
| updatedAt | Date | Updated date |

---

## Roles

Purpose:

Define user roles.

| Field | Type |
|-|-|
| id | String |
| roleName | String |
| description | String |
| permissions | JSON |
| status | String |

Example:

```json
{
 "users":["read","create"],
 "reports":["read"]
}
```

---

## Permissions

Purpose:

Store access permissions.

| Field | Type |
|-|-|
| id | String |
| module | String |
| action | String |
| description | String |

Example:

```
users.create

patients.read

reports.export
```

---

## Settings

Purpose:

Store system configuration.

| Field | Type |
|-|-|
| id | String |
| key | String |
| value | String |
| description | String |

Example:

```
APP_NAME = Clinic System

THEME = dark
```

---

## Logs

Purpose:

Application logging.

| Field | Type |
|-|-|
| id | String |
| level | String |
| message | String |
| userId | String |
| createdAt | Date |

Levels:

```
INFO

WARNING

ERROR

DEBUG
```

---

## AuditLogs

Purpose:

Track user activities.

| Field | Type |
|-|-|
| id | String |
| userId | String |
| action | String |
| module | String |
| oldValue | JSON |
| newValue | JSON |
| timestamp | Date |

Example:

```
User admin updated patient record
```

---

# Business Table Example

Example:

Patients

| Field | Type | Description |
|-|-|-|
| id | String | Primary Key |
| hn | String | Hospital Number |
| cid | String | Citizen ID |
| name | String | Patient Name |
| birthday | Date | Birth Date |
| phone | String | Telephone |
| status | String | Status |
| createdAt | Date | Created |
| updatedAt | Date | Updated |

---

# Primary Key Standard

Every table must have:

```
id
```

Recommended format:

```
USR-000001

PAT-000001

LOG-000001
```

Generate using:

```javascript
function generateId(prefix){
  return prefix +
    "-" +
    Utilities.getUuid()
      .substring(0,8)
      .toUpperCase();
}
```

---

# Data Access Rules

Never:

```javascript
sheet.getRange(2,3)
```

Avoid column numbers.

---

Use Header Mapping:

Example:

```javascript
const headers = sheet
.getRange(1,1,1,sheet.getLastColumn())
.getValues()[0];


const nameIndex =
headers.indexOf("name");
```

---

# Repository Example

```javascript
class UserRepository {

  constructor(){
    this.sheet =
      SpreadsheetApp
      .getActive()
      .getSheetByName("Users");
  }


  findAll(){

    const data =
    this.sheet
    .getDataRange()
    .getValues();

    return data;
  }


  save(user){

    this.sheet.appendRow([
      user.id,
      user.username,
      user.email
    ]);

  }

}
```

---

# Validation Rules

Before saving:

Check:

- Required fields
- Data type
- Duplicate data
- Permission

Example:

```javascript
function validateUser(user){

 if(!user.email){
   throw new Error(
    "Email is required"
   );
 }

}
```

---

# Performance Rules

Avoid:

```javascript
for(each row){

 sheet.getRange()
 .setValue()

}
```

Use batch:

```javascript
sheet
.getRange()
.setValues(data);
```

---

# Backup Strategy

Recommended:

Daily backup

```
Database_Backup_YYYYMMDD
```

Store:

- Spreadsheet copy
- Export CSV
- Export JSON

---

# Best Practices

✓ Use repository layer

✓ Use header mapping

✓ Use validation

✓ Use audit logs

✓ Use batch operations

✓ Keep schema documented

✓ Never store passwords directly

---

# GitHub Copilot Prompt

Create a database layer following this schema.

Requirements:

- Generate Repository classes.
- Use Google Sheets.
- Use header mapping.
- Add validation.
- Add error handling.
- Add audit logging.
- Do not access Sheets directly from controllers.

---

# Database Checklist

- [ ] All tables documented
- [ ] Primary keys created
- [ ] Audit fields included
- [ ] Validation implemented
- [ ] Repository layer created
- [ ] Backup strategy defined
- [ ] No hardcoded column indexes
