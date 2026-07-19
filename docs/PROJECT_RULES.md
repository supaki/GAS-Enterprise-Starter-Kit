# Project Rules

## General Rules

Always follow Clean Architecture.

Always separate responsibilities.

Never mix UI and business logic.

Never duplicate code.

---

## Google Apps Script

One responsibility per file.

Recommended files

- Code.gs
- Router.gs
- API.gs
- Database.gs
- Auth.gs
- Config.gs
- Utils.gs
- Logger.gs

---

## HTML

Separate HTML into pages and reusable partials.

Do not place business logic inside HTML.

---

## CSS

Use Tailwind CSS.

Avoid custom CSS unless necessary.

Keep a consistent spacing system.

---

## JavaScript

Use ES2022.

Prefer modules.

Keep functions under 50 lines whenever practical.

Avoid global variables.

---

## Google Sheets

Never access spreadsheet columns by number.

Use header names.

Always validate data.

Batch operations whenever possible.

---

## API

Every response must follow

```json
{
  "success": true,
  "message": "",
  "data": [],
  "errors": []
}
```

---

## Error Handling

Every public function must use try/catch.

Return meaningful error messages.

Log unexpected exceptions.

---

## Naming Convention

Files

camel-case

Classes

PascalCase

Functions

camelCase

Constants

UPPER_SNAKE_CASE

Variables

camelCase

---

## UI

Responsive first.

Support Dark Mode.

Use consistent typography.

Use reusable components.

---

## Before Commit

- No TODO
- No placeholder code
- No duplicated logic
- No console debugging
- JSDoc added
- Error handling completed
- Responsive verified
- Accessibility checked

Only production-ready code may be committed.
