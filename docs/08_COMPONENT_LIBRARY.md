<!-- ====================================================================== -->
<!-- File: docs/08_COMPONENT_LIBRARY.md -->
<!-- ====================================================================== -->

# Component Library

Version 2.0

---

# Purpose

This document defines the reusable UI component standard for the application.

All user interfaces must be built using reusable components.

Do not create duplicated HTML structures.

---

# Component Philosophy

The application follows:

- Component-Based Design
- Atomic Design Concept
- SaaS UI Pattern
- Tailwind CSS Utility Approach

---

# Component Structure

```text
components/

├── layout/
│   ├── Navbar.html
│   ├── Sidebar.html
│   └── Footer.html
│
├── ui/
│   ├── Button.html
│   ├── Card.html
│   ├── Modal.html
│   ├── Toast.html
│   └── Loading.html
│
├── form/
│   ├── Input.html
│   ├── Select.html
│   └── Checkbox.html
│
└── data/
    ├── Table.html
    └── Pagination.html
```

---

# Design System

All components must follow:

- Tailwind CSS
- Responsive Design
- Accessibility
- Dark Mode
- Consistent spacing

---

# Layout Components

---

# Navbar

Purpose:

Top navigation.

Contains:

- Logo
- Search
- Notification
- User menu
- Theme switch

Example:

```html
<nav class="
flex
items-center
justify-between
p-4
bg-white
shadow
">

<h1>
Application Name
</h1>

</nav>
```

---

# Sidebar

Purpose:

Main navigation.

Features:

- Collapse
- Expand
- Active menu
- Icon
- Badge

Example menu:

```javascript
[
 {
  title:"Dashboard",
  icon:"dashboard",
  path:"/"
 },
 {
  title:"Users",
  icon:"people",
  path:"/users"
 }
]
```

---

# Footer

Contains:

- Copyright
- Version
- Links

---

# UI Components

---

# Button

Types:

| Type | Usage |
|-|-|
| Primary | Main action |
| Secondary | Alternative |
| Danger | Delete |
| Ghost | Minor action |

Example:

```html
<button
class="
px-4
py-2
rounded-xl
bg-blue-600
text-white
">

Save

</button>
```

---

# Card

Purpose:

Display information.

Structure:

```text
Card

Icon

Title

Value

Description

Action
```

Example:

Dashboard KPI Card.

---

# Statistic Card

Used for dashboards.

Contains:

- Label
- Number
- Trend
- Icon

Example:

```
Total Users

12,500

+12%

```

---

# Modal

Purpose:

Dialog interaction.

Types:

- Create
- Edit
- Confirm
- Preview

Requirements:

- Close button
- Keyboard support
- Overlay
- Responsive

---

# Toast Notification

Types:

Success

```javascript
showToast(
"Saved successfully",
"success"
);
```

Error

```javascript
showToast(
"Error occurred",
"error"
);
```

---

# Loading Component

Types:

- Spinner
- Skeleton
- Progress

Never show empty screen.

---

# Form Components

---

# Input

Requirements:

- Label
- Placeholder
- Validation
- Error message

Example:

```html
<label>
Email
</label>

<input
class="
border
rounded-xl
"
/>
```

---

# Select

Features:

- Search
- Multiple option
- Validation

---

# Checkbox

Used for:

- Permission
- Setting
- Selection

---

# Data Components

---

# Data Table

Features:

- Search
- Sort
- Filter
- Pagination
- Responsive

Example:

```javascript
const columns=[
{
 key:"name",
 label:"Name"
},
{
 key:"email",
 label:"Email"
}
];
```

---

# Pagination

Example:

```javascript
{
page:1,
limit:20,
total:500
}
```

---

# Empty State

Required when no data exists.

Contains:

- Icon
- Message
- Action

Example:

```
No users found

Create first user
```

---

# Chart Components

Using:

Chart.js

Supported:

- Line
- Bar
- Doughnut
- Area

Example:

```javascript
new Chart(ctx,{
type:"bar",
data:data
});
```

---

# Calendar Component

Features:

- Date selection
- Event display
- Month navigation

---

# Profile Component

Contains:

- Avatar
- Name
- Role
- Logout

---

# Notification Component

Features:

- Read/unread
- Badge
- Dropdown

---

# Component Rules

Every component must:

✓ Be reusable

✓ Have clear responsibility

✓ Support responsive

✓ Support dark mode

✓ Have documentation

✓ Have examples

---

# Component Naming

Use:

PascalCase

Examples:

```
UserCard

DataTable

LoginForm

SidebarMenu
```

---

# Best Practices

Do:

✓ Create reusable components

✓ Use props/configuration

✓ Separate UI from logic

✓ Keep components small


Avoid:

✗ Copy paste HTML

✗ Inline styles

✗ Huge components

---

# GitHub Copilot Prompt

Create reusable UI components following this library.

Requirements:

- Tailwind CSS
- Responsive
- Dark Mode
- Accessibility
- Reusable
- No duplicated HTML

---

# Component Checklist

- [ ] Component documented
- [ ] Responsive
- [ ] Dark mode support
- [ ] Reusable
- [ ] Tested
- [ ] Accessible
