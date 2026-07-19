# Frequently Asked Questions (FAQ)

## GAS Enterprise Starter Kit

Version 1.0


---

# General Questions

---

## Q1: What is GAS Enterprise Starter Kit?

Answer:

It is a production-ready framework for creating enterprise web applications using:

- Google Apps Script
- Google Sheets
- HTML Service
- Tailwind CSS
- JavaScript


---

## Q2: Who is this project for?

Answer:

Designed for:

- Developers
- System administrators
- Healthcare IT teams
- Organizations using Google Workspace


---

# Architecture Questions

---

## Q3: Why use MVC architecture?

Answer:

MVC separates responsibilities:
UI

↓

Controller

↓

Service

↓

Repository

↓

Database


Benefits:

- Easier maintenance
- Better testing
- Reusable components


---

## Q4: Why use Repository Pattern?

Answer:

To separate database operations from business logic.

Example:

Bad:


Service

↓

SpreadsheetApp


Good:


Service

↓

Repository

↓

SpreadsheetApp


---

# AI Agent Questions

---

## Q5: Why does Copilot need documentation first?

Answer:

Because AI needs project context.

Without documentation:

- Architecture may break
- Duplicate code may occur
- Wrong technology may be selected


---

## Q6: Which files should Copilot read first?

Answer:

Order:


.github/copilot-instructions.md

↓

.github/copilot-context.md

↓

.github/copilot-rules.md

↓

docs/30_AI_CONTEXT.md


---

# Development Questions

---

## Q7: Can I directly access Google Sheets from UI?

Answer:

No.

Always use:


UI

↓

Controller

↓

Service

↓

Repository

↓

Google Sheets


---

## Q8: Where should business logic be placed?

Answer:

Service Layer.

Example:


PatientService.gs


Not:

- HTML
- Controller
- Repository


---

# Security Questions

---

## Q9: Where should API keys be stored?

Answer:

Never in source code.

Use:

- Script Properties
- Secure environment variables


---

## Q10: Can passwords be stored in Google Sheets?

Answer:

Do not store plain passwords.

Use secure authentication methods and hashing.


---

# Deployment Questions

---

## Q11: How do I deploy GAS Web App?

Answer:

Follow:


docs/34_DEPLOYMENT_GUIDE.md


---

## Q12: What should be checked before production?

Answer:

Checklist:


Architecture

Security

Testing

Documentation

Backup

Deployment settings


---

# Troubleshooting

---

## Q13: Application works locally but fails after deployment.

Check:

- Authorization
- Deployment settings
- Permissions
- Script properties


---

## Q14: Spreadsheet operations are slow.

Check:

- Too many Spreadsheet calls
- Missing batch operations
- Missing caching


---

# Documentation Questions

---

## Q15: When should documentation be updated?

Answer:

After:

- New features
- Architecture changes
- Security changes
- API changes


---

# Need More Help?

Review:


docs/README.md

docs/30_AI_CONTEXT.md

docs/38_COPILOT_PROMPT_LIBRARY.md

docs/39_COPILOT_AGENT_EXAMPLES.md
