<!-- ====================================================================== -->
<!-- File: docs/19_BUSINESS_RULES.md -->
<!-- ====================================================================== -->

# Business Rules

Version 2.0

---

# Purpose

This document defines the standards for designing and implementing business logic.

The objective is to ensure:

- Correct business behavior
- Consistent validation
- Maintainable rules
- Separation between UI and business logic
- Easier AI-assisted development

---

# Business Rule Concept

Business Rules define:

```
What the system must do

↓

Under what conditions

↓

With what restrictions

↓

What result should happen
```

---

# Business Rule Principles

Business rules must:

✓ Be independent from UI

✓ Be documented

✓ Be testable

✓ Be reusable

✓ Be implemented in Service Layer

---

# Architecture Position

Business Logic belongs here:

```text
Controller

↓

Service Layer

↓

Business Rules

↓

Repository

↓

Database
```

---

# Wrong Architecture

Do not:

```text
HTML

↓

Google Sheet

↓

Business Logic
```

Example:

```javascript
if(status=="APPROVED"){
// logic
}
```

inside HTML.

---

# Correct Architecture

```javascript
class OrderService {


approveOrder(id){

const order =
repository.findById(id);


if(
!canApprove(order)
){

throw new Error(
"Cannot approve"
);

}


return repository.update(
order
);

}

}
```

---

# Business Rule Categories

---

# 1. Validation Rules

Define:

Input requirements.

Example:

User Email:

```
Required

Must be valid format

Must be unique
```

---

Example:

```javascript
function validateEmail(email){

if(!email){

throw new Error(
"Email required"
);

}

}
```

---

# 2. Calculation Rules

Define:

How values are calculated.

Example:

Discount:

```
If customer type = VIP

Discount = 10%
```

---

Example:

```javascript
function calculateDiscount(customer){

if(
customer.type==="VIP"
){

return 0.10;

}

return 0;

}
```

---

# 3. Authorization Rules

Define:

Who can perform actions.

Example:

```
Only Admin can delete users
```

---

Implementation:

```javascript
if(
role!=="ADMIN"
){

throw new Error(
"Permission denied"
);

}
```

---

# 4. Workflow Rules

Define:

Process sequence.

Example:

Approval:

```
Draft

↓

Submitted

↓

Approved

↓

Completed
```

---

# 5. Status Rules

Define:

Allowed status changes.

Example:

Allowed:

```
Draft

→

Submitted
```

Not allowed:

```
Completed

→

Draft
```

---

# Status Transition Table

| Current | Next | Allowed |
|-|-|-|
| Draft | Submitted | Yes |
| Submitted | Approved | Yes |
| Submitted | Rejected | Yes |
| Completed | Draft | No |

---

# 6. Data Integrity Rules

Ensure:

Data consistency.

Examples:

- Unique ID
- Required fields
- Reference validation

---

# Rule Definition Template

Every business rule should use:

```markdown
# Rule ID


Name:


Description:


Condition:


Action:


Error Message:


Test Case:
```

---

# Example Business Rule

```markdown
# RULE-USER-001

Name:

Unique Email


Description:

Each user must have unique email.


Condition:

Email already exists


Action:

Reject creation


Error:

Email already registered


Test:

Create duplicate email
```

---

# Business Rule Naming

Format:

```
RULE-[MODULE]-[NUMBER]
```

Examples:

```
RULE-USER-001

RULE-PATIENT-002

RULE-REPORT-003
```

---

# Service Layer Example

```javascript
class PatientService {


createPatient(data){


this.validate(data);


this.checkDuplicate(
data.cid
);


return this.repository
.save(data);


}


}
```

---

# Rule Engine Concept

For large systems:

```text
Business Rules

↓

Rule Engine

↓

Service Layer

↓

Application
```

---

# Rule Configuration

For changing rules:

Store in:

```
Settings Sheet
```

Example:

| Key | Value |
|-|-|
| MAX_UPLOAD_SIZE | 10 |
| DISCOUNT_RATE | 0.10 |

---

# Business Rule Processing Flow

```text
User Request

↓

Validate Input

↓

Check Business Rules

↓

Execute Action

↓

Save Data

↓

Create Audit Log

↓

Return Result
```

---

# Error Handling Rules

Business errors must be meaningful.

Wrong:

```
Error 500
```

Correct:

```
Cannot approve request.
Required review is missing.
```

---

# Business Rule Testing

Every rule requires:

- Positive test
- Negative test
- Boundary test

---

# Example Test

Rule:

```
Age must be >=18
```

Test:

| Input | Result |
|-|-|
| 20 | Pass |
| 18 | Pass |
| 17 | Fail |

---

# AI Assisted Business Analysis

Before coding:

Prompt:

```
Analyze this business requirement.

Identify:

- Business rules
- Validation rules
- Workflow rules
- Permission rules
- Status transitions
- Exception cases

Create documentation first.
```

---

# GitHub Copilot Business Logic Prompt

```
Act as Business Analyst and Senior Developer.

Analyze this feature.

Create:

1. Business rules
2. Validation logic
3. Workflow
4. Data rules
5. Permission rules
6. Test scenarios

After approval implement Service Layer.
```

---

# Business Rule Review Checklist

## Analysis

- [ ] Requirement understood
- [ ] Rules documented
- [ ] Exceptions identified

---

## Development

- [ ] Rules in Service Layer
- [ ] UI independent
- [ ] Validation implemented

---

## Testing

- [ ] Positive cases tested
- [ ] Negative cases tested
- [ ] Boundary cases tested

---

## Maintenance

- [ ] Rule ID assigned
- [ ] Documentation updated
- [ ] Changes tracked

---

# Final Business Rule Approval

Process:

```
Requirement

↓

Business Analysis

↓

Rule Definition

↓

Development

↓

Testing

↓

Approval
```

---

# End of Business Rules
