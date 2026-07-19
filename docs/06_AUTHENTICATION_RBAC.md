<!-- ====================================================================== -->
<!-- File: docs/06_AUTHENTICATION_RBAC.md -->
<!-- ====================================================================== -->

# Authentication & RBAC

Version 2.0

---

# Purpose

This document defines authentication and authorization standards.

The system must support secure user management using Role-Based Access Control (RBAC).

---

# Authentication Concept

Authentication answers:

> Who are you?

Authorization answers:

> What can you do?

Flow:

```text
User

↓

Login

↓

Verify Identity

↓

Create Session

↓

Load Role

↓

Check Permission

↓

Allow Access
```

---

# Authentication Architecture

```text
Frontend

↓

Auth Controller

↓

Auth Service

↓

User Repository

↓

Users Sheet
```

---

# User Authentication Methods

Supported:

1. Google Account Authentication
2. Internal Username/Password
3. External Identity Provider (Future)

---

# User Sheet Structure

Sheet:

Users

| Field | Type | Description |
|-|-|-|
| id | String | User ID |
| username | String | Login name |
| email | String | Email |
| passwordHash | String | Password hash |
| roleId | String | User role |
| status | String | Account status |
| lastLogin | Date | Last login |
| createdAt | Date | Created |
| updatedAt | Date | Updated |

---

# Password Security

Never store:

```
plain password
```

Wrong:

```javascript
password = "123456"
```

Correct:

```
passwordHash
```

Example:

```javascript
function hashPassword(password){

return Utilities
.computeDigest(
 Utilities.DigestAlgorithm.SHA_256,
 password
)
.map(function(byte){

 return ('0'+
 (byte & 0xFF)
 .toString(16))
 .slice(-2);

})
.join('');

}
```

---

# Session Management

Session contains:

```json
{
"userId":"USR001",
"username":"admin",
"role":"ADMIN",
"expires":"datetime"
}
```

Storage options:

- CacheService
- UserProperties
- Script Properties

---

# Login Example

```javascript
function login(username,password){

 const user =
 userRepository
 .findByUsername(username);


 if(!user){
   throw new Error(
   "User not found"
   );
 }


 if(
 hashPassword(password)
 !== user.passwordHash
 ){

 throw new Error(
 "Invalid password"
 );

 }


 return createSession(user);

}
```

---

# RBAC Concept

Role-Based Access Control

Structure:

```text
User

↓

Role

↓

Permission

↓

Resource
```

---

# Default Roles

## Admin

Full access.

Permissions:

```
*
```

---

## Manager

Manage business data.

Example:

```
users.read

users.create

reports.read
```

---

## Staff

Daily operation.

Example:

```
patients.read

patients.create
```

---

## Viewer

Read only.

Example:

```
reports.read
```

---

# Roles Sheet

Structure:

| Field | Description |
|-|-|
| id | Role ID |
| roleName | Name |
| permissions | JSON |
| status | Active |

Example:

```json
{
"users":[
"read",
"create"
],
"reports":[
"read"
]
}
```

---

# Permission Naming

Format:

```
module.action
```

Example:

```
users.create

users.update

patients.delete

reports.export
```

---

# Permission Check

Example:

```javascript
function hasPermission(
user,
permission
){

return user.permissions
.includes(permission);

}
```

---

# Authorization Middleware

Example:

```javascript
function authorize(
permission
){

const user =
getCurrentUser();


if(
!hasPermission(
user,
permission
)
){

throw new Error(
"Access denied"
);

}

}
```

---

# Route Protection

Example:

```javascript
function getUsers(){

authorize(
"users.read"
);


return userService
.getAll();

}
```

---

# Security Rules

Always:

✓ Validate session

✓ Check permission

✓ Log important actions

✓ Expire sessions

✓ Limit failed login attempts

---

# Audit Events

Record:

Login

Logout

Create

Update

Delete

Permission denied

---

# Future Extension

Support:

- Multi tenant
- Organization
- Department
- Branch permission
- Attribute Based Access Control

---

# GitHub Copilot Prompt

Implement authentication system.

Requirements:

- Create Auth Service.
- Create User Repository.
- Create Session Manager.
- Implement RBAC.
- Add Permission Middleware.
- Add Audit Logging.
- Never expose passwords.

---

# Checklist

- [ ] Authentication implemented
- [ ] Password protected
- [ ] Session management added
- [ ] RBAC implemented
- [ ] Permission checking added
- [ ] Audit log enabled
- [ ] Security reviewed
