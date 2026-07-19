<!-- ====================================================================== -->
<!-- File: docs/26_HTML_TEMPLATE_GUIDE.md -->
<!-- ====================================================================== -->

# HTML Template Guide

Version 2.0

---

# Purpose

This document defines the standard HTML development approach for Google Apps Script Web Applications using HTML Service.

The objective is to create:

- Modern SaaS UI
- Maintainable HTML structure
- Reusable layouts
- Responsive interfaces
- Secure frontend rendering

---

# HTML Architecture

The application uses:

```
Google Apps Script HTML Service

+

HTML5

+

Tailwind CSS

+

JavaScript ES6+
```

---

# HTML Application Structure

Recommended:

```
web/

├── index.html

├── layout.html

├── navbar.html

├── sidebar.html

├── footer.html


├── pages/

│   ├── dashboard.html

│   ├── users.html


├── components/

│   ├── card.html

│   ├── table.html


├── styles/

│   └── css.html


└── scripts/

    └── app.js
```

---

# HTML Template Concept

Google Apps Script supports reusable templates.

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

# Include Pattern

Use:

```javascript
function include(filename){

return HtmlService
.createHtmlOutputFromFile(filename)
.getContent();

}
```

---

# Example

index.html:

```html
<!DOCTYPE html>

<html>

<head>

<?!= include('styles/css'); ?>

</head>


<body>

<?!= include('layout'); ?>


<?!= include('scripts/app'); ?>

</body>

</html>
```

---

# Layout System

Standard:

```
Application Layout


├── Sidebar

├── Header

├── Content

└── Footer
```

---

Example:

```html
<div class="flex">


<aside>

Sidebar

</aside>


<main class="flex-1">

Content

</main>


</div>
```

---

# Tailwind CSS Integration

Recommended:

Use CDN for prototype:

```html
<script src="
https://cdn.tailwindcss.com
"></script>
```

---

Production:

Use compiled Tailwind CSS.

---

# Tailwind Configuration

Example:

```javascript
tailwind.config = {

darkMode:'class',

theme:{

extend:{}

}

}
```

---

# Responsive Design

Always support:

```
Mobile

Tablet

Desktop
```

---

Example:

```html
<div
class="
grid

grid-cols-1

md:grid-cols-2

lg:grid-cols-4
">

</div>
```

---

# Dark Mode Support

Use:

```html
<div
class="
bg-white

dark:bg-gray-900

text-gray-900

dark:text-white
">

</div>
```

---

# Page Template Standard

Every page:

```html
<section>


<header>

Page Title

</header>


<div>

Content

</div>


</section>
```

---

# Dashboard Template

Standard SaaS dashboard:

```
Header

↓

KPI Cards

↓

Charts

↓

Data Tables

↓

Activities
```

---

Example:

```html
<div class="grid">


<div>

Users KPI

</div>


<div>

Revenue KPI

</div>


</div>
```

---

# Component Rendering Pattern

Avoid:

Large HTML string creation.

Bad:

```javascript
element.innerHTML =
"<div>...</div>";
```

---

Better:

```javascript
renderUserCard(user);
```

---

# Component Example

Card:

```html
<div
class="
rounded-xl

shadow

p-6

bg-white
">

<h3>

Title

</h3>


<p>

Value

</p>


</div>
```

---

# Form Template Standard

Every form:

```
Title

↓

Fields

↓

Validation

↓

Actions
```

---

Example:

```html
<form>


<label>
Name
</label>


<input
class="
border rounded-xl
"
/>


<button>

Save

</button>


</form>
```

---

# Input Rules

Every input requires:

- Label
- Placeholder
- Validation
- Error message

---

# Table Template Standard

Required:

- Header
- Body
- Loading state
- Empty state
- Pagination

---

Example:

```html
<table>


<thead>

<tr>

<th>Name</th>

</tr>

</thead>


<tbody>

</tbody>


</table>
```

---

# Modal Template

Structure:

```html
<div>


<header>

Title

</header>


<section>

Content

</section>


<footer>

Actions

</footer>


</div>
```

---

# Toast Notification

Example:

```html
<div>

Saved successfully

</div>
```

---

# Loading State

Use:

Skeleton:

```html
<div
class="
animate-pulse
">

Loading

</div>
```

---

# Empty State

Example:

```html
<div>


<h3>

No Data

</h3>


<p>

Create your first record

</p>


</div>
```

---

# HTML Security

Never directly insert user input.

Bad:

```javascript
innerHTML =
userInput;
```

---

Use:

```javascript
textContent =
userInput;
```

---

# XSS Protection

Before rendering:

```
Escape HTML

↓

Render
```

---

Example:

```javascript
function escapeHTML(str){

return str
.replace(
/</g,
"&lt;"
);

}
```

---

# Accessibility Standard

Every page should support:

✓ Keyboard navigation

✓ Screen reader

✓ Focus state

✓ Proper labels

---

Example:

```html
<button
aria-label="Save">

Save

</button>
```

---

# SEO / Metadata

Include:

```html
<title>
Application Name
</title>


<meta
name="viewport"
content="
width=device-width,
initial-scale=1
">
```

---

# Performance Rules

Avoid:

- Huge HTML files
- Duplicate CSS
- Multiple API calls
- Large DOM

---

Use:

- Component reuse
- Lazy loading
- Pagination

---

# HTML Naming Convention

Files:

```
lowercase.html
```

Examples:

```
dashboard.html

user-card.html
```

---

# HTML Review Checklist

## Structure

- [ ] Template separated
- [ ] Components reusable
- [ ] Layout consistent

---

## UI

- [ ] Tailwind applied
- [ ] Responsive
- [ ] Dark mode supported

---

## Security

- [ ] XSS protected
- [ ] Input escaped

---

## UX

- [ ] Loading state
- [ ] Error state
- [ ] Empty state

---

# GitHub Copilot HTML Prompt

```
Act as Senior Frontend Architect.

Create Google Apps Script HTML Service template.

Requirements:

- Tailwind CSS
- Modern SaaS UI
- Responsive
- Dark mode
- Component based
- Accessible

Follow HTML_TEMPLATE_GUIDE.md.
```

---

# Copilot UI Refactoring Prompt

```
Review this HTML template.

Improve:

- Structure
- Reusability
- Responsive design
- Accessibility
- Tailwind usage

Keep business logic unchanged.
```

---

# Final HTML Quality Gate

Before release:

```
HTML Review

↓

Responsive Test

↓

Accessibility Test

↓

Security Check

↓

Deploy
```

---

# End of HTML Template Guide
