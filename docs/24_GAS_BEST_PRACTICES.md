<!-- ====================================================================== -->
<!-- File: docs/24_GAS_BEST_PRACTICES.md -->
<!-- ====================================================================== -->

# Google Apps Script Best Practices

Version 2.0

---

# Purpose

This document defines enterprise development standards for Google Apps Script applications.

The objective is to create applications that are:

- Maintainable
- Secure
- Performant
- Scalable
- Easy for AI-assisted development

---

# GAS Development Philosophy

Google Apps Script applications should follow:

```
Clean Code

+

Modular Architecture

+

Service Separation

+

Reusable Functions

+

Secure Configuration
```

---

# Recommended Architecture

Use:

```
MVC + Clean Architecture
```

Structure:

```
Frontend

↓

Controller

↓

Service

↓

Repository

↓

Google Services
```

---

# Project File Structure

Recommended:

```
src/

├── Config.gs

├── Constants.gs


├── controllers/

│   ├── UserController.gs


├── services/

│   ├── UserService.gs


├── repositories/

│   ├── UserRepository.gs


├── models/

│   ├── User.gs


├── utils/

│   ├── Validator.gs

│   ├── Logger.gs


├── web/

│   ├── index.html

│   ├── css.html

│   └── js.html
```

---

# Naming Convention

## Files

Use:

```
PascalCase
```

Examples:

```
UserService.gs

ReportController.gs
```

---

## Functions

Use:

```
camelCase
```

Examples:

```javascript
getUserById()

createReport()
```

---

## Classes

Use:

```
PascalCase
```

Example:

```javascript
class UserService{

}
```

---

# V8 Runtime Standard

Always enable:

```
V8 Runtime
```

Benefits:

- Modern JavaScript
- Classes
- Arrow functions
- Async patterns

---

# Use Const and Let

Recommended:

```javascript
const userId =
request.userId;


let status =
"ACTIVE";
```

Avoid:

```javascript
var userId;
```

---

# Configuration Management

Never:

```javascript
const PASSWORD =
"123456";
```

---

Use:

```javascript
PropertiesService
.getScriptProperties();
```

---

Example:

```javascript
const CONFIG = {

SHEET_ID:
PropertiesService
.getScriptProperties()
.getProperty(
"SHEET_ID"
)

};
```

---

# Entry Point Functions

Recommended:

Only expose:

```javascript
doGet()

doPost()
```

---

Example:

```javascript
function doGet(){

return HtmlService
.createTemplateFromFile(
"index"
)
.evaluate();

}
```

---

# HTML Template Pattern

Use:

```javascript
include()
```

Example:

```javascript
function include(file){

return HtmlService
.createHtmlOutputFromFile(
file
)
.getContent();

}
```

---

HTML:

```html
<?!= include('css'); ?>

<?!= include('js'); ?>
```

---

# Spreadsheet Access Rules

Never:

```javascript
sheet
.getRange()
.getValue()
```

inside loops.

---

Use:

```javascript
getValues()

setValues()
```

---

# Repository Pattern Example

```javascript
class UserRepository{


findAll(){

const sheet =
this.getSheet();


return sheet
.getDataRange()
.getValues();

}


}
```

---

# Service Layer Rules

Service handles:

✓ Business logic

✓ Validation

✓ Workflow

✓ Permission checking

---

Service should NOT:

✗ Handle HTML

✗ Direct UI response

---

# Controller Rules

Controller handles:

- Request
- Response
- Error handling

Example:

```javascript
function createUserAPI(data){

try{

return UserService
.create(data);

}

catch(error){

return ErrorHandler
.handle(error);

}

}
```

---

# Utility Function Standards

Utilities should be:

- Small
- Reusable
- Independent

Example:

```javascript
class Validator{


static required(value){

return value!==undefined;

}


}
```

---

# Logging Standard

Use centralized logger.

Example:

```javascript
LoggerService.log({

action:
"CREATE_USER",

user:
"user001"

});
```

---

# Trigger Management

Use triggers carefully.

Types:

## Time Trigger

Example:

```
Daily backup
```

---

## Event Trigger

Example:

```
On form submit
```

---

# Trigger Rules

Avoid:

- Too many triggers
- Duplicate execution
- Heavy processing

---

# Error Handling Standard

Every external operation:

must use:

```javascript
try{

}

catch(error){

}
```

---

# API Design

Recommended response:

```json
{
"success":true,
"data":{}
}
```

Error:

```json
{
"success":false,
"message":"Error"
}
```

---

# Security Rules

Never expose:

- Password
- Token
- API key
- Internal error

---

# Performance Rules

Always:

✓ Batch read

✓ Batch write

✓ Cache data

✓ Limit response size

✓ Avoid unnecessary executions

---

# Code Quality Rules

Code must:

- Be readable
- Have meaningful names
- Avoid duplication
- Include comments when needed

---

# Comment Standard

Good:

```javascript
// Validate user permission
```

Bad:

```javascript
// Loop
for(...)
```

---

# Testing Functions

Create:

```javascript
testXXX()
```

Example:

```javascript
function testUserService(){

}

```

---

# Deployment Rules

Before deploy:

- Remove debug code
- Update version
- Backup database
- Test permissions

---

# GAS Security Checklist

## Code

- [ ] No secrets
- [ ] Validation exists
- [ ] Error handling exists

---

## Data

- [ ] Sheet protected
- [ ] Access controlled

---

## Deployment

- [ ] Permission reviewed
- [ ] Version created

---

# GitHub Copilot GAS Review Prompt

```
Act as Senior Google Apps Script Engineer.

Review this project.

Check:

1. Architecture
2. File organization
3. Code quality
4. Security
5. Performance
6. Error handling
7. Maintainability

Provide:

- Issues
- Explanation
- Recommended fixes

Follow GAS_BEST_PRACTICES.md.
```

---

# Copilot GAS Refactoring Prompt

```
Refactor this Google Apps Script code.

Requirements:

- Follow MVC
- Use Service Layer
- Use Repository Pattern
- Improve readability
- Add validation
- Add error handling
- Optimize Spreadsheet operations

Do not change business behavior.
```

---

# Final GAS Quality Gate

Before Production:

```
Code Review

↓

Security Review

↓

Performance Review

↓

Testing

↓

Deployment
```

---

# End of GAS Best Practices
