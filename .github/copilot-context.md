# AI Context

## Project Vision

This repository is an enterprise starter kit for building modern web applications using Google Apps Script and Google Sheets.

The goal is to provide a reusable foundation that minimizes development time while maximizing code quality.

---

## Design Philosophy

The project should feel similar to professional SaaS platforms.

Examples

- Google Workspace
- Notion
- Linear
- Vercel
- Supabase

Characteristics

- Clean
- Modern
- Fast
- Responsive
- Minimal
- Accessible

---

## Development Principles

- Clean Architecture
- MVC
- SOLID
- DRY
- KISS
- Separation of Concerns

---

## Backend

Use Google Apps Script services.

Avoid business logic inside HTML.

Prefer Service Layer and Repository Layer.

Use Script Properties for configuration.

Cache frequently used data.

Batch read and write spreadsheet operations.

---

## Frontend

Use Tailwind CSS.

Use reusable UI components.

Avoid duplicated HTML.

Create modular JavaScript.

---

## Database

Google Sheets is the primary database.

Every sheet should contain

- id
- createdAt
- updatedAt
- createdBy
- updatedBy
- status

Never hardcode column indexes.

Use column names.

---

## Performance

Reduce SpreadsheetApp calls.

Use CacheService whenever possible.

Avoid unnecessary loops.

Use pagination.

---

## Security

Validate every input.

Escape HTML output.

Implement RBAC.

Log important operations.

Never expose secrets.

Store credentials only in Script Properties.

---

## Expected Quality

Every module should be maintainable.

Every component should be reusable.

Every page should be responsive.

Every feature should be production ready.
