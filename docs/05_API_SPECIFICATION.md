<!-- ====================================================================== -->
<!-- File: docs/05_API_SPECIFICATION.md -->
<!-- ====================================================================== -->

# API Specification

Version 2.0

---

# Purpose

Define API standards for communication between:

- Frontend
- Google Apps Script Backend
- External Systems

---

# API Architecture

```text
Frontend

↓

API Controller

↓

Service Layer

↓

Repository

↓

Google Sheets
```

---

# API Design Principles

Every API must:

- Have clear purpose
- Validate input
- Return standard response
- Handle errors
- Log important actions

---

# Response Standard

All APIs must return:

```json
{
 "success": true,
 "message": "Success",
 "data": {},
 "errors": []
}
```

---

# Success Example

```json
{
 "success":true,
 "message":"User created",
 "data":{
   "id":"USR-001"
 },
 "errors":[]
}
```

---

# Error Example

```json
{
 "success":false,
 "message":"Validation failed",
 "data":null,
 "errors":[
   "Email required"
 ]
}
```

---

# API Naming Convention

Use:

```
verb + noun
```

Examples:

```
getUsers()

createUser()

updateUser()

deleteUser()
```

---

# Authentication API

## Login

Function:

```
login()
```

Request:

```json
{
 "username":"admin",
 "password":"123456"
}
```

Response:

```json
{
 "success":true,
 "data":{
   "token":"",
   "role":"admin"
 }
}
```

---

# User API

## Get Users

Function:

```
getUsers()
```

Response:

```json
{
 "success":true,
 "data":[
  {
   "id":"USR001",
   "username":"admin"
  }
 ]
}
```

---

## Create User

Function:

```
createUser(user)
```

Input:

```json
{
 "username":"john",
 "email":"john@test.com"
}
```

---

## Update User

Function:

```
updateUser(user)
```

---

## Delete User

Function:

```
deleteUser(id)
```

---

# Controller Example

```javascript
function apiCreateUser(data){

 try{

  const service =
  new UserService();


  return {
   success:true,
   data:
   service.create(data)
  };


 }catch(error){

  Logger.log(error);

  return {
   success:false,
   message:error.message,
   errors:[error.message]
  };

 }

}
```

---

# Service Example

```javascript
class UserService{


constructor(){

 this.repo =
 new UserRepository();

}


create(data){

 validateUser(data);

 return this.repo.save(data);

}


}
```

---

# API Error Codes

| Code | Meaning |
|-|-|
|200|Success|
|400|Validation Error|
|401|Unauthorized|
|403|Forbidden|
|404|Not Found|
|500|Server Error|

---

# API Security

Every API must check:

- Authentication
- Permission
- Input validation
- User role

---

# Logging

Record:

- User
- Action
- Timestamp
- Module
- Result

---

# Performance

Use:

- CacheService
- Pagination
- Batch operations

Avoid:

- Loading unnecessary records
- Multiple spreadsheet calls

---

# GitHub Copilot Prompt

Generate API functions following this specification.

Requirements:

- Use Controller-Service-Repository architecture.
- Return standard JSON.
- Add validation.
- Add error handling.
- Add permission checking.
- Add logging.

---

# API Checklist

- [ ] Standard response format
- [ ] Validation completed
- [ ] Authentication checked
- [ ] Permission checked
- [ ] Error handling added
- [ ] Logging implemented
- [ ] Performance optimized
