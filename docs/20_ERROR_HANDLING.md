<!-- ====================================================================== -->
<!-- File: docs/20_ERROR_HANDLING.md -->
<!-- ====================================================================== -->

# Error Handling

Version 2.0

---

# Purpose

This document defines the standard error handling strategy for Google Apps Script Enterprise Applications.

The objective is to ensure:

- Stable application behavior
- Clear user communication
- Easy debugging
- Secure error management
- Consistent error responses

---

# Error Handling Principles

The application must:

✓ Detect errors early

✓ Provide meaningful messages

✓ Log technical details

✓ Protect sensitive information

✓ Recover gracefully

---

# Error Handling Architecture

```text
User Action

↓

Frontend Validation

↓

API Controller

↓

Service Layer

↓

Repository

↓

Database

↓

Error Handler

↓

Response
```

---

# Error Categories

| Category | Description |
|-|-|
| Validation Error | Invalid user input |
| Authentication Error | Login failure |
| Authorization Error | Permission denied |
| Business Error | Rule violation |
| Database Error | Data operation failure |
| System Error | Unexpected failure |

---

# Error Classification

---

# 1. Validation Error

Example:

User does not enter email.

Response:

```json
{
"success":false,
"code":"VALIDATION_ERROR",
"message":"Email is required"
}
```

---

# 2. Authentication Error

Example:

Wrong password.

Response:

```json
{
"success":false,
"code":"AUTH_ERROR",
"message":"Invalid username or password"
}
```

---

# 3. Authorization Error

Example:

User tries restricted action.

Response:

```json
{
"success":false,
"code":"FORBIDDEN",
"message":"You do not have permission"
}
```

---

# 4. Business Error

Example:

Cannot approve completed request.

Response:

```json
{
"success":false,
"code":"BUSINESS_ERROR",
"message":"Invalid status transition"
}
```

---

# 5. System Error

Example:

Unexpected exception.

Response:

```json
{
"success":false,
"code":"SYSTEM_ERROR",
"message":"System error occurred"
}
```

---

# Standard Error Response

All APIs must return:

```json
{
"success":false,
"code":"",
"message":"",
"data":null,
"errors":[]
}
```

---

# Error Code Standard

Format:

```
MODULE_ERROR_TYPE
```

Example:

```
USER_VALIDATION_ERROR

AUTH_LOGIN_ERROR

REPORT_EXPORT_ERROR
```

---

# Error Code Table

| Code | Meaning |
|-|-|
| VALIDATION_ERROR | Input invalid |
| AUTH_ERROR | Authentication failed |
| FORBIDDEN | Permission denied |
| NOT_FOUND | Data not found |
| DUPLICATE | Duplicate data |
| DATABASE_ERROR | Database failure |
| SYSTEM_ERROR | Unknown error |

---

# Backend Error Handler

Create centralized handler:

Example:

```javascript
class ErrorHandler {


static handle(error){

Logger.log(
error.message
);


return {

success:false,

code:
"SYSTEM_ERROR",

message:
"System error occurred",

errors:[]

};

}


}
```

---

# Controller Error Handling

Example:

```javascript
function createUser(data){

try{

const service =
new UserService();


return {

success:true,

data:
service.create(data)

};


}catch(error){


return ErrorHandler
.handle(error);


}

}
```

---

# Service Layer Errors

Business errors should be clear.

Example:

```javascript
if(
user.status==="INACTIVE"
){

throw new Error(
"Inactive user cannot login"
);

}
```

---

# Repository Errors

Database errors:

Example:

```javascript
try{

sheet.appendRow(data);

}

catch(error){

throw new Error(
"DATABASE_ERROR"
);

}
```

---

# Frontend Error Handling

Frontend must:

- Display user friendly message
- Stop invalid action
- Provide recovery option

---

# Toast Error Example

```javascript
showToast(
"Unable to save data",
"error"
);
```

---

# Form Error Example

Display:

```
Email

[____________]

❌ Invalid email format
```

---

# Loading Error Flow

```text
Start Loading

↓

API Request

↓

Success

OR

Error

↓

Hide Loading

↓

Show Message
```

---

# Network Error Handling

Example:

```javascript
google.script.run
.withSuccessHandler(
success
)
.withFailureHandler(
error
)
.getUsers();
```

---

# Error Logging Strategy

Log:

✓ User ID

✓ Action

✓ Module

✓ Timestamp

✓ Error Code

✓ Error Message

---

# Do Not Log

Never store:

✗ Password

✗ Token

✗ API Key

✗ Sensitive personal data

---

# Error Log Structure

Sheet:

```
Logs
```

Fields:

| Field | Description |
|-|-|
| id | Log ID |
| level | ERROR |
| module | Module name |
| action | Action |
| message | Error |
| userId | User |
| timestamp | Time |

---

# Debug Workflow

When error occurs:

```text
Receive Error

↓

Check User Message

↓

Check Log

↓

Identify Layer

↓

Fix Root Cause

↓

Test

↓

Deploy
```

---

# Debug Priority

Check:

1. Frontend
2. API
3. Controller
4. Service
5. Repository
6. Database

---

# Error Prevention Strategy

Before production:

Implement:

- Validation
- Permission check
- Exception handling
- Logging
- Monitoring

---

# Common GAS Errors

---

## Authorization Error

Cause:

Missing permission.

Solution:

Check:

- Deployment settings
- OAuth permission

---

## Execution Timeout

Cause:

Large operations.

Solution:

- Batch processing
- Cache
- Pagination

---

## Spreadsheet Error

Cause:

Invalid range.

Solution:

- Validate sheet
- Check headers

---

# GitHub Copilot Error Analysis Prompt

```
Act as Senior Debugging Engineer.

Analyze this error.

Provide:

1. Error category
2. Root cause
3. Affected layer
4. Security impact
5. Fix strategy
6. Prevention method

Do not modify code before explaining.
```

---

# Copilot Refactoring Prompt

```
Improve error handling in this module.

Requirements:

- Add try/catch
- Use standard error response
- Add logging
- Hide sensitive information
- Improve user messages
```

---

# Error Handling Checklist

## Backend

- [ ] Try/catch implemented
- [ ] Standard response used
- [ ] Errors logged

---

## Frontend

- [ ] User messages clear
- [ ] Loading handled
- [ ] Recovery option provided

---

## Security

- [ ] Sensitive data hidden
- [ ] Stack trace not exposed

---

## Production

- [ ] Monitoring enabled
- [ ] Logs reviewed
- [ ] Error patterns analyzed

---

# Final Error Handling Flow

```
Detect

↓

Handle

↓

Log

↓

Respond

↓

Improve
```

---

# End of Error Handling
