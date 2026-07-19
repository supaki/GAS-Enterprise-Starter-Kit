<!-- ====================================================================== -->
<!-- File: docs/14_PERFORMANCE_GUIDE.md -->
<!-- ====================================================================== -->

# Performance Guide

Version 2.0

---

# Purpose

This document defines performance optimization standards for Google Apps Script Enterprise Applications.

The objective is to build applications that are:

- Fast
- Reliable
- Scalable
- Efficient
- User friendly

---

# Performance Principles

Follow:

- Reduce execution time
- Minimize external calls
- Optimize data access
- Cache frequently used data
- Process data in batches

---

# Performance Architecture

```text
Frontend

↓

Optimized API

↓

Service Layer

↓

Repository

↓

Optimized Google Sheets Access
```

---

# Google Apps Script Limitations

Google Apps Script has limitations:

- Execution time
- Spreadsheet operations
- Memory usage
- Concurrent users

Therefore optimization is required.

---

# Main Performance Problems

Common problems:

| Problem | Cause |
|-|-|
| Slow loading | Too many Sheet calls |
| Timeout | Large loops |
| API delay | Heavy processing |
| UI lag | Large DOM |
| Memory issue | Large objects |

---

# Google Sheets Optimization

## Rule 1: Avoid Repeated Access

Bad:

```javascript
for(let i=0;i<1000;i++){

sheet
.getRange(i,1)
.getValue();

}
```

Problem:

1000 Spreadsheet calls.

---

Correct:

```javascript
const data =
sheet
.getDataRange()
.getValues();
```

One call.

---

# Batch Write

Bad:

```javascript
rows.forEach(row=>{

sheet.appendRow(row);

});
```

---

Good:

```javascript
sheet
.getRange(
2,
1,
rows.length,
rows[0].length
)
.setValues(rows);
```

---

# Header Mapping

Never:

```javascript
row[5]
```

Because column changes break code.

---

Use:

```javascript
const index =
headers.indexOf(
"email"
);
```

---

# Pagination

Never load all records.

Bad:

```
10,000 rows
↓
Browser
```

---

Good:

```
Page 1

20 records

↓

Page 2
```

---

# Pagination Example

Request:

```json
{
"page":1,
"limit":20
}
```

Response:

```json
{
"data":[],
"total":500
}
```

---

# Cache Strategy

Use:

```
CacheService
```

For:

- Settings
- Master data
- Dashboard statistics

---

# Cache Example

```javascript
function getSettings(){

const cache =
CacheService
.getScriptCache();


let data =
cache.get(
"settings"
);


if(data){

return JSON.parse(data);

}


data =
loadSettings();


cache.put(
"settings",
JSON.stringify(data),
300
);


return data;

}
```

---

# Cache Duration

Recommended:

| Data | Time |
|-|-|
| Configuration | 1 hour |
| Master Data | 30 min |
| Dashboard | 5 min |
| User Session | 30 min |

---

# Lock Service

Use for:

- Shared data updates
- Sequential operations

Example:

```javascript
const lock =
LockService
.getScriptLock();


lock.waitLock(30000);

try{

saveData();

}

finally{

lock.releaseLock();

}
```

---

# API Optimization

## Reduce Payload

Bad:

```json
{
"users":[
all fields
]
}
```

---

Good:

```json
{
"id":"USR001",
"name":"John"
}
```

---

# API Response Rules

Always include:

```json
{
"success":true,
"data":[],
"meta":{
"page":1,
"total":100
}
}
```

---

# Frontend Performance

## Minimize DOM

Avoid:

Thousands of HTML elements.

---

Use:

- Pagination
- Lazy loading
- Virtual scrolling

---

# JavaScript Optimization

Avoid:

```javascript
for(){

document.querySelector()

}
```

---

Use:

```javascript
const element =
document.querySelector();
```

---

# Debounce Search

For search box:

```javascript
function debounce(
fn,
delay
){

let timer;

return function(){

clearTimeout(timer);

timer =
setTimeout(
fn,
delay
);

};

}
```

---

# Lazy Loading

Load:

- Charts
- Reports
- Large tables

Only when needed.

---

# Image Optimization

Use:

- Compressed images
- WebP format
- Correct size

---

# UI Performance

Use:

- Skeleton loading
- Progressive rendering
- Avoid blocking operations

---

# Database Performance

Rules:

✓ Index important fields

✓ Limit query size

✓ Avoid full scan

✓ Archive old data

---

# Large Data Strategy

For >50,000 records:

Consider:

- Separate archive sheet
- External database
- MySQL
- BigQuery

---

# Monitoring

Track:

- Execution time
- API response
- Error rate
- User experience

---

# Performance Metrics

Recommended:

| Metric | Target |
|-|-|
| Page load | < 3 seconds |
| API response | < 2 seconds |
| Database operation | Optimized |
| Error rate | < 1% |

---

# Performance Review Process

```text
Measure

↓

Identify bottleneck

↓

Optimize

↓

Test

↓

Compare results
```

---

# GitHub Copilot Performance Prompt

```
Act as Performance Engineer.

Review this application.

Analyze:

- Google Sheets operations
- API response time
- Cache usage
- Frontend rendering
- Memory usage

Identify bottlenecks.

Refactor for better performance.

Maintain functionality.
```

---

# Performance Checklist

## Backend

- [ ] Batch operations used
- [ ] Cache implemented
- [ ] LockService used
- [ ] API optimized

---

## Database

- [ ] Pagination implemented
- [ ] Header mapping used
- [ ] Large data handled

---

## Frontend

- [ ] Lazy loading
- [ ] Debounce search
- [ ] Optimized rendering

---

## Production

- [ ] Performance tested
- [ ] Monitoring enabled
- [ ] Bottlenecks reviewed

---

# End of Performance Guide
