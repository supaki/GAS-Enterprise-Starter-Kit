<!-- ====================================================================== -->
<!-- File: docs/07_CODING_STANDARDS.md -->
<!-- ====================================================================== -->

# Coding Standards

Version 2.0

---

# Purpose

Define coding standards for all Google Apps Script, JavaScript, HTML, and CSS code.

The goal is:

- Clean code
- Maintainability
- Consistency
- Scalability

---

# General Principles

Follow:

- Clean Code
- SOLID
- DRY
- KISS
- Separation of Concerns

---

# JavaScript Standard

Use:

ES2022

Example:

```javascript
const users = [];

let count = 0;
```

Avoid:

```javascript
var users=[];
```

---

# Naming Convention

## Variables

camelCase

Example:

```javascript
userName

patientList
```

---

## Functions

camelCase

Example:

```javascript
getUsers()

savePatient()
```

---

## Classes

PascalCase

Example:

```javascript
class UserService {

}
```

---

## Constants

UPPER_CASE

Example:

```javascript
const MAX_LOGIN_ATTEMPTS = 5;
```

---

# Function Rules

A function should:

- Do one thing
- Be easy to test
- Have clear name

Avoid:

```javascript
function processEverything(){

}
```

Prefer:

```javascript
function validateUser(){

}

function saveUser(){

}

function sendNotification(){

}
```

---

# Function Length

Recommended:

< 50 lines

If longer:

Refactor into smaller functions.

---

# Comments

Good:

```javascript
// Calculate total amount
// including discount
```

Bad:

```javascript
// Add 1
x++;
```

---

# JSDoc Requirement

Every public function requires documentation.

Example:

```javascript
/**
 * Get users from database
 * @returns {Array}
 */
function getUsers(){

}
```

---

# Error Handling

Always:

```javascript
try{

}
catch(error){

 Logger.log(error);

}
```

Never ignore errors.

Wrong:

```javascript
catch(e){}
```

---

# Google Apps Script Rules

Avoid:

```javascript
for(each row){

sheet.appendRow();

}
```

Use batch:

```javascript
sheet
.getRange()
.setValues(data);
```

---

# Spreadsheet Access Rules

Wrong:

```javascript
SpreadsheetApp
.getActive()
.getSheetByName()
```

inside every function.

Correct:

Create Repository.

---

# HTML Rules

Never:

```html
<script>
// huge javascript
</script>
```

Separate:

```
js/app.js
```

---

# CSS Rules

Prefer:

Tailwind CSS

Avoid:

```html
style="color:red"
```

---

# File Responsibility

| File | Responsibility |
|-|-|
| Controller | Request handling |
| Service | Business logic |
| Repository | Database |
| Utils | Helper |
| Config | Configuration |

---

# Git Workflow

Commit messages:

Feature:

```
feat: add user dashboard
```

Bug:

```
fix: resolve login issue
```

Documentation:

```
docs: update api guide
```

---

# Code Review Checklist

Before merge:

✓ Code formatted

✓ No duplicate code

✓ No debug logs

✓ Error handling exists

✓ Security reviewed

✓ Documentation updated

✓ Tests completed

---

# GitHub Copilot Prompt

Review this code according to coding standards.

Check:

- Architecture
- Security
- Performance
- Naming
- Error handling
- Maintainability

Refactor if necessary.

---

# Checklist

- [ ] ES2022 used
- [ ] Naming correct
- [ ] JSDoc added
- [ ] Errors handled
- [ ] No duplicate code
- [ ] Repository pattern followed
- [ ] Clean code applied
