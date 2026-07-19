<!-- ====================================================================== -->
<!-- File: docs/21_PERFORMANCE_GUIDE.md -->
<!-- ====================================================================== -->

# Performance Guide

Version 2.0

---

# Purpose

This document defines enterprise-level performance optimization standards for Google Apps Script Web Applications.

The goal is to build applications that are:

- Fast
- Scalable
- Reliable
- Cost efficient
- Ready for production users

---

# Performance Philosophy

Performance is not only about speed.

It includes:

```
Speed

+

Resource Efficiency

+

Scalability

+

User Experience

+

System Stability
```

---

# Performance Architecture

```text
User Browser

↓

Optimized UI

↓

API Layer

↓

Service Layer

↓

Repository Layer

↓

Google Sheets Database
```

---

# Performance Optimization Areas

| Area | Objective |
|-|-|
| Frontend | Faster rendering |
| Backend | Faster execution |
| Database | Reduce operations |
| API | Reduce payload |
| Cache | Reduce repeated work |
| Monitoring | Detect problems |

---

# Google Apps Script Performance Rules

---

# Rule 1: Minimize Spreadsheet Calls

Spreadsheet operations are expensive.

Avoid:

```javascript
for(let i=0;i<data.length;i++){

sheet
.getRange(i,1)
.getValue();

}
```

Problem:

```
1000 rows

=

1000 API calls
```

---

Recommended:

```javascript
const data =
sheet
.getDataRange()
.getValues();
```

One operation.

---

# Rule 2: Batch Processing

Bad:

```javascript
records.forEach(item=>{

sheet.appendRow(item);

});
```

---

Good:

```javascript
sheet
.getRange(
2,
1,
records.length,
records[0].length
)
.setValues(records);
```

---

# Rule 3: Reduce Data Transfer

Do not return:

```
All database columns
```

Return only required fields.

Example:

Bad:

```json
{
"id":"",
"name":"",
"address":"",
"phone":"",
"history":"",
"note":""
}
```

---

Good:

```json
{
"id":"",
"name":""
}
```

---

# Repository Optimization

Repository responsibilities:

- Efficient data access
- Data filtering
- Mapping
- Pagination

---

Example:

```javascript
class UserRepository{


findActiveUsers(){

return this.sheet
.getDataRange()
.getValues()
.filter(
row=>row[3]=="ACTIVE"
);

}


}
```

---

# Pagination Strategy

Never load unlimited records.

---

Request:

```json
{
"page":1,
"size":20
}
```

---

Response:

```json
{
"data":[],
"page":1,
"total":500
}
```

---

# Search Optimization

Use:

- Debounce
- Server-side filtering
- Indexed fields

---

Frontend:

```javascript
debounce(
search,
500
);
```

---

# Cache Architecture

Cache reduces:

- Execution time
- Spreadsheet calls
- API load

---

# Cache Levels

```text
Browser Cache

↓

Script Cache

↓

Database
```

---

# CacheService Example

```javascript
function getDashboard(){

const cache =
CacheService
.getScriptCache();


let result =
cache.get(
"dashboard"
);


if(result){

return JSON.parse(result);

}


result =
generateDashboard();


cache.put(
"dashboard",
JSON.stringify(result),
300
);


return result;

}
```

---

# Cache Strategy Table

| Data | Cache |
|-|-|
| System Settings | Long |
| Master Data | Medium |
| Dashboard | Short |
| Transaction Data | No |

---

# Lock Service

Use when multiple users update data.

Example:

```javascript
const lock =
LockService
.getScriptLock();


lock.waitLock(30000);

try{

saveTransaction();

}

finally{

lock.releaseLock();

}
```

---

# Frontend Performance

---

# Component Optimization

Components should:

- Load only required data
- Avoid unnecessary rendering
- Reuse UI elements

---

# Loading Pattern

Recommended:

```
Open Page

↓

Show Skeleton

↓

Load Data

↓

Render UI
```

---

# Avoid Blocking UI

Bad:

```
Click

↓

Wait 10 seconds

↓

Show Result
```

---

Good:

```
Click

↓

Loading

↓

Progress

↓

Result
```

---

# JavaScript Optimization

Avoid:

```javascript
document
.querySelector()
```

inside loops.

---

Use:

```javascript
const element =
document.querySelector();
```

---

# Event Optimization

Use:

- Event delegation
- Debounce
- Throttle

---

# API Performance

API should:

- Validate input quickly
- Return only necessary data
- Handle errors consistently

---

# API Response Standard

```json
{
"success":true,
"data":{},
"meta":{
"executionTime":"120ms"
}
}
```

---

# Dashboard Optimization

Dashboard should:

Load:

```
Summary First

↓

Details Later
```

---

# Chart Optimization

Do:

- Limit records
- Aggregate data
- Cache results

---

# Large Data Management

When data exceeds Google Sheets capability:

Options:

## Option 1

Archive old data

---

## Option 2

Separate sheets

---

## Option 3

External Database

Example:

```
MySQL

PostgreSQL

BigQuery
```

---

# Performance Monitoring

Monitor:

- Execution time
- API latency
- Error frequency
- Sheet operation count

---

# Performance Log Example

```
Action:

LOAD_DASHBOARD


Duration:

850 ms


Status:

SUCCESS
```

---

# Performance Testing

Test:

## Normal Load

Example:

```
10 users
```

---

## Heavy Load

Example:

```
100 users
```

---

## Large Data

Example:

```
50,000 records
```

---

# Performance Checklist

## Backend

- [ ] Batch operations used
- [ ] Cache implemented
- [ ] LockService applied
- [ ] Efficient queries

---

## Database

- [ ] No excessive calls
- [ ] Pagination available
- [ ] Data archived

---

## Frontend

- [ ] Responsive loading
- [ ] Optimized rendering
- [ ] No blocking operations

---

## Production

- [ ] Performance tested
- [ ] Monitoring active
- [ ] Bottlenecks reviewed

---

# GitHub Copilot Performance Audit Prompt

```
Act as Enterprise Performance Engineer.

Review this Google Apps Script application.

Analyze:

1. Spreadsheet operations
2. API performance
3. Cache strategy
4. Frontend rendering
5. Memory usage
6. Scalability risks

Provide:

- Performance issues
- Root causes
- Optimization solutions
- Refactoring suggestions

Do not change business logic.
```

---

# Copilot Optimization Prompt

```
Optimize this module for production.

Requirements:

- Reduce execution time
- Minimize Spreadsheet calls
- Add caching where appropriate
- Improve readability
- Maintain existing functionality
- Follow project architecture
```

---

# Final Performance Approval

Before Production:

```
Measure

↓

Optimize

↓

Test

↓

Monitor

↓

Improve
```

---

# End of Performance Guide
