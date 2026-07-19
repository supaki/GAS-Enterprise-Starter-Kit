<!-- ====================================================================== -->
<!-- File: docs/09_FOLDER_STRUCTURE.md -->
<!-- ====================================================================== -->

# Folder Structure

Version 2.0

---

# Purpose

Define the standard project structure for Google Apps Script Web Applications.

The structure must support:

- MVC
- Clean Architecture
- Maintainability
- Scalability
- Team Development

---

# Root Structure

```text
GAS-Enterprise-App/

│
├── .github/
│   └── copilot-instructions.md
│
├── docs/
│   ├── AI_CONTEXT.md
│   ├── PROJECT_RULES.md
│   ├── 00_AI_INSTRUCTIONS.md
│   ├── 01_PROJECT_OVERVIEW.md
│   └── ...
│
├── src/
│
├── assets/
│
├── examples/
│
└── README.md
```

---

# Source Structure

```text
src/

├── backend/
│
│   ├── Code.gs
│   ├── Router.gs
│   ├── Config.gs
│   ├── Auth.gs
│   ├── API.gs
│   ├── Logger.gs
│   └── Utils.gs
│
├── controllers/
│
│   ├── UserController.gs
│   └── ReportController.gs
│
├── services/
│
│   ├── UserService.gs
│   └── ReportService.gs
│
├── repositories/
│
│   ├── UserRepository.gs
│   └── ReportRepository.gs
│
├── models/
│
│   └── User.gs
│
└── frontend/

    ├── pages/
    │
    ├── components/
    │
    ├── js/
    │
    └── css/
```

---

# Backend Structure

---

# Code.gs

Responsibility:

Application entry point.

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

# Router.gs

Responsibility:

Routing requests.

Example:

```javascript
function route(action,data){

switch(action){

case "getUsers":

return getUsers(data);

}

}
```

---

# Controller

Example:

```
UserController.gs
```

Responsibility:

- Receive request
- Validate
- Call service

---

# Service

Example:

```
UserService.gs
```

Responsibility:

- Business logic
- Rules
- Processing

---

# Repository

Example:

```
UserRepository.gs
```

Responsibility:

- Spreadsheet access
- CRUD

---

# Frontend Structure

```text
frontend/

pages/

dashboard.html

users.html


components/

Navbar.html

Sidebar.html


js/

app.js

api.js

auth.js


css/

styles.css
```

---

# Naming Rules

Files:

```
PascalCase.gs

UserService.gs
```

Functions:

```
camelCase()

getUsers()
```

Classes:

```
PascalCase

UserService
```

---

# Configuration

Never store:

- API keys
- Passwords
- Secrets

inside code.

Use:

```
Script Properties
```

---

# Environment

Recommended:

```
Config.gs
```

Contains:

- Application settings
- Feature flags
- Environment values

---

# Development Workflow

1. Create Repository
2. Define Database
3. Create Model
4. Create Repository
5. Create Service
6. Create Controller
7. Create API
8. Create UI
9. Test
10. Deploy

---

# GitHub Copilot Prompt

Generate project structure following this document.

Requirements:

- Use MVC
- Use Service Layer
- Use Repository Pattern
- Separate Frontend and Backend
- Create reusable components

---

# Folder Checklist

- [ ] MVC structure created
- [ ] Backend separated
- [ ] Frontend separated
- [ ] Repository layer exists
- [ ] Service layer exists
- [ ] Components reusable
- [ ] Configuration separated
