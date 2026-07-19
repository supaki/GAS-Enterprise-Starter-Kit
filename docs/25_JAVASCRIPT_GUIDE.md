<!-- ====================================================================== -->
<!-- File: docs/25_JAVASCRIPT_GUIDE.md -->
<!-- ====================================================================== -->

# JavaScript Development Guide

Version 2.0

---

# Purpose

This document defines JavaScript coding standards for Google Apps Script Web Applications.

The objective is to ensure:

- Clean JavaScript code
- Maintainable frontend and backend logic
- Modern ES6+ development
- Better AI-assisted coding
- Consistent project quality

---

# JavaScript Standard

The project uses:

```
JavaScript ES6+

+

Google Apps Script V8 Runtime

+

Modern Browser JavaScript
```

---

# Core Principles

Follow:

✓ Clean Code

✓ Single Responsibility

✓ Reusable Functions

✓ Clear Naming

✓ Avoid Duplication

✓ Defensive Programming

---

# ES6+ Features

Recommended:

- const / let
- Arrow Functions
- Template Literals
- Classes
- Destructuring
- Spread Operator
- Modules Pattern

---

# Variable Declaration

Use:

```javascript
const name =
"John";


let count =
0;
```

---

Avoid:

```javascript
var name =
"John";
```

---

# Naming Convention

## Variables

camelCase:

```javascript
userName

totalAmount
```

---

## Functions

camelCase:

```javascript
getUser()

saveReport()
```

---

## Classes

PascalCase:

```javascript
UserService

ReportRepository
```

---

## Constants

UPPER_CASE:

```javascript
MAX_LOGIN_ATTEMPTS

DEFAULT_TIMEOUT
```

---

# Function Design

A function should:

- Do one thing
- Have clear input
- Have clear output

---

Bad:

```javascript
function process(){

login();

save();

sendEmail();

createReport();

}
```

---

Good:

```javascript
function createUser(){

validateUser();

saveUser();

}
```

---

# Function Size

Recommended:

```
10-30 lines
```

If longer:

Split into smaller functions.

---

# Arrow Functions

Use:

```javascript
const formatName =
(name)=>
name.toUpperCase();
```

---

# Template Literals

Use:

```javascript
const message =
`Hello ${name}`;
```

---

Avoid:

```javascript
"Hello "
+
name;
```

---

# Object Design

Use clear objects:

```javascript
const user={

id:"USR001",

name:"John",

role:"ADMIN"

};
```

---

# Destructuring

Example:

```javascript
const {

name,

email

}=user;
```

---

# Spread Operator

Example:

```javascript
const updatedUser={

...user,

status:"ACTIVE"

};
```

---

# Array Processing

Use:

## map()

Transform data.

Example:

```javascript
const names =
users.map(
user=>user.name
);
```

---

## filter()

Select data.

Example:

```javascript
const activeUsers =
users.filter(
user=>user.status==="ACTIVE"
);
```

---

## reduce()

Calculate.

Example:

```javascript
const total =
items.reduce(
(sum,item)=>
sum+item.price,
0
);
```

---

# Avoid Nested Loops

Bad:

```javascript
for(){

for(){

}

}
```

Problem:

Performance issue.

---

Use:

- Map
- Object lookup
- Filtering

---

# Class Design

Use classes for:

- Service
- Repository
- Controller
- Models

---

Example:

```javascript
class UserService{


constructor(repository){

this.repository =
repository;

}


create(data){

return this.repository
.save(data);

}


}
```

---

# Constructor Rules

Constructor should:

- Initialize dependencies
- Not execute heavy logic

---

# Object-Oriented Pattern

Recommended:

```
Controller

↓

Service

↓

Repository
```

---

# Async Pattern

For frontend:

Use:

```javascript
async function loadData(){

const result =
await fetchData();

return result;

}
```

---

# Promise Handling

Always handle errors:

```javascript
try{

await save();

}

catch(error){

showError();

}
```

---

# Google Apps Script Async Pattern

Use:

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

# JSON Handling

Standard:

```javascript
JSON.stringify()

JSON.parse()
```

---

Example:

```javascript
const json =
JSON.stringify(data);
```

---

# Data Validation

Never trust input.

Example:

```javascript
function validateUser(user){

if(!user.email){

throw new Error(
"Email required"
);

}

}
```

---

# Error Handling

Bad:

```javascript
catch(e){

alert(e);

}
```

---

Good:

```javascript
catch(error){

Logger.log(
error.message
);

throw error;

}
```

---

# Defensive Programming

Check before use:

Bad:

```javascript
user.name
```

---

Good:

```javascript
user &&
user.name
```

---

# Null Handling

Use:

```javascript
const name =
user?.name ?? "";
```

---

# Frontend JavaScript Structure

Recommended:

```
js/

├── app.js

├── api.js

├── ui.js

├── validation.js

├── utils.js
```

---

# API Service Pattern

Example:

```javascript
const UserAPI={


getAll(){

return
google.script.run
.getUsers();

}


};
```

---

# UI Management Pattern

Separate:

```
Data Logic

↓

UI Rendering
```

---

Example:

Bad:

```javascript
getData(){

document.innerHTML=data;

}
```

---

Good:

```javascript
const data =
getData();


renderTable(data);
```

---

# Event Handling

Use:

```javascript
button
.addEventListener(
"click",
handler
);
```

---

Avoid:

Inline:

```html
onclick=""
```

---

# Local Storage Usage

Use for:

- Theme
- UI preferences
- Temporary settings

Do not store:

- Password
- Token
- Sensitive data

---

# Code Comment Rules

Comment:

Why?

Not:

What?

---

Good:

```javascript
// Cache dashboard data to reduce Sheet calls
```

---

Bad:

```javascript
// Get data
```

---

# JavaScript Security

Prevent:

- XSS
- Unsafe HTML injection
- Exposed secrets

---

Use:

```javascript
escapeHTML()
```

before displaying user input.

---

# Performance Rules

Avoid:

- Repeated DOM queries
- Large loops
- Unnecessary rendering

---

Use:

- Cache
- Batch processing
- Lazy loading

---

# JavaScript Review Checklist

## Code Quality

- [ ] ES6+ used
- [ ] Naming correct
- [ ] Functions focused

---

## Architecture

- [ ] Logic separated
- [ ] Components reusable
- [ ] No duplicate code

---

## Security

- [ ] Input validated
- [ ] Output escaped
- [ ] No secrets

---

## Performance

- [ ] Efficient loops
- [ ] Optimized rendering
- [ ] Minimal API calls

---

# GitHub Copilot JavaScript Review Prompt

```
Act as Senior JavaScript Engineer.

Review this code.

Check:

- ES6+ usage
- Clean Code
- Architecture
- Performance
- Security
- Maintainability

Provide:

1. Problems
2. Explanation
3. Refactoring suggestions

Follow JAVASCRIPT_GUIDE.md.
```

---

# Copilot Refactoring Prompt

```
Refactor this JavaScript module.

Requirements:

- Use ES6+
- Improve readability
- Reduce complexity
- Separate responsibilities
- Add validation
- Improve error handling

Maintain existing behavior.
```

---

# Final JavaScript Quality Gate

Before merging:

```
Code Review

↓

Refactoring

↓

Testing

↓

Performance Check

↓

Release
```

---

# End of JavaScript Development Guide
